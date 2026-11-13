# Tarjeta electrónica del Turbo Flux Gris (MBF12AG y MBF12AH)

Documento de Ernesto: «Tarjeta_electr_nica_Turbo_Flux_MBF12AG-AH.pdf», recibido el 2026-11-13 con la etiqueta «Revision y componente MBF16AG Y MBF12AH». El documento indica como modelos **MBF12AG y MBF12AH** (Turbo Flux Gris). Método que indica: revisión de componente, 40 minutos.

El PDF vive en Google Drive, carpeta **Boiler MBF12AG-AH**: https://drive.google.com/file/d/1knh9j2-Et09R6VWREllxY4Ub8S876Ysb/view?usp=drivesdk (ver también `referencias/indice-drive.md`).

## Identificación de componentes en la tarjeta

El diagrama del documento ubica en la tarjeta electrónica las conexiones de los principales componentes:

| Componente | Función orientativa | Puntos de revisión |
|---|---|---|
| Alimentación AC, 120 V | Suministra energía eléctrica a la tarjeta. | Verificar alimentación, conexión firme y señales de calentamiento. |
| Termostato bimetálico (de gas) | Elemento de protección térmica. | Revisar continuidad con el equipo desenergizado y según procedimiento del fabricante. |
| Motor extractor de gases | Apoya la extracción de los gases de combustión. | Inspeccionar conector, cableado, obstrucciones y funcionamiento durante el arranque. |
| Capacitor de 1.5 µF | Componente asociado al motor extractor en el diagrama. | Comprobar estado físico y capacitancia con instrumento adecuado, tras aplicar el procedimiento seguro de descarga. |
| Electroválvulas solenoides de gas | Controlan eléctricamente el paso de gas. | Revisar conectores y cableado; confirmar la activación mediante el procedimiento autorizado. |
| Emisores de chispa | Producen la chispa de encendido. | Revisar aislamiento, conexiones, electrodos y posición conforme al manual. |
| Sensor de flama | Detecta la presencia de llama. | Inspeccionar limpieza, posición, aislamiento y cableado. **No puentear la protección.** |
| Sensor de flujo de agua | Detecta demanda o circulación de agua. | Revisar conector y comprobar que exista flujo suficiente; medir según especificación. |
| Termistores de entrada y salida de agua | Miden la temperatura del agua antes y después del calentamiento. | Revisar conectores y comparar resistencia con la tabla temperatura-resistencia del fabricante. |
| Display | Interfaz de visualización del equipo. | Revisar el conector y el cableado conforme al manual de servicio. |

## Valores que trae el diagrama

- **Alimentación de la tarjeta: 120 V CA.**
- **Termistor de entrada de agua: 10 kΩ.**
- **Termistor de salida de agua: 10 kΩ.** (Consistentes con los boletines E0 y E4 del Turbo Flux MBF16AF, que marcan NTC de 10 kΩ a 25 °C.)
- **Capacitor del motor extractor: 1.5 µF.**

El documento **no** muestra numeración de terminales, pinout completo, voltajes de salida ni tablas de medición. Esos datos deben confirmarse en la documentación técnica del modelo; **no deben deducirse únicamente por el color de los cables**.

## Secuencia recomendada de revisión (del documento)

1. **Confirmar el síntoma:** registrar si el equipo no enciende, no detecta flujo, no genera chispa, no confirma flama o se detiene durante la operación.
2. **Inspección visual:** buscar terminales flojas, sulfatación, humedad, cables dañados y señales de sobrecalentamiento.
3. **Revisar por circuitos:** comprobar alimentación y conexiones; después evaluar sensores y actuadores de acuerdo con la secuencia descrita en el manual.
4. **Evitar sustituir la tarjeta sin evidencia:** un sensor, el cableado, la alimentación, el motor extractor o el sistema de encendido pueden producir síntomas similares.

## Seguridad (del documento)

- El equipo combina electricidad y gas. Antes de desconectar conectores o medir continuidad/resistencia, interrumpir la alimentación eléctrica y cerrar el suministro de gas cuando corresponda.
- Las mediciones energizadas solo deben realizarlas técnicos capacitados, con instrumentos adecuados y siguiendo el procedimiento autorizado.
- **No puentear sensores o protecciones, no forzar electroválvulas y nunca buscar fugas con una llama.**
