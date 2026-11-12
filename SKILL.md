# Diagnóstico de boilers Mirage

## Identificar el equipo

- Pregunta primero el modelo exacto y el código de error en pantalla antes de dar pasos de revisión.

- Ubica el equipo en una de estas familias usando `referencias/indice.md`.

  - Eléctrico de 1 servicio, con el manual MBE051G
  - Eléctrico de 1.5 servicios, con el manual MBE081G y la ficha de los modelos MBE040B y MBE081G
  - Gas LP de Flux Series, con los manuales MBF06ED y MBF06EF del Flux blanco y la serie MBFxxxB y MBFxxxC del Flux rojo
  - 10 litros con WiFi, modelos MBF10AD y MBF10AE
  - Turbo Flux, modelos MBF16AF y MBF16AG, con su diagrama explosivo

## Diagnosticar por código

- Busca el código en `referencias/indice.md` y abre el boletín que corresponde a ese modelo y a ese código.

- Explica la revisión paso a paso, en el orden del boletín, con la medición esperada en cada paso.

- Entrega el PDF del boletín al técnico cuando lo pida, en vez de resumir todo el manual. La media no vive en este repositorio: vive en Google Drive, ver la sección siguiente.

## Qué debe llevar cada respuesta de diagnóstico (regla de Ernesto)

- **El boletín del código, el manual del modelo y el diagrama eléctrico.** No des solo los pasos: acompaña siempre la respuesta con ese material (los enlaces están en `referencias/indice-drive.md`).

- **De dónde salen los 110 V.** En estos equipos todos los elementos y bobinas (válvulas, bomba, seguro de tapa, motor) trabajan con **110 V**, y ese voltaje sale de la tarjeta: la alimentación de 110 V entra a la tarjeta principal y la tarjeta lo entrega a cada elemento. Al diagnosticar, indica en qué punto del diagrama se revisa la salida de 110 V hacia el elemento sospechoso.

- **Las mediciones de resistencia se hacen siempre con el equipo desconectado.**
- **Si el diagnóstico indica cambiar una pieza, muestra la foto de esa pieza.** Cuando la conclusión sea reemplazar un componente (tarjeta, bomba, retractor, termostato, sensor, válvula, etc.), entrega también su foto desde `referencias/indice-drive.md` cuando exista, para que el técnico identifique la pieza exacta antes de cambiarla, y di qué medición confirma que esa pieza es la falla.

## Códigos con más de un boletín

- Lee `referencias/guia-rapida-turbo-flux.md` cuando un Turbo Flux marque E1, E3 o E6.

- Pregunta qué revisión va a hacer antes de elegir el boletín, porque cada código tiene variantes con mediciones distintas.

- Da solo el boletín de la variante elegida, por ejemplo el E3 de válvula o el E6 de vacío.

## Casos confirmados por Ernesto

- Lee `referencias/casos-diagnostico.md` cuando el síntoma no sea un código de error, por ejemplo que el equipo hace chispa y la flama sigue encendida.

- Son casos reales ya validados por Ernesto, con su criterio de diagnóstico. Aplícalos tal cual antes de improvisar otra ruta.

## Calentadores de paso (curso de Ernesto)

- Lee `referencias/calentadores-de-paso.md` para los fundamentos de los calentadores de paso del curso de capacitación de Ernesto (Módulo 2): componentes y lógica de encendido, importancia del flujo (diseño 5–6 L/min, prueba de la cubeta de 20 L), presión de gas de trabajo (2.74 kPa = 11 pulgadas de columna de agua), diagnóstico por síntoma del gas LP de 1 servicio, pruebas del eléctrico de 1.5 servicios (triac, resistencia 4–7 Ω, sensor NTC de 47 kΩ a 25 °C) y el mantenimiento con descalcificado del intercambiador.
- Este documento complementa los boletines y los casos confirmados; si el boletín del modelo dice otra cosa, manda el boletín del modelo.
- Los valores marcados con ⚠️ en el documento están **por confirmar**: avísalo cuando los uses.
- **Nunca sugieras quitar el apagado automático de 20 minutos** de los equipos de gas: es una norma de seguridad.

## Media en Google Drive

- Toda la media (PDFs y videos) vive en la carpeta compartida de Google Drive de Ernesto, «Github / Boiler de paso»: https://drive.google.com/drive/folders/1AqTHFo0pSG_mzXwL9D6HbnqI1cgAWVcv — compartida con enlace, solo lectura, para el equipo.

- Busca el enlace directo de cada archivo en `referencias/indice-drive.md` y entrega ese enlace al técnico para que lo baje o lo vea. Ese es el medio de entrega, no los archivos del repositorio.
- **Fotos de componentes (regla de Ernesto):** si el técnico pregunta cómo es una pieza, muéstrale su foto de Drive desde el índice. Ejemplo: el **módulo de ignición del MBF16AF (Turbo Flux)** tiene fotos en la carpeta Boiler MBF16AF: el módulo en la mano con su arnés, el módulo ya instalado, el conector del display (5 V, CN9) y la medición de su alimentación de línea (122.5 V CA).

- Actúa como el medio entre el técnico y ese conocimiento: el técnico pregunta por modelo y código, tú ubicas el boletín o video correcto y lo entregas, sin que él tenga que buscar en carpetas.

## Videos de procedimiento

- Consulta la lista de videos en `referencias/indice-drive.md` cuando el técnico necesite ver el procedimiento, y entrégale el enlace de Drive del video correcto.

- Los videos viven en Drive por su peso (hay uno de 1.87 GB), así que nunca intentes bajarlos del repositorio.

## Códigos de la app oficial de Mirage

- Lee `referencias/codigos-app-mirage.md` para el resumen de códigos de la app oficial de Mirage en Línea Blanca (11 equipos) y su cruce con los boletines: qué códigos empatan con boletín, cuáles solo están en la app (p. ej. el nE de Turbo Flux y las lavadoras LMA017/LMA019/LMA022D/LMA022M/LMA022N) y cuáles solo están en el archivo (MBF10AD y MBE051G, que la app no cubre).

- La app es resumen oficial; cuando un código tenga boletín, manda el procedimiento del boletín, que trae las mediciones.

## Lavadoras Mirage

- Lee `referencias/lavadoras-mirage.md` cuando la falla sea de una lavadora Mirage: semiautomáticas de doble tina LMS-013M, LMS-016M y LMS-022M, y automática análoga de 22 kg LMA022G.

- Ese documento trae componentes, valores de medición, diagramas, códigos de error, modo test y procedimientos de diagnóstico por código, de la capacitación 2025 de Ernesto.

## Categorías nuevas (en preparación)

- A petición de Ernesto (2026-11-12), la skill se amplía a más línea blanca. Ya existen las carpetas en Drive y las referencias, **aún sin material**: **Dispensadores** (`referencias/dispensadores.md`), **Microondas** (`referencias/microondas.md`), **Congeladores** (`referencias/congeladores.md`) y **Refrigeradores** (`referencias/refrigeradores.md`). Su media vivirá en las carpetas del mismo nombre en la raíz de la carpeta «Github» de Drive, registradas en `referencias/indice-drive.md`.
- Si preguntan por un equipo de estas categorías, di que la categoría está en preparación y todavía no hay material cargado; no inventes códigos ni procedimientos para ellas.

## Huecos conocidos

- Avisa que al modelo de 10 litros con WiFi le falta el boletín del código E4, porque solo hay E0, E1, E2, E3 y E5.

- Di con claridad cuando un modelo o código no tenga boletín en el repositorio, en vez de aplicar el boletín de otro modelo.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.
