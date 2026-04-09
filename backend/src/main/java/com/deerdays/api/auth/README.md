# Módulo de Autenticación (`auth`)

Gestiona el acceso a la plataforma: registro, inicio de sesión y emisión de tokens JWT mediante OAuth2.

## Responsabilidades

- Registro de nuevos usuarios.
- Autenticación y generación de tokens de acceso (JWT) y refresco.
- Validación y renovación de sesiones.
- Cierre de sesión e invalidación de tokens.

## Tecnologías

- Spring Security + OAuth2 Resource Server
- JWT (JSON Web Tokens)

## Endpoints principales

| Método | Ruta                   | Descripción                          |
|--------|------------------------|--------------------------------------|
| POST   | `/auth/register`       | Registro de nuevo usuario            |
| POST   | `/auth/login`          | Inicio de sesión, devuelve JWT       |
| POST   | `/auth/refresh`        | Renovación del token de acceso       |
| POST   | `/auth/logout`         | Cierre de sesión                     |
