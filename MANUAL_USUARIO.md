# Manual de Usuario - CheckInn

## 1. Introducción

### 1.1. ¡Bienvenido a CheckInn!
CheckInn es una plataforma web integral diseñada para facilitar la búsqueda, reserva y gestión de alojamientos turísticos. Nuestro objetivo es conectar de manera eficiente a huéspedes con una amplia variedad de opciones de alojamiento, y a propietarios con las herramientas necesarias para administrar sus propiedades y alcanzar a una mayor audiencia.

### 1.2. Propósito de la Plataforma
CheckInn busca simplificar la experiencia de planificar viajes, ofreciendo una interfaz intuitiva y funcionalidades robustas tanto para quienes buscan un lugar donde quedarse como para quienes ofrecen sus espacios.

### 1.3. ¿A Quién va Dirigido este Manual?
Este manual está dirigido a los tres tipos de usuarios de la plataforma CheckInn:
*   **Huéspedes:** Personas que buscan y reservan alojamientos.
*   **Propietarios de Alojamiento:** Individuos o empresas que listan y gestionan sus propiedades en la plataforma.
*   **Administradores del Sistema:** Personal encargado de la supervisión, mantenimiento y gestión general de la plataforma CheckInn.

### 1.4. Cómo Usar este Manual
Este manual está estructurado en secciones, cada una dedicada a un aspecto específico de la plataforma o a un tipo de usuario. Puede navegar directamente a la sección de su interés utilizando el índice. Recomendamos leer la sección de "Registro y Gestión de Cuenta General" antes de pasar a las guías específicas por rol.

## 2. Requisitos Previos y Acceso

### 2.1. Navegadores Web Recomendados
Para una experiencia óptima con CheckInn, recomendamos utilizar las últimas versiones de los siguientes navegadores web:
*   Google Chrome
*   Mozilla Firefox
*   Safari
*   Microsoft Edge

Aunque la plataforma podría funcionar en otros navegadores, no podemos garantizar la total compatibilidad.

### 2.2. Conexión a Internet
Se requiere una conexión a internet estable para acceder y utilizar todas las funcionalidades de CheckInn.

### 2.3. Cómo Acceder a la Plataforma
Puede acceder a CheckInn ingresando la siguiente dirección en su navegador web:
*   URL Principal: `http://localhost:3001` (o la URL de producción correspondiente)

## 3. Registro y Gestión de Cuenta General

Esta sección cubre las funcionalidades básicas de gestión de cuentas que son comunes para todos los usuarios antes de interactuar con sus roles específicos.

### 3.1. Creación de una Nueva Cuenta (Registro)
Para utilizar la mayoría de las funcionalidades de CheckInn, necesitará crear una cuenta.
1.  Diríjase a la página principal de CheckInn.
2.  Haga clic en el botón "Registrarse" o "Crear Cuenta" (generalmente ubicado en la esquina superior derecha).
3.  Se le presentará un formulario de registro. Complete los campos requeridos:
    *   Nombre
    *   Apellido
    *   Correo Electrónico (Email): Asegúrese de que sea una dirección válida, ya que podría ser utilizada para confirmaciones o recuperación de cuenta.
    *   Contraseña: Elija una contraseña segura (se recomienda una combinación de letras mayúsculas, minúsculas, números y símbolos, con una longitud mínima de 6 caracteres según los requisitos del sistema).
    *   Confirmar Contraseña: Vuelva a ingresar la contraseña para verificar.
4.  (Opcional) Acepte los Términos y Condiciones y la Política de Privacidad si se le solicita.
5.  Haga clic en el botón "Registrarse" o "Crear Cuenta" para enviar el formulario.
6.  Si el registro es exitoso, es posible que sea redirigido a la página de inicio de sesión o directamente a su panel de control inicial. Podría recibir un correo de bienvenida (funcionalidad dependiente de la configuración del sistema).

### 3.2. Inicio de Sesión (Login)
Una vez que tenga una cuenta, puede iniciar sesión:
1.  Diríjase a la página principal de CheckInn.
2.  Haga clic en el botón "Iniciar Sesión" o "Login".
3.  Ingrese su Correo Electrónico y Contraseña en los campos correspondientes.
4.  Haga clic en el botón "Iniciar Sesión".
5.  Si las credenciales son correctas, será redirigido a su panel de control o a la página principal ya autenticado.

### 3.3. Recuperación de Contraseña (Funcionalidad Futura)
*(Nota: Esta funcionalidad podría no estar implementada en la versión actual. Se describe un flujo común).*
Si olvida su contraseña:
1.  En la página de inicio de sesión, busque un enlace como "¿Olvidó su contraseña?" o "Recuperar Contraseña".
2.  Haga clic en este enlace.
3.  Se le pedirá que ingrese la dirección de correo electrónico asociada a su cuenta.
4.  Siga las instrucciones que se le envíen a su correo electrónico para restablecer su contraseña. Esto usualmente implica hacer clic en un enlace seguro y luego ingresar una nueva contraseña.

### 3.4. Edición de Perfil Básico
Una vez iniciada la sesión, generalmente podrá editar la información básica de su perfil:
1.  Busque una opción como "Mi Perfil", "Mi Cuenta" o su nombre de usuario, usualmente en el menú de navegación.
2.  Dentro de la sección de su perfil, debería encontrar opciones para:
    *   Modificar su nombre y apellido.
    *   Cambiar su dirección de correo electrónico (esto podría requerir una verificación adicional).
    *   Cambiar su contraseña actual por una nueva.

### 3.5. Cierre de Sesión (Logout)
Es importante cerrar sesión cuando haya terminado de usar la plataforma, especialmente si está en una computadora compartida.
1.  Busque una opción como "Cerrar Sesión", "Logout" o un icono de salida, usualmente en el menú de navegación o en el desplegable de su perfil.
2.  Haga clic en esta opción. Será redirigido a la página de inicio o a la página de login.

---

## 4. Guía para Huéspedes

Esta sección está diseñada para ayudar a los usuarios con rol de Huésped a navegar y utilizar eficazmente las funcionalidades de CheckInn para encontrar y reservar alojamientos.

### 4.1. Introducción al Panel del Huésped
Una vez que haya iniciado sesión como huésped, generalmente será recibido con una página de inicio personalizada o un panel de control. Desde aquí, podrá acceder a las principales funcionalidades disponibles para usted:
*   **Búsqueda de Alojamientos:** El punto de partida para encontrar dónde quedarse.
*   **Mis Reservas:** Un historial de sus reservas pasadas y futuras.
*   **Mi Perfil:** Para gestionar su información personal y configuración de cuenta.
*   (Otras funcionalidades que puedan estar disponibles)

### 4.2. Búsqueda de Alojamientos
Encontrar el alojamiento perfecto es fácil con nuestras herramientas de búsqueda.

#### 4.2.1. Uso de la Barra de Búsqueda Principal
La barra de búsqueda principal, usualmente ubicada de forma prominente en la página de inicio o en la sección de "Alojamientos", le permite iniciar su búsqueda. Los campos típicos son:
*   **Destino:** Ingrese la ciudad, región o país donde desea buscar alojamiento (ej. "Córdoba", "Patagonia", "Argentina"). A medida que escribe, pueden aparecer sugerencias.
*   **Fecha de Check-in:** Seleccione la fecha en la que planea llegar.
*   **Fecha de Check-out:** Seleccione la fecha en la que planea irse.
*   **Cantidad de Huéspedes/Personas:** Especifique cuántas personas (adultos y, si es relevante, niños) se alojarán.

Una vez completados estos campos, haga clic en el botón "Buscar".

#### 4.2.2. Página de Resultados y Aplicación de Filtros
Después de realizar una búsqueda inicial, será llevado a una página que muestra una lista de alojamientos que coinciden con sus criterios básicos. Para refinar aún más su búsqueda, puede utilizar los filtros disponibles, que comúnmente incluyen:
*   **Tipo de Alojamiento:** (ej. Hotel, Apartamento, Cabaña).
*   **Rango de Precios:** Ajuste el control deslizante o ingrese un precio mínimo y máximo por noche.
*   **Cantidad de Estrellas:** Filtre por la clasificación de estrellas del alojamiento.
*   **Características Específicas:** Seleccione servicios o comodidades importantes para usted (ej. Wi-Fi, Piscina, Desayuno incluido, Admite mascotas, Estacionamiento).
*   **Puntuación de Huéspedes:** Filtre por la calificación promedio dada por otros usuarios.
*   (Otros filtros relevantes como distancia al centro, etc.)

Cada vez que aplique o modifique un filtro, la lista de resultados se actualizará automáticamente o después de hacer clic en un botón de "Aplicar Filtros".

#### 4.2.3. Visualización de Resultados de Búsqueda
Los alojamientos se mostrarán típicamente en formato de lista o cuadrícula, cada uno con:
*   Una imagen principal.
*   Nombre del alojamiento.
*   Tipo y ubicación (ciudad).
*   Precio promedio por noche (o precio total para las fechas seleccionadas).
*   Puntuación promedio.
*   Un botón o enlace para "Ver Detalles" o similar.

Puede ordenar los resultados por criterios como precio, popularidad, puntuación, etc.

### 4.3. Visualización de Detalles del Alojamiento
Al hacer clic en un alojamiento específico de la lista de resultados, accederá a su página de detalles, donde encontrará información completa:

*   **Galería de Imágenes:** Múltiples fotos del exterior, interior, habitaciones y áreas comunes del alojamiento.
*   **Nombre y Descripción General:** Un resumen detallado del alojamiento, su ambiente y lo que ofrece.
*   **Ubicación:** Dirección completa y, a menudo, un mapa interactivo mostrando su ubicación y puntos de interés cercanos.
*   **Tipos de Habitación Disponibles (para las fechas seleccionadas):**
    *   Nombre del tipo de habitación (ej. "Habitación Doble Standard", "Suite con Vistas").
    *   Descripción de la habitación.
    *   Capacidad (adultos, niños).
    *   Precio por noche o total para la estancia.
    *   Características específicas de la habitación (ej. baño privado, balcón, aire acondicionado).
    *   Botón para seleccionar o reservar ese tipo de habitación.
*   **Servicios y Características Generales del Alojamiento:** Un listado completo de todas las comodidades (ej. Wi-Fi, piscina, restaurante, gimnasio, spa, estacionamiento).
*   **Puntuaciones y Comentarios:** Lea las opiniones y calificaciones dejadas por huéspedes anteriores. Esto puede darle una idea más clara de la experiencia de otros.
*   **Políticas del Alojamiento:** Información importante sobre horarios de check-in/check-out, políticas de cancelación, si se admiten mascotas, métodos de pago aceptados, etc.

### 4.4. Proceso de Reserva

Una vez que haya encontrado un alojamiento y un tipo de habitación que le guste, puede proceder a la reserva.

#### 4.4.1. Selección de Habitación y Fechas
1.  En la página de detalles del alojamiento, si sus fechas ya están seleccionadas, los tipos de habitación disponibles y sus precios para esas fechas se mostrarán.
2.  Si necesita ajustar las fechas o la cantidad de huéspedes, usualmente habrá una opción para hacerlo directamente en esta página.
3.  Seleccione el tipo de habitación deseado y la cantidad de habitaciones (si aplica).
4.  Haga clic en un botón como "Reservar Ahora", "Seleccionar" o similar junto al tipo de habitación elegido.

#### 4.4.2. Resumen de la Reserva y Datos del Huésped
Será llevado a una página de resumen de la reserva donde deberá:
1.  **Verificar los Detalles:** Confirme que el alojamiento, tipo de habitación, fechas de check-in y check-out, cantidad de huéspedes y precio total son correctos.
2.  **Ingresar Datos del Huésped Principal:** Su nombre y apellido (a menudo se autocompletan si ha iniciado sesión). Es posible que se soliciten datos adicionales como número de teléfono o nacionalidad.
3.  **(Opcional) Ingresar Nombres de Otros Huéspedes:** Si la plataforma lo requiere.
4.  **(Opcional) Añadir Peticiones Especiales:** Si tiene alguna solicitud particular (ej. cama supletoria, habitación en planta baja, llegada tardía), puede haber un campo para ello. Estas peticiones suelen estar sujetas a disponibilidad.

#### 4.4.3. Información de Pago
Esta sección dependerá de la configuración de la plataforma:
*   **Reserva sin Pago Inmediato (Pago en el Hotel):** Es posible que solo necesite confirmar la reserva, y el pago se realizará directamente en el alojamiento.
*   **Pago Online Parcial o Total:**
    1.  Se le presentarán los métodos de pago aceptados (ej. tarjeta de crédito/débito).
    2.  Deberá ingresar los detalles de su tarjeta (número, fecha de vencimiento, CVV) en un formulario seguro.
    3.  Confirme la dirección de facturación si es necesario.

#### 4.4.4. Confirmación Final
1.  Revise una última vez todos los detalles de la reserva y la información de pago.
2.  Acepte los términos y condiciones de la reserva y la política de cancelación.
3.  Haga clic en el botón "Confirmar Reserva", "Pagar y Reservar" o similar.

#### 4.4.5. Reserva Exitosa
Si la reserva se procesa correctamente:
1.  Verá una página de confirmación con todos los detalles de su reserva y un número o código de confirmación.
2.  Generalmente, recibirá un correo electrónico de confirmación con esta misma información. Guarde este correo.
3.  Su reserva ahora debería aparecer en la sección "Mis Reservas".

### 4.5. Gestión de Mis Reservas
Puede ver y gestionar sus reservas en cualquier momento.

1.  Inicie sesión en su cuenta CheckInn.
2.  Navegue a la sección "Mis Reservas" o "Mi Historial de Viajes".
3.  Verá una lista de sus reservas futuras y pasadas.
4.  Para cada reserva, podrá ver:
    *   Nombre del alojamiento y fechas.
    *   Estado de la reserva (ej. Confirmada, Cancelada, Completada).
    *   Opción para ver detalles completos.
5.  Al hacer clic en "Ver Detalles", accederá a toda la información de esa reserva específica.
6.  **Cancelar una Reserva:** Si necesita cancelar, busque una opción de "Cancelar Reserva". Tenga en cuenta que se aplicarán las políticas de cancelación del alojamiento, que pueden implicar cargos dependiendo de cuán cerca esté la fecha de check-in. Lea atentamente estas políticas antes de confirmar la cancelación.

### 4.6. Dejar Puntuaciones y Comentarios
Después de completar su estancia en un alojamiento reservado a través de CheckInn, se le podría invitar a dejar una puntuación y un comentario sobre su experiencia.

1.  Vaya a la sección "Mis Reservas" y busque la reserva correspondiente a la estancia completada.
2.  Debería haber una opción o enlace para "Dejar un Comentario", "Puntuar Estancia" o similar.
3.  Se le pedirá que califique diferentes aspectos del alojamiento (ej. limpieza, ubicación, servicio, comodidad) en una escala (ej. de 1 a 5 o de 1 a 10).
4.  Tendrá un espacio para escribir un comentario detallando su experiencia. Sea honesto y constructivo.
5.  Envíe su puntuación y comentario. Usualmente, estos serán revisados por administradores antes de ser publicados.

## 5. Guía para Propietarios de Alojamiento

Esta sección está destinada a los usuarios que desean listar y administrar sus propiedades en CheckInn. Cubre desde el registro de un nuevo alojamiento hasta la gestión diaria de habitaciones, precios y reservas.

### 5.1. Introducción al Panel del Propietario
Al iniciar sesión con una cuenta que tiene permisos de propietario (o después de un proceso de registro específico para propietarios, si aplica), accederá a un panel de control con herramientas diseñadas para la gestión de sus alojamientos. Desde aquí podrá:
*   Añadir y editar sus alojamientos.
*   Gestionar los tipos de habitación, sus características y disponibilidad.
*   Establecer precios.
*   Ver y administrar las reservas entrantes.
*   Consultar las puntuaciones y comentarios de los huéspedes.

### 5.2. Registro y Publicación de un Nuevo Alojamiento
Para empezar a ofrecer su propiedad a los huéspedes:

1.  **Acceder a la Opción de Registro:** En su panel de propietario, busque un botón o enlace como "Añadir Nuevo Alojamiento", "Registrar Propiedad" o similar.
2.  **Completar Formulario de Alta del Alojamiento:** Se le presentará un formulario detallado. Asegúrese de completar la siguiente información con precisión:
    *   **Nombre del Alojamiento:** El nombre comercial o como desea que se muestre (ej. "Hotel Paraíso Azul", "Cabañas del Bosque").
    *   **Tipo de Alojamiento:** Seleccione de una lista el tipo que mejor describe su propiedad (ej. Hotel, Apartamento, Casa de Huéspedes, Cabaña).
    *   **Descripción Detallada:** Describa su alojamiento, sus puntos fuertes, ambiente, y qué lo hace especial. Sea atractivo y honesto.
    *   **Dirección Completa:** Calle, número, ciudad, provincia/estado, código postal.
    *   **País y Ciudad:** Específicos para la búsqueda.
    *   **Estrellas (si aplica):** La clasificación de su alojamiento.
    *   **Capacidad General (informativa):** Número total de personas que podría albergar la propiedad en general (esto se refinará con las habitaciones).
    *   **Teléfono de Contacto y Email Público:** Para consultas.
    *   **Horarios de Check-in y Check-out:** Horas estándar.
    *   **Políticas Generales del Alojamiento:** Reglas importantes, política de mascotas, cancelación general (se puede detallar por tipo de habitación luego), etc.
    *   **Latitud y Longitud (Opcional/Automático):** Para la ubicación exacta en el mapa. A veces se puede autocompletar con la dirección o ajustar manualmente.
3.  **Carga de Imágenes del Alojamiento:**
    *   Suba fotografías de alta calidad que muestren el exterior, la recepción, áreas comunes (lobby, restaurante, piscina, jardines, etc.).
    *   Seleccione una imagen como "Principal" o "Portada", que será la primera que vean los huéspedes.
    *   Puede añadir un orden o etiquetas a las imágenes.
4.  **Definición de Características Generales del Alojamiento:**
    *   Seleccione de una lista las características y servicios que ofrece su alojamiento a nivel general (ej. Wi-Fi Gratuito, Estacionamiento, Restaurante, Piscina, Gimnasio, Spa, Servicio de Lavandería, Admite Mascotas).
5.  **Guardar/Publicar:** Una vez completada toda la información, guarde los cambios. Dependiendo del flujo del sistema, el alojamiento podría requerir aprobación de un administrador antes de ser visible públicamente, o podría publicarse inmediatamente.

### 5.3. Gestión de Tipos de Habitación
Un alojamiento puede ofrecer diferentes tipos de habitaciones. Debe definirlos para que los huéspedes puedan elegir.

1.  **Acceder a la Gestión de Tipos de Habitación:** Dentro de la gestión de un alojamiento específico, busque una sección o pestaña como "Tipos de Habitación", "Configurar Habitaciones" o similar.
2.  **Crear Nuevo Tipo de Habitación:**
    *   **Nombre del Tipo:** Sea descriptivo (ej. "Habitación Doble Standard", "Suite Junior con Balcón", "Estudio Familiar").
    *   **Descripción:** Detalles sobre este tipo de habitación, sus vistas, mobiliario especial, etc.
    *   **Capacidad de Adultos y Menores:** Número máximo de adultos y niños que pueden alojarse en este tipo de habitación.
    *   **Tamaño (m²):** (Opcional) El tamaño aproximado de la habitación.
    *   **Detalle de Camas:** Descripción de la configuración de camas (ej. "1 Cama Queen", "2 Camas Individuales", "1 Cama King + 1 Sofá Cama").
    *   **Precio Base por Noche:** El precio estándar para este tipo de habitación. Podrá ajustarlo luego por temporadas o promociones si la plataforma lo permite (`precios_habitacion`).
    *   **Política de Cancelación Específica (si difiere de la general):** Flexible, moderada, estricta.
    *   **Incluye Desayuno (Sí/No).**
    *   **Horarios de Check-in/Check-out Específicos (si difieren).**
3.  **Cargar Imágenes para el Tipo de Habitación:** Suba fotos específicas que muestren cómo es este tipo de habitación.
4.  **Definir Características Específicas del Tipo de Habitación:** Seleccione de una lista las comodidades que se encuentran DENTRO de este tipo de habitación (ej. Baño Privado, Aire Acondicionado, TV, Minibar, Balcón, Caja Fuerte, Wi-Fi en la habitación).
5.  **Guardar Cambios.** Repita este proceso para cada tipo de habitación que ofrezca su alojamiento.

### 5.4. Gestión de Habitaciones (Instancias Físicas)
Una vez definidos los tipos de habitación, puede que necesite gestionar las habitaciones físicas individuales, especialmente si cada una tiene un número o identificador único y desea rastrear su estado o reservas de forma individual.

1.  **Acceder a la Gestión de Habitaciones Físicas:** Dentro de la gestión de un alojamiento, busque una sección "Habitaciones" o "Inventario Físico".
2.  **Listar Habitaciones Existentes:** Verá una lista de las habitaciones físicas ya creadas para ese alojamiento.
3.  **Añadir Nueva Habitación Física:**
    *   **Número de Habitación/Identificador:** (ej. "101", "A2", "Cabaña Sol"). Debe ser único dentro del alojamiento.
    *   **Seleccionar Tipo de Habitación:** Asocie esta habitación física a uno de los `tipo_habitacion` que creó anteriormente.
    *   **Plazas:** Número de personas que caben (puede autocompletarse desde el tipo, pero podría ser específico).
    *   **Precio Específico (si aplica):** Si esta habitación física tiene un precio ligeramente diferente al base de su tipo.
    *   **Estado Inicial:** (ej. Habilitada, Mantenimiento, Clausurada).
    *   **Notas Internas:** Cualquier comentario relevante sobre esta habitación.
4.  **Editar Detalles de una Habitación:** Modificar la información anterior.
5.  **Cambiar Estado de una Habitación:** Marcarla como no disponible temporalmente por mantenimiento, etc.
6.  **Guardar Cambios.**

### 5.5. Gestión de Precios y Disponibilidad

#### 5.5.1. Inventario por Tipo de Habitación (`habitacion_inventario`)
Si la plataforma utiliza un sistema de inventario agregado por tipo de habitación:
1.  Vaya a la sección de "Inventario" o "Disponibilidad por Tipo" para su alojamiento.
2.  Para cada `tipo_habitacion` que haya definido, especifique la **Cantidad Total** de habitaciones de ese tipo que posee su establecimiento. (ej. 10 Habitaciones Doble Standard, 5 Suites Junior).
Esto ayuda al sistema a saber cuántas habitaciones de un tipo particular pueden ser reservadas simultáneamente.

#### 5.5.2. Precios por Temporada/Promociones (`precios_habitacion`)
Si desea variar los precios de sus tipos de habitación según la fecha:
1.  Acceda a la sección de "Tarifas Avanzadas", "Precios por Temporada" o similar, usualmente dentro de la gestión de un `tipo_habitacion` específico.
2.  **Crear Nueva Regla de Precio:**
    *   Seleccione el `tipo_habitacion` al que aplica.
    *   **Fecha de Inicio y Fecha de Fin:** El período durante el cual este precio especial estará vigente.
    *   **Precio por Noche:** El nuevo precio para ese período.
    *   **Moneda.**
    *   **Marcar como Promoción (Opcional):** Si es una oferta especial.
    *   **Notas (Opcional):** ej. "Tarifa Fin de Semana Largo", "Promo Verano".
3.  Guarde la regla. Puede crear múltiples reglas para diferentes períodos y tipos de habitación. El sistema aplicará el precio más específico según las fechas de la reserva.

#### 5.5.3. Bloquear Fechas (Calendario de Disponibilidad)
(Esta funcionalidad puede variar)
Si necesita bloquear todas las habitaciones de un tipo, o todo el alojamiento, para fechas específicas (ej. por un evento privado o reformas):
1.  Busque una herramienta de "Calendario de Disponibilidad" o "Bloquear Fechas".
2.  Seleccione el alojamiento o el tipo de habitación.
3.  Seleccione las fechas de inicio y fin del bloqueo.
4.  Confirme el bloqueo. Estas fechas no estarán disponibles para nuevas reservas.

### 5.6. Gestión de Reservas Entrantes
Es crucial estar al tanto de las reservas que realizan los huéspedes.

1.  **Acceder al Listado de Reservas:** En su panel de propietario, habrá una sección "Reservas", "Reservas Entrantes" o similar.
2.  **Visualizar Reservas:** Verá una lista de todas las reservas para sus alojamientos, que usualmente se pueden filtrar por:
    *   Fecha de llegada/salida.
    *   Estado de la reserva (ej. Pendiente, Confirmada, Pagada, Cancelada, Activa/En Curso, Completada).
    *   Alojamiento específico (si tiene varios).
    *   Nombre del huésped o número de reserva.
3.  **Ver Detalles de una Reserva:** Haga clic en una reserva para ver toda su información:
    *   Datos del huésped (nombre, contacto).
    *   Alojamiento y habitación(es) reservada(s).
    *   Fechas de check-in y check-out.
    *   Número de adultos y niños.
    *   Precio total y estado del pago.
    *   Peticiones especiales del huésped.
4.  **Gestionar Reservas (según el flujo):**
    *   **Confirmar Reserva:** Si las reservas nuevas llegan como "Pendientes" y requieren su confirmación manual.
    *   **Marcar como Pagada:** Si el pago se realiza por fuera de la plataforma o en el check-in.
    *   **Cancelar Reserva (Propietario):** Si por alguna razón excepcional necesita cancelar una reserva (esto debe manejarse con cuidado y comunicarse claramente al huésped).
    *   **Registrar Check-in/Check-out del Huésped:** Si la plataforma tiene esta funcionalidad para el seguimiento.

### 5.7. Visualización de Puntuaciones y Comentarios
Conocer la opinión de sus huéspedes es vital para mejorar su servicio.

1.  Acceda a la sección "Puntuaciones", "Comentarios" o "Reseñas" en su panel.
2.  Verá una lista de las puntuaciones y comentarios dejados por los huéspedes que se han alojado en sus propiedades.
3.  Podrá ver la calificación detallada (si aplica por categorías) y el texto del comentario.
4.  (Opcional) Algunas plataformas permiten a los propietarios responder públicamente a los comentarios. Si esta opción está disponible, úsela de manera profesional y constructiva.

## 6. Guía para Administradores del Sistema

Esta sección está dedicada a los usuarios con rol de Administrador, quienes tienen la responsabilidad de supervisar y gestionar la operativa general de la plataforma CheckInn.

### 6.1. Introducción al Panel de Administración
Al iniciar sesión con una cuenta de Administrador, se presentará un panel de control centralizado (Backend Admin) que proporciona acceso a todas las herramientas de gestión de la plataforma. Este panel es distinto al que ven los huéspedes o propietarios y ofrece una visión global y control sobre:
*   Gestión de todos los usuarios (huéspedes, propietarios, otros administradores).
*   Gestión de todos los alojamientos listados.
*   Configuraciones globales de la plataforma (tipos de alojamiento, características).
*   Moderación de contenido (puntuaciones, comentarios).
*   Supervisión de todas las reservas.
*   (Opcional) Acceso a reportes y estadísticas.

### 6.2. Gestión de Usuarios
Los administradores pueden gestionar todas las cuentas de usuario en la plataforma.

#### 6.2.1. Ver Listado de Usuarios
*   Acceda a la sección "Usuarios" o "Gestión de Usuarios" en el panel de administración.
*   Se mostrará una tabla o lista con todos los usuarios registrados, incluyendo información como ID de usuario, nombre, apellido, email, rol (huésped, propietario, admin), fecha de registro y estado (activo/inactivo).

#### 6.2.2. Buscar y Filtrar Usuarios
*   Utilice la barra de búsqueda para encontrar usuarios por nombre, email u otros criterios.
*   Aplique filtros para ver usuarios por rol, estado, etc.

#### 6.2.3. Editar Perfil de Usuario
*   Seleccione un usuario de la lista para ver sus detalles.
*   Desde la vista de detalle del usuario, podrá:
    *   **Modificar datos personales:** Nombre, apellido (con precaución).
    *   **Cambiar el Rol del Usuario:** Ascender un huésped a propietario, o viceversa (esta acción debe realizarse con conocimiento de sus implicaciones). Asignar o remover permisos de administrador.
    *   **Activar/Desactivar Cuenta:** Una cuenta desactivada no podrá iniciar sesión.
    *   **Restablecer Contraseña (Opcional):** Algunos sistemas permiten al admin enviar un enlace de restablecimiento o asignar una temporal.

#### 6.2.4. Eliminar Usuarios
*   Seleccione un usuario y busque la opción "Eliminar".
*   **Precaución:** Eliminar un usuario es una acción permanente y podría tener implicaciones en datos asociados (reservas, puntuaciones). Confirme siempre esta acción. Algunas plataformas podrían optar por "desactivar" en lugar de eliminar completamente para mantener la integridad histórica.

### 6.3. Gestión de Alojamientos
Los administradores tienen control total sobre todos los alojamientos en la plataforma.

#### 6.3.1. Ver Listado de Alojamientos
*   Acceda a la sección "Alojamientos" o "Gestión de Alojamientos".
*   Se mostrará una lista de todas las propiedades, con información como nombre, propietario (si aplica), tipo, ciudad, estado (publicado, pendiente de aprobación, desactivado).

#### 6.3.2. Aprobar/Rechazar Nuevos Alojamientos
*   Si existe un flujo donde los propietarios envían sus alojamientos para aprobación:
    *   Habrá una pestaña o filtro para "Alojamientos Pendientes de Aprobación".
    *   Revise cada solicitud, verificando la calidad de la información, imágenes y que cumpla con las políticas de la plataforma.
    *   **Aprobar:** El alojamiento se hace visible públicamente.
    *   **Rechazar:** El alojamiento no se publica. Es buena práctica notificar al propietario el motivo del rechazo.

#### 6.3.3. Editar Detalles de Cualquier Alojamiento
*   Seleccione un alojamiento de la lista para ver y modificar todos sus detalles (similar a lo que puede hacer el propietario, pero con acceso a cualquier propiedad).
*   Esto incluye información general, imágenes, características, gestión de tipos de habitación y habitaciones físicas asociadas.

#### 6.3.4. Desactivar/Activar Alojamientos
*   Puede cambiar el estado de un alojamiento para hacerlo temporalmente no visible o no reservable (ej. "Desactivado") sin eliminarlo.
*   "Activar" lo vuelve a hacer visible y reservable.

#### 6.3.5. Eliminar Alojamientos
*   Seleccione un alojamiento y busque la opción "Eliminar".
*   **Precaución:** Esto eliminará el alojamiento y potencialmente sus habitaciones, imágenes y podría afectar reservas asociadas (dependiendo de las reglas de la base de datos como ON DELETE CASCADE). Confirme cuidadosamente.

### 6.4. Gestión de Configuraciones Globales

#### 6.4.1. Tipos de Alojamiento Globales
*   Acceda a "Configuración" > "Tipos de Alojamiento".
*   Podrá:
    *   **Añadir Nuevos Tipos:** (ej. "Glamping", "Bed & Breakfast").
    *   **Editar Tipos Existentes:** Cambiar nombre o descripción.
    *   **Eliminar Tipos:** Solo si no hay alojamientos actualmente asignados a ese tipo (o manejar la reasignación).

#### 6.4.2. Características Globales de Alojamientos
*   Acceda a "Configuración" > "Características de Alojamiento".
*   Podrá:
    *   **Añadir Nuevas Características:** (ej. "Cargador EV", "Espacio de Coworking"). Incluir icono si el sistema lo soporta.
    *   **Editar Características Existentes.**
    *   **Eliminar Características:** Considerar cómo afecta a los alojamientos que ya la tenían seleccionada.

#### 6.4.3. Características Globales de Tipos de Habitación
*   Acceda a "Configuración" > "Características de Habitación".
*   Similar a las características de alojamiento, pero para las comodidades específicas dentro de las habitaciones (ej. "Ducha con hidromasaje", "Smart TV").

### 6.5. Moderación de Contenido
Mantener la calidad y adecuación del contenido generado por los usuarios es crucial.

#### 6.5.1. Revisar Puntuaciones y Comentarios
*   Acceda a una sección de "Moderación" > "Puntuaciones y Comentarios".
*   Verá una lista de las reseñas enviadas por los huéspedes, especialmente aquellas marcadas como "Pendientes de Aprobación" o reportadas por otros usuarios.
*   **Aprobar:** El comentario se hace visible en la página del alojamiento.
*   **Rechazar/Eliminar:** Si el comentario viola las políticas de contenido (spam, ofensivo, irrelevante). Notificar al usuario es opcional pero recomendable.
*   **Editar (con precaución):** Solo para corregir errores tipográficos menores, nunca para cambiar el sentido de la opinión del huésped.

### 6.6. Supervisión de Reservas
Los administradores pueden ver y, en casos necesarios, intervenir en todas las reservas del sistema.

#### 6.6.1. Ver Todas las Reservas
*   Acceda a la sección "Reservas Globales" o similar.
*   Se mostrará un listado completo de todas las reservas, con filtros por fecha, estado, usuario, alojamiento, etc.

#### 6.6.2. Ver Detalles y Modificar Reservas
*   Seleccione una reserva para ver todos sus detalles.
*   **Modificar (con extrema precaución):** Cambiar fechas, huéspedes o habitación solo debe hacerse en circunstancias excepcionales y con el consentimiento del huésped y/o propietario. Registrar siempre el motivo del cambio.
*   **Cancelar Reservas:** Un administrador puede cancelar cualquier reserva si es necesario (ej. fraude detectado, problema grave con el alojamiento). Se debe notificar a las partes afectadas.
*   **Cambiar Estado de Pago:** Si se requiere intervención manual.

### 6.7. (Opcional) Reportes y Estadísticas
Si la plataforma incluye un módulo de reportería:
*   Acceda a la sección "Reportes" o "Estadísticas".
*   Podrá visualizar gráficos y datos sobre:
    *   Número de registros de usuarios (huéspedes, propietarios).
    *   Número de alojamientos activos.
    *   Número de reservas por período.
    *   Ingresos generados (si se gestionan pagos).
    *   Alojamientos más populares o mejor valorados.
    *   Ocupación promedio.
    *   Otros indicadores clave de rendimiento (KPIs).

## 7. Solución de Problemas Comunes (FAQ)

Esta sección aborda algunas de las preguntas y problemas más comunes que pueden surgir al utilizar CheckInn.

### Para Todos los Usuarios

**P1: No puedo iniciar sesión. ¿Qué hago?**
*   **R:** Verifique que está utilizando el correo electrónico y la contraseña correctos. Asegúrese de que la tecla "Bloq Mayús" no esté activada. Si sigue sin poder acceder, intente utilizar la función de "Recuperar Contraseña" (si está disponible) en la página de inicio de sesión. Si el problema persiste, contacte con el soporte técnico.

**P2: Olvidé mi contraseña. ¿Cómo la recupero?**
*   **R:** En la página de inicio de sesión, busque un enlace como "¿Olvidó su contraseña?". Haga clic ahí y siga las instrucciones, que usualmente implican ingresar su correo electrónico para recibir un enlace de restablecimiento. (Nota: Esta funcionalidad puede depender de la implementación actual).

**P3: ¿Cómo cambio mi correo electrónico o contraseña una vez iniciada la sesión?**
*   **R:** Vaya a la sección "Mi Perfil" o "Mi Cuenta" después de iniciar sesión. Allí debería encontrar opciones para actualizar su información personal, incluyendo su correo electrónico y contraseña.

**P4: La página web no se carga correctamente o veo errores extraños.**
*   **R:** Intente refrescar la página (F5 o Ctrl+R/Cmd+R). Asegúrese de tener una conexión a internet estable y de estar utilizando un navegador web recomendado y actualizado. Borrar la caché y las cookies de su navegador para el sitio CheckInn también puede ayudar. Si el problema continúa, podría ser un inconveniente temporal de la plataforma; inténtelo más tarde o contacte a soporte.

### Para Huéspedes

**P5: No encuentro alojamientos para mi destino o fechas.**
*   **R:** Verifique que el nombre del destino esté escrito correctamente. Pruebe con nombres de ciudades o regiones más amplias. Asegúrese de que las fechas de check-in y check-out sean lógicas (check-in antes que check-out y no en el pasado). Intente ampliar su rango de fechas o buscar sin fechas específicas para ver la disponibilidad general en el destino. Algunos destinos pueden tener poca oferta o estar completamente reservados para las fechas seleccionadas.

**P6: ¿Cómo sé si mi reserva está confirmada?**
*   **R:** Después de completar el proceso de reserva, debería ver una página de confirmación con un número de reserva. Además, recibirá un correo electrónico de confirmación con todos los detalles. También puede verificar el estado de su reserva en la sección "Mis Reservas" de su panel de huésped.

**P7: Necesito cancelar mi reserva. ¿Cómo lo hago y hay algún costo?**
*   **R:** Vaya a "Mis Reservas", seleccione la reserva que desea cancelar y busque la opción "Cancelar Reserva". Antes de confirmar, revise cuidadosamente la política de cancelación asociada a esa reserva, ya que podría haber cargos dependiendo de la antelación con la que cancele.

**P8: ¿Cómo puedo contactar al propietario del alojamiento antes o después de reservar?**
*   **R:** (Esta funcionalidad puede variar) Algunas plataformas ofrecen un sistema de mensajería interna para contactar al propietario después de confirmada la reserva. Si no, los detalles de contacto del alojamiento (teléfono/email) pueden estar visibles en la página de detalles del alojamiento o en la confirmación de su reserva.

### Para Propietarios

**P9: Mi nuevo alojamiento no aparece en los resultados de búsqueda.**
*   **R:** Si acaba de registrar su alojamiento, es posible que necesite ser aprobado por un administrador antes de ser público. Verifique el estado de su alojamiento en su panel de propietario. Asegúrese también de que toda la información obligatoria esté completa y de que el alojamiento esté marcado como "Activo" o "Publicado".

**P10: ¿Cómo actualizo la disponibilidad de mis habitaciones?**
*   **R:** Puede gestionar la disponibilidad a través de varias vías:
    *   Marcando habitaciones físicas individuales como "Habilitada" o "Mantenimiento" en la sección de gestión de habitaciones.
    *   Ajustando la `cantidad_total` en el `habitacion_inventario` si usa ese sistema.
    *   Utilizando herramientas de calendario para bloquear fechas específicas si están disponibles.
    *   Las reservas confirmadas automáticamente marcan esas habitaciones/fechas como no disponibles.

**P11: Un huésped canceló su reserva. ¿Se actualiza automáticamente la disponibilidad?**
*   **R:** Sí, generalmente cuando una reserva se cancela (ya sea por el huésped o por un administrador), el sistema debería liberar automáticamente la disponibilidad de la habitación para esas fechas.

**P12: ¿Cómo respondo a un comentario de un huésped?**
*   **R:** (Esta funcionalidad puede variar) Si la plataforma lo permite, en la sección de "Puntuaciones y Comentarios" de su panel, debería ver una opción para "Responder" junto a cada comentario.

### Para Administradores

**P13: Un propietario informa que no puede editar su alojamiento.**
*   **R:** Verifique que la cuenta del propietario esté activa y tenga los permisos correctos. Asegúrese de que no haya algún bloqueo o estado inusual en el alojamiento específico desde el panel de administración.

**P14: Necesito eliminar un usuario pero mantener su historial de reservas por razones legales/auditoría.**
*   **R:** En lugar de una eliminación completa (que podría borrar datos asociados debido a las cascadas de la base de datos), considere "Desactivar" la cuenta del usuario. Esto previene el inicio de sesión pero mantiene los registros históricos. Consulte las políticas de retención de datos de su organización.

## 8. Contacto y Soporte

Si no encuentra la respuesta a su pregunta en este manual o necesita asistencia adicional, no dude en contactarnos.

*   **Soporte Técnico por Email:** `soporte@checkinn.com` (Reemplace con el email real)
*   **Teléfono de Soporte:** `+XX-XXX-XXXXXXX` (Reemplace con el número real, si aplica)
*   **Horario de Atención:** Lunes a Viernes, de 9:00 AM a 6:00 PM (Su zona horaria)

Para ayudarnos a resolver su problema más rápidamente, por favor incluya la siguiente información al contactarnos (si es relevante):
*   Su nombre de usuario o correo electrónico registrado.
*   Una descripción detallada del problema que está experimentando.
*   Pasos que siguió antes de que ocurriera el problema.
*   Fechas, nombres de alojamiento o números de reserva relevantes.
*   Capturas de pantalla del error o de la sección donde ocurre el problema (si es posible).

Nos esforzamos por responder a todas las consultas en un plazo de 24-48 horas hábiles.
```
