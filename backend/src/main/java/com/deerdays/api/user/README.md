# Módulo de Usuarios (`user`)

Gestiona los perfiles de usuario, sus preferencias y el proceso de verificación universitaria.

## Responsabilidades

- Consulta y actualización del perfil de usuario (nombre, bio, avatar, universidad).
- Cambio de contraseña y configuración de cuenta.
- Proceso de verificación universitaria (envío y validación de credenciales).
- Gestión del avatar/imagen de perfil (coordinado con el módulo `media`).

## Estados de verificación

| Estado        | Descripción                                      |
|---------------|--------------------------------------------------|
| `UNVERIFIED`  | Usuario registrado sin verificación universitaria|
| `PENDING`     | Verificación enviada, pendiente de revisión      |
| `VERIFIED`    | Vinculación universitaria acreditada             |

## Roles disponibles

`STUDENT` · `MODERATOR` · `ADMIN`

## Endpoints principales

| Método | Ruta                          | Descripción                              |
|--------|-------------------------------|------------------------------------------|
| GET    | `/users/me`                   | Perfil del usuario autenticado           |
| PATCH  | `/users/me`                   | Actualizar perfil propio                 |
| PATCH  | `/users/me/password`          | Cambiar contraseña                       |
| POST   | `/users/me/verify`            | Iniciar proceso de verificación          |
| GET    | `/users/{id}`                 | Ver perfil público de otro usuario       |
