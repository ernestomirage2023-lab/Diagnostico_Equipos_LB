---
equipo: boiler
marca: [pendiente]
modelos: [MBF06ZB, MBF06ZC, MBF10BB, MBF10BC, MBF16NB, MBF16NC, MBF06ED, MBF06EF]
tipo: gas (L.P. y natural), encendido por chispa, alimentado con baterías
servicios: 1 o 2
etiquetas: [boiler, gas, revision-completa, logica-funcionamiento, fallas, chispa, flujo, presion-gas]
actualizado: 2026-11-11
Boiler a gas MBF: lógica de funcionamiento y revisión completa
1. Modelos
Grupo	Modelos	Notas
Con display	MBF06ZB, MBF06ZC, MBF10BB, MBF10BC, MBF16NB, MBF16NC	Muestran temperatura y códigos de error (E2, E3)
Por tipo de gas	MBF06ED (Gas L.P.), MBF06EF (Gas Natural)	[pendiente confirmar si tienen display]
Equipos para 1 o 2 servicios: el consumo de agua define la velocidad del flujo.
2. Verificaciones previas (antes de revisar fallas)
Tipo de gas: confirmar que el equipo es del mismo gas que la instalación (L.P. o natural). Quemadores, válvulas, entradas y espreas son de tamaño distinto según el gas. Un equipo con gas equivocado no debe instalarse.
Gas disponible: que haya suministro.
Baterías: deben ser alcalinas. Las de carbón-zinc solo funcionan por poco tiempo.
Agua: presión y flujo acordes a las características del equipo (ver prueba de flujo, sección 6).
3. Lógica de funcionamiento (secuencia normal)
Se abre una llave de agua y el agua pasa por el sensor de flujo (sensor magnético). El imán se desplaza con el flujo y, al llegar a su posición, indica que hay flujo.
El sensor manda la señal de encendido al módulo de ignición.
El módulo genera chispa en dos chisperos conectados por cable.
Mientras hace chispa, el módulo manda voltaje a la bobina de la válvula de gas. Al recibir voltaje, el émbolo se contrae y la válvula abre para permitir el paso del gas. Si la válvula no opera, no funciona nada del equipo.
Sale el gas y se enciende la flama.
El sensor de flama (de seguridad) detecta la flama y avisa al módulo: la chispa se detiene y el equipo queda funcionando con retroalimentación (sensor de flama → módulo → válvula).
Si el sensor de flama pierde la señal, el módulo cierra la válvula y la flama se apaga.
El termostato de la parte superior es otra protección. Tiene un bimetal interno que se abre cuando el equipo pasa de 85 °C: al abrirse se pierde la señal y el equipo se apaga para protegerse.
4. Fallas y puntos a revisar (en orden)
Falla 1: No enciende / no hace chispa
Primero tener la etapa inicial completa: gas, flujo de agua correcto y baterías alcalinas en buen estado.
Revisar el sensor magnético / de flujo: el imán debe desplazarse con el flujo y dar señal de encendido al módulo. Si no se desplaza o no da señal, el equipo no enciende. (Ver video en la sección 9.)
Si el sensor responde, revisar el módulo de ignición.
Revisar el cable de los chisperos y el de la señal de flama. Con más de 1 año de uso, los cables se pueden tostar por el calor, endurecerse, abrirse y dar mal contacto. Cambiar si están así.
Si el cableado está bien y el módulo no genera chispa, solicitar cambio de módulo.
Falla 2: Hace chispa pero no sale flama / la válvula no abre
Verificar si la válvula opera: al hacer chispa, el émbolo debe contraerse y abrir el paso del gas. Si no opera, el equipo no funciona.
El empaque de la válvula puede quedar pegado: despegarlo.
Medir voltaje en dos puntos: el que sale de la tarjeta y el que recibe la bobina.
Sale voltaje de la tarjeta y la bobina lo recibe, pero el émbolo no se mueve: problema de bobina o válvula.
No sale voltaje de la tarjeta: problema de la tarjeta; solicitar cambio.
Falla 3: Hay flama pero el equipo sigue haciendo chispa
Si hay flama visible y el equipo sigue pidiendo chispa por más de 1 segundo, la señal del sensor de flama no llega al módulo.
Revisar el cableado del sensor de flama: que no esté quemado ni tostado.
Si el cableado está bien, el módulo no recibe la señal y debe cambiarse.
Falla 4: Hay flama pero se apaga en poco tiempo
Revisar la continuidad del termostato de la parte superior. Su bimetal se abre por arriba de 85 °C y corta la señal; con el equipo frío debe tener continuidad [confirmar]. Si está frío y no tiene continuidad, el termostato está dañado.
Si el termostato abre porque el equipo sí se calentó de más, buscar la causa del sobrecalentamiento: flujo de agua bajo (ver falla 5 y prueba de flujo).
Revisar el sensor de flama y su cableado (falla 3).
Revisar la presión dinámica del gas (falla 6): si cae al abrir la válvula, la flama también puede apagarse por eso.
Falla 5: Enciende pero no calienta (o calienta de más)
Casi siempre es el flujo de agua.
Flujo bajo: el equipo puede sobrecalentarse y el agua sale muy caliente.
Flujo alto: el agua no alcanza a calentar.
Hacer la prueba de flujo (sección 6) y revisar la capacidad del equipo.
Falla 6: Enciende pero la flama es pequeña / se apaga al abrir la válvula
Revisar la presión de gas, estática y dinámica.
Presión estática: se mide con la válvula del equipo cerrada. Debe estar en la presión ideal.
Presión dinámica: se mide con la válvula abierta y el equipo funcionando. Debe mantenerse cerca de la ideal.
Síntoma típico: la estática está bien, pero al abrir la válvula la presión baja. Entonces el equipo se apaga, o la flama baja y el agua calienta menos.
Conclusión: si la presión cae al abrir la válvula, el problema está en el suministro de gas (no en el equipo). Causas a descartar (a confirmar): tanque con poco gas, regulador, línea o manguera insuficiente o restringida.
Valores de referencia de presión (L.P. y natural): [pendiente]
5. Códigos de error (modelos con display)
Código	Significado	Qué revisar
E2	Bajo voltaje: detecta menos de 2.5 V	Cambiar baterías por alcalinas nuevas
E3	Exceso de temperatura / sensor de salida [confirmar descripción]	Flujo de agua (bajo flujo sobrecalienta), sensor de salida
6. Prueba de flujo de agua
Llenar una cubeta de 20 litros: debe tardar entre 3 y 4 minutos para que el equipo opere bien (equivale a unos 5 a 6.7 L/min).
Tarda más de 4 min (flujo bajo): el agua saldrá muy caliente.
Tarda menos de 3 min (flujo excesivo): el equipo no calienta bien.
Regla general: a mayor flujo, menos calienta; a menor flujo, más calienta. El flujo depende del consumo y de la presión del agua, por eso en un equipo de 1 o 2 servicios abrir más llaves a la vez cambia la temperatura.
7. Checklist de revisión completa
[ ] El equipo corresponde al gas de la instalación (L.P. o natural)
[ ] Hay suministro de gas
[ ] Baterías alcalinas y con voltaje suficiente
[ ] Presión y flujo de agua correctos (cubeta de 20 L en 3 a 4 min)
[ ] El sensor magnético / de flujo se desplaza y da señal
[ ] El módulo genera chispa en los dos chisperos
[ ] Cables de chisperos y de sensor de flama sin quemar ni endurecer
[ ] La válvula abre (empaque no pegado) y la bobina recibe voltaje
[ ] El sensor de flama detecta y la chispa se detiene en menos de 1 s
[ ] Continuidad del termostato superior
[ ] Presión de gas dinámica y estática correctas
8. Refacciones
Clave	Descripción	Falla que resuelve
[pendiente]	Módulo de ignición	1, 3
[pendiente]	Tarjeta	2
[pendiente]	Bobina / válvula	2
[pendiente]	Cables de chisperos y sensor de flama	1, 3
9. Material relacionado
Video sensor magnético (carpeta Videos en Drive): https://drive.google.com/drive/u/0/folders/18HaHIlO2AsSRkCKFARBOwZf1frnLv2E6
Video termostato (bimetal, abre a más de 85 °C): https://drive.google.com/file/d/1eyaGCsnOqVX2OOv0wqGQyAD_aq6_n5Ph/view?usp=drive_link
Video válvula / bobina (recibe voltaje y se contrae con la chispa): https://drive.google.com/file/d/1pTbSueucMA7daVBgmvqNl9FwBKxIv9Ii/view?usp=drive_link
Video presión dinámica y estática: https://drive.google.com/file/d/1-dYpzs57t78WJcRR7Z8lKcHwvAnvQQoj/view?usp=drive_link
Video flama pequeña: [pendiente]
Video flujo de agua (a mayor flujo calienta menos, a menor flujo calienta más): https://drive.google.com/file/d/1WzMl3IpTaYr92pX7nca8X-E1kEVL3-Y6/view?usp=drive_link
Manual de servicio: [pendiente]
