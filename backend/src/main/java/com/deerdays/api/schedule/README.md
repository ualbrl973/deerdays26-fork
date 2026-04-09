# Módulo de Horarios (`schedule`)

Permite a los estudiantes crear, gestionar y compartir su horario académico personalizado.

## Responsabilidades

- Creación y gestión del horario semanal del usuario.
- Añadir, editar y eliminar asignaturas del horario.
- Registro de asistencia por sesión.
- Compartir el horario con otros usuarios de la plataforma.

## Estructura del horario

Un horario se compone de **entradas**, cada una con:
- Asignatura (referencia al módulo `subject`)
- Día de la semana y franja horaria
- Aula / ubicación (opcional)

## Endpoints principales

| Método | Ruta                               | Descripción                            |
|--------|------------------------------------|----------------------------------------|
| GET    | `/schedule`                        | Obtener el horario del usuario actual  |
| POST   | `/schedule/entries`                | Añadir asignatura al horario           |
| PATCH  | `/schedule/entries/{id}`           | Editar una entrada del horario         |
| DELETE | `/schedule/entries/{id}`           | Eliminar una entrada del horario       |
| POST   | `/schedule/entries/{id}/attendance`| Registrar asistencia a una sesión      |
| GET    | `/schedule/user/{userId}`          | Ver el horario compartido de otro usuario |
