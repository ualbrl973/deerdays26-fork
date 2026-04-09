# Módulo de Notificaciones (`notification`)

Gestiona el sistema de alertas en tiempo real para informar a los usuarios de eventos relevantes.

## Responsabilidades

- Generación de notificaciones desde otros módulos (mensajes, solicitudes de amistad, likes, etc.).
- Listado de notificaciones del usuario con estado de lectura.
- Marcado individual o masivo como leídas.
- Envío opcional por email (delegado al módulo `mail`).

## Tipos de notificación

| Tipo                  | Módulo origen    |
|-----------------------|------------------|
| `NEW_MESSAGE`         | `messaging`      |
| `FRIEND_REQUEST`      | `friendship`     |
| `POST_LIKE`           | `forum`          |
| `POST_COMMENT`        | `forum`          |
| `REVIEW_POSTED`       | `review`         |

## Endpoints principales

| Método | Ruta                                | Descripción                          |
|--------|-------------------------------------|--------------------------------------|
| GET    | `/notifications`                    | Listar notificaciones del usuario    |
| PATCH  | `/notifications/{id}/read`          | Marcar una notificación como leída   |
| PATCH  | `/notifications/read-all`           | Marcar todas como leídas             |
