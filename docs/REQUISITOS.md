# Higanbana · Requisitos

> Documento vivo. Fuente: los PDFs de planeación (Plan v1, Plan técnico fases 0 y 1,
> Estudio de entrenamiento por casos y Brief para Itzel). Si algo cambia, se actualiza aquí
> en un Pull Request.

## 1. Qué es

Web app de fitness **gratuita** y **completamente responsive** (se usa sobre todo desde el
celular) para principiantes de 18 a 35 años que entrenan en casa o en el gym y no saben por
dónde empezar. Diferenciador: rutinas por bloques **A, B y C** (método ABCD): si solo hay
15 minutos, se hace el bloque A y el día cuenta.

**No es** una app médica, de nutrición ni de rehabilitación. No promete resultados estéticos.

## 2. Requisitos funcionales (priorizados con ABCD)

### A · MVP (sin esto no hay app)
- RF-01 Registro e inicio de sesión con correo (Supabase Auth).
- RF-02 Aviso de privacidad visible antes del registro.
- RF-03 Consentimiento expreso y separado para datos de salud (casilla sin marcar por defecto), guardado como historial.
- RF-04 Cuestionario de inicio: lugar (casa / gym / ambos), objetivo, días disponibles y preguntas de seguridad.
- RF-05 Filtro de seguridad: menor de 18 bloquea; síntomas con esfuerzo piden consultar a un profesional; embarazo/posparto sin rutina automática; condición cardiometabólica o lesión reciente limitan intensidad.
- RF-06 Catálogo de ejercicios con ficha en texto (posición, pasos, dónde sentirlo, errores comunes, versión fácil/difícil, señal para parar) y su fuente.
- RF-07 Rutina recomendada del día dividida en bloques A/B/C, para casa y gym.
- RF-08 Marcar una sesión como completada (el bloque A cuenta como día completo).
- RF-09 Historial simple de sesiones.
- RF-10 Borrar la cuenta y descargar mis datos.
- RF-11 Aviso visible: la app no sustituye la consulta médica.

### B · Segunda versión
- RF-12 Ajuste opcional por ciclo menstrual (como sugerencia + "¿cómo te sientes hoy?").
- RF-13 Ajuste diario por sueño y por cómo se siente la usuaria.
- RF-14 Gráficas de progreso.
- RF-15 Panel admin solo con totales (nunca registros individuales de salud) y límite de registros con lista de espera.
- RF-16 Objetivos de gym: hipertrofia, fuerza y resistencia.

### C · Cuando ya haya usuarias
- RF-17 Rachas y logros (la flor que abre pétalos: semilla → brote → flor).
- RF-18 Compartir progreso en redes.
- RF-19 PWA con recordatorios.

### D · Delegar
- Identidad de marca, logo, paleta final, ilustraciones y redes: **Itzel**.

### E · Eliminado por ahora
- Feed social, chat, IA generativa, pagos, app nativa.

## 3. Requisitos no funcionales

| ID | Requisito |
|----|-----------|
| RNF-01 | **Responsive mobile-first**: se diseña primero para celular y escala a tablet y escritorio. |
| RNF-02 | Accesibilidad: Lighthouse 90+; contraste WCAG AA (4.5:1 en texto). Los errores llevan ícono y texto, no solo color. |
| RNF-03 | Seguridad: JWT verificado en la API **y** RLS en cada tabla de Supabase. |
| RNF-04 | Ningún secreto en el repo; si falta una variable de entorno, la app no arranca. |
| RNF-05 | Datos de salud tratados como sensibles (ley mexicana de protección de datos): mínimos, opcionales y borrables. |
| RNF-06 | Pruebas: Vitest para el motor y la API; Playwright para 2–3 flujos clave. CI en cada Pull Request. |
| RNF-07 | Monitoreo de errores en producción (Sentry). |
| RNF-08 | Rendimiento móvil aceptable: imágenes optimizadas (WebP) y caché del catálogo. |
| RNF-09 | Escalable: el contenido es dato, no código; reglas versionadas; textos en español e inglés desde el inicio. |
| RNF-10 | Idioma inicial: español. |

## 4. Stack acordado

pnpm workspaces · TypeScript estricto · React + Vite · Hono + Zod (@hono/zod-openapi + Swagger)
· Supabase (Postgres, Auth, RLS) · Vitest + Playwright · Sentry · Vercel · GitHub Actions.

## 5. Dudas abiertas (sección 12 del estudio)

- [ ] ¿Habrá una persona profesional (entrenador/a certificado/a o fisioterapia) que revise el contenido?
- [ ] Edad mínima: ¿18 años?
- [ ] Peso y estatura: ¿opcionales o fuera del MVP?
- [ ] Cardio en el MVP: ¿plan de carrera de 9 semanas o solo caminata y cuerda?
- [ ] Gym promedio en México: ¿qué equipo suponemos?
- [ ] Hipopresivos: ¿en el MVP o después?
