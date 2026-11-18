# Refrigeradores

Categoría creada el 2026-11-12 a petición de Ernesto, dentro del proyecto Diagnostico_Equipos_LB. **Ya tiene material inicial.**

- Lo que hay de esta categoría está en **`referencias/refrigeracion-domestica-modulo-5.md`** (Módulo 5 del curso de Ernesto): el **ciclo de refrigeración** por compresión de vapor y los **tipos de equipos** (refrigeradores de una puerta; diferencias por distribución del sistema, control de temperatura y uno o dos evaporadores).
- Del **curso** (Módulo 5) aún no hay lección de revisión de componentes de refrigeradores; pero desde el 2026-11-18 **sí hay un manual de servicio completo de un modelo: el MRX12FS** (abajo), con valores de medición, códigos de error y procedimientos. Para otros modelos de refrigerador sin manual, di que ese material está pendiente y no inventes procedimientos.
- La carpeta de Drive **Github / Refrigeradores** (https://drive.google.com/drive/folders/1m4BeVUxRpl9kiTMpMaUKNUAbWYjSFTUX) ya tiene sus 2 primeros archivos registrados en `referencias/indice-drive.md`: el documento del **refrigerador/frigobar REFX90** (21 págs.) y el **diagrama explosivo del MRX33ES** (enviados por Ernesto el 2026-11-12).
- Conforme Ernesto comparta más material de esta categoría, se registrará en `referencias/indice-drive.md` y se documentará aquí, siguiendo las mismas reglas de respuesta de la skill.

## Manual de servicio del MRX12FS (desde el 2026-11-18)

- En Drive (carpeta Refrigeradores) está el **Manual de Servicio Técnico en español del MRX12FS** (63 págs.), elaborado a partir del manual de servicio en inglés del fabricante: seguridad, instalación y puesta en marcha, partes principales y dimensiones, sistema de control eléctrico (parámetros, diagrama de circuito y terminales de la tarjeta principal), sistema de refrigeración, desmontaje de partes, sistema de sensores con **tabla R/T**, funciones y operación, compresor y **solución de problemas**. Hay versión **PDF** y versión **editable DOCX**; ambas están en `referencias/indice-drive.md`.
- **Datos clave del MRX12FS (del manual):** alimentación **115 V / 60 Hz**; compresor **EZ65H1Y** (resistencia del devanado Rmc **6.83 Ω ±7 %**; PTC **8EA14B3-02**); vacío del sistema **< 6 Pa**.
- **Códigos de error (se indican con los LED del panel):** **E1** = falla del sensor de la cámara de refrigeración (LED ① y ②); **E5** = falla del sensor de descongelación del congelador (LED ① y ③); **E7** = falla del sensor de temperatura ambiente (LED ① y ④). Revisión de los tres: verificar terminales de conexión (bien insertadas y sin suciedad), medir la resistencia del sensor contra la tabla R/T; si el valor es incorrecto, cambiar el sensor; si la falla persiste, cambiar la tarjeta principal.
- **Tabla R/T de sensores (valores de referencia):** −30 °C = **33.81 kΩ**; 25 °C = **2.005 kΩ**; 44 °C = **0.914 kΩ**. La tabla completa (75 valores) está en el manual.
- **Modo de prueba:** mantener presionado el botón de ajuste **10 segundos**; da acceso a enfriamiento forzado y descongelación forzada (detalle en el manual, cap. 9.7).
- ⚠️ **Discrepancia señalada en el propio manual, pendiente de validación:** el equipo es de 115 V, pero la tabla de parámetros eléctricos lista la resistencia de descongelación y el fusible a **230 V**. No des ese dato por confirmado sin la validación de Ernesto.
