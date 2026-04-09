# Módulo de Universidades (`university`)

Gestiona el catálogo de instituciones universitarias registradas en la plataforma.

## Responsabilidades

- CRUD de universidades (nombre, país, ciudad, dominio de email corporativo).
- Búsqueda de universidades por nombre o país.
- Soporte al proceso de verificación universitaria de usuarios (módulo `user`).

## Relaciones

- Una universidad puede tener múltiples **asignaturas** (módulo `subject`).
- Los usuarios verificados se asocian a una universidad concreta.

## Endpoints principales

| Método | Ruta                       | Descripción                               |
|--------|----------------------------|-------------------------------------------|
| GET    | `/universities`            | Listado de universidades con búsqueda     |
| GET    | `/universities/{id}`       | Detalle de una universidad                |
| POST   | `/universities`            | Registrar universidad *(admin)*           |
| PATCH  | `/universities/{id}`       | Editar universidad *(admin)*              |
| DELETE | `/universities/{id}`       | Eliminar universidad *(admin)*            |
