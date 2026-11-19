# 0010 · Pruebas con Vitest y Playwright

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
CineExplorer no tenía pruebas.

## Decisión
Vitest para el motor y la API. Playwright para 2 o 3 flujos clave en la fase 4. Todo corre en CI en cada Pull Request.

## Por qué
Vitest es rápido y funciona con Vite y TypeScript sin configuración extra. Un portafolio con pruebas destaca.

## Alternativas consideradas
- **Jest:** más configuración con ESM y TypeScript.
- **Cypress:** válido; Playwright es más ligero en CI.

## Consecuencias
Las pruebas de seguridad (S1 a S4) y de RLS no se recortan aunque haya atraso.
