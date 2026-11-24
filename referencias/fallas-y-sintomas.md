# Fallas y síntomas — cómo se dice vs. dónde se diagnostica

Documento vivo (instrucción de Ernesto, 2026-11-23): los clientes y los técnicos describen las fallas con sus propias palabras, no con el nombre técnico. Esta tabla traduce **lo que la gente dice** a la ficha o código donde se diagnostica. Se nutre con cada falla nueva que se registra en la skill; no se inventan equivalencias: cada renglón apunta a material que ya existe en la documentación.

## Diccionario de interpretación (el mismo de la app)

La app de diagnóstico interpreta la búsqueda con este diccionario de sinónimos; **la skill usa el mismo**: si el técnico o el cliente usa cualquiera de estas palabras, se entiende el término técnico de la primera columna y se busca la falla con ese término.

| Término técnico | También se dice |
|---|---|
| temporizador | timer, reloj, relojes |
| centrifuga / centrifugado | seca, secado, secar, exprime, exprimir |
| drena / drenaje | desagüa, desagüe, descarga, descargar |
| enciende | prende, arranca, arranque, encendido |
| calienta | caliente, calentar, calentamiento, calor |
| enfría | fría, frío, helada, tibia (cuando sale tibia es que no enfría) |
| termostato | termostatos, térmico |
| compresor | refrigeración, refrigerante |
| resistencia | resistencias |
| succión | bomba (en el dispensador, «la bomba» suele ser el problema de succión) |
| flama | llama |
| tapa | puerta |
| batería | pilas, pila |
| válvula | electroválvula, solenoide |
| tarjeta | PCB, placa |
| display | pantalla |
| capacitor | condensador |
| fuga | gotea, goteo, tira agua, charco |
| nivel | presostato |
| ruido | vibra, vibración, zumba |
| apaga | apagado |
| gira | giro, girar |
| llena / llenado | llenar |
| cable | arnés |
| fusible | fusibles |
| chispa | chispea, chispeo, electrodo |
| humo | hollín, tizna |
| explota / explosión | tronido, detonación |
| teclado | botones, membrana, panel |
| escarcha | hielo, congela, congelado |
| quemado | huele (a quemado) |
| reinicia | reinicio, resetea |
| alarma | pita, pitido |

**Reglas de interpretación:**

1. Las frases de relleno no cambian la falla: «no funciona», «no trabaja», «falla», «tiene problema» se ignoran; lo que manda es el **componente o la acción** («no funciona el reloj» = falla del temporizador).
2. Primero se busca la frase en la **correlación de quejas** (más abajo): si la queja está ahí, se va directo a su falla y modelos.
3. Si no está, se interpreta con este diccionario y se busca la ficha por el término técnico.
4. Interpretar no es inventar: si la falla interpretada no tiene ficha ni material documentado, se dice claramente (ver los ⚪ de la correlación).

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

---

# Correlación oficial: quejas del cliente → fallas de diagnóstico → modelos

Fuente: documento de Ernesto **«Mirage_Fallas_por_tipo_de_producto»** (2026-11-23) — la lista de quejas tal como las reporta el cliente, por tipo de producto. Cada queja se correlaciona con la falla de diagnóstico y los modelos donde aplica, **solo con material documentado**:

- ✅ **Con ficha o procedimiento documentado**
- 🔶 **Parcial:** hay componentes, valores o casos documentados, pero no una ficha por síntoma
- ⚪ **Sin diagnóstico documentado todavía** — no se inventa procedimiento; queda registrado como hueco por cubrir

## Lavadora

| Queja del cliente | Correlación | Modelos |
|---|---|---|
| No enciende | 🔶 LMS: fusible 10 A (sin fusible no trabaja nada). LMA: alimentación y tarjeta principal (ella entrega los 110 V a los actuadores) | LMS013M/016M/022M · LMA022G y familia |
| No lava | ✅ LMS: rama de lavado — selector → reloj de lavado → motor de lavado (5.4/5.3/10.7 Ω, capacitor 46 µF). 🔶 LMA: motor y capacitor 60 µF; prueba de lavado en seco del modo test | LMS · LMA022G |
| No seca | ✅ LMS: ficha **No centrifuga / no seca** (§3.10). 🔶 LMA: no avanza a centrifugado → sensor de nivel no reinicia (ficha Nivel de llenado) | LMS · LMA |
| No drena | ✅ LMA: código **E2** (bomba 20–40 Ω en la G, bloqueo, sensor que reinicie). ⚪ LMS sin ficha | LMA022G/M/N |
| No ingresa agua a la tina | ✅ LMA: código **E1** + ficha **Nivel de llenado** (mallas, válvulas ≈1.07 kΩ, manguera del sensor) | LMA022G |
| Se tira el agua | 🔶 LMA: válvula de entrada que no cierra (resorte/diafragma, Módulo 3) y nivel de llenado; sin ficha propia | LMA |
| Despliega código de error / Código de Error | ✅ Tabla de códigos por LED de la LMA022G y `codigos-app-mirage.md`; cada código lleva a su boletín/procedimiento | LMA022G/M/N, LMA017/019, LMA022D |
| Emite ruido inusual | 🔶 LMA: procedimiento «Motor — ruido anormal» (§7). ⚪ LMS sin documentar | LMA022G |
| No termina o interrumpe el ciclo | 🔶 Se relaciona con los tiempos excedidos de **E1** (llenado) y **E2** (drenado); sin ficha propia | LMA |
| Se reinicia ciclo | ⚪ Sin documentar | — |

## Boiler de paso

| Queja del cliente | Correlación | Modelos |
|---|---|---|
| No calienta | ✅ Flujo excesivo (cubeta 19 L en <2 min), presión de gas 11" c.a., caso folio 213843 | Flux gas y Turbo Flux |
| Se apaga y enciende intermitente | 🔶 Sensores de temperatura (boletines E0/E4 del MBF10AD y MBF16AF); caso MBF12AG del folio 214806, causa sin confirmar | MBF10AD, MBF16AF, MBF12AG |
| No enciende | ✅ Baterías (el par >3 V), sensor magnético y su prueba, termostato bimetálico | Flux Blanco MBF06ED/EF y gas en general |
| No hace chispa | 🔶 Módulo de ignición y emisores de chispa (material del MBF16AF; lista de revisión del caso de explosiones) | Turbo Flux, Flux gas |
| Arroja humo | ⚪ Sin documentar | — |
| Explotó | 🔶 Caso MBF06ED con explosiones (reportado 2026-11-13, en investigación): baterías, quemador, emisores, válvula y presión de gas | MBF06ED |
| Código de error | ✅ Boletines por código y modelo (MBF16AF E0–E7; MBF10AD E0–E3/E5; tabla propia del MBF12AG) | Turbo Flux |
| Tira agua | ⚪ Sin ficha documentada | — |
| No sale agua | 🔶 Flujo mínimo de apertura (MBE051G: 1.2 L/min) y sensor de flujo/magnético | Eléctricos y Flux gas |

## Microondas

| Queja del cliente | Correlación | Modelos |
|---|---|---|
| No calienta | 🔶 Módulo 4: cadena de alto voltaje — fusible 15 A, capacitor HV 0.80 µF/2,000 V (descarga obligatoria), diodo HV (un solo sentido), transformador HV y magnetrón; valores documentados, sin ficha por síntoma | Microondas (Módulo 4) |
| No enciende | 🔶 Módulo 4: fusible de entrada 15 A/250 V, switch de monitoreo y switches de puerta | Microondas |
| Hace ruido | ⚪ Sin documentar | — |
| No funciona teclado | ⚪ Sin documentar | — |
| Huele a quemado | ⚪ Sin documentar | — |
| Activa alarma | ⚪ Sin documentar | — |

## Congelador, Refrigerador, Frigobar

| Queja del cliente | Correlación | Modelos |
|---|---|---|
| No enciende | 🔶 Módulo 5: compresor, relé PTC y termostato | Congeladores y refrigeradores |
| No congela | 🔶 Módulo 5: ciclo de refrigeración y rangos por etapa del control (1–7); manual del MRX12FS (solución de problemas) | Congeladores · MRX12FS |
| No enciende luz | 🔶 Congelador: tarjeta de iluminación LED con switch de balín | Congeladores |
| No enfría | 🔶 Ciclo de refrigeración (Módulo 5); manual de servicio del MRX12FS | Refrigeradores · MRX12FS |
| Fuga de gas | ⚪ Sin procedimiento documentado | — |
| Ruido inusual | ⚪ Sin documentar | — |
| No cierra puerta | ⚪ Sin documentar | — |
| Se sobre calienta | ⚪ Sin documentar | — |
| Se congela de más | 🔶 Termostato y rangos del control (Módulo 5) | Congeladores |
| Código de Error | ✅ Solo **MRX12FS**: códigos E1/E5/E7 por LED (`refrigeradores.md`) | MRX12FS |
| Hacer escarcha | ⚪ Sin documentar | — |

## Dispensador

| Queja del cliente | Correlación | Modelos |
|---|---|---|
| No enciende | 🔶 Fusible **5 A** en la caja de controles (MDD30HC/HD) e interruptor | MDD30 · MDD10 |
| No enfría | ✅ Ficha **No enfría el agua** (`dispensadores.md`) | MDD10 · MDD30 |
| No calienta | ✅ Ficha **No calienta el agua** (`dispensadores.md`): termostatos 85/90 °C, resistencia 26/33 Ω | MDD10 · MDD30 |
| Ruido inusual | ✅ Ficha **Hace ruido** (`dispensadores.md`): si el ruido es del compresor, medir su **amperaje y compararlo contra la placa de datos**; amperaje anormal = compresor dañado (Ernesto, 2026-11-24). Si el ruido es al despachar (MDD30), es la bomba/succión | MDD10 · MDD30 |
| Se congela | ⚪ Sin ficha (el termostato de baja del MDD30 está documentado solo como componente) | MDD30 |
| Huele a quemado | ⚪ Sin documentar | — |
| No sale agua | ✅ **Bomba sin succión** (boletín DISX30): vacío y sello de succión; ≈14.5 VCD en la bomba = alimentación buena | MDD30 |
| Fuga agua | ✅ Caso de campo: fuga debajo del depósito de agua fría (orificio central y vástago roscado, Módulo 5 §3.3) | MDD10 |
| Bomba no funciona | ✅ Diagnóstico de la bomba: voltaje en su conector (≈14.5 VCD bueno; 24/40 V o 5/3 V = tarjeta) | MDD30 |

## Campana

Sin diagnóstico documentado: de campanas Velox solo hay **listados de explosivo** en la skill, ningún procedimiento. Quejas del documento: No enciende · No enciende luz · Botones no funciona · Motores no funciona · Turbina con ruido · Huele a quemado. ⚪ Todas pendientes de material.

## Parrilla

Sin diagnóstico documentado: de parrillas Sparx solo hay **listados de explosivo**, ningún procedimiento. Quejas del documento: No hace chispa · No regula gas · Fuga gas · No enciende flama · Huele a quemado · No hay flama. ⚪ Todas pendientes de material.
