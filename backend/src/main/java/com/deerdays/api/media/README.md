# Módulo de Medios (`media`)

Gestiona la subida, almacenamiento y recuperación de archivos multimedia (imágenes, documentos).

## Responsabilidades

- Subida de archivos adjuntos a posts, mensajes y perfiles.
- Validación de tipo y tamaño de archivo.
- Almacenamiento de archivos (local en desarrollo, objeto en producción).
- Generación de URLs de acceso a los recursos almacenados.

## Tipos de archivo soportados

- Imágenes: `jpg`, `png`, `webp`, `gif`
- Documentos: `pdf`

## Endpoints principales

| Método | Ruta                    | Descripción                              |
|--------|-------------------------|------------------------------------------|
| POST   | `/media/upload`         | Subir un archivo, devuelve su URL        |
| GET    | `/media/{filename}`     | Recuperar un archivo por nombre          |
| DELETE | `/media/{filename}`     | Eliminar un archivo                      |
