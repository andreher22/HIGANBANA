# 0012 · Despliegue en Vercel

- **Estado:** Aceptada
- **Fecha:** 2026-11-19

## Contexto
Itzel necesita ver los cambios de diseño sin instalar nada.

## Decisión
Dos proyectos de Vercel desde el mismo repo: uno con raíz `apps/web` y otro con `apps/api`. Vista previa automática por Pull Request. Variables de entorno solo en Vercel; en el repo solo va `.env.example`.

## Por qué
Despliegue continuo y una URL por PR para revisar el diseño.

## Alternativas consideradas
- **Netlify:** similar; Vercel ya se conoce por CineExplorer.

## Consecuencias
Activar el límite de gasto en Vercel y las alertas de uso en Supabase desde el primer día.
