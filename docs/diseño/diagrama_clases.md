# Diseño del Sistema: Diagrama de Clases

A continuación se detalla el modelo de dominio de la aplicación TaskFlow, representando las entidades principales y sus relaciones.

```mermaid
classDiagram
    class Usuario {
        +UUID id
        +String nombre
        +String email
        +String passwordHash
        +iniciarSesion()
        +cerrarSesion()
    }

    class Tarea {
        +UUID id
        +String titulo
        +String descripcion
        +Date fechaCreacion
        +Date fechaVencimiento
        +EstadoTarea estado
        +Prioridad prioridad
        +cambiarEstado(nuevoEstado)
        +asignarUsuario(Usuario)
    }

    class Tablero {
        +UUID id
        +String nombre
        +agregarTarea(Tarea)
        +eliminarTarea(Tarea)
    }

    Usuario "1" -- "0..*" Tarea : asignado a
    Usuario "1" -- "1..*" Tablero : propietario
    Tablero "1" *-- "0..*" Tarea : contiene
