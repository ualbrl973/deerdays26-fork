# Módulo de Reseñas (`review`)

Permite a los estudiantes valorar y comentar asignaturas para orientar a futuros compañeros.

## Responsabilidades

- Creación, edición y eliminación de reseñas sobre asignaturas.
- Valoración numérica (puntuación) y comentario textual.
- Cálculo y actualización de la puntuación media por asignatura.
- Soporte para reseñas en modo anónimo.
- Listado y filtrado de reseñas por asignatura o usuario.

## Relaciones

- Cada reseña pertenece a un **usuario** (módulo `user`) y a una **asignatura** (módulo `subject`).
- Un usuario solo puede dejar una reseña por asignatura.

## Endpoints principales

| Método | Ruta                               | Descripción                           |
|--------|------------------------------------|---------------------------------------|
| GET    | `/reviews/subject/{subjectId}`     | Listar reseñas de una asignatura      |
| POST   | `/reviews/subject/{subjectId}`     | Crear reseña sobre una asignatura     |
| PATCH  | `/reviews/{id}`                    | Editar reseña propia                  |
| DELETE | `/reviews/{id}`                    | Eliminar reseña propia                |
