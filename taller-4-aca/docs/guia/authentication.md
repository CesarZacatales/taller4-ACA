# Autenticación

La autenticación es el proceso de verificar la identidad de un usuario o sistema antes de permitir el acceso a recursos protegidos. A continuación se presentan los conceptos clave y pasos comunes en la autenticación.

## Conceptos clave

- **Usuario:** Persona o sistema que solicita acceso.
- **Credenciales:** Información utilizada para verificar la identidad (por ejemplo, nombre de usuario y contraseña).
- **Autorización:** Proceso posterior a la autenticación que determina los permisos del usuario.

## Métodos comunes de autenticación

1. **Contraseña:** El usuario proporciona una contraseña secreta.
2. **Autenticación de dos factores (2FA):** Se requiere un segundo método, como un código enviado al teléfono.
3. **OAuth:** Permite el acceso mediante cuentas de terceros (Google, Facebook, etc.).
4. **Tokens:** Uso de tokens de acceso para sesiones seguras.

## Buenas prácticas

- Utilizar contraseñas seguras y únicas.
- Implementar 2FA siempre que sea posible.
- Almacenar contraseñas de forma cifrada.
- Expirar sesiones inactivas automáticamente.

## Ejemplo de flujo de autenticación

1. El usuario ingresa sus credenciales.
2. El sistema verifica las credenciales.
3. Si son válidas, se concede acceso y se genera una sesión.
4. Si no son válidas, se deniega el acceso.

---
!!! warning
    Si introduces credenciales incorrectas, tu cuenta podría bloquearse temporalmente.
> La autenticación es fundamental para proteger la información y los recursos de cualquier sistema.
