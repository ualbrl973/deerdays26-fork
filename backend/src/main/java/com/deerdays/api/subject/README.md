# Módulo de Asignaturas (`course`)

Gestiona el catálogo de asignaturas universitarias disponibles en la plataforma.

## Responsabilidades

- CRUD de asignaturas (nombre, código, descripción, créditos, universidad asociada).
- Búsqueda y filtrado por nombre, código o universidad.
- Exposición de la puntuación media calculada desde el módulo `review`.

## Relaciones

- Cada asignatura pertenece a una **universidad** (módulo `university`).
- Una asignatura puede tener múltiples **reseñas** (módulo `review`).
- Una asignatura puede aparecer en los **horarios** de múltiples usuarios (módulo `schedule`).

## Endpoints principales

| Método | Ruta                  | Descripción                                                              |
| ------ | --------------------- | ------------------------------------------------------------------------ |
| GET    | `/api/courses`        | Listar/buscar asignaturas (filtros: `q`, `degree`, `faculty`, `year`, `semester`, `type`) |
| GET    | `/api/courses/{id}`   | Detalle de asignatura con grupos y sesiones                              |
