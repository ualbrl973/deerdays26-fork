# Módulo de Mensajería (`messaging`)

Proporciona comunicación privada entre usuarios: conversaciones individuales y grupos de chat.

## Responsabilidades

- Creación y gestión de conversaciones individuales (1:1).
- Creación y administración de grupos de mensajería.
- Envío y recepción de mensajes de texto y adjuntos multimedia.
- Historial de mensajes con paginación.
- Estado de lectura de mensajes.

## Tipos de conversación

| Tipo       | Descripción                              |
|------------|------------------------------------------|
| `DIRECT`   | Conversación privada entre dos usuarios  |
| `GROUP`    | Grupo con múltiples participantes        |

## Endpoints principales

| Método | Ruta                                     | Descripción                            |
|--------|------------------------------------------|----------------------------------------|
| GET    | `/messaging/conversations`               | Listar conversaciones del usuario      |
| POST   | `/messaging/conversations`               | Crear conversación directa o grupo     |
| GET    | `/messaging/conversations/{id}/messages` | Historial de mensajes                  |
| POST   | `/messaging/conversations/{id}/messages` | Enviar mensaje                         |
| DELETE | `/messaging/messages/{id}`               | Eliminar un mensaje propio             |
