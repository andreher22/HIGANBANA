# 0009 · Acceso a datos: cliente de Supabase, Drizzle después

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
La API necesita leer y escribir en Postgres.

## Decisión
Empezar con el cliente oficial de Supabase. Pasar a Drizzle si la API crece.

## Por qué
Menos piezas en la fase 1.

## Alternativas consideradas
- **Prisma:** útil, pero más pesado en serverless y requiere el connection pooler de Supabase.
- **Drizzle desde el inicio:** más control, pero más configuración temprana.

## Consecuencias
Las migraciones SQL viven en `supabase/migrations/`, independientes de la librería elegida.
