# Lavadoras — Curso de Diagnóstico y Reparación de Equipos de Línea Blanca (Mirage), Módulo 3

> **Fuente:** Módulo 3 del curso, transcrito de los videos de capacitación.
> **Uso en la skill:** validar respuestas técnicas contra este contenido y contra `referencias/lavadoras-mirage.md` (el documento de Ernesto). Si un dato no aparece en ninguno de los dos, la skill debe decir que **no está documentado** y no inventarlo.
> **Nota sobre calidad:** los textos vienen de transcripción automática. Los valores marcados con ⚠️ requieren confirmación contra el video, el manual o medición en campo antes de tomarse como definitivos. La sección «Validación cruzada» registra qué ya se contrastó y qué sigue en duda.

## Estructura del módulo

| # | Lección | Estado |
|---|---------|--------|
| 1 | Tipos y funcionamiento de lavadoras automáticas y semiautomáticas | ✅ Incluida |
| 2 | Tipos de componentes en lavadoras | ✅ Incluida |
| 3 | Revisión de componentes y fallas comunes en lavadoras | ✅ Incluida |
| 4 | Modo Test en lavadoras automáticas | ✅ Incluida |
| 5 | Cuestionario Módulo #3 | ⏳ Pendiente (sin transcripción) |

---

## 1. Tipos y funcionamiento

### Automática vs semiautomática

| Tipo | Funcionamiento |
|------|----------------|
| **Automática** | Los ciclos (lavado, enjuague y centrifugado) se realizan de forma automática, según el ciclo seleccionado. |
| **Semiautomática** | Los ciclos se manipulan de forma manual: el usuario ajusta los tiempos según su preferencia; el lavado y el centrifugado se hacen conforme a la necesidad del cliente. |

### Semiautomáticas (doble tina)

- Capacidades: **13, 16 y 22 kg** (modelos LMS-013M, LMS-016M y LMS-022M).
- Partes externas: panel de control (ahí están los elementos para manipular tiempos, programas, enjuague y tiempos de centrifugado), cubierta de lavado, platina de lavado, base, cubierta de secado y **cubierta de seguridad** (si se abre durante el centrifugado, el equipo se detiene), cable de alimentación y manguera de drenaje.
- Instalación: lugar **resguardado** (sin sol directo, lluvia, nieve ni polvo) y **terreno estable**, para que el equipo funcione correctamente.
- La capacidad de la tina de centrifugado **no** corresponde a la de lavado; el curso remite al manual para las equivalencias de carga por prenda (la diapositiva de equivalencias no se transcribió completa).

### Automática de 22 kg

- Capacidad **22 kg** (LMA022G). Panel de control con: selector de nivel de agua, selector de temperatura de agua, selector de ciclo, selector de opciones, botón de encendido, indicador de estado de ciclo y botón de inicio/pausa.
- Tapa de cristal, tina de acero inoxidable, **modo test**, códigos de diagnóstico en el panel LED, seguro de tapa con seguridad para menores y **sistema por agitador** *(la transcripción decía «sistema fuera jittador»; Ernesto confirmó el 2026-11-12 que es el sistema por agitador, igual que en su documento de lavadoras)*.

---

## 2. Componentes

### Lavadora automática

- **Eléctricos/electrónicos:** dos tarjetas — la **tarjeta del panel** (ciclos y nivel de agua) y la **tarjeta principal** (potencia y programación de los ciclos) —, **sensor de nivel**, **sensor de impacto**, **seguro de tapa** con su **sensor magnético** (detecta la tapa cerrada para proceder con el ciclo) y depósito de detergente en la parte superior.
- **De trabajo:** motor asíncrono, **retractor** (ayuda a la transmisión a liberar la tina para el centrifugado) y **bomba de drenaje**.
- Vista inferior: motor, banda, retractor, transmisión y bomba de agua.

### Lavadora semiautomática (manual)

- **Timers de control** (temporizador de lavado y temporizador de secado), transmisión y **dos motores**: motor de lavado y motor de secado.
- Cada motor lleva su **resorte de suspensión** y el de secado un **freno** que reduce la velocidad al terminar el secado.

### Componentes mecánicos

- No llevan corriente: su diagnóstico es **visual y auditivo** (comportamiento de la transmisión, estado de la banda, suspensión, sensor de impacto).

---

## 3. Revisión de componentes y fallas comunes

### 3.1 Semiautomáticas

#### Motores de lavado y de secado

- Cada motor tiene **dos bobinas** (primaria y secundaria) con un punto común. Se miden con el multímetro en resistencia:
  - Bobina 1 ≈ **5.4 Ω** y bobina 2 ≈ **5.3 Ω** (ejemplo del curso; varía según modelo y capacidad).
  - Entre extremos debe dar **la suma de las dos** (≈ **10.7 Ω** en el ejemplo).
- Revisión visual/auditiva: vibración excesiva, juego o arrastre de la flecha o del cuerpo interno del motor.

#### Temporizador (timer) de lavado

- Alterna el giro del motor: **3 segundos por lado** en ciclo normal y **6 segundos por lado** en ciclo intenso (lo define el selector de ciclo).
- **Falla típica:** gira solo para un lado — el contacto de ese sentido está dañado. Diagnóstico: retirar el timer y medir con continuidad entre el común y cada salida; el contacto debe ir cambiando cada 3 segundos.
- El temporizador de secado es un solo contacto cerrado que energiza el motor de secado (va directo al capacitor y al motor).
- Circuito: la alimentación de **110–120 V** entra directa; hay un switch interno de seguridad dentro del timer.
- **Daño frecuente:** los contactos del timer se queman por **arco eléctrico causado por sobrecarga** (exceso de corriente por exceso de carga). Al reparar conexiones: hacerlas con **soldadura y termofit** (tubo termorretráctil) para evitar futuros cortos, y limpiar las terminales.

#### Suspensión y bota de agua

- La suspensión y la **bota de agua** se dañan por **exceso de carga**: la tina se ladea, la suspensión se rompe y la bota se rasga. Hay que decirle al cliente que el daño es por exceso de carga.

#### Válvula de drenaje (3 vías)

- **Falla:** al llenar la tina de lavado, el agua se pasa a la tina de secado (o no deja de tirar). Causa típica: **suciedad en la válvula** — clips, pelos, basura, pelusa — que impide el sellado. Limpiar la válvula.

### 3.2 Automática (LMA022G)

**Regla de oro del curso:** en cada componente se hace **doble revisión** — el componente **y** que la tarjeta le esté entregando el voltaje. Todos los componentes de la automática trabajan con **110 V** que entrega la tarjeta principal: si no le llega voltaje al componente, la falla puede ser la tarjeta (por ejemplo, un relevador que no hace contacto), no el componente.

#### Motor asíncrono

- Devanados: **4.3 Ω + 4.3 Ω = 8.6 Ω** entre extremos (en el ejemplo del curso se midieron 4.4 / 8.3 / 4.1 Ω).
- Datos del curso: **2/5 HP, 300 W, 120 V, 1600 RPM**, con **protector térmico que actúa arriba de 60 °C** *(confirmado por Ernesto el 2026-11-12; la transcripción traía una frase confusa de «40 grados»)*.
- Fallas: no enciende (revisar voltaje de la tarjeta, capacitor dañado, **resorte de fricción del embrague** atascado, devanado del motor) o hace ruido.
- **Capacitor:** medir capacitancia con el multímetro y comparar contra el valor de su placa (varía por modelo).

#### Válvula de entrada de agua

- Bobina ≈ **1 kΩ**.
- Fallas: no entra agua o no se detiene el ingreso. Revisar: **filtro de entrada tapado con sarro**, bobina en corto, resorte interno o diafragma dañado, fuga en la manguera del sensor de nivel (interruptor de presión).
- La válvula de llenado de **agua caliente** en algunos casos se puede desarmar y limpiar por dentro.
- **Advertencia del curso:** si el cliente no tiene conectada la toma de agua caliente, **no usar las opciones caliente ni tibia**: la bobina se energiza en seco y puede dañar la tarjeta y el equipo.

#### Retractor

- Libera el **cintillo del embrague** para que la tina gire en el centrifugado.
- Fallas: no se activa o no regresa. Revisar: palanca del clutch atorada, que le llegue el voltaje correcto y el motor interno del retractor.
- Resistencia de su bobina: **1.6 kΩ** — confirmado por Ernesto el 2026-11-12 (el curso trae el mismo valor; quedan descartados el 1.09 kΩ marcado por verificar en su documento, el 1.9 kΩ del póster y los 190 Ω de unas láminas).

#### Sensor de nivel

- Es un presostato electrónico: trabaja por diferencia de presión y manda la señal de nivel (bajo, medio, alto) a la tarjeta.
- Medición: **capacitancia entre los terminales 1–2 y 2–3**, y **resistencia entre el 1 y el 3** (el rango de resistencia varía si el sensor tiene agua o no).
- Trae un ajuste central (tipo llave Allen) para subir o bajar el nivel: **la marca no recomienda moverlo**; viene calibrado de fábrica aunque el cliente pida más agua.

#### Bomba de drenaje

- Fallas: fuga de agua, no drena o está atorada (varillas, clips, monedas, basura).
- Revisar: que le llegue el voltaje correcto y la resistencia de su bobina según el modelo (confirmado por Ernesto el 2026-11-12): **LMA022G: 20–40 Ω**; **LMA022M y LMA022N: 15–20 Ω**. En el ejemplo del código E2, el curso midió 15.9 Ω en el equipo mostrado.
- Si la bomba está bien y no recibe voltaje, la falla es la tarjeta.

#### Códigos por LED (panel)

- **E1 — llenado tarda más de 30 minutos.** La válvula está alimentada con 110 V pero no circula agua: llave cerrada, filtros sucios o sarro en la instalación (no siempre es daño de fábrica). Revisar voltaje de la tarjeta y resistencia de la bobina (1 kΩ) de las válvulas de agua fría y caliente.
- **E2 — drenado tarda más de 10 minutos.** Medición de la bomba en su conector (cable naranja contra neutro): ejemplo del curso, **15.9 Ω**; con el equipo encendido en modo test se verifica que la tarjeta entregue voltaje y la bomba trabaje; si se escucha ruido, revisión visual desarmando la bomba.
- **E3 — tapa no cerrada (los dos últimos LEDs).** Revisar la cadena: que la tapa conserve su **imán**, el **sensor magnético** (continuidad: cierra al acercar el imán) y el **seguro de tapa**, al que la tarjeta manda un **pulso momentáneo de 110 V** (en el multímetro puede verse solo una variación, no los 110 V sostenidos). Al levantar la parte superior, cuidado con el **sensor de impacto**, que puede quedar doblado y dañarse.
- **F8 — falla del sensor de nivel.** A veces es solo mal ajuste de terminales o conectores dañados (incluso mordidos por roedores). Medir resistencia y capacitancia en los terminales 1, 2 y 3 del sensor y revisar el conector.

#### Cableado y alimentación

- Revisar el cableado **de punta a punta**: un cable con un solo filamento haciendo contacto puede dar continuidad y aun así fallar en operación.
- La lavadora trae un **fusible en la entrada de voltaje**, dentro del forro del cable de alimentación: si a la tarjeta no le llega corriente, revisar también ese fusible.

---

## 4. Modo Test (automática de 22 kg)

El modo test comprueba si cada componente y ciclo trabaja como debe. Hay tres pruebas; en las tres, primero se **gira la perilla selectora de ciclos hacia abajo** y se **presionan ambos botones**:

| Prueba | Combinación | Qué hace |
|--------|-------------|----------|
| **Lavado en seco** | Perilla de **nivel de agua** hasta **ALTO** | Simula el ciclo de lavado por **≈5 minutos**, girando para ambos lados con diferente intensidad, y cierra el seguro de tapa *(el curso transcribió 3 minutos; Ernesto confirmó el 2026-11-12 que son ≈5, como dice su documento)*. |
| **Centrifugado** | Perilla de **temperatura** hasta **FRÍA** | Activa la bomba de drenado por 5 segundos y simula el centrifugado por 3 minutos. |
| **Llenado de agua** | Perilla de **opciones** hasta **Pre remojo** | Activa las válvulas de llenado por 1 minuto *(la transcripción repetía la combinación del centrifugado; la correcta es la del documento de Ernesto, confirmada por él el 2026-11-12)*. |

---

## 5. Cuestionario Módulo #3

> ⏳ **Pendiente.** No hay transcripción de esta evaluación. Agregar preguntas y respuestas correctas cuando estén disponibles; sirven como base de validación para la skill.

---

## Validación cruzada (hecha por Poly el 2026-11-12 contra el material de Ernesto)

**Confirmado contra `lavadoras-mirage.md` y los casos de la skill:**

- Capacidades semiautomáticas **13, 16 y 22 kg** — la Lección 1 transcribe «tres kilos», pero la Lección 3 dice 13, 16 y 22, y coincide con los modelos LMS-013M/016M/022M.
- Timer de lavado: **3 s normal / 6 s intenso**, contactos café (común) que alternan — igual que el documento de Ernesto.
- La semiautomática es manual de verdad: la energía va **directa del timer a los motores** (110–120 V), sin tarjetas — igual que la definición de Ernesto.
- Motor de la automática: **4.3 + 4.3 = 8.6 Ω** — idéntico al documento y al caso 10 de la skill.
- Válvula de entrada: **1 kΩ** — idéntico (medido 1.073/1.077 kΩ en campo).
- Sensor de nivel: capacitancia en dos pares y resistencia entre extremos — mismo procedimiento del documento (40–50 nF y 20–40 Ω).
- E3 con los **dos últimos LEDs** y la cadena imán → sensor magnético → pulso de 110 V al seguro — idéntico al caso 9 de la skill y al diagnóstico por video del 2026-11-12.
- **E1 llenado > 30 minutos**: el curso lo respalda (la tabla del documento que decía 5 minutos queda descartada; la app de Mirage también marca >30 min).
- La válvula de drenaje de la semiautomática que se pasa por suciedad (clip/pelusa) coincide con las fotos de Ernesto de la válvula LMS tapada con pelusa.

**Dudas resueltas por Ernesto (2026-11-12):**

1. **Retractor: 1.6 kΩ** — el valor del curso es el bueno; descartados 1.09 kΩ, 1.9 kΩ y 190 Ω.
2. **Bomba de drenaje por modelo:** LMA022G **20–40 Ω**; LMA022M y LMA022N **15–20 Ω**.
3. **Modo test, lavado en seco: ≈5 minutos** — manda el documento de Ernesto; los «3 minutos» eran error de transcripción.
4. **Modo test, llenado:** es otra perilla — la de **opciones en Pre remojo** (como dice su documento).
5. **Motor de la automática:** la protección es el **protector térmico, que actúa arriba de 60 °C**.
6. **Lección 1:** «sistema fuera jittador» es el **sistema por agitador**.

**Pendiente:** la diapositiva de equivalencias de carga por prenda de la Lección 1 quedó cortada en la transcripción; falta su documento fuente.

## Reglas para la skill

1. Responder y validar con base en este documento, `referencias/lavadoras-mirage.md`, los boletines y los casos confirmados; citar la fuente.
2. Si algo no aparece, decir que **no está documentado**.
3. No recomendar ajustar la calibración del sensor de nivel: la marca no lo recomienda.
4. Para valores marcados con ⚠️, indicar que están pendientes de confirmación.
5. En toda revisión de componente de la automática, aplicar la doble revisión: componente **y** voltaje de 110 V que entrega la tarjeta.
