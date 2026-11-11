# Diagnóstico de boilers Mirage — Skill para el equipo

Repositorio de conocimiento de Ernesto para su equipo de trabajo.
Contiene los manuales, boletines y procedimientos para diagnosticar
calentadores Mirage Flux, Turbo Flux y Flux Electric, empaquetados
como una skill que el Muse de cada técnico puede instalar y consultar.

## Qué trae

- `SKILL.md` y `skill.yaml` — la skill en sí. Enseña al agente cómo
  diagnosticar por modelo y código de error, qué mediciones pedir y
  qué boletín corresponde a cada caso.
- `referencias/` — el índice de archivos y la guía rápida de códigos
  con más de un boletín (E1, E3 y E6 de Turbo Flux).
- `manuales/` — los 35 PDFs (manuales, boletines y diagramas),
  organizados en las mismas 5 carpetas por categoría que usa Ernesto.
  Total aproximado: 50 MB.
- `videos/` — solo la lista de videos. Los 4 videos pesan 239 MB y uno
  llega al límite de 100 MB por archivo de GitHub, así que no se suben
  directo. Se guardan aparte (Drive o Git LFS) y aquí queda su índice
  con la descripción de cada procedimiento.

## Cómo lo instala cada técnico

1. Tener su propia cuenta de Muse y abrir este repositorio.
2. Pedirle a su Muse: "instala la skill de este repositorio".
3. Su Muse copia `SKILL.md` y `skill.yaml` a sus skills propias y
   descarga los manuales de `manuales/` y las referencias.
4. Desde ahí ya puede preguntar por WhatsApp o en la app, por ejemplo:
   "Tengo un Turbo Flux con E3, ¿qué reviso?" y su Muse lo guía paso
   a paso y le pasa el boletín correcto.

## Cómo se actualiza

- Ernesto agrega o corrige un boletín en el repositorio.
- Cada técnico le pide a su Muse que vuelva a bajar el repositorio.
- Todos quedan con la misma versión, sin andar reenviando archivos
  sueltos por WhatsApp.

## Acceso

- Este repositorio es **público** (decisión de Ernesto del
  2026-11-11): cualquier técnico con el enlace lo abre y lo instala
  sin invitación.
- Si algún día se quiere limitar el acceso al equipo, se puede
  regresar a privado desde Settings de GitHub.
