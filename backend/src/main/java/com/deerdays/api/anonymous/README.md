# Módulo de Modo Anónimo (`anonymous`)

Permite a los usuarios autenticados participar en la plataforma ocultando su identidad real.

## Responsabilidades

- Generación y gestión de identidades anónimas por usuario.
- Asociación interna entre la identidad anónima y el usuario real (solo visible para moderadores/admins).
- Aplicación del modo anónimo en posts, comentarios y mensajes.

## Notas de diseño

- Un mismo usuario puede tener distintos alias anónimos según el contexto.
- La identidad real nunca se expone públicamente; solo los moderadores pueden desvelarla en casos de abuso.

## Endpoints principales

| Método | Ruta                        | Descripción                              |
|--------|-----------------------------|------------------------------------------|
| POST   | `/anonymous/activate`       | Activar modo anónimo en la sesión actual |
| DELETE | `/anonymous/deactivate`     | Desactivar modo anónimo                  |
| GET    | `/anonymous/identity`       | Consultar el alias anónimo activo        |
