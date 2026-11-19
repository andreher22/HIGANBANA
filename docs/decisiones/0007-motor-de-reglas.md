# 0007 · Motor de reglas como paquete aparte

- **Estado:** Aceptada
- **Fecha:** 2026-11-19
- **Versión:** (se anota al instalar)

## Contexto
Las reglas de seguridad, armado de rutina, ajustes y progresión (estudio de entrenamiento) son el corazón de la app.

## Decisión
`packages/engine` en TypeScript puro: recibe un perfil y devuelve una decisión. No sabe nada de la base de datos ni de la web.

## Por qué
Se prueba rápido y sin servicios externos; los casos del estudio se vuelven pruebas automáticas. Es la pieza estrella del portafolio.

## Alternativas consideradas
- **Reglas dentro de la API:** más difícil de probar y de reutilizar.

## Consecuencias
Cada rutina guarda la versión de reglas con que se generó, para poder explicarla y reproducirla.
