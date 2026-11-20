# Acuerdos de trabajo

Cómo trabajamos juntas en Higanbana. Si algo cambia, se actualiza aquí con un Pull Request.

## Equipo

| Persona | Rol | GitHub |
|---|---|---|
| Andrea | Desarrollo: código, base de datos, motor de reglas, despliegue, documentación técnica | [@andreher22](https://github.com/andreher22) |
| Itzel | Diseño: identidad de marca (logo, paleta, tipografía, ilustraciones), redes sociales y algunas tareas en el repo | [ItzelGalvanContreras](https://github.com/ItzelGalvanContreras) |

## Qué entrega cada una

**Itzel**
- Logo de Higanbana y sus variantes (primera entrega: noviembre 2026).
- Paleta de colores final, siguiendo el brief: dos tonos por color y contraste mínimo de 4.5:1 en texto.
- Tipografía, ícono de la flor (semilla → brote → flor) e ilustraciones (fase 7).
- Contenido para redes sociales en el lanzamiento (fase 9).
- Formatos preferidos: **SVG** para logo e íconos, **PNG/WebP** para imágenes, colores en **HEX**.

**Andrea**
- La app: web, API, motor de reglas y base de datos.
- Aplicar la identidad de Itzel en la app (variables de color en `tokens.css`).
- Vistas previas por Pull Request para que Itzel revise el diseño sin instalar nada (desde la fase 1).

## Comunicación

- **Canal:** WhatsApp para el día a día.
- **Decisiones importantes:** se anotan en un issue o en `docs/decisiones/` para que no se pierdan en el chat.
- **Puesta al día:** [por acordar: por ejemplo, una llamada corta al cerrar cada fase].

## Cómo revisamos

- Itzel es colaboradora del repo y puede comentar issues y Pull Requests.
- Para cambios visuales, Andrea le comparte el PR (y su vista previa de Vercel, desde la fase 1) e Itzel deja comentarios ahí.
- Un cambio de diseño se fusiona cuando Itzel lo aprueba o lo comenta como listo.

## Cómo trabajamos en el repo

Las dos seguimos el mismo flujo (ver [decisión 0001](decisiones/0001-flujo-de-ramas.md)):

1. Tomar un issue del tablero **Higanbana · Roadmap** y moverlo a *In Progress*.
2. Crear una rama desde `develop`: `tipo/numero-descripcion` (ej. `feat/20-agregar-logo`).
3. Commits con formato `tipo: descripción`.
4. Pull Request con **base `develop`** y la plantilla llena (`Closes #N`).
5. Merge, borrar la rama y cerrar el issue.

Itzel tendrá issues asignados en algunas fases para practicar GitHub.
**Nunca** se trabaja directo en `main` ni en `develop`.

## Créditos

- **Por ahora:** Itzel aparece en el README como autora de la marca e identidad visual.
- **Portafolio:** Higanbana es un proyecto en conjunto. Las dos pueden mostrarlo en su portafolio, cada una describiendo su parte.
- La identidad visual (logo, paleta, ilustraciones) la diseña Itzel y tiene todos los derechos reservados; el código es MIT (ver [README](../README.md#licencia)).
