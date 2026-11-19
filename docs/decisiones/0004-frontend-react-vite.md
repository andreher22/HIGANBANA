# 0004 · Frontend con React + Vite

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
Se necesita una web responsive (mobile-first), que se usa sobre todo desde el celular.

## Decisión
React + Vite, organizado por función: `features/auth`, `features/onboarding`, `features/rutinas`, `features/progreso`. Colores como variables CSS en `styles/tokens.css`.

## Por qué
Es lo que ya se domina y Vite es rápido en desarrollo. Las variables CSS permiten aplicar la paleta de Itzel sin tocar componentes.

## Alternativas consideradas
- **Next.js:** más funciones de servidor, pero se duplicaría el backend (lección de CineExplorer).

## Consecuencias
La API va aparte (ver 0005). TanStack Query recomendado para caché y estados de carga.
