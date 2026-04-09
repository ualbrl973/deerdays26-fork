# Módulo de Correo (`mail`)

Servicio interno encargado del envío de correos electrónicos transaccionales a los usuarios.

## Responsabilidades

- Envío de correos de bienvenida tras el registro.
- Correos de verificación de dirección de email.
- Notificaciones por email (recuperación de contraseña, alertas importantes).
- Renderizado de plantillas HTML para los mensajes.

## Notas de diseño

- Este módulo actúa como **servicio interno**; no expone endpoints REST públicos.
- Es invocado por otros módulos (`auth`, `user`, `notification`) mediante inyección de dependencias.
- Las plantillas de email se ubican en `resources/templates/mail/`.
