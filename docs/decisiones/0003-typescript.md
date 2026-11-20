# 0003 · TypeScript estricto en todo

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
CineExplorer se hizo en JavaScript. Aquí habrá datos de salud y reglas de seguridad.

## Decisión
TypeScript en los cuatro paquetes, con `strict` y `noUncheckedIndexedAccess` en `tsconfig.base.json`.

## Por qué
Atrapa errores antes de ejecutar y es un salto notable para el portafolio.

## Alternativas consideradas
- **JavaScript con JSDoc:** menos configuración, pero menos garantías.

## Consecuencias
Curva de aprendizaje inicial. Los tipos salen de los esquemas Zod para no escribirlos dos veces.
