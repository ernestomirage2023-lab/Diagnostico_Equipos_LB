---
name: lavadoras-mirage-capacitacion-2025
description: Conocimiento técnico de lavadoras Mirage (semiautomática doble tina LMS-013M/016M/022M y automática análoga 22 kg LMA022G): componentes, valores de medición, diagramas, códigos de error, modo test y lógica de funcionamiento.
---

# Lavadoras Mirage – Capacitación 2025

> Fuente 1: `CAPACITACION_LAVADORAS_2025.pdf` (presentación del Ing. Ernesto Acosta, Ingeniero en Línea Blanca, Mirage).
> Fuente 2: <https://especialistas.mirage.mx/modotestlavadoraautomatica/> (Especialistas Mirage, 13-feb-2025).
>
> Convención de etiquetas: **[PDF]** = viene en la presentación · **[WEB]** = viene de la página de Especialistas · **[INFERIDO]** = deducción mía a partir del diagrama, **debe validarse** · **[VERIFICAR]** = dato ilegible o contradictorio.

---

## 0. Índice

1. Orden del día y alcance
2. Portafolio Mirage mencionado
3. Lavadora semiautomática doble tina (LMS)
4. Lavadora automática análoga 22 kg (LMA022G)
5. Modo test (lavado en seco, centrifugado, llenado)
6. Códigos de error
7. Procedimientos de diagnóstico por código
8. Tabla maestra de valores de medición
9. Lógica de funcionamiento (modelo para memoria)
10. Fallas comunes
11. Pendientes / dudas

---

## 1. Orden del día y alcance [PDF]

- Atención al cliente
- Lavadora doble tina
- Lavadora automática

Mensaje de la sesión (Trabajo en equipo): la fuerza de la empresa está en su mano de obra, apoyada por herramientas y conocimiento adecuados.

## 2. Portafolio Mirage mencionado [PDF]

| Producto | Modelos / detalle |
|---|---|
| Dispensador de agua | DISX 30 (garrafón oculto), DISX 10 |
| Congelador | Congelador HB, de 3.5 a 10 pies |
| Microondas | 0.7 / 1.1 pies |
| Boiler de paso | Combustión 1 y 2 servicios (Gas LP / Gas Natural); Eléctrico 1.5 servicios (FLUX Electric) |
| Lavadoras | Semiautomáticas y automáticas (este documento) |

---

## 3. Lavadora semiautomática doble tina (manual)

**Modelos:** LMS-013M, LMS-016M, LMS-022M (13, 16 y 22 kg). Panel con 4 perillas + 2 botones laterales (5).

**Beneficios comerciales [PDF]:** mayor limpieza, total control, diseño ligero y silencioso, mayor seguridad.

### 3.1 Componentes externos [PDF]

Filtro atrapa pelusa, panel de control, cubierta de lavado, cubierta de secado, cubierta de seguridad, tina de lavado, marco, gabinete, base, cable de alimentación, manguera de drenaje.

**Marcas de llenado (filtro/tina):** altura máxima de contención de agua (H), nivel máximo, nivel medio, nivel bajo.

**Panel de control (numeración del PDF):**

| # | Control |
|---|---|
| 1 | Tiempo de lavado |
| 2 | Programa (normal / lavado intenso) |
| 3 | Ciclo (lavado / enjuague) |
| 4 | Tiempo de secado |
| 5 | Botones/ perillas laterales (ambos extremos) – [VERIFICAR función exacta] |

### 3.2 Instalación [PDF]

- La manguera de drenaje **no debe ser mayor a 3 m** de largo.
- La altura máxima de la manguera de drenaje debe ser **menor a 15 cm**.
- Colocar el extremo de la manguera en un **resumidero o coladera**.
- **No instalar** en: lugares expuestos a luz solar directa, lugares expuestos a lluvia o nieve, terreno irregular o inestable.

### 3.3 Tabla de equivalencias de carga (Anexo A) [PDF]

| Prenda seca | Piezas | Equivalente kg |
|---|---|---|
| Camisas | 3 | 1 |
| Camisas de niño | 5 | 1 |
| Camisetas, calzoncillos | 2 | 1 |
| Cobijas individuales | 1 | 7 |
| Fundas almohadas | 6 | 1 |
| Manteles grandes | 1 | 1/2 |
| Pijama algodón | 1 | 1/2 |
| Ropa de mezclilla | 2 | 3 |
| Toallas de baño grande | 1 | 1 |
| Toalla de lino | 8 | 1 |
| Trajecitos de niño | 5 | 1 |
| Vestidos de mujer | 2 | 1 |
| Traje de adulto | 2 | 2 |
| Pañales de tela | 3 | 1/2 |

### 3.4 Componentes internos [PDF]

Resorte, freno, motor de lavado, motor de secado, temporizador de lavado, temporizador de secado.

### 3.5 Valores de medición de motores (multímetro/pinza) [PDF]

| Componente | Medición (Ω) | Lectura de las 3 combinaciones de cables |
|---|---|---|
| Motor de lavado | 5.4 / 5.3 / 10.7 | dos devanados ≈ 5.3–5.4 y suma ≈ 10.7 |
| Motor de secado | 31 / 30.5 / 61.5 | dos devanados ≈ 30.5–31 y suma ≈ 61.5 |

> Regla práctica **[INFERIDO]**: en motor monofásico con capacitor, la medición entre los dos extremos = suma de las otras dos. Si no se cumple, devanado dañado.

### 3.6 Temporizador de lavado [PDF]

- 3 cables: **café (común)**, **amarillo** y **naranja**.
- Ciclo de contactos con base de **3 segundos**: el común alterna entre amarillo y naranja (ON/OFF alternado) → invierte el sentido del motor/capacitor para el vaivén del agitador.
- Prueba: puntas en café–amarillo y café–naranja; se debe ver continuidad alternada.

### 3.7 Temporizador de secado [PDF]

- 2 cables (rojo-morado). Contacto **OFF → ON → OFF** según la posición de la perilla (OFF al inicio y al final del recorrido, ON durante el tiempo programado).
- Prueba: continuidad con la perilla en ON, abierto en OFF.

### 3.8 Diagrama eléctrico LMS022M [PDF]

- Alimentación **110 V**, **fusible 10 A / 250 V**.
- **Rama de secado:** línea → *switch tapa secado* → *timer de secado* → *motor de secado 110 V* con **capacitor 18 µF**.
- **Rama de lavado:** línea → *selector* → *timer de lavado* → *motor de lavado 110 V* con **capacitor 46 µF**.
- **Selector** (programa): **Normal = 3 seg** / **Intenso = 6 seg** (tiempo de giro antes de invertir).
- Neutro común (línea gris/azul) a ambos motores.
- El PDF marca en rojo dos puntos de revisión: el **bloque de contactos del timer de lavado** y el **selector** (en el selector se muestra lectura **OL** = circuito abierto con el multímetro en una posición).

### 3.9 Fallas comunes (solo imágenes en el PDF) [PDF – VERIFICAR descripción]

Las 5 diapositivas "Casos de fallas comunes" no traen texto. Lo que se ve:

1. Tapa de secado / cubierta de seguridad deformada o con residuo, y fotos de **amortiguadores/hules** de la tina y del soporte (desgaste).
2. **Trampa/codo de drenaje** abierta con **pelusa y residuos** (obstrucción por basura).
3. **Empalmes de cables con termocontráctil amarillo** en el timer (reparaciones previas en cables café/amarillo/naranja) y **contactos de cobre** dentro del interruptor de tapa/secado.
4. **Flecha de transmisión/agitador** de LMS022M (código de pieza `12238000000088`) y LMS016M (código `12238000000065`); base/agitador de la tina con 3 círculos azules.

---

## 4. Lavadora automática análoga 22 kg (LMA022G)

**Descripción comercial [PDF]:** fáciles de manejar, no maltratan la ropa, **tina vertical de acero inoxidable de 22 kg**, **control analógico**, tapa de cristal.

**Características:** Test Mode, ciclo ecológico, lavado rápido, diseño elegante, App Library, auto limpieza, llenado inteligente, protección a menores, sistema por agitador.

### 4.1 Panel de control [PDF]

| # | Control | Opciones |
|---|---|---|
| 1 | Selector de nivel de agua | Auto, alto, medio, bajo |
| 2 | Selector de temperatura | Temperatura directa: fría / tibia / caliente |
| 3 | Selector de ciclo | Ropa blanca, ropa de color, ropa deportiva, lavado rápido, normal, lavado ecológico, súper lavado, cobijas/edredones, solo lavado, solo centrifugado, remojo, enjuague centrifugado, lavado de tina. Secuencia indicada: *remojo → lavado → enjuague → centrifugado → seguro* |
| 4 | Selector de opciones | OFF, pre remojo, ciclo suavizante [VERIFICAR texto], centrifugado extra |
| 5 | Botón de encendido | — |
| 6 | Indicador de estado de ciclo | LEDs de avance |
| 7 | Botón inicio/pausa | — |

### 4.2 Componentes [PDF]

- **Electrónica:** tarjeta de panel, tarjeta principal.
- **Sensores:** sensor de nivel de agua, sensor de impacto, doble sensor de seguridad + seguro de tapa, sensor magnético.
- **Actuadores:** válvulas de entrada (fría, caliente, suavizante), bomba de drenaje, retractor, motor asíncrono.
- **Mecánica:** transmisión/embrague, banda Poli V, suspensión delantera (resorte), suspensión trasera (varillas con resorte), tina de acero inoxidable, tapa de cristal, depósito para detergente.

### 4.3 Datos de placa del motor [PDF]

Welling **YXB300-4**, monofásico de inducción, **2/5 HP (300 W), 120 V / 60 Hz, 4.5 A, 1600 RPM**, protección térmica, capacitor **60 µF / 300 V**, máx. 40 °C ambiente. Advertencia: desconectar la lavadora antes de dar servicio.

### 4.4 Conectores de la tarjeta principal (según diagrama de funcionamiento) [PDF]

| Conector | Pines | Conecta con |
|---|---|---|
| CN1 | L, N | Alimentación 110 V |
| CN2 | 12V, TXD, RXD, GND, 5V, NC | Panel de control (comunicación) y sensor de nivel |
| CN3 | DJ+, JS, PS, DJ− | Motor (L1/L2) y retractor |
| CN4 | + / − | Seguro de tapa (bobina) |
| CN5 | XDJ, RJS, SPS | Válvulas (fría, suavizante, caliente) y bomba |

> La asignación fina de pines a cada carga es **[INFERIDO]** del diagrama; validar contra la tarjeta real.

---

## 5. Modo test – lavadora automática 22 kg [WEB]

> Es una obligación del técnico conocerlo. La **prueba de lavado en seco** es obligatoria al instalar (muestra al usuario que la lavadora funciona correctamente). Centrifugado y llenado son "casi obligatorias".

### 5.1 Entrar al modo test (común a las 3 pruebas)

1. Girar la **perilla principal (ciclos)** a cualquiera de las **3 posiciones de abajo** (donde no hay ciclo).
2. Presionar **primero encendido** y luego **inicio de ciclo**, rápidamente. Los LEDs se quedan encendidos = ya estás en modo test.

### 5.2 Prueba de lavado en seco

3. Girar la **perilla de nivel de agua a ALTO**. El LED de lavado parpadea, **cierra el seguro de tapa** y arranca un ciclo de lavado de **≈ 5 minutos**.

### 5.3 Prueba de centrifugado (valida transmisión y bomba)

3. Girar la **perilla de temperatura a FRÍA**. El LED de centrifugado parpadea → se activa el **seguro de tapa** → entra la **bomba de drenado** → la **tina gira rápido** (transmisión correcta).

### 5.4 Prueba de llenado (valida entrada de agua)

3. Girar la **perilla de opciones a Pre remojo**. *(La página termina aquí; el resultado esperado — llenado normal de la tina — se infiere del título de la prueba. [VERIFICAR con el video])*

### 5.5 Comentarios de técnicos en la página [WEB]

- *Enciende pero no deja seleccionar ciclo ni detecta cierre de tapa* → revisar primero **seguro/sensor de tapa y su cableado**; si están bien, probable falla de **tarjeta de control**.
- *El seguro se quita y no centrifuga* → pregunta sin respuesta publicada.

---

## 6. Códigos de error (LMA022G) [PDF]

| Código | Situación | Patrón LED (6 LEDs, ○ apagado · ◎ intermitente · ● encendido)* |
|---|---|---|
| **E1** | Baja presión de agua o falla de electroválvula por más de 5 min | ○○○○○◎ |
| **E2** | Tiempo de drenado mayor a 10 min; sensor de nivel no se ha reiniciado | ○○○○◎○ |
| **E3** | La tapa no está cerrada para iniciar | ○○○○◎◎ |
| **E4** | Unidad desequilibrada en modo centrifugado | ○○○◎○○ |
| **E5** | Exceso de vibración en el proceso de secado | ○○◎●◎● |
| **F5** | Falla en detección de la carga | ○○◎○◎○ |
| **F8** | Falla del sensor de nivel de agua | ○○◎◎○○ |
| **Fd** | Falla el seguro de la tapa | ○○◎○○◎ |

\* Patrones transcritos de la imagen; **[VERIFICAR]** posición exacta de cada LED. El PDF incluye códigos QR a la app (Google Play / App Store) con la guía de códigos.

> **[VERIFICAR]** Contradicción: la tabla de códigos dice E1 = "más de **5 min**", pero las diapositivas de diagnóstico dicen "El llenado de agua toma demasiado tiempo **> 30 min**". Falta definir cuál es el valor correcto.

---

## 7. Procedimientos de diagnóstico por código [PDF]

Recordatorio del PDF: **los componentes trabajan con 110 V**. Mediciones de resistencia siempre con equipo desconectado.

### E1 – Llenado de agua > 30 min
1. Revisar **mallas/filtros de las mangueras de entrada** (HOT/COLD): en las fotos aparecen filtros azules tapados con sarro/sedimento.
2. Verificar llaves abiertas y presión de agua.
3. Medir **bobinas de las válvulas** (fría / caliente / suavizante): ≈ **1.07 kΩ** (medido en válvula y en tarjeta principal: 1.073 / 1.077 kΩ).
4. Revisar válvula despiezada: émbolo, resorte, núcleo y diafragma/sello (diapositivas de válvula).
5. Verificar **manguera del sensor de nivel** (sin fuga/tapón) y conectores en tarjeta.
6. Si bobinas y mangueras están bien → tarjeta principal.

### E2 – Desagüe > 10 min
1. Inspeccionar bomba de drenaje (parte baja trasera) y manguera: bloqueo por suciedad.
2. Medir bobina de bomba: **15.9 Ω** medido en tarjeta principal (especificación del diagrama: 15–20 Ω).
3. Verificar sensor de nivel (que reinicie al vaciar).
4. Si la bomba está bien → tarjeta.

### E3 – Tapa abierta
1. Revisar **doble sensor de seguridad y seguro de tapa** (en la bisagra superior derecha de la tapa); **cuidado con el sensor de impacto** al abrir/manipular.
2. Con multímetro en continuidad: **activado = 000.0** (cerrado) y **desactivado = OL** (abierto).
3. Verificar tornillos/pestañas de la tapa que accionan el interruptor (se marcan tornillos en el borde de la tapa).
4. Al cerrar, debe escucharse el **clic** del seguro (icono de audio en el PDF).

### E4 / E5 – Desbalance / vibración
- Revisar nivelación, distribución de carga, **suspensiones** (delantera y trasera), **sensor de impacto**.

### F8 – Sensor de nivel o arnés
1. Medir en el conector del sensor de nivel (tarjeta de control / conector nivel):
   - Resistencia entre pines: **20 – 55 Ω**
   - Capacitancias (dos pares): **40 – 50 nF** cada una
2. Revisar manguera del sensor y arnés (ver fallas de arnés abajo).

### Fd – Seguro de tapa
- Bobina del seguro (L): **60 – 70 Ω**. Revisar sensor magnético y cableado.

### Motor (no enciende / ruido anormal)
- Bobinas medidas: **4.4 Ω / 8.5 Ω / 4.1 Ω** (≈ 4.3 Ω cada devanado y ≈ 8.6 Ω entre extremos, según diagrama: A–B 8.6, A–C 4.3, B–C 4.3).
- Puntos a revisar: tarjeta no envía voltaje, capacitor dañado, **resorte de fricción del embrague atascado**, embobinado dañado.
- Capacitor: falla si no marca capacitancia o es baja (placa: 60 µF).

### Retractor
- Resistencia **≈ 1.09 kΩ** (diagrama: 1.9 kΩ / 190 Ω en distintas láminas – **[VERIFICAR]**).
- Fallas: sin activación o sin reinicio → palanca del clutch atascada, falla de tarjeta, motor retractor dañado.

### Sensor de nivel de agua (fallas)
- Sin activación/sin reinicio → fuga de manguera del sensor, falla en tarjeta, falla interna del sensor.

### Bomba de drenado (fallas)
- Fuga o no drena → presurizar/inspeccionar abatimiento de la bomba, bloqueo por suciedad, corto o circuito abierto, falla de sensor de nivel o de tarjeta.

### Válvula de entrada (fallas)
- No se detiene o no entra agua → fuga en manguera del interruptor de presión, sensor de nivel no se activa, controlador, bobina en corto/abierta, parte hidráulica, filtro bloqueado.

### Arnés
- Fotos de arnés **cortado/pelado, aislante abierto y cables expuestos**: revisar continuidad y daños físicos antes de cambiar tarjeta.

---

## 8. Tabla maestra de valores de medición

| Elemento | Valor | Modelo | Fuente |
|---|---|---|---|
| Motor lavado semiauto | 5.4 / 5.3 / 10.7 Ω | LMS | PDF |
| Motor secado semiauto | 31 / 30.5 / 61.5 Ω | LMS | PDF |
| Capacitor motor lavado | 46 µF | LMS022M | PDF |
| Capacitor motor secado | 18 µF | LMS022M | PDF |
| Fusible | 10 A / 250 V | LMS022M | PDF |
| Timer lavado base | 3 s (Normal) / 6 s (Intenso) | LMS022M | PDF |
| Motor automática (L1, L2) | 4.3 Ω c/u; extremos 8.6 Ω | LMA022G | PDF |
| Motor medido en banco | 4.4 / 8.5 / 4.1 Ω | LMA022G | PDF |
| Capacitor motor automática | 60 µF / 300 V | LMA022G | PDF |
| Retractor | **1.6 kΩ** | LMA022G | Confirmado por Ernesto (2026-11-12); antes: 1.09 kΩ aquí, 1.9 kΩ / 190 Ω en diagramas |
| Bomba de drenaje | 15–20 Ω (diagrama) / 15.9 Ω medido / 20–40 Ω en lámina "digital" | LMA022G | PDF – VERIFICAR |
| Seguro de tapa (bobina) | 60–70 Ω | LMA022G | PDF |
| Válvulas (bobina) | ≈ 1 kΩ (1.07–1.077 kΩ medido) | LMA022G | PDF |
| Sensor de nivel R | 20–40 Ω (20–55 Ω en F8) | LMA022G | PDF |
| Sensor de nivel C | 40–50 nF (dos pares) | LMA022G | PDF |
| Interruptor de tapa | 0 Ω cerrado / OL abierto | LMA022G | PDF |
| Alimentación | 110–120 V, 60 Hz | ambas | PDF |

---

## 9. Lógica de funcionamiento (modelo para memoria)

### 9.1 Semiautomática (LMS) – lógica electromecánica **[INFERIDO del diagrama]**

```
Línea 110V → Fusible 10A
 ├─ Rama SECADO:  Switch tapa secado (NC al cerrar tapa) → Timer secado → Motor secado (+ cap 18µF) → Neutro
 └─ Rama LAVADO:  Selector (Normal/Intenso) → Timer lavado → Motor lavado (+ cap 46µF) → Neutro
Timer lavado: contactos alternan cada 3 s (Normal) o 6 s (Intenso) entre dos devanados
              → cambia el sentido de giro (vaivén del agitador/pulsador)
```

Reglas:
- Sin cierre de **tapa de secado** → el motor de secado **no puede energizarse** (seguridad). El **freno** detiene el tambor al abrir la tapa.
- Los dos motores son **independientes**: pueden fallar por separado.
- Diagnóstico por eliminación: fusible → switch tapa → timer → selector → capacitor → devanados del motor.

### 9.2 Automática análoga (LMA022G) – máquina de estados **[INFERIDO, validar]**

```
OFF
 └─ ENCENDIDO (botón 5) → lectura de selectores (1 nivel, 2 temperatura, 3 ciclo, 4 opciones)
     └─ INICIO (botón 7)
         ├─ Verificar TAPA cerrada (sensor magnético / seguro)  → si no: E3 · si falla seguro: Fd
         ├─ DETECCIÓN DE CARGA (nivel Auto)  → si falla: F5
         ├─ LLENADO: válvula fría/caliente (según temperatura) hasta nivel del sensor
         │     → si >T sin alcanzar nivel: E1 · sensor/arnés mal: F8
         ├─ LAVADO: motor + retractor en posición "lavado" (embrague) → agitador (vaivén)
         ├─ DRENADO: bomba → hasta que el sensor de nivel reinicie
         │     → si >10 min: E2
         ├─ [ENJUAGUE: repetir llenado/lavado/drenado; válvula de suavizante si aplica]
         ├─ CENTRIFUGADO: seguro de tapa activo → bomba drenando → retractor libera embrague → tina gira
         │     → desbalance: E4 · vibración excesiva: E5 (sensor de impacto)
         └─ FIN (secuencia indicada en el panel: remojo → lavado → enjuague → centrifugado → seguro)
```

Roles de cada componente:

| Componente | Función en el ciclo |
|---|---|
| Tarjeta principal | Cerebro: lee selectores, controla motor, válvulas, bomba, retractor, seguro |
| Tarjeta de panel | Interfaz de perillas y LEDs (comunica por CN2: 12 V, 5 V, TXD/RXD, GND) |
| Sensor de nivel (presostato con RC) | Mide el nivel por presión del aire de la manguera; la tarjeta lee R y C |
| Válvulas fría / caliente / suavizante | Entrada de agua; cada una con bobina ≈ 1 kΩ a 110 V |
| Bomba de drenaje | Vaciado; bobina ≈ 15–20 Ω |
| Motor asíncrono + capacitor | Movimiento por banda Poli V hacia la transmisión |
| Retractor (motor) | Mueve la palanca del clutch: selecciona agitar vs. centrifugar |
| Transmisión/embrague | Convierte giro del motor en agitación o giro de tina |
| Seguro de tapa + sensor magnético | Bloquea tapa durante centrifugado; confirma cierre |
| Sensor de impacto | Detecta golpe/desbalance de la tina |
| Suspensiones | Absorben vibración; fallas → E4/E5 |

### 9.3 Árbol rápido de diagnóstico (para uso en la memoria)

```
¿Enciende?  no → alimentación / fusible interno / tarjeta
¿Muestra código? → ir a sección 7 con el código
¿No muestra código y no arranca? → modo test (sección 5) por partes:
    lavado en seco OK?    → motor, retractor y seguro de tapa OK
    centrifugado OK?      → transmisión + bomba OK
    llenado (pre remojo)  → válvulas + sensor de nivel OK
```

---

## 10. Fallas comunes resumidas

| Síntoma | Causas probables |
|---|---|
| No llena / llena lento | Mallas de entrada tapadas, válvula, sensor de nivel, tarjeta |
| No drena | Bomba bloqueada, manguera obstruida, sensor de nivel |
| No centrifuga | Seguro de tapa, retractor/clutch, bomba, transmisión, tarjeta |
| Ruido/vibración | Suspensiones, balance de carga, nivelación, rodamientos/transmisión |
| Motor no gira | Capacitor, devanado, resorte de fricción del embrague, tarjeta |
| Enciende pero no selecciona ciclo / no detecta tapa | Seguro/sensor de tapa y cableado → tarjeta de control |
| Falla intermitente | Arnés dañado/empalmes, conectores sulfatados |

---

## 11. Pendientes / dudas

1. Video de Drive del modo test (`drive.google.com/file/d/10uHnlaTI16BZPVoeZUdoeR_1Mpr7K-LL`) y el de Vimeo de la página: **no pude ver su contenido**; completar la prueba de llenado y cualquier paso adicional.
2. Valor correcto de **E1** (5 min vs 30 min).
3. Descripción de las diapositivas **"Casos de fallas comunes"** (solo imágenes).
4. Patrones LED de los códigos (confirmar posición).
5. Valores de **retractor** y **bomba** (varían entre láminas).
6. Varias láminas dicen "automática **digital**" pero muestran contenido de la LMA022G **análoga**; confirmar si existe un modelo digital distinto.
7. Texto exacto de la opción 4 del selector ("ciclo suavizante").
