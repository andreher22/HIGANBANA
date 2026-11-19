# 0002 · Monorepo con pnpm workspaces

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
El proyecto tiene cuatro partes que comparten código: web, API, motor de reglas y esquemas.

## Decisión
Un solo repositorio con pnpm workspaces: `apps/web`, `apps/api`, `packages/shared`, `packages/engine`.

## Por qué
Maneja varios paquetes en un repo sin herramientas extra, y los esquemas se comparten sin publicarlos.

## Alternativas consideradas
- **Varios repositorios:** duplicar configuración y sincronizar versiones a mano.
- **npm/yarn workspaces o Turborepo:** posibles; pnpm es rápido y estricto con las dependencias. Turborepo se puede sumar si el build crece.

## Consecuencias
El repo no debe vivir en una carpeta sincronizada (OneDrive) cuando se instalen dependencias.
