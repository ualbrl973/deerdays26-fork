# Módulo de Administración (`admin`)

Proporciona las herramientas de gestión global de la plataforma, accesibles únicamente para usuarios con rol **Administrador**.

## Responsabilidades

- Gestión de usuarios: alta, baja, cambio de roles y suspensiones.
- Configuración general de la plataforma.
- Acceso a estadísticas y métricas de uso.
- Supervisión de reportes y acciones de moderación.

## Rol requerido

`ADMIN`

## Endpoints principales

| Método | Ruta                    | Descripción                        |
|--------|-------------------------|------------------------------------|
| GET    | `/admin/users`          | Listado de todos los usuarios      |
| PATCH  | `/admin/users/{id}/role`| Cambiar el rol de un usuario       |
| DELETE | `/admin/users/{id}`     | Eliminar un usuario                |
| GET    | `/admin/stats`          | Estadísticas generales             |
