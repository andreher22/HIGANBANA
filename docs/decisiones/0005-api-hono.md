# 0005 · API con Hono

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
CineExplorer tuvo dos backends paralelos (Express local y funciones de Vercel), lo que duplicó trabajo y bugs.

## Decisión
Una sola API con Hono, que corre igual en local (Node) y en Vercel. Toda escritura de datos de la usuaria pasa por la API; leer el catálogo público puede ir directo a Supabase.

## Por qué
Un solo código para ambos entornos. Concentra la lógica importante (plan, límites, panel admin) en un lugar que se puede probar.

## Alternativas consideradas
- **Express:** conocido, pero menos natural en serverless.
- **Solo la API automática de Supabase:** menos trabajo, pero la lógica quedaría repartida en el frontend.

## Consecuencias
La conexión de Hono con Vercel cambia seguido: seguir la guía oficial el día de instalarla.
