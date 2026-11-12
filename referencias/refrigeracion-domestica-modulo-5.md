# Refrigeración doméstica — Curso de Diagnóstico y Reparación de Equipos de Línea Blanca (Mirage), Módulo 5

> **Fuente:** Módulo 5 del curso, transcrito de los videos de capacitación.
> **Uso en la skill:** primer material de las categorías **Dispensadores**, **Refrigeradores** y **Congeladores**. Los tres equipos comparten el mismo principio (el ciclo de refrigeración por compresión de vapor); lo que cambia son los valores y los componentes de cada uno. Validar respuestas técnicas contra este contenido; si un dato no aparece aquí, la skill debe decir que **no está documentado** y no inventarlo.
> **Nota sobre calidad:** los textos vienen de transcripción automática. Los valores marcados con ⚠️ requieren confirmación contra el video o el equipo antes de tomarse como definitivos.
> **Nota de seguridad:** los congeladores del curso trabajan con refrigerante **R600a**, que es **inflamable**: nada de flama abierta ni chispas al trabajar el sistema sellado.

## Estructura del módulo

| # | Lección | Estado |
|---|---------|--------|
| 1 | Ciclo de refrigeración en refrigeradores y dispensadores | ✅ Incluida |
| 2 | Tipos de equipos Mirage con refrigeración doméstica | ✅ Incluida |
| 3 | Componentes y revisión del dispensador | ✅ Incluida |
| 4 | Congelador: funcionamiento y diagnóstico | ✅ Incluida |

> El módulo no trae una lección de revisión de componentes específica de **refrigeradores**: de ellos cubre el ciclo (Lección 1) y los tipos (Lección 2). No inventar procedimientos de refrigerador que no estén documentados.

---

## 1. Ciclo de refrigeración (común a los tres equipos)

Proceso termodinámico de **compresión de vapor**, en 4 pasos:

1. **Compresión:** el compresor succiona el refrigerante en estado gaseoso, a baja presión, desde el evaporador, y lo comprime: suben su temperatura y su presión.
2. **Condensación:** el gas caliente pasa al **condensador**, donde se enfría y se convierte en **líquido**.
3. **Expansión:** el líquido pasa por el **tubo capilar o la válvula de expansión**, que le reduce la presión y la temperatura.
4. **Evaporación:** en el **evaporador**, el refrigerante absorbe el calor del interior del equipo y el ciclo reinicia.

## 2. Tipos de equipos

- **Refrigeradores de una puerta**, **dispensadores** y **congeladores**.
- Las diferencias entre equipos: la **distribución del sistema de refrigeración**, el **control de temperatura** y si cuentan con **uno o dos evaporadores**.
- Esto influye en el diagnóstico y la reparación: no todos presentan los mismos fallos ni el mismo acceso a los componentes.

---

## 3. Dispensador de agua

> **Manuales y especificaciones en Drive** (carpeta Github / Dispensadores, ver `referencias/indice-drive.md`): manual del **MDD30HD** blanco de garrafón oculto, manual del **MDD10CS**, manuales Disx10 y Disx30, y las **fichas de especificaciones** DISX30-2025-MDD30HD, Disx10 y Disx30 rev. 2. Para cualquier diagnóstico se entrega también el manual del modelo, como en las demás categorías.

### 3.1 Dispensador MDD10 — garrafón superior (por gravedad)

- Sistema de ahorro energético: mantiene el agua fría o caliente con consumo mínimo. Dos salidas: **agua fría y agua caliente**, para beber o preparar alimentos.
- **Depósito interno de acero inoxidable**: higiene, sin acumulación de bacterias ni olores.
- El **garrafón se coloca en la parte superior** y alimenta **por gravedad**, sin bomba.
- Partes: perforador (parte superior), **indicador de estatus** (si está calentando o si el compresor está encendido), **seguro contra quemaduras** en la llave de agua caliente, recipiente antiderrames, compartimiento inferior de almacenamiento (**no** enfría), interruptor de encendido y fusibles, control de temperatura del agua fría (termostato) y compresor.
- **Tanque de agua caliente:** lleva una **resistencia que se abraza al tanque** de acero inoxidable y **dos termostatos**:
  - **85 °C — termostato de trabajo:** al llegar el agua a esa temperatura, abre el contacto y la resistencia deja de calentar.
  - **90 °C — termostato de protección:** si el primero falla o se queda pegado, este corta la corriente a la resistencia.

**Mediciones de este modelo:**

| Componente | Medición | Valor |
|------------|----------|-------|
| **Resistencia del tanque caliente** | Resistencia entre sus terminales | **26 Ω** |
| **Compresor** (retirar antes el relevador térmico) | Terminales 1–2 | **10 Ω** |
| | Terminales 2–3 | **20 Ω** |

*(Entre extremos, la medición debe dar la suma de los dos devanados, como en todo compresor.)*

### 3.2 Dispensador MDD30 — garrafón inferior (con bomba)

- Bajo nivel de ruido, diseño elegante, doble temperatura (fría y caliente) y depósitos de acero inoxidable.
- El **garrafón va integrado en la parte inferior**: se conecta una manguera y una **bomba** succiona el agua hacia los tanques para enfriarla o calentarla.
- Componentes: termostatos, compresor, tanque de agua caliente, termostato de baja, **tarjeta display**, **bomba** y **sensor de nivel**. *(Los dos modelos del curso son el **MDD10** y el **MDD30** — confirmado por Ernesto el 2026-11-12; la transcripción llamaba a este «el de 30».)*

**Mediciones de este modelo:**

| Componente | Medición | Valor |
|------------|----------|-------|
| **Resistencia del tanque caliente** | Resistencia entre sus terminales | **33 Ω** (tanque alimentado a 120 V) |
| **Bomba de agua** | Voltaje que le entrega la tarjeta | **12 V de corriente directa** |

**Diagnóstico de la bomba (doble revisión, como en lavadoras):**

- La tarjeta entrega **12 VCD** y la bomba no trabaja → la falla es la **bomba**.
- La tarjeta entrega un voltaje anormal — casos vistos por el instructor: **24 o 40 V**, o por debajo: **5 o 3 V** — → la falla es la **tarjeta**.
- Si el equipo debería estar llenando y la tarjeta no manda el voltaje → también es la tarjeta.

**Falla conocida — bomba sin succión por pérdida de vacío** *(explicación de Ernesto, 2026-11-12; video oficial DISX30)*: en el MDD30 de garrafón oculto, si al conectar queda **algún espacio** o la **manguera se jala**, se genera una entrada de aire y **se pierde el vacío**: la bomba no succiona como debe, **no sube el agua y el equipo marca falla**. Antes de condenar la bomba o la tarjeta, revisar el conjunto de succión del garrafón: el **cabezal** con sus tubos y cople, la **liga**, el **codo** y sus **seguros** (clips), y sobre todo el **sello de vacío** de la unión del codo con la manguera — la manguera debe entrar completa y quedar asegurada con su clip, sin espacio, igual que la conexión superior que sube al tanque. Material relacionado en la carpeta de Dispensadores: `Boletin_DISX30_Bomba sin succión.pdf` y el video `Bomba Dispensador.mp4` (muestra el despiece del cabezal y el sello de vacío).
- El instructor remite al **diagrama del dispensador** (área de calentamiento y de enfriamiento) para el diagnóstico. Los diagramas ya están en la carpeta de Dispensadores de Drive: **Diagrama Dispensador MDD30HD**, **Diagrama Electrico Dispensador MDD30HC** y **Diagrama Explosivo MDD10CB** (ver `referencias/indice-drive.md`), junto con los manuales Disx10 y Disx30.

### 3.3 Caso de campo (Ernesto, 2026-11-12): fuga debajo del depósito de agua fría

**Síntoma:** el dispensador tira agua por debajo del equipo y la fuga se localiza **debajo del depósito de agua fría**.

**Diagnóstico con el material de Ernesto (fotos y videos en la carpeta de Dispensadores de Drive):**

- Al abrir el equipo se ve el depósito de agua fría con su aislamiento de unicel y, en el fondo, un **disco plástico con un orificio central** (en la foto de Ernesto está marcado en verde): **por ese orificio central se va el agua hacia abajo**.
- Por debajo del depósito baja un **vástago metálico roscado** con su rondana y tuerca (junto al compresor). En los videos el vástago y la unión se ven **húmedos**: el agua escurre por esa unión y gotea debajo del equipo.
- **Revisión:** vaciar el depósito, revisar por dentro el orificio central del fondo y por fuera el apriete y el sello de la unión del vástago inferior; ahí es donde se concentra la fuga de este caso. Para identificar las piezas del fondo del depósito, apoyarse en el **Diagrama Explosivo del MDD10CB** (carpeta de Dispensadores de Drive).

**Media del caso (carpeta Github / Dispensadores, ver `referencias/indice-drive.md`):**

- Foto del depósito de agua fría desde arriba: https://drive.google.com/file/d/1o-GfBgWTdfhx75FwTAhw3RMKA82lAQdS/view?usp=drivesdk
- Foto con el orificio central del fondo marcado en verde: https://drive.google.com/file/d/1ToR0aWcGFrZxM-Xzjt09AmyPTmGLHHsp/view?usp=drivesdk
- Video del vástago inferior del depósito: https://drive.google.com/file/d/14FZI3DAOUK03yOrbRNdV0bGNcq5kGDkY/view?usp=drivesdk
- Video del goteo en la unión del vástago: https://drive.google.com/file/d/1uoUreYPHLxktP0zTwe4boESCFErefNPb/view?usp=drivesdk

---

## 4. Congelador

### 4.1 Características

- Alimentación: **110–120 V** *(el curso menciona ambos valores; Ernesto confirmó el 2026-11-12 que los dos son normales)*.
- Interior con recubrimiento de aluminio, canastilla, **luz LED** interior y seguro con llave para limitar quién lo controla.
- **Modelos: 100, 150, 200, 250 y 300 litros.**
- Refrigerante **R600a**.

### 4.2 Rangos de temperatura (control de 1 a 7)

| Nivel | Modo | Rango |
|-------|------|-------|
| 1 a 3 | Congelación suave | **5 a −5 °C** (en el punto medio cruza por debajo de 0 °C y ya congela) |
| 4 a 5 | Congelación moderada | **−5 a −15 °C** |
| 6 a 7 | Congelación máxima | **−15 a −28 °C** |

- Para conservar proteínas (res, puerco, pollo) por más tiempo, la referencia es **−18 °C**.
- Es una **refrigeración por etapas** *(confirmado por Ernesto el 2026-11-12; la transcripción solo asignaba niveles al rango suave y los demás se completaron por continuidad de la escala 1–7)*.

### 4.3 Componentes y revisión

**Relé PTC (relé térmico de arranque):**

- Suministra **momentáneamente** la corriente al **devanado de arranque** para producir el torque necesario para que el motor arranque.
- Cuando el motor alcanza aproximadamente el **75 % de su velocidad**, el relé interrumpe el paso de energía al devanado de arranque y el motor sigue trabajando solo con el **devanado de marcha**.
- También protege: si hay un corto o una fuga de corriente por parte del compresor, se abre y lo protege.

**Termostato:**

- Revisar su **continuidad**: debe mandar la señal al compresor para que funcione (aplica el mismo diagrama de los demás equipos).

**Compresor:**

- Revisar el devanado interno midiendo entre las terminales: dos mediciones parciales y la de extremos, que debe dar **la suma** de las dos. Los valores del compresor del congelador son **diferentes a los del dispensador** *(confirmado por Ernesto el 2026-11-12; no aplicar aquí el 10 Ω / 20 Ω del dispensador. Los valores exactos quedaron confusos en la transcripción y están pendientes de documentar)*.
- Revisar también el **aislamiento contra el chasis / puesta a tierra**: no debe haber continuidad de las terminales a la carcasa.

---

## Validación (hecha por Poly el 2026-11-12)

**Consistente con el funcionamiento estándar de estos equipos:**

- El ciclo de compresión de vapor en 4 pasos y sus componentes (compresor, condensador, capilar/válvula de expansión, evaporador).
- Dispensador con doble termostato en el tanque caliente (trabajo 85 °C + protección 90 °C): esquema de seguridad correcto.
- Compresor: la medición entre extremos da la suma de los devanados parciales.
- Bomba del dispensador alimentada a **12 VCD** desde la tarjeta y la doble revisión tarjeta/componente (si el voltaje es anormal, la falla es la tarjeta).
- Relé PTC: arranque momentáneo del devanado auxiliar y corte al llegar a velocidad (el curso lo ubica en ≈75 %).
- Conservación de proteínas a **−18 °C** como referencia.

**Dudas resueltas por Ernesto (2026-11-12):**

1. **Compresor del congelador:** sus valores son **diferentes** a los del dispensador (pendiente documentar los exactos).
2. **Dispensadores:** son dos modelos — **MDD10** (garrafón superior) y **MDD30** (garrafón inferior con bomba).
3. **Voltaje del congelador:** 110 o 120 V, **ambos son normales**.
4. **Niveles del congelador:** sí, es **refrigeración por etapas** (suave, moderada y máxima sobre la escala 1–7).
5. **Refrigerante:** sí, **todos los congeladores usan R600a**.
6. **Diagrama del dispensador:** sí lo tiene — los diagramas del MDD30HD, MDD30HC y el explosivo del MDD10CB ya están en la carpeta de Dispensadores de Drive.

## Reglas para la skill

1. Responder y validar solo con base en este documento; si algo no aparece, decir que **no está documentado**.
2. De **refrigeradores** solo hay ciclo y tipos: no inventar procedimientos de revisión de componentes para ellos hasta que llegue material.
3. Recordar la seguridad con **R600a** (inflamable) al hablar del sistema sellado del congelador.
4. Para valores marcados con ⚠️, indicar que están pendientes de confirmación.
