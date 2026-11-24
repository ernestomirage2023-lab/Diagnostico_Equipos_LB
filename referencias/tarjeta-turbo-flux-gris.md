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

## Manual del usuario del Turbo Flux 11 L Gris (agregado el 2026-11-20)

Ernesto compartió el **manual del usuario** del Turbo Flux 11 L Gris (MBF12AG / MBF12AH), 28 páginas; vive en Drive, carpeta **Boiler MBF12AG-AH**: https://drive.google.com/file/d/1EpobPrTyNmKkhN1-WLw8p64afjTh-QDM/view?usp=drivesdk

**Conectividad:** el MBF12AG / MBF12AH **tiene WiFi** (confirmado por Ernesto el 2026-11-24), igual que el Turbo Flux 10 L MBF10AD / MBF10AE.

**Especificaciones (capítulo 5):** descarga forzada; operación 115 V~; MBF12AG = gas L.P., MBF12AH = gas natural; piloto de encendido automático; capacidad de prueba 11 L/min; carga térmica 19.2 kW; diferencial de temperatura >25 °C; presión mínima de apertura 2.9 PSI (0.02 MPa); presión máxima de trabajo (agua) 65.26 PSI / 0.45 MPa; presión de operación de gas: **L.P. 2.74 kPa (= 11" c.a.)**, natural 1.76 kPa; eficiencia energética 93 %; intercambiador de cobre libre de oxígeno; conexiones entrada-salida 1/2"; diámetro de chimenea 60 mm; dimensiones 320×510×145 mm; peso 10.78 kg.

**Códigos de diagnóstico oficiales (capítulo 11 del manual):**

| Código | Causa (resumen del manual) | Revisión / solución |
|---|---|---|
| E0 | Sensor de temperatura del agua de salida: conector flojo o mal contacto; sensor dañado (abierto, cortocircuito o piezas metálicas sueltas). | Ajustar el terminal del sensor de salida; reemplazar el sensor si está dañado. |
| E1 | Falla en el sistema de combustión: válvula de gas cerrada; presión o composición del gas anormales (apagado accidental de la llama); falla en la aguja de encendido de la llama o en el cableado. | Abrir la válvula de gas; confirmar tipo y presión de gas; verificar quemador, boquilla, panel de control de aire, válvula proporcional y válvula seccionadora; revisar la aguja de encendido y reemplazar partes defectuosas. |
| E2 | **Velocidad del ventilador anormal**; el pin de retroalimentación está doblado y en contacto con otras partes metálicas; el terminal del pin de retroalimentación está flojo y toca una parte metálica; el cable del pin de retroalimentación está roto. | Verificar que no haya obstrucciones en la chimenea de escape y que la turbina gire libremente; reemplazar el conjunto de la aguja de retroalimentación de encendido si el pin está doblado; insertar el terminal del pin firmemente; verificar si el cable está desconectado y reemplazarlo. |
| E3 | El termostato se activa o el cable está defectuoso; la presión de suministro o la composición del gas no coinciden (combustión anormal); el programa de control o la configuración son incorrectos; el sistema de combustión está dañado. | Verificar el controlador de temperatura o el circuito y reemplazar las partes dañadas; confirmar tipo y presión de gas; comprobar programa y parámetros contra la tabla; revisar el sistema de combustión. |
| E4 | Sensor de temperatura del agua de entrada: conector flojo o mal contacto; sensor dañado. | Ajustar el terminal del sensor; reemplazar el sensor de temperatura de entrada. |
| E5 | Durante la operación no se detectó el cierre del interruptor de presión de viento durante 2 segundos consecutivos (manguera de presión de viento rota); el voltaje de alimentación es demasiado bajo, lo que disminuye la velocidad del ventilador. | Verificar la manguera de presión de viento; confirmar que la fuente de alimentación y el voltaje del ventilador cumplan los requisitos de diseño. |
| E6 | Presión o composición del gas no coinciden; programa de control o parámetros incorrectos; el sensor de temperatura de salida no coincide con la real (la mostrada es mucho más alta); sistema de combustión dañado; aletas del intercambiador mal soldadas (transferencia de calor lenta: tras cerrar la válvula, el agua del tubo se sigue calentando). | Confirmar tipo y presión de gas; verificar programa y parámetros; probar el sensor de salida contra la temperatura real y reemplazarlo si no coincide; revisar el sistema de combustión; detectar aletas mal soldadas y reemplazar las partes dañadas. |
| E7 | El conector de la válvula está flojo o tiene mal contacto; la bobina de la válvula tiene un cortocircuito. | Asegurar el terminal; verificar la bobina de la válvula y reemplazar las partes dañadas. |
| E8 | Fuga en la válvula de gas. | Revisar la válvula de gas. |
| E9 | Falla en encendido de la flama. | Revisar el sistema de encendido. |
| En | Protección del temporizador de funcionamiento de 40 minutos. | Cerrar el grifo para cortar el flujo de agua y, después de unos segundos, abrir la llave nuevamente para reiniciar la protección. |

⚠️ Estos códigos son **del Turbo Flux Gris (MBF12AG/AH)** según su manual; **no** son los mismos significados que los del Turbo Flux MBF16AF (donde, por ejemplo, E2 es fuga en la cámara de combustión). No mezclar las tablas entre modelos.

## Seguridad (del documento)

- El equipo combina electricidad y gas. Antes de desconectar conectores o medir continuidad/resistencia, interrumpir la alimentación eléctrica y cerrar el suministro de gas cuando corresponda.
- Las mediciones energizadas solo deben realizarlas técnicos capacitados, con instrumentos adecuados y siguiendo el procedimiento autorizado.
- **No puentear sensores o protecciones, no forzar electroválvulas y nunca buscar fugas con una llama.**
