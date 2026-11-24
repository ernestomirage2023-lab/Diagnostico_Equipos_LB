# Dispensadores

Categoría creada el 2026-11-12 a petición de Ernesto, dentro del proyecto Diagnostico_Equipos_LB. **Ya tiene su primer material.**

- El contenido técnico de la categoría está en **`referencias/refrigeracion-domestica-modulo-5.md`** (Módulo 5 del curso de Ernesto, compartido con refrigeradores y congeladores): ciclo de refrigeración y la revisión de los dos modelos — **MDD10** (garrafón superior por gravedad: resistencia del tanque caliente 26 Ω, termostatos de 85/90 °C, compresor 10 Ω / 20 Ω) y **MDD30** (garrafón inferior con bomba: resistencia 33 Ω, bomba alimentada a 12 VCD desde la tarjeta; medición de campo de Ernesto en un MDD30HD, 2026-11-19: **14.50 VCD en el conector de la bomba**, con fotos muestra en Drive) —, con las confirmaciones de Ernesto del 2026-11-12.
- **Fusible del DISX30 (MDD30HC/HD): 5 A**, ubicado en la **caja de controles**; el manual indica que puede reemplazarse en caso de que se ponga en circuito abierto (manual del usuario DISX30, pág. 10, «Conexión Eléctrica»).
- La carpeta de Drive **Github / Dispensadores** (https://drive.google.com/drive/folders/1IzJRrikGDn6KNMSjWT6MHGRHIegikE8K) ya tiene 24 archivos registrados en `referencias/indice-drive.md`: manuales Disx10/Disx30 (incluidos el del MDD30HD blanco de garrafón oculto y el del MDD10CS), fichas de especificaciones (DISX30-2025, Disx10, Disx30 rev. 2), diagramas (MDD30HD, eléctrico MDD30HC, explosivo MDD10CB), boletines (bomba sin succión DISX30, alarma de nivel bajo MDD30HC, check valve DISK10), video de la bomba, el video de la llave de agua caliente del MDD10CB y el material del caso **fuga debajo del depósito de agua fría** (documentado en la sección 3.3 del documento del Módulo 5).
- Conforme Ernesto comparta más material de esta categoría, se registrará en `referencias/indice-drive.md` y se documentará aquí, siguiendo las mismas reglas de respuesta de la skill.

## Falla de diagnóstico: no calienta el agua

**Lógica:** el tanque caliente lleva una **resistencia abrazada al tanque** de acero inoxidable, controlada por **termostatos**. El diagnóstico es por eliminación, en este orden (resistencias con el equipo desconectado):

1. **Alimentación:** interruptor de encendido y, en el MDD30 (DISX30), el **fusible de 5 A de la caja de controles** — si está abierto, no llega corriente al área de calentamiento.
2. **Que haya agua en el tanque:** en el MDD30, si la bomba no sube agua (falla de succión/vacío, ver Módulo 5 §3.2), el tanque caliente queda sin agua y no hay nada que calentar. Primero se confirma que el equipo sí sube agua.
3. **Termostatos (MDD10, valores documentados):** son dos — el de **trabajo, 85 °C** (al llegar el agua a esa temperatura abre el contacto y la resistencia deja de calentar) y el de **protección, 90 °C** (si el de trabajo falla o se queda pegado, este corta la corriente a la resistencia). En frío, ambos deben dar **continuidad**; uno abierto en frío = no calienta nunca.
4. **Resistencia del tanque caliente:** **MDD10: 26 Ω** · **MDD30: 33 Ω** (tanque alimentado a 120 V). Abierta o fuera de valor = no calienta.
5. **Voltaje a la resistencia:** si termostatos y resistencia están bien y no llega voltaje, revisar cableado y tarjeta (en el MDD30, la tarjeta display/control).

> En el MDD10, el **indicador de estatus** muestra si el equipo está calentando: si el indicador marca calentando y el agua sale fría, la falla está en resistencia o termostatos, no en la orden de encendido. Del MDD30 no hay valores de termostato documentados; los 85/90 °C documentados son del MDD10.

## Falla de diagnóstico: no enfría el agua

**Lógica:** el agua fría la produce el **ciclo de refrigeración** (compresor), controlado por el **termostato de temperatura del agua fría** (en el MDD30 figura además un **termostato de baja**). Diagnóstico en orden:

1. **Que haya agua y que sí suba:** en el MDD30, sin succión (vacío perdido) no hay agua en el tanque frío — revisar primero la bomba y el sello de vacío (Módulo 5 §3.2).
2. **Ajuste del termostato de frío:** verificar que el control de temperatura del agua fría no esté en mínimo o apagado.
3. **¿Arranca el compresor?** En el MDD10, el **indicador de estatus** muestra si el compresor está encendido. Si no arranca: revisar alimentación, el termostato de frío (continuidad) y el relevador térmico.
4. **Medición del compresor (MDD10):** retirar antes el **relevador térmico**; terminales **1–2: 10 Ω**, terminales **2–3: 20 Ω**; entre extremos debe dar la **suma** de los dos devanados. Si la suma no se cumple, devanado dañado.
5. Si el compresor trabaja sin parar y no enfría, el problema pasa al ciclo de refrigeración (ver el ciclo y sus etapas en el Módulo 5) — no condenar piezas sin esa revisión.

> Del MDD30 **no hay valores de compresor documentados** en el material del curso: no se inventan; se diagnostica por arranque, termostato y ciclo.

## Falla de diagnóstico: hace ruido (ruido inusual)

**Lógica:** primero se identifica la fuente del ruido. Si el ruido viene del **compresor** (suena mientras el equipo enfría), la prueba que manda es el **amperaje** (dictada por Ernesto el 2026-11-24):

1. **Medir el amperaje del compresor** con la pinza amperimétrica, con el compresor trabajando.
2. **Compararlo contra la placa de datos** del equipo: el amperaje medido debe corresponder al nominal que marca la placa. No hay un valor universal: cada modelo se juzga contra su propia placa.
3. **Amperaje fuera de lo que marca la placa (consumo anormal) = compresor dañado** — el ruido viene del esfuerzo/devanados del compresor y la solución es el cambio del compresor.
4. **Comprobación complementaria (MDD10):** medir los devanados del compresor (retirando antes el relevador térmico): terminales **1–2: 10 Ω**, terminales **2–3: 20 Ω**; entre extremos debe dar la **suma**. Si la suma no se cumple, devanado dañado.

> Si el ruido es **al despachar o al subir agua** (MDD30), la fuente es la **bomba**, no el compresor: revisar primero el vacío de succión (la bomba se escucha pero no sube el agua, ver «No sale agua» / boletín DISX30) y el voltaje en su conector (≈14.5 VCD = alimentación buena).

## Pieza: llave de agua caliente del MDD10

- **Llave de agua caliente, DISX10 blanco — número de parte MDD10CB-24** (la del gris MDD10CS es la MDD10CS-24). Es la llave original del dispensador **MDD10CB**: cuerpo blanco con **palanca roja** y **seguro** — el seguro se levanta para poder despachar, como protección contra el despacho accidental de agua caliente.
- **Video de la pieza** (Ernesto, 2026-11-24): muestra la llave en la mano, su palanca y cómo se levanta el seguro: https://drive.google.com/file/d/15hO-snWtYdfN4c6XtsDeh89u010uZ_JG/view?usp=drivesdk
- La foto de catálogo de esta pieza en S3 **no existe** (error 403, como varias del MDD10): para identificarla se usa este video.
