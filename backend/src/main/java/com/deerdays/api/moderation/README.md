# Módulo de Moderación (`moderation`)

Herramientas para mantener un entorno seguro y respetuoso, accesibles para moderadores y administradores.

## Responsabilidades

- Recepción y gestión de reportes de contenido inapropiado.
- Revisión de reportes pendientes y toma de acciones (advertencia, eliminación, suspensión).
- Registro de acciones disciplinarias sobre usuarios.
- Desvelado de identidad anónima en casos justificados (coordinado con el módulo `anonymous`).

## Estados de un reporte

| Estado       | Descripción                                  |
|--------------|----------------------------------------------|
| `PENDING`    | Reporte recibido, pendiente de revisión      |
| `RESOLVED`   | Reporte revisado y acción tomada             |
| `DISMISSED`  | Reporte descartado por el moderador          |

## Roles requeridos

`MODERATOR` o `ADMIN`

## Endpoints principales

| Método | Ruta                              | Descripción                          |
|--------|-----------------------------------|--------------------------------------|
| POST   | `/moderation/reports`             | Crear un reporte de contenido        |
| GET    | `/moderation/reports`             | Listar reportes pendientes           |
| PATCH  | `/moderation/reports/{id}/resolve`| Resolver un reporte                  |
| PATCH  | `/moderation/reports/{id}/dismiss`| Descartar un reporte                 |
