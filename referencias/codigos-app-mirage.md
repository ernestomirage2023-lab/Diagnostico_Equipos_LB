# Códigos de la app oficial de Mirage — Línea Blanca

Referencia extraída el 2026-11-11 de la app oficial «Códigos Diagnóstico» de Mirage (https://codigos-error-app.mirage-apps.com/families), sección Línea Blanca: 11 equipos, 61 entradas de código. Aquí va el resumen por equipo; el detalle completo de soluciones vive en la app.

## Calentador de paso

### FLUX ELECTRIC (modelos MBE040B y MBE081G)

- **E1** — Protección por alta temperatura.
- **E3** — Falla en sensor de temperatura.

### FLUX, de gas (modelos MBF06ZB, MBF06ZC, MBF10BB, MBF10BC, MBF10BR, MBF16NB, MBF16NC, MBF16NG)

- **E2** — Voltaje de batería baja.
- **EE** — Protección por alta temperatura (>90 °C, termostato).

### TURBO FLUX (modelo MBF16AF)

- **E0** — Fallo en sensor de salida de agua.
- **E1** — Fallo en circuito eléctrico del sensor de flama.
- **E2** — Protección de fugas en cámara de combustión.
- **E3** — El encendido falló o se apagó accidentalmente.
- **E4** — Fallo en sensor de entrada de agua.
- **E5** — Protección por sobrecalentamiento (>75 °C).
- **E6** — Turbo extractor dañado o cámara de extracción obstruida (motor, capacitor, sensor de vacío).
- **E7** — Falla por válvula abierta o desconectada.
- **nE** — Debe cambiarse el cable de encendido.

## Lavadora Automática-Digital

### LMA017D, LMA017E, LMA019D y LMA019E (idénticos entre sí)

- **E1** — El llenado toma demasiado tiempo (>1 hora).
- **E2** — El drenado toma demasiado tiempo (>10 minutos).
- **E3** — Tapa abierta.
- **E4** — Lavadora desbalanceada.

### LMA022D

- **C9** — Falla de la PCB.
- **CL** — Tapa abierta más de 20 segundos con «Bloqueo de control» activo.
- **E1** — El llenado toma demasiado (1 hora).
- **E2** — La descarga toma demasiado (10 minutos).
- **E3** — Tapa abierta.
- **E4** — Lavadora desequilibrada.
- **F2** — Falla de la PCB.
- **F5** — Falla en la detección de carga.
- **F8** — Falla en sensor de nivel de agua.
- **Fd** — Falla en bloqueo de la tapa.

## Lavadora Automática-Perilla (códigos por patrón de LEDs)

### LMA022G (8 patrones)

1. Llenado demasiado tiempo (>30 minutos).
2. Drenado más de 10 minutos.
3. Tapa abierta.
4. Lavadora desequilibrada.
5. Lavadora desnivelada; falla en sensor de impacto.
6. Falla en la detección de carga.
7. Falla en sensor de nivel de agua.
8. Falla en cerradura de puerta.

### LMA022M (7 patrones)

1. Alarma de llenado durante más de 1 hora.
2. Alarma de drenado durante más de 10 minutos.
3. Tapa no cerrada para iniciar el secado.
4. Exceso de vibración en el secado.
5. Falla en sensor de nivel de agua.
6. Falla en el seguro de la tapa.
7. Bloqueo de niños intermitente; falla de comunicación.

### LMA022N (7 patrones)

Igual que LMA022M, excepto la entrada 2: tiempo de drenaje ≥ 6 minutos, revisar sensor de nivel, su manguera y la bomba de drenado.

> Nota: las imágenes de los patrones LED de LMA022M (entradas 2 a 7) y LMA022N no cargaron en la app al extraer esto; sus descripciones y soluciones sí se verificaron. Los patrones de LMA022G y la entrada 1 de M sí se verificaron.

## Cruce con los boletines y documentos de Ernesto

**Empatan (hay boletín o documento):**

- **TURBO FLUX E0 a E7:** todos tienen boletín en el archivo (E1 con variantes de reinicio de tarjeta y voltaje; E3 con cables, limpieza y válvula; E6 con motor y vacío). La app es el resumen; los boletines traen el procedimiento con mediciones.
- **FLUX ELECTRIC E1:** empata con el boletín de código E1 del Flux Eléctrico. El **E3** de la app empata con lo que cubre el video del Flux Electric (código E3 y sensores); no hay boletín PDF específico de E3 en el archivo.
- **LMA022G: empate completo, 8 de 8.** Las 8 entradas de la app coinciden con los 8 códigos del documento de lavadoras de Ernesto (E1, E2, E3, E4, E5, F5, F8 y Fd). Detalle útil: en el llenado la app marca >30 minutos, que apoya el valor de las diapositivas de diagnóstico del documento, no el de 5 minutos de su tabla (contradicción que el documento ya traía marcada para verificar).

**Solo en la app (sin boletín en el archivo):**

- **TURBO FLUX nE** (cable de encendido): no hay boletín.
- **FLUX de gas E2 y EE:** la app los amarra a la serie Z/B/N (MBF06ZB/ZC, MBF10BB/BC/BR, MBF16NB/NC/NG); los boletines del archivo son de la serie ED/EF, sin códigos E2/EE (el de baterías y el de termostato bimetálico tocan los temas, sin ser de código).
- **Lavadoras LMA017D/E, LMA019D/E, LMA022D, LMA022M y LMA022N:** no hay documentos de estos modelos en el archivo; la app es, por hoy, la única referencia. Ojo: LMA022M no es la LMS-022M semiautomática del documento de lavadoras.

**Solo en el archivo (la app no los cubre):**

- **MBF10AD/MBF10AE (10 L con WiFi):** la app no trae este equipo; los boletines E0, E1, E2, E3 y E5 del archivo son la única referencia.
- **MBE051G (eléctrico 1 servicio):** la app no lo lista; quedan su manual, el boletín de «equipo no calienta» y el boletín de error E4 (código que la app no muestra para Flux Electric).
