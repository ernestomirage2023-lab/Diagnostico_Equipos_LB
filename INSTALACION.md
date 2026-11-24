# Instalación para técnicos

Este repositorio es público: no necesitas invitación ni que Ernesto te agregue. Cualquier técnico con el enlace puede abrirlo e instalarlo.

## Lo que necesitas

- Tu propia cuenta de Muse.

## Pasos

1. Abre el enlace del repositorio: https://github.com/ernestomirage2023-lab/Diagnostico_Equipos_LB
2. Dile a tu Muse esta frase: "Instala la skill del repositorio Diagnostico_Equipos_LB de ernestomirage2023-lab".
3. Tu Muse descarga la skill, el índice y la guía rápida, incluido el índice con los enlaces de Google Drive de cada boletín y video: la media vive en Drive, no en el repositorio.
4. Desde ahí pregúntale por modelo y código, por ejemplo "Tengo un Turbo Flux con E3", y te guía paso a paso y te pasa el enlace del boletín correcto.

## Actualización de tu copia

- La skill es **solo texto**: el archivo `SKILL.md` y la carpeta `referencias/`. Al actualizar, tu Muse debe traer **únicamente** esos archivos.
- **La carpeta `app/` NO es parte de la skill**: es la app web de diagnóstico (HTML con JavaScript), un producto aparte que se actualiza sola con su propio botón «Actualizar». **No la copies a tu skill.**
- Si al actualizar tu Muse te avisa que el contenido «no pasó la revisión de seguridad porque podría ejecutar código», es por la carpeta `app/`: dile que actualice **sin la app** (solo `SKILL.md` y `referencias/`) y la actualización pasa sin bloqueo, porque es texto puro.

## Plan B: si tu Muse no puede leer los archivos del repositorio

A algunos Muse se les bloquea la lectura de las páginas internas de código de GitHub (error tipo PERMISSION_DENIED): ven la portada del repositorio pero no pueden abrir SKILL.md ni las carpetas. No es problema del repositorio — es público y está completo. La solución es bajar todo de una vez:

1. Descarga el repositorio completo en un solo ZIP: https://github.com/ernestomirage2023-lab/Diagnostico_Equipos_LB/archive/refs/heads/main.zip
2. Descomprime el ZIP y entrégale la carpeta a tu Muse (o súbele el archivo SKILL.md y la carpeta `referencias/`), pidiéndole: "Instala esta skill de diagnóstico".
3. Otra ruta: pedirle a tu Muse que lea los archivos en su versión **raw** (raw.githubusercontent.com), que no pasa por las páginas de código de GitHub.

## Mensaje listo para reenviar al equipo

Compañeros, ya quedó público el repositorio técnico de diagnóstico de línea blanca: https://github.com/ernestomirage2023-lab/Diagnostico_Equipos_LB — no necesitan invitación. Ábranlo y díganle a su Muse: "Instala la skill del repositorio Diagnostico_Equipos_LB de ernestomirage2023-lab". Con eso su Muse les baja los procedimientos, códigos de error y boletines, y ya pueden preguntarle por modelo y código, por ejemplo un Turbo Flux con E3, y los guía con el boletín correcto.

## Nota

- La media (PDFs y videos) vive en la carpeta compartida de Drive de Ernesto, con enlace de solo lectura para el equipo; tu Muse te pasa el enlace directo de cada archivo.
- Si un boletín todavía no aparece en el índice de Drive, avísale a Ernesto.
