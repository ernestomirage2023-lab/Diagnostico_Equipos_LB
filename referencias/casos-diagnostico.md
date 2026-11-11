# Casos de diagnóstico confirmados por Ernesto

Casos reales, validados por Ernesto, para fallas que se describen por síntoma y no por código de error.

## MBF06ED — Hace chispa y la flama sigue encendida

**Síntoma:** el equipo genera chispa, la flama enciende, y sigue chispeando ya con la flama puesta.

**Clave del modelo:** en el MBF06ED la tarjeta que genera la chispa también hace la lectura de todo, incluida la flama. No hay un módulo lector separado.

**Lo que se descarta con el síntoma:**

- El generador de chispa: sí hay chispa, esa etapa trabaja.
- La válvula y el paso de gas: la flama sí enciende.

**Revisión, en orden:**

1. Electrodo de lectura: limpio y dentro de la flama.
2. Cable del electrodo hasta la tarjeta: sano y bien conectado.
3. Si la señal de lectura llega bien y el equipo sigue sin registrar la flama, la falla está en la tarjeta, en su etapa de lectura.

**Conclusión:** sospechosa principal, la tarjeta. La etapa de chispa funciona; la de lectura, no, y viven en la misma pieza.

## MBF06ED — No enciende, con baterías nuevas

**Síntoma:** al abrir el agua el equipo no enciende nada (ni clic, ni chispa), y las baterías son nuevas.

**Lógica:**

- Baterías nuevas casi descartan falta de energía; solo se confirma polaridad correcta y terminales limpios.
- Si no hay ni un intento, lo probable es que el equipo no esté detectando el flujo de agua, así que ni siquiera manda el encendido.

**La prueba del puente (la que divide el diagnóstico):**

1. Desconecta el sensor magnético de su conector.
2. Puentea los dos cables del conector del lado del equipo (el arnés), simulando el sensor cerrado, como si hubiera flujo.
3. Abre la llave del agua caliente.

**Interpretación:**

- Con el puente el equipo **sí enciende**: tarjeta, chispa y válvula trabajan; la falla está en la detección, es decir, el sensor magnético o el imán/flotador que no se mueve (revisar sarro en el conjunto de agua).
- Con el puente **sigue sin encender**: no es el sensor; sigue tarjeta o cableado.

**Confirmación con multímetro (boletín del sensor magnético):** sin contacto con el imán debe marcar abierto (O.L); en contacto con el imán debe cerrar (beep). Si no cierra con el imán, el sensor está malo y se cambia.

**Material de apoyo en Drive:** boletín «Boiler 6 Lts Blanco Sensor Magnético» y video «Magnetico prueba» (enlaces en `referencias/indice-drive.md`).

## MBF06ED — Hay chispa, pero la flama nunca abre

**Síntoma:** al abrir el agua sí se oye/ve la chispa, pero la flama nunca abre.

**Centro del problema:** la bobina de la válvula de gas. Tres causas posibles (criterio de Ernesto):

1. La tarjeta de control no entrega voltaje a la bobina.
2. Baterías: no hay, o no alcanzan — puede alcanzar para la chispa, pero no el voltaje que necesita la bobina para abrir.
3. El empaque o la bobina está pegada: falla mecánica; aunque le llegue voltaje, no abre.

**Cómo se separa:** mide si le llega voltaje a la bobina.

- No llega voltaje → tarjeta de control o baterías.
- Sí llega voltaje y no abre → bobina o empaque pegado.

**Material de apoyo:** boletines del 6 L blanco de electroválvulas y de prueba de válvula, y el video de la bobina de gas.

## Turbo Flux MBF16AF — Enciende bien, pero a los pocos segundos se apaga solo

**Síntoma:** el equipo arranca y enciende, pero a los pocos segundos se apaga solo.

**Lógica:** si encendió, el arranque está bien; el corte viene de una protección o de una alimentación que se cae. Causas a revisar (criterio de Ernesto):

1. **Termostato:** hacerle su revisión de diagnóstico; puede estar cortando muy pronto y el equipo se protege.
2. **Transformador con falla:** no entrega la corriente suficiente; bajo carga el voltaje se cae y el equipo se apaga.
3. **Motor del ventilador:** no genera el vacío suficiente; también revisar que no esté en corto y medirlo.
4. **Sensor de vacío:** no actúa como debe ser, y sin esa señal el equipo corta.
5. **Tarjeta:** que no tenga falsos contactos ni terminales sulfatadas, que nada esté fallando en ella, y revisar que su alimentación sea la correcta.

**Material de apoyo:** boletines Turbo Flux E6 de vacío (sensor y manguera de succión), E6 de motor (capacitor de 2.5 µF y resistencias del motor) y E1 de voltaje (salida del transformador).

## MBF10AD — Marca código E2

**Síntoma:** el display marca el código de falla E2.

**Centro del problema:** el módulo de ignición (la tarjeta) y su alimentación, según el boletín del modelo y el criterio de Ernesto. Revisión, en orden:

1. **Voltaje de entrada:** menor a 110 VCA provoca operación inestable del módulo, con ausencia o intermitencia de chispa y bloqueos de seguridad.
2. **Conectores:** que no estén flojos ni sulfatados; causan caída de voltaje hacia el módulo y encendidos erráticos o falta total de ignición.
3. **Falsos contactos:** vibraciones, humedad o arneses mal sujetos generan interrupciones momentáneas y reinicios del módulo.
4. **Reinicio de la tarjeta:** desconectar el equipo y volver a conectarlo a los 5 minutos, para que la tarjeta se reinicie.
5. Si el E2 persiste con todo lo anterior bien, el módulo está dañado y hay que **reemplazar la tarjeta**.

**Material de apoyo:** boletín de código E2 del MBF10AD/MBF10AE (en Drive).

## MBE081G — El display enciende, pero el agua no calienta

**Síntoma:** en el Flux Electric de 1.5 servicios, al haber flujo el display enciende y el equipo detecta el flujo, pero el agua no calienta nada.

**Lógica:** si el display enciende con el flujo, la alimentación y la detección de flujo trabajan. Lo que no está llegando es la señal (los pulsos) para calentar. Revisión (criterio de Ernesto):

1. **Tarjeta (de display/control):** detecta el flujo pero no manda la señal; problema en la tarjeta.
2. **Triac:** revisar que esté generando los pulsos; es el que conmuta la potencia hacia la resistencia.
3. **Resistencia:** medirla; si está dañada o abierta, hay señal pero no calienta.
4. **Fusible de la tarjeta:** medirlo; puede estar abierto.

**Material de apoyo:** boletín de triac/resistencia del Flux Eléctrico y el video del Flux Electric (resistencia, triac, sensores y protector térmico).

## MBF06ED — Con poca presión de agua no arranca; con la llave bien abierta sí

**Síntoma:** el equipo enciende bien con buen flujo, pero con poca presión de agua no arranca.

**Clave del modelo:** el equipo necesita un flujo mínimo de 5 litros por minuto para poder encender. Si el flujo no llega a ese mínimo, no es una descompostura: el equipo simplemente no alcanza su punto de arranque.

**Lo que puede estar limitando el flujo (instalación, no el equipo):**

- La restricción de la regadera (el ahorrador): quitarla, probar el equipo y ver si el problema se mantiene.
- Las bajas de presión de la instalación hidráulica de la casa: codos, el tipo de regadera y demás elementos que recortan el flujo antes de llegar al equipo.

**Confirmación:** en la salida de agua caliente, quitar la manguera y observar el equipo con salida libre. Si ahí enciende normal, el equipo está bien instalado y trabajando correctamente, y el problema queda en la instalación.
