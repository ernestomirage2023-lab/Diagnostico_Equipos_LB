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

## Códigos con más de un boletín

- Lee `referencias/guia-rapida-turbo-flux.md` cuando un Turbo Flux marque E1, E3 o E6.

- Pregunta qué revisión va a hacer antes de elegir el boletín, porque cada código tiene variantes con mediciones distintas.

- Da solo el boletín de la variante elegida, por ejemplo el E3 de válvula o el E6 de vacío.

## Casos confirmados por Ernesto

- Lee `referencias/casos-diagnostico.md` cuando el síntoma no sea un código de error, por ejemplo que el equipo hace chispa y la flama sigue encendida.

- Son casos reales ya validados por Ernesto, con su criterio de diagnóstico. Aplícalos tal cual antes de improvisar otra ruta.

## Media en Google Drive

- Toda la media (PDFs y videos) vive en la carpeta compartida de Google Drive de Ernesto, «Github / Boiler de paso»: https://drive.google.com/drive/folders/1AqTHFo0pSG_mzXwL9D6HbnqI1cgAWVcv — compartida con enlace, solo lectura, para el equipo.

- Busca el enlace directo de cada archivo en `referencias/indice-drive.md` y entrega ese enlace al técnico para que lo baje o lo vea. Ese es el medio de entrega, no los archivos del repositorio.

- Actúa como el medio entre el técnico y ese conocimiento: el técnico pregunta por modelo y código, tú ubicas el boletín o video correcto y lo entregas, sin que él tenga que buscar en carpetas.

## Videos de procedimiento

- Consulta la lista de videos en `referencias/indice-drive.md` cuando el técnico necesite ver el procedimiento, y entrégale el enlace de Drive del video correcto.

- Los videos viven en Drive por su peso (hay uno de 1.87 GB), así que nunca intentes bajarlos del repositorio.

## Huecos conocidos

- Avisa que al modelo de 10 litros con WiFi le falta el boletín del código E4, porque solo hay E0, E1, E2, E3 y E5.

- Di con claridad cuando un modelo o código no tenga boletín en el repositorio, en vez de aplicar el boletín de otro modelo.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.
