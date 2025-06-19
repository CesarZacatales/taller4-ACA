# Límites de tasa (Rate Limits)

Los límites de tasa son restricciones que se aplican para controlar la cantidad de solicitudes que un usuario o aplicación puede realizar a una API en un período de tiempo determinado. Su objetivo principal es proteger los recursos del servidor y garantizar un servicio estable para todos los usuarios.

## ¿Por qué existen los límites de tasa?

- Prevenir el abuso del servicio.
- Mantener la estabilidad y disponibilidad de la API.
- Distribuir los recursos de manera equitativa entre los usuarios.

## Tipos comunes de límites

- **Por usuario:** Límite de solicitudes por usuario autenticado.
- **Por IP:** Límite de solicitudes por dirección IP.
- **Por aplicación:** Límite de solicitudes por aplicación registrada.

## Respuestas típicas ante exceder el límite

Cuando se supera un límite de tasa, la API suele responder con el código de estado HTTP `429 Too Many Requests`. Además, puede incluir cabeceras indicando cuándo se puede volver a intentar.

## Buenas prácticas

- Consultar la documentación de la API para conocer los límites.
- Implementar reintentos exponenciales en caso de recibir un error 429.
- Monitorear el uso de la API para evitar alcanzar los límites.

## Ejemplo de cabeceras de límite de tasa

```http
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 50
X-RateLimit-Reset: 1688167200
```

- **X-RateLimit-Limit:** Número máximo de solicitudes permitidas.
- **X-RateLimit-Remaining:** Solicitudes restantes en el período actual.
- **X-RateLimit-Reset:** Tiempo en que el límite se restablece (en formato UNIX timestamp).

---

Consulta siempre la documentación oficial de la API para detalles específicos sobre los límites de tasa aplicados.