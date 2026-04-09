# Módulo de Amistades (`friendship`)

Gestiona las relaciones entre usuarios: envío de solicitudes, aceptación y listado de amigos.

## Responsabilidades

- Envío y recepción de solicitudes de amistad.
- Aceptación, rechazo o cancelación de solicitudes.
- Listado de amigos y solicitudes pendientes.
- Eliminación de amistades existentes.

## Estados de una relación

| Estado      | Descripción                                      |
|-------------|--------------------------------------------------|
| `PENDING`   | Solicitud enviada, pendiente de respuesta        |
| `ACCEPTED`  | Amistad establecida                              |
| `REJECTED`  | Solicitud rechazada                              |
| `BLOCKED`   | Usuario bloqueado                                |

## Endpoints principales

| Método | Ruta                              | Descripción                          |
|--------|-----------------------------------|--------------------------------------|
| POST   | `/friendship/request/{userId}`    | Enviar solicitud de amistad          |
| PATCH  | `/friendship/{id}/accept`         | Aceptar solicitud                    |
| PATCH  | `/friendship/{id}/reject`         | Rechazar solicitud                   |
| DELETE | `/friendship/{id}`                | Eliminar amistad                     |
| GET    | `/friendship/friends`             | Listar amigos del usuario actual     |
| GET    | `/friendship/pending`             | Listar solicitudes pendientes        |
