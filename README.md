# CSAM IA — Diagnóstico de Línea Blanca Mirage

Skill de diagnóstico técnico para el equipo de los **Centros de Servicio Autorizados Mirage (CSAM)**. El técnico pregunta por un equipo, un código de error o un síntoma, y su asistente lo guía paso a paso con el boletín, el manual, el diagrama eléctrico, el video y la foto de la pieza que correspondan — sin tener que preguntar caso por caso.

## Cómo está organizado el sistema

| Pieza | Dónde vive | Para qué |
|---|---|---|
| La **skill** (texto: reglas, diagnósticos, índices) | Este repositorio de GitHub | Es el conocimiento consultable |
| La **media** (manuales, boletines, diagramas, videos y fotos) | Google Drive, carpeta compartida en solo lectura | 441 archivos; GitHub no guarda binarios |
| El **asistente de cada técnico** | Su propia cuenta de Muse | Localiza el material y lo entrega en la conversación |

## Equipos que cubre

- **Boilers de gas Flux (tiro natural):** Blanco MBF06ED/EF y Rojo MBF06ZB/ZC, MBF10BB/BC/BR y MBF16NB/NC/NG.
- **Boilers Turbo Flux (tiro forzado):** MBF16AF/AG; 10 L WiFi MBF10AD/AE; Gris MBF12AG/AH (también con WiFi).
- **Boilers eléctricos:** MBE051G (1 servicio) y MBE081G (1.5 servicios), con su cableado y protecciones.
- **Lavadoras automáticas LMA** (017D, 019D, 022D, 022G, 022M, 022N) y **semiautomáticas LMS** (013, 016 y 022, series L y M).
- **Dispensadores de agua:** MDD10CB/CS (DISX10) y MDD30HC/HD (DISX30).
- **Microondas:** MWD020E y MWD031E.
- **Congeladores** MCP (10–30 HB), **refrigeradores** MRX y serie REFX, frigobar MRX33ES.
- **Campanas** Velox MCV60/90 y **parrillas** MPS60GB/MPS90GB (listados de piezas).
- **Secadora a gas** SMG022D (listado de piezas).

## Qué trae el repositorio

- **`SKILL.md`** — la skill en sí: identidad **CSAM IA**, reglas de uso y la **personalidad y protocolo de diagnóstico del Ingeniero de Soporte Técnico Mirage** (protocolo en 6 etapas: identificación del equipo, identificación de la falla, análisis técnico, verificación con valores documentados, interpretación de resultados y conclusión), con seguimiento obligatorio al cierre de cada diagnóstico.
- **`referencias/protocolo-seguridad.md`** — la **Política Suprema** de seguridad y hermeticidad que rige a la skill, con prioridad absoluta.
- **`referencias/indice.md` e `indice-drive.md`** — el índice de todo el material y el enlace de Drive de cada archivo.
- **Diagnóstico:** `casos-diagnostico.md` (casos reales confirmados), `fallas-y-sintomas.md` (diccionario síntoma → ficha, con la correlación de las quejas del cliente), `codigos-app-mirage.md` (61 códigos de la app oficial) y las guías por familia (calentadores de paso, lavadoras, microondas, dispensadores, congeladores, refrigeradores), incluida la tarjeta del Turbo Flux Gris con su tabla de códigos propia.
- **Cursos integrados:** Módulo 2 «Calentadores de paso», Módulo 3 «Lavadoras», Módulo 4 «Microondas» y Módulo 5 «Refrigeración doméstica».
- **`referencias/refacciones-lb.md`** — la base de refacciones de línea blanca (988 registros, 713 números de parte, del MASTERDATA oficial): cada pieza con su posición en el diagrama explosivo y su foto. Las **262 fotos viven en Drive** (carpetas «Refacciones LB» y «Refacciones Tienda Mirage»); al cambiar una pieza se muestra su foto para identificarla, y si un número está sustituido se entrega el actualizado.
- **Diagramas explosivos** en texto de más de 25 modelos (`referencias/explosivo-*.md`).
- **`app/`** — la **app CSAM IA** de diagnóstico (un solo HTML, sin internet para consultar): buscador por modelo, código o síntoma, 134 fichas didácticas y botón «Actualizar» que compara su versión contra `app/version.json` de este repositorio.
- **`INSTALACION.md`** — los pasos de instalación y el plan alternativo de descarga completa.

## Cómo trabaja un diagnóstico con la skill

1. Identifica el **modelo exacto** y el código de error o síntoma.
2. Localiza el **boletín** que corresponde y guía la revisión **en el orden del boletín**, con la medición esperada en cada paso.
3. Toda respuesta lleva el **manual del modelo y el diagrama eléctrico**, y explica de dónde salen los voltajes que se miden (las resistencias se miden con el equipo desconectado).
4. Si hay que **cambiar una pieza**, muestra su **foto** y su número de parte vigente.
5. Cierra con conclusión, acción recomendada y **seguimiento** («¿te fue útil?», «¿revisamos alguna foto, video o documento?»).

Nada se inventa: cada valor, código y procedimiento sale de la documentación cargada; si un dato no está documentado, la skill lo dice.

## Instalación (para cada técnico)

1. Entra a **muse.ai** y crea tu usuario.
2. Dile a Muse: **«Instala la skill del repositorio Diagnostico_Equipos_LB»** y autoriza los permisos que pida.
3. Ya queda cargada: pregunta por modelo, código o síntoma.

Si la instalación automática falla, `INSTALACION.md` trae el plan alternativo (descargar el repositorio completo en ZIP).

## Actualizaciones

- Solo **Ernesto y Poly** escriben y actualizan estos documentos; las copias de los técnicos son **de solo consulta**. Quien tenga un caso o un dato nuevo, se lo pasa a Ernesto para incluirlo en la versión oficial.
- Cuando hay material nuevo, se avisa con el mensaje de **«Actualización de documentos»** y cada técnico actualiza su copia; la carpeta de Drive siempre está al día y la app se actualiza con su propio botón.

## Reglas de la casa

- **Confidencialidad:** la skill entrega únicamente el documento, video o foto que el técnico pidió para su diagnóstico, sin compartir datos personales ni la organización interna del material.
- **Formatos que se comparten:** solo material técnico en **PDF, MP4, MOV, JPG o PNG**.
- **Seguridad primero:** mediciones con el equipo desconectado cuando corresponde, nada de anular protecciones ni sensores, y en gas, detección de fugas antes que todo.
