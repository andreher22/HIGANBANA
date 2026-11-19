# 0011 · Errores en producción con Sentry

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
Sin monitoreo, los errores se descubren cuando una usuaria se queja.

## Decisión
Sentry (plan gratuito) en la web y en la API.

## Por qué
Enterarse de los errores antes que la usuaria.

## Alternativas consideradas
- **Solo los logs de Vercel:** no agrupan errores ni avisan.

## Consecuencias
Nunca enviar datos de salud en los reportes de error. Revisar los límites del plan gratuito antes de lanzar.
