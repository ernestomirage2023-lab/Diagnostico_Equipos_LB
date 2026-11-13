# Calentadores de paso — Curso de Diagnóstico y Reparación de Equipos de Línea Blanca (Mirage)

> **Fuente:** Módulo 2 del curso, transcrito de los videos de capacitación.
> **Uso en la skill:** validar respuestas técnicas contra este contenido. Si un dato no aparece aquí, la skill debe decir que **no está en el curso** y no inventarlo.
> **Nota sobre calidad:** los textos vienen de transcripción automática. Los valores marcados con ⚠️ requieren confirmación contra el video o el manual antes de tomarse como definitivos.

## Estructura del módulo

| # | Lección | Estado |
|---|---------|--------|
| 1 | Tipos de calentadores | ✅ Incluida |
| 2 | Componentes y lógica de funcionamiento de los calentadores de paso | ✅ Incluida |
| 3 | Diagnóstico y reparación de fallas | ✅ Incluida |
| 4 | Mantenimiento de calentadores de paso | ✅ Incluida |
| 5 | Ejercicio Boiler | ⏳ Pendiente (sin transcripción) |
| 6 | Cuestionario #2 | ⏳ Pendiente (sin transcripción) |

---

## 1. Tipos de calentadores

### Clasificación

| Tipo | Combustible / alimentación | Capacidades |
|------|----------------------------|-------------|
| Calentador de gas | Gas LP o gas natural | 1, 2 o 3 servicios |
| Calentador eléctrico | 220 V | 1 y 1.5 servicios |

### Requisitos esenciales para instalar un calentador de gas

1. **Fuente de gas** (gas LP o natural).
2. **Flujo de agua.**
3. **Área ventilada.**

### Ventilación y ubicación

- **40 cm libres en cada uno de los lados** del equipo, para una buena combustión.
- **Al menos 60 cm en la parte superior**, en la descarga de gases.
- El equipo debe estar **resguardado**: dentro de un espacio o, como mínimo, con un techo que lo proteja de la humedad y la lluvia.

---

## 2. Componentes y lógica de funcionamiento

### 2.1 Componentes del calentador de paso de gas

- Termostato
- Sensor de chispa (emisor de chispa)
- Válvula de ahorro
- Sistema de ignición
- Electroválvulas de gas
- Recolector de gas
- Intercambiador de calor
- Sensor de flama
- Quemador
- Sensor magnético (sensor de flujo)
- Caja de baterías

### 2.2 Función de cada componente

| Componente | Función |
|------------|---------|
| **Termostato (protección por alta temperatura)** | Protege el equipo de altas temperaturas. Es un **contacto normalmente cerrado**; en una de sus terminales lleva una lámina bimetálica que, con el calor, abre la señal y corta el voltaje a las válvulas. |
| **Sensor magnético (sensor de flujo)** | Detecta el flujo de agua dentro del equipo y manda la señal al módulo de ignición para iniciar el encendido. Funciona con un imán dentro de la tubería. |
| **Electroválvulas de gas** | Controlan el gas: permiten u obstruyen el paso hacia el quemador. |
| **Emisores de chispa** | Permiten el paso de corriente eléctrica para generar el arco que enciende el quemador. |
| **Sensor de flama** | Detecta la flama dentro del quemador y, con una señal de bajo voltaje, confirma al sistema de ignición que hay flama calentando el equipo, para mantener las válvulas operando. |
| **Sistema de ignición** | Es el "cerebro" del equipo. Recibe el voltaje, manda señal a las válvulas y recibe señal del termostato y del sensor de flujo. |
| **Válvula de ahorro** | En posición **normal** el quemador trabaja al **100 %**; en **ahorro** trabaja al **50 %**. |

### 2.3 Lógica de funcionamiento (3 estados)

| Estado | Nombre | Qué ocurre |
|--------|--------|------------|
| **1** | Espera | Validar que el switch esté encendido, que las baterías tengan carga y que el termostato esté en buen estado. |
| **2** | Encendido | El sensor magnético (sensor de flujo) detecta agua circulando y manda encender el equipo. |
| **3** | Operando | Se manda chispa y voltaje a la válvula para permitir el paso de gas. Con chispa + gas se genera la flama y se activa el sensor de flama, que retroalimenta a la válvula y al sistema de ignición para seguir operando. |

### 2.4 Importancia del flujo de agua (práctica del curso)

Equipo de referencia: **1 servicio, gas LP, diseñado para 5–6 L/min.**

| Condición de prueba | Resultado observado |
|---------------------|---------------------|
| ~7.5 L/min, entrada 18 °C, salida 28–29 °C | ΔT ≈ 10 °C. El equipo no calienta lo suficiente. |
| 7 L/min, controles al máximo, válvula en ahorro | ΔT ≈ 10 °C (entra ~28 °C, sale ~38–39 °C en la demostración de verano). |
| **5–6 L/min** (flujo de diseño) | **ΔT mayor a 25 °C.** Es el punto de mayor eficiencia. |
| Por debajo de ~3 L/min | Temperaturas muy altas. Ocurre en casas sin bomba o sin sistema de presión. |

Puntos clave:

- Si el cliente dice que **"el boiler enciende pero no calienta lo suficiente"**, revisar primero si hay **exceso de flujo de agua** y dejar el equipo operando en su rango de 5–6 L/min.
- Cambiar la válvula de **ahorro a normal** hace que el quemador trabaje al 100 % y sube la temperatura.
- En invierno la temperatura de entrada baja (12, 10, 15 °C), pero con ΔT de ~25 °C el agua sigue en rango de confort.
- Para bajar la temperatura de salida: reducir los controles de temperatura al mínimo y/o pasar la válvula a ahorro. Se busca el **punto medio de confort** del cliente (combinaciones entre máximo/normal, mínimo/normal, máximo/ahorro).

---

## 3. Diagnóstico y reparación de fallas

Guía basada en el calentador de paso de **gas LP, 1 servicio, 5–6 L/min**.

### 3.1 Fallas más comunes reportadas por el cliente

1. El quemador no enciende.
2. La flama se apaga inesperadamente.
3. El agua sale demasiado caliente.
4. El agua sale fría aun con el calentador funcionando.

### 3.2 El quemador no enciende

#### a) Suministro de gas y baterías

- Verificar que la válvula del tanque esté **abierta** y que haya suministro de gas.
- Baterías con voltaje **por encima de 3 V** (se requieren para el funcionamiento). Es el par de 2 pilas de 1.5 V: con 3.0 V o menos, la bobina de la válvula ya no se sostiene y se cambian las pilas.

#### b) Bobina de la válvula de gas

- Verificar que la bobina esté alimentada con **3 V de corriente directa**; es imprescindible para operar el equipo.
- Si el equipo se guardó en verano, el **empaque puede pegarse al cuerpo de la válvula** y la válvula queda pegada.
- Si hay duda sobre la bobina, medir su **resistencia interna** y el voltaje que la alimenta (entre los cables indicados en el diagrama).

#### c) Flujo de agua muy bajo

- Equipos de 1 servicio (5–6 L/min) requieren una **presión mínima de 1.45 psi** *(la transcripción decía "1.45 PSA"; la unidad es psi — validación del 2026-11-12: 1.45 psi ≈ 1 m de columna de agua, coherente con el caudal de diseño; ningún otro documento del archivo trae este dato)*, que equivale a un caudal de unos 5 L/min en la tubería.
- **Prueba práctica de la cubeta de 20 L** (sin caudalímetro):

| Tiempo en llenar 20 L | Interpretación |
|-----------------------|----------------|
| Alrededor de 4 min | Flujo correcto (≈ 5 L/min) |
| Más de 4 min; 7–8 min | Flujo demasiado bajo |
| 1–2 min | Flujo demasiado alto; también afecta el rendimiento |

- **Criterio de exceso de flujo (Ernesto, caso de campo 2026-11-12):** si la cubeta de **19 L se llena en menos de 2 minutos**, el flujo es de **≈9.5 L/min o más** contra los 5–6 L/min de diseño: hay **exceso de flujo** y el equipo **no calienta**, porque el agua pasa tan rápido por el intercambiador que no alcanza a tomar temperatura. Video de campo con cronómetro: `Prueba de la cubeta exceso de flujo.mp4` (carpeta Videos de Boiler de paso, en el índice de Drive).

- Revisar que el **sensor/filtro de entrada** no tenga sarro y esté limpio.

#### d) Sensor magnético (sensor de flujo)

- Un imán dentro de la tubería manda señal al módulo de ignición, que enciende chispa y válvula.
- **Síntoma de falla:** hay flujo de agua pero no hay chispa ni encendido.
- **Prueba 1 (puente):** con flujo de agua, hacer un **puente entre las dos terminales del conector** del sensor. Si enciende, el sensor es el problema.
- **Prueba 2 (continuidad):** multímetro en continuidad en las dos terminales del sensor. **Con flujo de agua el circuito debe cerrarse.** Si no cierra, revisar si el imán gira/funciona; si no, **cambiar el sensor magnético junto con la válvula de agua** (se pide como un solo conjunto).

#### e) Termostato abierto

- Es un **contacto normalmente cerrado**. Si el equipo llega a **80–85 °C** (según modelo) se abre y apaga el equipo para protegerlo.
- Si se queda abierto, el equipo lanza la flama pero se apaga, aunque el flujo y el sensor magnético estén bien.
- **Prueba:** multímetro en continuidad en las terminales, con el equipo **frío** debe marcar continuidad (cerrado).
- **Degradación por edad:** tras unos **4–7 años**, si el equipo se sobrecalienta o se activa muchas veces, los bimetales se degradan y empiezan a abrir a **40–50 °C** en lugar de 75–80 °C, y el equipo se vuelve deficiente.

#### f) Falsos contactos en cables de chispa y flama

- Si las puntas de los cables de los **emisores de chispa** y del **sensor de flama** están tostadas o quemadas: **recortar la punta del cable** y volver a conectar para eliminar falsos contactos.

### 3.3 La flama se apaga inesperadamente

| Causa | Detalle |
|-------|---------|
| **Termostato abriendo antes de tiempo** | Abre a 40–50 °C en lugar de 75–80 °C. El equipo trabaja unos minutos y se apaga. Verificar con continuidad. |
| **Mala combustión / falta de oxígeno** | La flama amarilla no calienta, genera hollín y ceniza negra en el quemador. Si se tapan las ventilaciones, el sensor de flama no se calienta lo suficiente y manda apagar. Revisar instalación y ventilación. |
| **Baterías débiles** | Encienden 1–3 min pero no tienen potencia para mantener la bobina de la válvula. Usar **2 pilas alcalinas de 1.5 V (3 V en total)**. Cambiar si están en el límite. |
| **Apagado por norma a los 20 minutos** | Por seguridad, **todos los equipos de gas se apagan a los 20 min** de operación continua. Para reactivar: cerrar la llave y abrir de nuevo (otros 20 min). **No se debe quitar esta función**, aunque el cliente lo pida. |
| **Baja presión de gas** | Ver 3.4. |

### 3.4 Presión de gas

- Presión de trabajo requerida: **2.74 kPa, constante.**
- Equivalencias: **11 pulgadas de columna de agua** y **6.36 oz/pulg²** *(confirmado por conversión el 2026-11-12: 2.74 kPa = 11.0 pulg. de columna de agua = 6.36 oz/pulg², exacto)*.
- **Presión estática** (circuito cerrado, sin consumo) puede verse buena, pero **al encender el equipo la presión puede caer**. Si además otro aparato consume gas (por ejemplo la estufa), la presión baja más y la flama se puede apagar.
- Verificar con un **manómetro**: con el equipo apagado la presión se mantiene, al encender baja y al apagar sube de nuevo. Si cae demasiado al operar, hay un problema de suministro.

### 3.5 El agua sale demasiado caliente

- **Presión baja o poco flujo:** el agua pasa lento por el intercambiador y sube la temperatura.
- Revisar los **controles**: si están en temperatura máxima, bajar el regulador de gas de máximo a mínimo y buscar el confort del cliente.

### 3.6 El agua sale fría con el equipo encendido

- **Distancia** entre el calentador y el servicio mayor a **10 m**: cada metro aproximadamente **un grado menos**.
- **Demasiados servicios simultáneos** (más regaderas o lavabos con agua caliente): hay demasiado flujo, el intercambiador no alcanza a calentar.
- **Controles de temperatura demasiado bajos:** subirlos.

### 3.6 bis Resumen rápido de diagnóstico (gas LP)

| Síntoma | Revisar primero |
|---------|-----------------|
| No enciende, sin chispa | Baterías (>3 V), bobina/válvula pegada, sensor magnético, termostato |
| No enciende, con flujo de agua | Sensor magnético (puente / continuidad) |
| No enciende, flujo bajo | Prueba de cubeta, sarro en sensor de entrada, presión de agua |
| Enciende y se apaga en minutos | Termostato degradado, baterías, flama amarilla/ventilación, presión de gas |
| Se apaga a los 20 min | Es normal por norma de seguridad |
| Agua muy caliente | Flujo bajo, controles, válvula ahorro/normal |
| Agua fría con equipo encendido | Distancia (>10 m), demasiados servicios, controles bajos |

### 3.7 Boiler eléctrico de 1.5 servicios

#### Componentes principales

- Display
- Sensor de temperatura de entrada
- Sensor de temperatura de salida
- Sensor de flujo
- Triac (control de potencia)
- Termostato de alta temperatura
- Resistencia

#### Pruebas de diagnóstico

| Componente | Prueba | Valor esperado |
|------------|--------|----------------|
| **Termostato de alta temperatura** | Continuidad entre terminales. Cuando se dispara, el botoncito central sobresale. Rearmar y confirmar continuidad. | Con continuidad al estar frío y rearmado |
| **Triac** | Entre terminales **1 y 3**: prueba de resistencia y prueba de diodos | Resistencia = **105.9 Ω**; diodos = **0.148 V** *(ambos confirmados contra el boletín Flux Eléctrico E1, modelos MBE081G/MBE040B, de Ernesto — validación del 2026-11-12)* |
| **Resistencia interna** (código 1: no calienta) | Medir resistencia | Entre **4 y 7 Ω** según modelo |
| **Sensor de temperatura (NTC)** | Medir a 25 °C | **47 kΩ** |
| **Sensor de temperatura a 0 °C** (agua con hielo) | Medir a 0 °C | ≈ **150.4 kΩ** *(validado por consistencia de la curva NTC el 2026-11-12: con 47 kΩ a 25 °C da un Beta de ≈3789 K, típico de estos sensores; pendiente solo la medición en campo)* |

#### Instalación eléctrica

- Alimentación **220 V**.
- Identificar fases: **azul y café**, más **tierra física**.
- Interruptor termomagnético (**breaker**) de **40 A doble**.
- **Cable calibre 8.**
- **Tierra física obligatoria** para cualquier eventualidad.

---

## 4. Mantenimiento de calentadores de paso

- **Frecuencia sugerida:** cada **6 meses**. Es esencial para mantener la vida útil del equipo.
- Como el equipo es difícil de desarmar y limpiar por completo, el curso propone un **lavado interno del intercambiador con una bomba** (descalcificado).

### Materiales

| Material | Cantidad |
|----------|----------|
| Mangueras | 2 |
| Conectores de PVC | 2 |
| Tubería de PVC | 1 |
| Cubeta | 20 L |
| Bomba sumergible | 1 |
| Vinagre blanco | 3 L |
| Bicarbonato de sodio | 200 g |

### Procedimiento

1. **Apagar el equipo.**
2. Conectar las mangueras a la **entrada y salida de agua**.
3. Conectar las mangueras a la tubería (circuito cerrado hacia la cubeta).
4. Conectar la **bomba sumergible** en la entrada del agua.
5. Preparar la mezcla en la cubeta: **vinagre + bicarbonato + agua hasta completar ~20 L**.
6. Encender la bomba y dejar circular **30 a 40 minutos**, para que el líquido arrastre sarro y suciedad del intercambiador.
7. Retirar la mezcla y hacer un **enjuague con agua limpia**.
8. Dejar circular agua limpia unos **5 minutos**, **sin encender el gas** del equipo.

> Es un mantenimiento sencillo que se puede hacer por temporada.

---

## 5. Ejercicio Boiler

> ⏳ **Pendiente.** No hay transcripción de esta lección. Agregar aquí el contenido cuando esté disponible.

## 6. Cuestionario #2

> ⏳ **Pendiente.** No hay transcripción ni preguntas de esta evaluación. Agregar preguntas y respuestas correctas cuando estén disponibles; sirven como base de validación para la skill.

---

## Valores por confirmar (⚠️)

| Dato | Lo que dice la transcripción | Por confirmar |
|------|------------------------------|---------------|
| Presión mínima de agua | "1.45 PSA" | ✅ Resuelto (2026-11-12): la unidad es **psi**; ≈1 m de columna de agua. El valor solo lo respalda el curso |
| Presión de gas en onzas | "6.36 h sobre pulgada cuadrada" | ✅ Resuelto (2026-11-12): **oz/pulg²**, confirmado por conversión (2.74 kPa = 11.0" c.a. = 6.36 oz/pulg²) |
| Triac, resistencia (terminales 1 y 3) | "105.9b" | ✅ Resuelto (2026-11-12): **105.9 Ω**, según el boletín Flux Eléctrico E1 de Ernesto |
| Triac, prueba de diodos | "0.148b" | ✅ Resuelto (2026-11-12): **0.148 V**, según el mismo boletín E1 |
| Sensor NTC a 0 °C | "1504kb" | ✅ Consistente (2026-11-12): **150.4 kΩ**; la curva NTC con 47 kΩ a 25 °C da Beta ≈3789 K. Pendiente solo medición en campo |

## Reglas para la skill

1. Responder y validar **solo con base en este documento**; citar la sección correspondiente.
2. Si algo no aparece, decir que **no está cubierto en el curso**.
3. No sugerir quitar el apagado automático de 20 minutos.
4. Para valores marcados con ⚠️, indicar que están pendientes de confirmación.
