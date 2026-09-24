# Análisis de Requisitos

## Requisitos Funcionales (RF)
* **RF01 - Autenticación:** El sistema debe permitir a los usuarios registrarse e iniciar sesión con correo y contraseña.
* **RF02 - Gestión de Tareas (CRUD):** Los usuarios deben poder crear, leer, actualizar y eliminar tareas.
* **RF03 - Estados de Tarea:** Toda tarea debe poder transicionar entre los estados: `Pendiente`, `En Progreso` y `Completada`.
* **RF04 - Asignación:** Un usuario debe poder asignar una tarea a otro usuario registrado.
* **RF05 - Filtrado:** El sistema debe permitir filtrar las tareas por estado y por prioridad (Alta, Media, Baja).

## Requisitos No Funcionales (RNF)
* **RNF01 - Rendimiento:** El tiempo de carga del tablero principal no debe superar los 2 segundos con una conexión estándar.
* **RNF02 - Usabilidad:** La interfaz debe ser completamente *responsive*, adaptándose a dispositivos móviles y tabletas.
* **RNF03 - Disponibilidad:** El sistema debe garantizar un uptime del 99.9%.
* **RNF04 - Seguridad:** Las contraseñas deben almacenarse encriptadas (bcrypt) y la sesión manejarse mediante tokens JWT.
