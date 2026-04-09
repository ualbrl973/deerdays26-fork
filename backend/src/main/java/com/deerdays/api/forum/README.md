# Módulo de Foros (`forum`)

Gestiona los espacios de debate de la comunidad: creación de posts, comentarios y reacciones.

## Responsabilidades

- CRUD de posts y categorías/hilos de debate.
- Comentarios anidados en posts.
- Sistema de likes/reacciones en posts y comentarios.
- Soporte para publicaciones en modo anónimo.
- Paginación y filtrado del feed de posts.

## Endpoints principales

| Método | Ruta                              | Descripción                         |
|--------|-----------------------------------|-------------------------------------|
| GET    | `/forum/posts`                    | Listado paginado de posts           |
| POST   | `/forum/posts`                    | Crear un nuevo post                 |
| GET    | `/forum/posts/{id}`               | Detalle de un post                  |
| DELETE | `/forum/posts/{id}`               | Eliminar un post                    |
| POST   | `/forum/posts/{id}/comments`      | Añadir comentario a un post         |
| POST   | `/forum/posts/{id}/like`          | Dar like a un post                  |
