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
