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

| Método | Ruta                     | Descripción                                              |
| ------ | ------------------------ | -------------------------------------------------------- |
| GET    | `/api/schedules`         | Horarios del usuario                                     |
| POST   | `/api/schedules`         | Crear horario                                            |
| PUT    | `/api/schedules/{id}`    | Actualizar horario (nombre, entries, semester)           |
| DELETE | `/api/schedules/{id}`    | Eliminar horario                                         |
