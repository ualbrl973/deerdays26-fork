# Módulo de Asignaturas (`courses`)

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

| Método | Ruta            | Descripción                             |
| ------ | --------------- | --------------------------------------- |
| GET    | `/courses`      | Listado paginado con búsqueda y filtros |
| GET    | `/courses/{id}` | Detalle de una asignatura               |
| POST   | `/courses`      | Crear asignatura _(admin)_              |
| PATCH  | `/courses/{id}` | Editar asignatura _(admin)_             |
| DELETE | `/courses/{id}` | Eliminar asignatura _(admin)_           |
