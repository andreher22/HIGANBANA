# Aviso de privacidad · BORRADOR v0.1

> ⚠️ **Borrador de trabajo, no es el aviso final.** Antes de abrir la app al público debe
> revisarlo una persona con conocimiento legal en protección de datos.
> Marco de referencia: **Ley Federal de Protección de Datos Personales en Posesión de los
> Particulares (LFPDPPP)**, publicada en el DOF el 20 de marzo de 2025, que abroga la ley de 2010.
> Los campos entre `[corchetes]` faltan por definir.

### Pendientes de verificar antes de publicar

- [ ] Leer el texto oficial de la ley en el DOF, sobre todo el artículo 15 (contenido mínimo del aviso) y las reglas de consentimiento para datos sensibles (si debe ser **expreso y por escrito**, y si una casilla en línea es suficiente).
- [ ] Confirmar cuál es la autoridad vigente (las funciones del INAI se transfirieron) y cómo se le contacta.
- [ ] Confirmar si existen nuevos lineamientos o reglamento posteriores a la ley de 2025.
- [ ] Definir responsable, domicilio y correo de contacto.
- [ ] Confirmar proveedores y dónde se alojan los datos (Supabase, Vercel, Sentry) y su región.

---

## 1. Quién es responsable de tus datos

**[Nombre de la persona responsable]**, desarrolladora de Higanbana, con domicilio para oír y
recibir notificaciones en **[domicilio]**, es responsable del tratamiento de tus datos personales.

Contacto para cualquier tema de privacidad: **[correo de privacidad]**

Higanbana es una aplicación **gratuita** y sin fines de lucro. No vendemos ni rentamos tus datos.

## 2. Qué datos pedimos

### Datos personales
- Nombre y correo electrónico (para tu cuenta).
- Fecha de nacimiento (para verificar que tienes 18 años o más).
- Sexo (puedes elegir "prefiero no decir").
- Dónde entrenas, equipo disponible, días y minutos por semana, experiencia y objetivo.
- Tus sesiones completadas, series, repeticiones y pruebas de atleta.

### Datos personales sensibles (salud)
Los siguientes datos son **sensibles**. Solo los tratamos si das tu **consentimiento expreso**,
en una casilla aparte que no viene marcada:

| Dato | ¿Obligatorio? | Para qué |
|---|---|---|
| Preguntas de seguridad: condición del corazón, presión alta, diabetes o enfermedad renal; síntomas al hacer esfuerzo; embarazo o parto reciente; lesión o cirugía reciente | **Sí**, para generar una rutina | Decidir si puedes empezar sola/o o si conviene consultar antes con un profesional de la salud |
| Zonas con dolor | Opcional | Quitar o sustituir ejercicios que carguen esa zona |
| Horas de sueño y cómo te sientes cada día | Opcional | Ajustar la intensidad de la sesión de ese día |
| Ciclo menstrual (fecha de inicio, duración, regularidad, síntomas) | Opcional | Sugerir ajustes según cómo te sientes |
| Peso y medidas corporales | Opcional | Mostrarte tu tendencia a lo largo de las semanas |
| Dolor reportado durante un ejercicio | Opcional | Ofrecerte una alternativa y mejorar las fichas |

**No pedimos** fotos, ubicación, datos bancarios ni datos de nutrición.
Las fotos de progreso, si las tomas, se quedan solo en tu teléfono.

## 3. Para qué usamos tus datos

**Finalidades necesarias** (sin ellas no podemos darte el servicio):
1. Crear y administrar tu cuenta.
2. Revisar que sea seguro que empieces a entrenar con la app.
3. Armar tu rutina por bloques A, B y C y ajustarla a tu perfil.
4. Guardar tu historial y mostrarte tu progreso.

**Finalidades secundarias** (puedes negarte y seguir usando la app):
5. Calcular estadísticas **agregadas y anónimas** para saber si la app funciona (por ejemplo, cuántas personas completan 4 semanas). Nunca se revisan registros individuales de salud.
6. Enviarte encuestas sobre tu experiencia.

Para negarte a las finalidades secundarias: **[cómo: opción en configuración o correo]**.

## 4. Con quién compartimos tus datos

**No vendemos, rentamos ni compartimos tus datos con fines comerciales.**

Para que la app funcione, usamos proveedores que almacenan o procesan datos por cuenta nuestra
y solo siguiendo nuestras instrucciones:

| Proveedor | Para qué | Región |
|---|---|---|
| Supabase | Base de datos y autenticación | [por confirmar] |
| Vercel | Alojamiento de la app | [por confirmar] |
| Sentry | Registro de errores técnicos (sin datos de salud) | [por confirmar] |

## 5. Cómo protegemos tus datos

- Cada persona solo puede ver sus propios datos (Row Level Security en la base de datos).
- Las conexiones van cifradas (HTTPS).
- El panel de administración solo muestra totales, nunca registros individuales de salud.
- Los reportes de errores no incluyen datos de salud.

## 6. Tus derechos (ARCO) y cómo ejercerlos

Tienes derecho a **Acceder** a tus datos, **Rectificarlos**, **Cancelarlos** y **Oponerte** a su
uso, así como a **revocar tu consentimiento**.

Dentro de la app puedes:
- **Descargar mis datos** (archivo con toda tu información).
- **Borrar datos de salud opcionales** (ciclo, medidas, sueño) en cualquier momento.
- **Retirar tu consentimiento de datos de salud.** Si lo retiras, dejamos de usar esos datos y ya no podemos generar rutinas automáticas.
- **Borrar mi cuenta**: se eliminan todos tus datos.

También puedes escribir a **[correo de privacidad]** indicando tu nombre, el correo de tu
cuenta y qué derecho quieres ejercer. Responderemos en un plazo de **[plazo según la ley]**.

## 7. Cuánto tiempo guardamos tus datos

Mientras tengas tu cuenta activa. Si borras tu cuenta, tus datos se eliminan
**[plazo: inmediato / en X días para respaldos]**.
El historial de consentimientos se conserva **[plazo]** como prueba de que diste o retiraste tu consentimiento.

## 8. Menores de edad

Higanbana es solo para personas de **18 años o más**. No generamos cuentas para menores de edad.

## 9. Higanbana no es un servicio médico

Higanbana da orientación general de entrenamiento y **no sustituye la consulta con un
profesional de la salud**. No diagnostica, no da tratamiento y no hace planes de nutrición.

## 10. Cambios a este aviso

Si cambiamos este aviso, te avisaremos dentro de la app. Si el cambio implica usar tus datos
para algo nuevo, te pediremos tu consentimiento otra vez.

**Versión:** 0.1 (borrador) · **Última actualización:** [fecha]

---

## Notas para el desarrollo

- La versión de este aviso se guarda en `consentimientos.version_aviso` (ver [modelo de datos](modelo-de-datos.md)).
- El aviso se muestra **antes** del registro. El consentimiento de salud es una **casilla separada, sin marcar**.
- Retirar el consentimiento agrega una fila con `aceptado = false`; no se edita la anterior.
- Si se agrega una finalidad nueva, hay que pedir el consentimiento otra vez.
