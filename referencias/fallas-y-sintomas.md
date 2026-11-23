# Fallas y síntomas — cómo se dice vs. dónde se diagnostica

Documento vivo (instrucción de Ernesto, 2026-11-23): los clientes y los técnicos describen las fallas con sus propias palabras, no con el nombre técnico. Esta tabla traduce **lo que la gente dice** a la ficha o código donde se diagnostica. Se nutre con cada falla nueva que se registra en la skill; no se inventan equivalencias: cada renglón apunta a material que ya existe en la documentación.

## Equivalencias de términos

| Se dice | Es en realidad |
|---|---|
| «timer», «el reloj» | El **temporizador**: reloj de lavado y reloj de secado en las LMS (§3.6 y §3.7 de `lavadoras-mirage.md`) |
| «no seca» (semiautomática) | **No centrifuga**: la tina de secado extrae la humedad por fuerza centrífuga, sin calor (§3.10 de `lavadoras-mirage.md`) |
| «exprimir» | Centrifugar |
| «no desagüa», «no tira el agua» | No drena (código **E2** en la LMA022G) |
| «se apaga solo a los 20 minutos» (boiler) | **No es falla**: apagado automático por norma (Módulo 2) |

## Lavadoras semiautomáticas LMS

| Síntoma (como se reporta) | Diagnóstico |
|---|---|
| «No centrifuga», «no seca», «la ropa sale muy mojada», «no gira la tina de secado» | Falla **No centrifuga / no seca** (§3.10 de `lavadoras-mirage.md`): rama de secado — fusible 10 A, switch de tapa, reloj de secado, capacitor 18 µF, motor de secado 31/30.5/61.5 Ω, freno |
| «No funciona el timer / el reloj» (de secado) | Mismo §3.10, paso del reloj de secado: continuidad con la perilla en ON, abierto en OFF |
| «Lava solo para un lado», «no hace el vaivén» | Reloj de lavado: contacto de ese sentido dañado; el común debe alternar cada 3 s (Normal) o 6 s (Intenso) entre amarillo y naranja (§3.6 de `lavadoras-mirage.md` y Módulo 3) |
| «No lava ni seca», «no hace nada» | Fusible **10 A / 250 V** abierto: sin fusible no trabaja ninguna de las dos ramas |

## Lavadora automática LMA (LMA022G)

| Síntoma (como se reporta) | Diagnóstico |
|---|---|
| «Llena de más», «no se detiene el llenado», «se pasa de nivel», «llena muy poquito», «no respeta el nivel» | Ficha **Nivel de llenado** (§7 de `lavadoras-mirage.md`): primero el estatus de la **manguera del sensor de nivel** (fuga, tapón, agua atrapada); medición del sensor 40–50 nF y 20–40 Ω; el ajuste Allen **no se mueve** |
| «No drena», «no desagüa», «se queda con agua» | Código **E2** (drenado > 10 min): bomba, bloqueo por suciedad, y que el sensor de nivel reinicie al vaciar |
| «Drena pero no centrifuga / no avanza» | El **sensor de nivel no reinicia** al vaciar (rama del E2, ver Nivel de llenado) |
| «Tarda mucho en llenar» | Código **E1** (llenado > 30 min): mallas/filtros de entrada, presión de agua, bobinas de válvula ≈ 1.07 kΩ, manguera del sensor |
| «Marca F8» | Falla del **sensor de nivel** o su arnés: terminales mal ajustados o conectores dañados (incluso mordidos por roedores) |

## Boilers (calentadores de paso)

| Síntoma (como se reporta) | Diagnóstico |
|---|---|
| «No calienta», «calienta poco», «sale tibia» | Primero **flujo excesivo**: cubeta de 19 L en menos de 2 min (≈9.5 L/min) = no alcanza a calentar; prueba con la llave parcialmente cerrada (caso del folio 213843, en `casos-diagnostico.md`) |
| «No enciende», «no prende» (Flux de gas) | Baterías: el par debe medir **arriba de 3 V**; sensor magnético y su prueba de puente; termostato bimetálico; electroválvulas (diagnóstico por síntoma del Flux Blanco, en `calentadores-de-paso.md` y boletines del MBF06ED) |
| «Hace explosiones» al encender | Caso abierto del MBF06ED: revisar baterías, quemador, emisores de chispa, válvula de gas y presión de gas (**11" c.a. = 2.74 kPa**) |

## Dispensadores

| Síntoma (como se reporta) | Diagnóstico |
|---|---|
| «No sale agua», «no succiona» (MDD30) | Boletín de **bomba sin succión**: primero el **vacío de succión** (sello; si entra aire pierde el vacío) antes de condenar bomba o tarjeta; voltaje en el conector de la bomba ≈ **14.5 VCD** = alimentación buena (bomba nominal 12 VCD) |
| «No calienta el agua», «sale fría por la caliente», «no calienta» | Ficha **No calienta el agua** (`dispensadores.md`): fusible 5 A (MDD30), termostatos de **trabajo 85 °C / protección 90 °C** (continuidad en frío), resistencia **26 Ω (MDD10) / 33 Ω (MDD30)**; en el MDD30 primero confirmar que sí sube agua |
| «No enfría el agua», «no sale fría», «el agua fría sale al tiempo» | Ficha **No enfría el agua** (`dispensadores.md`): ajuste del termostato de frío, ¿arranca el compresor?, medición del compresor MDD10 **10 Ω / 20 Ω** (retirar el relevador térmico); del MDD30 no hay valores de compresor documentados |
