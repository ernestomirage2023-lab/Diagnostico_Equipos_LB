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
