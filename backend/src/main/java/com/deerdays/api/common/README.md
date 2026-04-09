# Módulo Común (`common`)

Contiene utilidades, clases base y componentes transversales compartidos por el resto de módulos.

## Contenido habitual

- **Excepciones personalizadas** y manejador global de errores (`@ControllerAdvice`).
- **DTOs genéricos**: respuestas paginadas, envelopes de error/éxito.
- **Constantes** y enumeraciones globales (roles, estados, etc.).
- **Validadores** y anotaciones de validación reutilizables.
- **Utilidades** de fechas, strings y mapeo de objetos.

## Convenciones

Este módulo **no expone endpoints propios**. Sus clases son importadas por los demás módulos; no debe tener dependencias hacia ellos para evitar ciclos.
