# Decisiones técnicas

Cada archivo registra una decisión: qué se eligió, por qué y qué alternativas había.
Formato basado en los ADR (*Architecture Decision Records*).

**Reglas:**
- Un archivo por decisión, numerado: `NNNN-titulo-corto.md`.
- Una decisión aceptada no se borra. Si cambia, se crea una nota nueva que la **reemplaza** y la anterior se marca como `Reemplazada por NNNN`.
- La versión de cada herramienta se anota el día que se instala (las guías cambian seguido).

| # | Decisión | Estado |
|---|----------|--------|
| [0001](0001-flujo-de-ramas.md) | Flujo de ramas: Git Flow simplificado | Aceptada |
| [0002](0002-monorepo-pnpm.md) | Monorepo con pnpm workspaces | Aceptada |
| [0003](0003-typescript.md) | TypeScript estricto en todo | Aceptada |
| [0004](0004-frontend-react-vite.md) | Frontend con React + Vite | Aceptada |
| [0005](0005-api-hono.md) | API con Hono | Aceptada |
| [0006](0006-validacion-zod-openapi.md) | Zod compartido y documentación OpenAPI | Aceptada |
| [0007](0007-motor-de-reglas.md) | Motor de reglas como paquete aparte | Aceptada |
| [0008](0008-supabase.md) | Supabase: Postgres, Auth y RLS | Aceptada |
| [0009](0009-acceso-a-datos.md) | Acceso a datos: cliente de Supabase, Drizzle después | Aceptada |
| [0010](0010-pruebas.md) | Pruebas con Vitest y Playwright | Aceptada |
| [0011](0011-sentry.md) | Errores en producción con Sentry | Aceptada |
| [0012](0012-despliegue-vercel.md) | Despliegue en Vercel | Aceptada |

## Plantilla

```markdown
# NNNN · Título

- **Estado:** Propuesta | Aceptada | Reemplazada por NNNN
- **Fecha:** AAAA-MM-DD
- **Versión:** (se anota al instalar)

## Contexto
Qué problema hay que resolver.

## Decisión
Qué se eligió.

## Por qué
Razones principales.

## Alternativas consideradas
Qué más se evaluó y por qué no.

## Consecuencias
Qué implica (lo bueno y lo que hay que vigilar).
```
