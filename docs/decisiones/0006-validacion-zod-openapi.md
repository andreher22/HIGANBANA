# 0006 · Zod compartido y documentación OpenAPI

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
En CineExplorer el esquema de login estaba copiado 3 veces y con reglas distintas.

## Decisión
Esquemas Zod en `packages/shared`, usados por la web, la API y el motor. La API se documenta con `@hono/zod-openapi` + Swagger UI.

## Por qué
Una sola fuente de verdad: los mismos esquemas validan y documentan.

## Alternativas consideradas
- **Escribir la documentación OpenAPI a mano:** se desactualiza.

## Consecuencias
Cualquier cambio en la forma de los datos empieza en `packages/shared`.
