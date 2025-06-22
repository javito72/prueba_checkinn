# Documento de Decisiones de Arquitectura - CheckInn

## 1. Introducción
Este documento detalla las decisiones arquitectónicas clave tomadas durante el desarrollo de la plataforma CheckInn. El objetivo es proporcionar un entendimiento claro de por qué se eligieron ciertas tecnologías, patrones y estructuras, facilitando el mantenimiento futuro, la escalabilidad y la incorporación de nuevos desarrolladores al proyecto.

## 2. Stack Tecnológico Elegido y Justificación

La plataforma CheckInn se ha construido utilizando el siguiente stack tecnológico:

### 2.1. Backend
*   **Entorno de Ejecución: Node.js**
    *   **Justificación:** Node.js fue elegido por su naturaleza asíncrona y orientada a eventos, lo que lo hace altamente eficiente para aplicaciones I/O intensivas como una API web que maneja múltiples solicitudes de clientes. Su amplio ecosistema a través de NPM permite acceder a una vasta cantidad de librerías y herramientas. JavaScript como lenguaje único en frontend y backend (Isomorfismo parcial) puede simplificar el desarrollo y la reutilización de lógica o modelos de datos si fuera necesario en el futuro.
*   **Framework Web: Express.js**
    *   **Justificación:** Express.js es un framework minimalista y flexible para Node.js, ideal para construir APIs RESTful. Proporciona una capa robusta de funcionalidades básicas para el manejo de rutas, middleware y solicitudes/respuestas HTTP sin imponer una estructura rígida, lo que permite adaptarlo a las necesidades del proyecto. Su popularidad asegura una buena documentación y soporte de la comunidad.
*   **Base de Datos: MySQL (con `mysql2` driver)**
    *   **Justificación:** MySQL es un sistema de gestión de bases de datos relacional (RDBMS) maduro, robusto y ampliamente utilizado, adecuado para aplicaciones que requieren consistencia de datos y transacciones ACID (Atomicidad, Consistencia, Aislamiento, Durabilidad), como es el caso de un sistema de reservas. El driver `mysql2` es una implementación popular y eficiente para Node.js, con soporte para promesas, lo que facilita el uso de `async/await`.
*   **Autenticación: JSON Web Tokens (JWT)**
    *   **Justificación:** JWT fue elegido por ser un estándar abierto (RFC 7519) para crear tokens de acceso que permiten la propagación segura de identidad y privilegios. Son compactos, pueden ser enviados a través de URLs, parámetros POST o dentro de headers HTTP, y son auto-contenidos (llevan la información del usuario), lo que puede reducir la necesidad de consultar la base de datos en cada solicitud protegida (aunque se recomienda verificar la existencia del usuario para invalidar tokens de usuarios eliminados o con roles cambiados).
*   **Hashing de Contraseñas: `bcryptjs`**
    *   **Justificación:** `bcryptjs` (una implementación de bcrypt en JavaScript puro) es una librería robusta y recomendada para el hashing seguro de contraseñas. Bcrypt está diseñado para ser lento computacionalmente, lo que dificulta los ataques de fuerza bruta. Almacena la "sal" (salt) junto con el hash, protegiendo contra ataques de tablas precalculadas (rainbow tables).

### 2.2. Frontend
*   **Lenguajes Base: HTML5, CSS3, JavaScript Vanilla**
    *   **Justificación:** Se optó por JavaScript Vanilla (sin frameworks como React, Angular o Vue) para el frontend. Esta decisión pudo estar motivada por:
        *   **Simplicidad para el alcance del proyecto (MVP):** Para funcionalidades directas de manipulación del DOM y llamadas AJAX, un framework completo podría ser excesivo.
        *   **Menor curva de aprendizaje:** Si el equipo de desarrollo inicial estaba más familiarizado con JS puro.
        *   **Control total y ligereza:** Evitar el overhead de un framework si no todas sus características son necesarias.
        *   **Requisitos específicos del proyecto original.**
    *   HTML5 y CSS3 son los estándares para la estructura y el estilo de las páginas web.

## 3. Estructura del Backend
El backend sigue un patrón **Modular**, similar en algunos aspectos a MVC (Model-View-Controller), pero adaptado para una API RESTful donde las "Vistas" son las respuestas JSON.
*   **`controllers/`**: Contienen la lógica de manejo de solicitudes. Reciben la petición HTTP, validan los datos de entrada (aunque la validación podría ser más robusta o externalizada a middleware), interactúan con los modelos para operaciones de base de datos, y formulan la respuesta JSON al cliente.
*   **`models/`**: Responsables de toda la interacción con la base de datos. Encapsulan las consultas SQL y la lógica de acceso a datos. Devuelven los datos a los controladores. Esta separación permite cambiar la base de datos o la forma de acceder a ella con un impacto mínimo en los controladores.
*   **`routes/`**: Definen los endpoints de la API (URLs) y los métodos HTTP asociados (GET, POST, PUT, DELETE). Vinculan cada ruta a la función del controlador correspondiente y pueden aplicar middleware específico de la ruta.
*   **`middleware/`**: Contiene funciones que se ejecutan en el ciclo de solicitud-respuesta. Se utilizan para tareas transversales como la autenticación (`auth.middleware.js`), logging, manejo de errores, etc.
*   **`db.js`**: Centraliza la configuración y creación del pool de conexiones a la base de datos MySQL.
*   **`index.js`**: Punto de entrada de la aplicación. Configura el servidor Express, aplica middleware global (CORS, body-parser), monta las rutas principales y arranca el servidor.
*   **`routes.js` (raíz)**: Agrega todas las sub-rutas definidas en el directorio `routes/` bajo un router principal, que luego es montado en `index.js` bajo el prefijo `/api`.

**Justificación de esta estructura:**
*   **Separación de Responsabilidades (SoC):** Facilita la comprensión, el mantenimiento y las pruebas del código.
*   **Modularidad:** Permite desarrollar y modificar partes del sistema de forma independiente.
*   **Escalabilidad:** Es más sencillo añadir nuevas funcionalidades o modificar las existentes.

## 4. Manejo de Autenticación y Autorización
*   **Mecanismo:** Se utiliza JWT (JSON Web Tokens).
*   **Flujo de Autenticación (Login):**
    1.  El usuario envía credenciales (email/password) al endpoint `/api/auth/login`.
    2.  El `auth.controller.js` verifica las credenciales contra la base de datos usando `Usuario.findByEmail` y `Usuario.comparePassword`.
    3.  Si son válidas, se genera un JWT firmado con `process.env.JWT_SECRET`. El payload del token incluye `id_usuario`, `email` y `es_admin`.
    4.  El token se envía al cliente en la respuesta JSON.
*   **Almacenamiento del Token en Frontend:** El cliente (JavaScript en `public/js/login.js`) almacena el token en `sessionStorage`. `sessionStorage` persiste mientras la pestaña del navegador está abierta. Una alternativa podría ser `localStorage` para persistencia entre sesiones, pero con consideraciones de seguridad adicionales.
*   **Protección de Rutas:**
    1.  Para rutas que requieren autenticación, el frontend debe incluir el JWT en el header `Authorization` de la solicitud como `Bearer <token>`.
    2.  El middleware `authenticateToken` (`middleware/auth.middleware.js`) en el backend intercepta estas solicitudes.
    3.  Verifica la firma y la caducidad del token.
    4.  Si es válido, extrae el payload y lo añade a `req.user`, permitiendo que los controladores posteriores accedan a la información del usuario autenticado.
    5.  Si no es válido, devuelve un error 401 (No Autorizado) o 403 (Prohibido).
*   **Autorización (Roles - Admin):**
    1.  El middleware `isAdmin` (también en `auth.middleware.js`) se utiliza en rutas que requieren privilegios de administrador.
    2.  Este middleware se ejecuta *después* de `authenticateToken`.
    3.  Verifica si `req.user.es_admin` es verdadero. Para mayor seguridad, también vuelve a consultar la base de datos usando `Usuario.findById(req.user.id)` para confirmar que el usuario sigue existiendo y sigue siendo administrador, protegiendo contra el caso de que el rol del usuario haya cambiado desde que se emitió el token.

## 5. Interacción con la Base de Datos
*   **Driver:** Se utiliza `mysql2` directamente, sin un ORM (Object-Relational Mapper) completo como Sequelize o TypeORM.
    *   **Justificación:**
        *   **Control Total:** Permite un control granular sobre las consultas SQL, lo que puede ser beneficioso para optimizaciones específicas.
        *   **Menor Abstracción:** Más cercano al SQL, lo que puede ser preferido por desarrolladores con fuerte experiencia en SQL.
        *   **Menos Dependencias/Overhead:** Evita la complejidad y el posible overhead de un ORM si no se necesitan todas sus características avanzadas.
    *   **Desventajas Potenciales:** Más verboso, mayor riesgo de errores SQL si no se maneja con cuidado, y puede ser más tedioso mapear resultados a objetos manualmente (aunque los modelos aquí son relativamente simples).
*   **Pool de Conexiones:** `db.js` configura un pool de conexiones (`mysql.createPool`). Esto es crucial para el rendimiento y la escalabilidad, ya que reutiliza conexiones en lugar de abrir y cerrar una nueva para cada consulta.
*   **Promesas y `async/await`:** El pool se exporta con `.promise()`, lo que permite usar `async/await` para un código asíncrono más limpio y legible en los modelos.
*   **Transacciones Explícitas:** En operaciones críticas que involucran múltiples pasos y deben ser atómicas (o todo o nada), como la creación de una reserva (`Reserva.create`), se utilizan transacciones explícitas (`connection.beginTransaction()`, `connection.commit()`, `connection.rollback()`). Esto asegura la integridad de los datos.
*   **Seguridad (SQL Injection):** Los modelos utilizan consultas parametrizadas (con `?` como placeholders y pasando los valores en un array separado). Esta es la principal defensa contra ataques de inyección SQL.

## 6. Diseño del Frontend
*   **JavaScript Vanilla:** No se utiliza ningún framework de JavaScript moderno (React, Angular, Vue). La lógica del cliente se implementa con manipulación directa del DOM y llamadas `fetch` para interactuar con la API.
    *   **Archivos:** La lógica de frontend está organizada en archivos JavaScript separados por funcionalidad/página en `public/js/` (ej. `login.js`, `catalogo.js`, `registro_alojamiento.js`).
    *   **Comunicación con API:** Se utiliza la API `fetch` nativa del navegador para realizar solicitudes HTTP (GET, POST) a los endpoints del backend. Se manejan las respuestas JSON y se actualiza el DOM dinámicamente.
*   **Estructura de Archivos Estáticos:**
    *   `public/`: Raíz para todos los archivos servidos estáticamente por Express.
    *   `public/index.html`: Página principal.
    *   `public/pages/`: Contiene otras páginas HTML.
    *   `public/css/`: Hojas de estilo CSS.
    *   `public/js/`: Scripts de JavaScript para el cliente.
    *   `public/assets/`: Imágenes y otros recursos.
*   **Manejo del Estado (Simple):** El estado de la aplicación en el frontend (como el token de autenticación o la información del usuario) se maneja de forma sencilla, principalmente usando `sessionStorage`. Para aplicaciones más complejas, se consideraría una solución de gestión de estado más robusta.

## 7. Decisiones Específicas del Esquema de BD
*   **`habitaciones` vs. `habitacion_inventario`:**
    *   `habitaciones`: Representa las instancias físicas individuales de las habitaciones, cada una con un número, tipo y precio específico. Es a esta tabla a la que se vinculan las reservas.
    *   `habitacion_inventario`: Parece diseñada para llevar una cuenta agregada de cuántas habitaciones de un cierto `tipo_habitacion` existen en un `alojamiento`. Esto podría ser útil para vistas rápidas de disponibilidad general por tipo o para la configuración inicial por parte del propietario. La lógica de reserva actual parece centrarse más en encontrar una `id_habitacion` disponible de la tabla `habitaciones`. La relación y uso exacto entre estas dos podría clarificarse o simplificarse.
*   **ENUMs vs. Tablas de Lookup:** Se utilizan ENUMs para campos como `reservas.estado` o `habitaciones.estado`. Esto es simple para un conjunto fijo y pequeño de valores. Para valores que podrían cambiar o necesitar más metadatos, se podrían haber usado tablas de lookup separadas con FKs (ej. una tabla `estados_reserva`).
*   **Políticas de Borrado/Actualización en FKs:** El uso de `ON DELETE CASCADE`, `ON DELETE RESTRICT`, `ON DELETE SET NULL` está bien definido en el schema `initdb.sql`, lo que ayuda a mantener la integridad referencial. Por ejemplo, si se elimina un `alojamiento`, las `reservas` y `puntajes` asociados se eliminan en cascada.
*   **Trigger para `promedio_puntaje`:** La decisión de usar un trigger en la base de datos (`tr_actualizar_promedio_puntaje`) para actualizar el puntaje promedio y la cantidad de puntajes en `alojamientos` cada vez que se inserta un nuevo `puntaje` es una forma eficiente de mantener estos datos agregados actualizados sin necesidad de recálculos en la aplicación en cada lectura. Sin embargo, como se nota en el modelo `puntaje.model.js`, esto no cubre actualizaciones o eliminaciones de puntajes; se necesitarían triggers `AFTER UPDATE` y `AFTER DELETE` o lógica de aplicación para esos casos si se requiere precisión absoluta.

## 8. Cambios Significativos Respecto al Diseño Original (Si los Hubo)
*(Esta sección requeriría conocimiento histórico del proyecto que no poseo. Se deja como placeholder para ser completada por el equipo de desarrollo si aplica).*
*   Ejemplo: "Inicialmente se consideró MongoDB, pero se cambió a MySQL por la necesidad de transacciones ACID robustas para las reservas."
*   Ejemplo: "El sistema de autenticación se basaba en sesiones, pero se migró a JWT para facilitar la escalabilidad y el consumo por clientes móviles en el futuro."

## 9. Consideraciones de Seguridad Implementadas
*   **Hashing de Contraseñas:** Uso de `bcryptjs` con sales automáticas para almacenar contraseñas de forma segura.
*   **Prevención de SQL Injection:** Uso consistente de consultas parametrizadas en todos los modelos de datos.
*   **Autenticación con JWT:** Los tokens protegen los endpoints y transmiten la identidad del usuario de forma segura. Se usan expiraciones cortas para los tokens (`1h` en `auth.controller.js`), lo que limita la ventana de oportunidad si un token es comprometido.
*   **CORS:** Configurado con `app.use(cors('*'))` en `index.js`. Para producción, esto debería restringirse a los dominios del frontend permitidos para mayor seguridad.
*   **Protección de Rutas de Administrador:** El middleware `isAdmin` no solo confía en el payload del token sino que re-verifica el estado de administrador en la base de datos.
*   **Manejo de Errores:** Aunque básico, hay `try-catch` en los controladores y modelos para evitar que errores no controlados expongan detalles sensibles.

## 10. Limitaciones Conocidas o Futuras Mejoras Pensadas (Arquitectura)
*(Esta sección es especulativa basada en la revisión del código).*
*   **Validación de Entradas:** La validación de los datos de entrada en los controladores es mínima. Se podría implementar una capa de validación más robusta y centralizada (ej. usando librerías como Joi o express-validator) para asegurar la integridad de los datos antes de llegar a la lógica de negocio o a los modelos.
*   **Manejo de Errores Avanzado:** Implementar un middleware de manejo de errores global más sofisticado para estandarizar las respuestas de error y el logging.
*   **Frontend con Framework:** Para una mayor escalabilidad y mantenibilidad del frontend, especialmente si las interacciones se vuelven más complejas, se podría considerar la migración a un framework de JavaScript como React, Vue o Angular.
*   **Testing:** El `package.json` no especifica un script de prueba ni dependencias de testing. Incorporar pruebas unitarias, de integración y E2E mejoraría significativamente la robustez.
*   **Optimización de Consultas Complejas:** La consulta `Alojamiento.getAll` es compleja. A medida que los datos crezcan, podría necesitar optimización o estrategias de paginación más avanzadas.
*   **Configuración de CORS para Producción:** Como se mencionó, `cors('*')` es demasiado permisivo para un entorno de producción.
*   **Gestión de Archivos/Imágenes:** Actualmente las URLs de imágenes se guardan como VARCHAR. Para una gestión más robusta, se podría integrar con un servicio de almacenamiento de objetos (como AWS S3, Google Cloud Storage) o implementar una estrategia de servicio de archivos más detallada.
*   **Variables de Entorno:** Asegurar que todas las configuraciones sensibles (claves secretas, credenciales de BD) se manejen exclusivamente a través de variables de entorno y que el archivo `.env` nunca se suba al repositorio de código.
*   **Escalabilidad Horizontal:** Si bien Node.js es eficiente, para una alta carga, se necesitaría considerar estrategias de escalabilidad horizontal (múltiples instancias de la aplicación detrás de un balanceador de carga) y cómo esto afecta el manejo de JWT (no es un problema con JWT ya que son stateless, pero sí para otros mecanismos de sesión).
