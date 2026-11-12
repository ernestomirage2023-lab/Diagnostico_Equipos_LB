# Microondas — Curso de Diagnóstico y Reparación de Equipos de Línea Blanca (Mirage), Módulo 4

> **Fuente:** Módulo 4 del curso, transcrito de los videos de capacitación.
> **Uso en la skill:** es el primer material de la categoría Microondas. Validar respuestas técnicas contra este contenido; si un dato no aparece aquí, la skill debe decir que **no está documentado** y no inventarlo.
> **Nota sobre calidad:** los textos vienen de transcripción automática. Los valores marcados con ⚠️ requieren confirmación contra el video o el equipo antes de tomarse como definitivos.
> **⚠️ SEGURIDAD — leer antes de cualquier revisión:** el microondas trabaja con **alto voltaje** (miles de volts) y su capacitor **guarda carga aunque el equipo esté desconectado**. Antes de tocar cualquier componente interno hay que **descargar el capacitor** (procedimiento en la sección 3). Nunca operar el equipo con la puerta o los interruptores de seguridad anulados.

## Estructura del módulo

| # | Lección | Estado |
|---|---------|--------|
| 1 | Principio de funcionamiento del microondas | ✅ Incluida |
| 2 | Componentes principales del microondas y su función | ✅ Incluida |
| 3 | Revisión de componentes del microondas: seguridad y cuidados | ✅ Incluida |

---

## 1. Principio de funcionamiento

- El microondas calienta con **ondas electromagnéticas de alta frecuencia: 2.45 GHz**, generadas por el **magnetrón**, que transforma la energía eléctrica en microondas.
- Las microondas llegan al interior del horno por una **guía de ondas** y se distribuyen de manera uniforme con el **plato giratorio** o un **agitador de ondas**.
- Las ondas penetran el alimento y hacen vibrar rápidamente las **moléculas de agua y grasa**, generando calor por fricción: el alimento se calienta desde el interior, de forma rápida y eficiente.
- En resumen: **magnetrón + guía de ondas + vibración molecular** = la electricidad se convierte en calor directo en los alimentos.

### Funciones del teclado y diagnóstico rápido

| Función | Qué hace | Si falla, revisar |
|---------|----------|-------------------|
| **Display** | Muestra tiempo, nivel de potencia y estado del equipo | Si no enciende o parpadea: tarjeta o alimentación |
| **Cocción rápida** | Prepara alimentos comunes con un solo toque | Si no responde: teclado o microcontrolador |
| **Botón de potencia** | Ajusta el nivel de energía según el alimento | Si no cambia el nivel: tarjeta de control |
| **Cocción por peso** | Ajusta tiempo y potencia automáticamente según el peso | Si no trabaja bien: error de programación o sensor |
| **Inicio / detener** | El botón más usado; arranca y detiene el equipo | Si falla, el equipo no arranca: verificar respuesta con multímetro o plantilla de pruebas |

---

## 2. Componentes principales y su función

| Componente | Función |
|------------|---------|
| **Fuente de poder (transformador de alto voltaje)** | Recibe la energía de la red y la transforma para alimentar el circuito de alto voltaje. |
| **Capacitor de alto voltaje** | Trabaja junto con el diodo: acumula energía y entre los dos **elevan el voltaje** que alimenta al magnetrón. |
| **Diodo de alto voltaje** | Con el capacitor forma el circuito que entrega el alto voltaje al magnetrón (permite el paso de corriente en un solo sentido). |
| **Magnetrón** | El corazón del microondas: un tubo que convierte la energía eléctrica (del orden de **4,000 V**) en ondas electromagnéticas de 2.45 GHz que calientan el alimento. |
| **Guía de ondas** | El conducto que **conduce** las microondas desde el magnetrón hacia la cámara de cocción, de manera eficiente. |
| **Ventilador** | Enfría el magnetrón y mueve el aire dentro del equipo para evitar sobrecalentamiento. |
| **Cavidad de cocción** | El espacio donde se colocan los alimentos. |
| **Plato giratorio** | Gira el alimento para una distribución uniforme de las microondas y un calentamiento parejo. |

En el diagrama eléctrico del curso el equipo se alimenta con **120 V**, lleva un **fusible de entrada de 15 A / 250 V**, iluminación interna de la cavidad, un **termostato de protección en la línea**, la tarjeta de control y los interruptores (switches) de la puerta.

---

## 3. Revisión de componentes: seguridad y cuidados

Un buen diagnóstico identifica desgaste, daños o conexiones sueltas que pueden causar problemas eléctricos, pérdida de potencia o **riesgo de fuga de radiación**. La inspección técnica protege al usuario, prolonga la vida del equipo y garantiza una cocción eficiente.

### 3.1 Capacitor de alto voltaje — descarga obligatoria

**Antes de tocar el capacitor o cualquier parte del circuito de alto voltaje, descárgalo siempre:**

1. Con unas pinzas (herramienta aislada), **puentea las dos terminales del capacitor** y espera unos **5 segundos**.
2. Confirma con el multímetro en volts que marque **0 V**: sin carga, sin potencia interna.
3. Recién entonces se puede medir el componente.

**Datos del capacitor (ejemplo del curso):**

- Capacitancia: **0.80 µF**, con variación del **±3 %**.
- Resistencia interna (de descarga): **10 MΩ**.
- Voltaje de trabajo: **2,000 V** *(confirmado por Ernesto el 2026-11-12; la transcripción decía «2,000 y algo»)*.

**Medición:** en capacitancia debe acercarse a su valor nominal (0.80 µF en el ejemplo); la resistencia interna debe tender a los **10 MΩ** (en el ejemplo del curso la lectura llegó a ≈9.5 MΩ: componente en buen estado).

### 3.2 Magnetrón

- Medir las **dos terminales del filamento**: deben dar **continuidad** entre ellas.
- Medir de **cada terminal al cuerpo (carcasa) del magnetrón**: **no** debe dar continuidad. Si da, el magnetrón está aterrizado y dañado.

### 3.3 Transformador de alto voltaje

- **Primario:** debe dar **continuidad con resistencia baja** *(confirmado por Ernesto el 2026-11-12; la frase de la transcripción había quedado cortada)*.
- **Secundarios** (el devanado que va al magnetrón y el de filamento): deben dar **continuidad** entre sus terminales.
- **De cualquier terminal a tierra (carcasa):** debe estar **abierto** (sin continuidad). Si hay continuidad a tierra, el transformador está dañado.

### 3.4 Termostato de protección

- Es un contacto **normalmente cerrado**: por debajo de su temperatura debe dar **continuidad**.
- En el equipo del curso abre a los **105 °C** y corta el circuito para proteger los demás componentes. Es el termostato de la **cavidad** *(confirmado por Ernesto el 2026-11-12)*.
- Si está abierto en frío, está dañado.

### 3.5 Interruptores de puerta (3 microswitches)

La puerta lleva **tres switches** de seguridad; hay que revisar la lógica de cada uno con la puerta abierta y cerrada:

| Switch | Tipo | Con puerta cerrada | Con puerta abierta |
|--------|------|--------------------|--------------------|
| 1 | Normalmente abierto (NA) | Continuidad | Sin continuidad |
| 2 | Normalmente cerrado (NC) — switch de monitoreo | Sin continuidad | **Continuidad (cierra al abrir)** — protege si fallan los de enclavamiento: al cerrar, provoca el corto que quema el fusible de entrada *(confirmado por Ernesto el 2026-11-12)* |
| 3 | Normalmente abierto (NA) | Continuidad | Sin continuidad |

- Unos switches mandan la señal a la tarjeta de que la puerta está cerrada y otros protegen el equipo: **nunca se anulan ni se puentean**.

### 3.6 Motor del ventilador (extractor)

- Elimina el calor producido por el magnetrón y el transformador.
- Revisar la **resistencia interna de su bobina** y que **no tenga continuidad con la tierra o la carcasa** del equipo.

### 3.7 Motor del plato giratorio

- Verificar que a su conector le lleguen **120 V**:
  - **Sin voltaje** → daño en la tarjeta.
  - **Con voltaje y no gira** → el motor está dañado.

### 3.8 Diodo de alto voltaje

- Permite el paso de corriente en un solo sentido: se revisa con el multímetro en **prueba de diodos** — debe dar señal (conducir) **en un solo sentido**; al invertir las puntas no debe marcar *(confirmado por Ernesto el 2026-11-12; la transcripción describía el método de forma confusa)*.

### 3.9 Fusibles

- **Fusible de entrada (línea): 15 A, 250 V** *(confirmado por Ernesto el 2026-11-12)*. Revisar continuidad en sus dos terminales.
- Al final de la lección el curso menciona un fusible «del capacitor al magnetrón», y la presentación del Módulo IV trae una diapositiva titulada **«FUSIBLE Capacitor-Magnetron»** en la revisión de componentes (sin valor visible). Ernesto confirmó que el fusible del equipo es el de la entrada (15 A / 250 V), sin un segundo fusible confirmado: si un equipo en campo trae fusible de alto voltaje, se documenta en ese momento.
- **Material del modelo en Drive** (carpeta Github / Microondas): manuales de los **Xwave MWD020 y MWD031**, diagramas explosivos **MWD020E y MWD031E** y la presentación del Módulo IV (`Presentacion_LB.pdf`), que confirma los ~4,000 V del magnetrón y los switches de puerta NA/NC/NA de este documento.

---

## Validación (hecha por Poly el 2026-11-12)

**Consistente con el funcionamiento estándar de un microondas:**

- Frecuencia de **2.45 GHz** y calentamiento por vibración de moléculas de agua y grasa.
- Circuito de alto voltaje: transformador + capacitor + diodo entregando del orden de **4,000 V** al magnetrón.
- Capacitor de **0.80 µF** con resistencia interna de descarga de **10 MΩ** y la **descarga obligatoria** antes de medir o tocar: procedimiento correcto y es LA regla de seguridad de este equipo.
- Pruebas del magnetrón (continuidad de filamento, aislamiento a carcasa), del transformador (continuidad de devanados, abierto a tierra) y del termostato (NC, continuidad en frío).
- Fusible de línea de **15 A / 120 V**.

**Dudas resueltas por Ernesto (2026-11-12):**

1. **Voltaje del capacitor: 2,000 V** (no 2,100).
2. **Fusible:** el del equipo es el **de la entrada: 15 A, 250 V**; no hay un segundo fusible confirmado.
3. **Switch de monitoreo (NC):** así es — con la puerta cerrada está abierto y **cierra al abrir la puerta**.
4. **Primario del transformador:** continuidad **con resistencia** (baja).
5. **Diodo de alto voltaje:** se prueba con el multímetro en **prueba de diodos**; debe dar señal en un solo sentido.
6. **Termostato de 105 °C:** es el de la **cavidad**.

## Reglas para la skill

1. Responder y validar solo con base en este documento; si algo no aparece, decir que **no está documentado**.
2. **Seguridad primero:** en cualquier procedimiento interno del microondas, recordar la **descarga del capacitor** antes de tocar componentes, y nunca sugerir anular los interruptores de puerta.
3. Para valores marcados con ⚠️, indicar que están pendientes de confirmación.
