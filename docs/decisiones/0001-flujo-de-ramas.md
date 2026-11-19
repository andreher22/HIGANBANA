# 0001 · Flujo de ramas: Git Flow simplificado

- **Estado:** Aceptada
- **Fecha:** 2026-11-19

## Contexto
Dos personas (desarrollo y diseño) y una app que se lanzará a usuarias reales. `main` debe estar siempre estable.

## Decisión
- `main`: solo versiones estables. Recibe cambios únicamente desde `release/*` o `hotfix/*`.
- `develop`: integración. Todo el trabajo se junta aquí primero.
- Ramas de trabajo desde `develop`, con el número del issue: `feat/`, `fix/`, `docs/`, `chore/` (ej. `docs/4-decisiones`).
- Todo entra por Pull Request. Commits con formato Conventional Commits (`tipo: descripción`).
- `main` se queda como rama por defecto en GitHub; al abrir un PR se cambia la base a `develop` (la plantilla de PR lo recuerda).

## Por qué
Separa lo que ven las usuarias de lo que está en construcción, deja historial y revisión de cada cambio, y es un flujo usado en equipos reales.

## Alternativas consideradas
- **GitHub Flow** (solo `main` + ramas): más simple, pero sin una rama de integración antes de producción.
- **Trabajar directo en `main`**: rápido, pero sin revisión ni historial claro.

## Consecuencias
- Los issues no se cierran solos al fusionar en `develop` (GitHub solo lo hace en la rama por defecto): se cierran a mano.
- Las ramas no tienen reglas de protección por ahora; la disciplina es manual. Revisarlo al llegar el CI (fase 1).
