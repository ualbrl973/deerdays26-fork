# Módulo de Foros (`forum`)

Gestiona los espacios de debate de la comunidad: boards, posts, comentarios, reacciones y contenido guardado.

## Responsabilidades

- CRUD de boards (foros por universidad) con soporte de fijado.
- Posts con paginación por cursor, marcado como pregunta y detección de posts HOT.
- Comentarios anidados (máximo 2 niveles).
- Sistema de likes en posts y comentarios.
- Guardado (scrap) de posts para acceso posterior.
- Reportes de contenido inapropiado.
- Búsqueda de posts dentro de un board.
- Soporte para publicaciones en modo anónimo.

## Endpoints principales

### Boards

| Método | Ruta                                      | Descripción                            |
| ------ | ----------------------------------------- | -------------------------------------- |
| GET    | `/api/forum/boards`                       | Listar foros de la universidad         |
| POST   | `/api/forum/boards`                       | Crear foro                             |
| POST   | `/api/forum/boards/{forumId}/toggle-pin`  | Fijar / desfijar foro                  |

### Posts

| Método | Ruta                                            | Descripción                              |
| ------ | ----------------------------------------------- | ---------------------------------------- |
| GET    | `/api/forum/boards/{forumId}/posts`             | Listar posts (cursor pagination)         |
| GET    | `/api/forum/boards/{forumId}/posts/questions`   | Posts marcados como pregunta             |
| GET    | `/api/forum/boards/{forumId}/posts/hot`         | Post HOT destacado del foro              |
| GET    | `/api/forum/posts/{postId}`                     | Detalle de post con comentarios          |
| POST   | `/api/forum/posts`                              | Crear post                               |
| GET    | `/api/forum/posts/search`                       | Buscar posts en un foro (`?forumId=&q=`) |

### Comentarios

| Método | Ruta                                         | Descripción                          |
| ------ | -------------------------------------------- | ------------------------------------ |
| POST   | `/api/forum/posts/{postId}/comments`         | Crear comentario (max 2 niveles)     |

### Interacciones

| Método | Ruta                                          | Descripción                       |
| ------ | --------------------------------------------- | --------------------------------- |
| POST   | `/api/forum/posts/{postId}/like`              | Toggle like en post               |
| POST   | `/api/forum/comments/{commentId}/like`        | Toggle like en comentario         |
| POST   | `/api/forum/posts/{postId}/scrap`             | Toggle guardar post               |
| POST   | `/api/forum/reports`                          | Reportar post o comentario        |

### Vistas del usuario

| Método | Ruta                      | Descripción                              |
| ------ | ------------------------- | ---------------------------------------- |
| GET    | `/api/forum/me/posts`     | Mis publicaciones (cursor)               |
| GET    | `/api/forum/me/comments`  | Posts donde comenté (cursor)             |
| GET    | `/api/forum/me/scraps`    | Posts guardados (cursor)                 |
| GET    | `/api/forum/hot`          | Posts HOT globales (cursor)              |
