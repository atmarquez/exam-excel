# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog
and this project adheres to Semantic Versioning.

---

## [1.1.1] - 2026-07

### ✨ Added
- Consulta rápida de respuestas mediante clic simple una vez respondida la pregunta.
- Visualización inmediata de la retroalimentación de cualquier respuesta sin modificar la respuesta contabilizada.
- Indicador visual persistente de la respuesta seleccionada por el usuario mediante un marco de resaltado dedicado.
- Posibilidad de revisar todas las retroalimentaciones de una pregunta antes de avanzar a la siguiente.

---

### 🔄 Changed
- Mejora del flujo de revisión de respuestas tras responder una pregunta.
- Sustitución del sistema de resaltado mediante bordes de celda por un indicador visual independiente basado en Shape.
- El indicador de respuesta seleccionada ahora cubre toda la fila de la respuesta (columnas B:M).
- Revisión de la lógica de limpieza visual al iniciar una nueva pregunta y al comenzar una nueva sesión.

---

### 🛠 Fixed
- Corregido un problema que eliminaba los bordes originales de las respuestas al utilizar la consulta rápida de retroalimentación.
- Corregido un problema visual que provocaba la aparición de distintos tonos de borde azul al resaltar respuestas.
- Corregido un problema por el que el color de una respuesta consultada desaparecía al navegar entre respuestas mediante clic simple.
- Corregido un problema que impedía identificar claramente la respuesta seleccionada por el usuario tras consultar otras respuestas.
- Corregido el reseteo incorrecto de los contadores de sesión al iniciar un nuevo examen: Los contadores se reinician ahora correctamente en las celdas P5:P8.
- Corregida la limpieza del indicador de respuesta seleccionada al comenzar una nueva sesión.
- Corregida la limpieza del indicador de respuesta seleccionada al avanzar a la siguiente pregunta.

---

### 💡 Usability Improvements
- La revisión posterior de respuestas es ahora más rápida e intuitiva.
- Se mantiene claramente diferenciada la respuesta contabilizada frente a las respuestas simplemente consultadas.
- Mayor consistencia visual entre preguntas, sesiones y navegación por retroalimentaciones.

---

## [1.1.0] - 2026-06

### ✨ Added
- Sistema de persistencia de relojes entre sesiones:
  - Guardado automático de `SegundosSesion`
  - Guardado automático de `SegundosInicioPregunta`
- Recuperación del estado del cronómetro al continuar la sesión
- Guardado automático del estado al cerrar Excel (`Workbook_BeforeClose`)
- Función `EsModoAutomatico()` como punto central de decisión del modo
- Validación de consistencia de datos de tiempo (control de valores corruptos)
- Mejora del flujo al continuar sesión:
  - No se inicia el reloj si la pregunta ya está respondida
- Mejora del comportamiento del modo automático:
  - Pausa automática al responder
  - Reanudación automática en nueva pregunta

---

### 🔄 Changed
- Eliminada la variable global `modoAutoTimer` como fuente de verdad
- El modo del sistema pasa a ser controlado exclusivamente por la UI:
  - Celda `Principal!G14` (Automático / Manual)
- Refactor del control de relojes para depender de `EsModoAutomatico()`
- Reestructuración de `ActivarModoAutomatico`:
  - Controla correctamente estados de pregunta respondida
  - Evita incoherencias de ejecución del reloj
- Mejora en la coherencia del flujo:
  - Diferenciación clara entre iniciar, pausar y cambiar modo
- Limpieza del código eliminando lógica duplicada de estado

---

### 🛠 Fixed
- Problema donde el reloj seguía en ejecución tras responder en modo automático
- Problema donde el modo automático no se mantenía entre ejecuciones
- Problema donde el reloj arrancaba con preguntas ya respondidas
- Posibles inconsistencias en tiempos al cargar sesión (valores negativos o inválidos)
- Sincronización incorrecta entre estado interno y UI

---

### 🧹 Removed
- Eliminado almacenamiento redundante del modo automático en hoja "Sesion"
- Eliminado uso de variables globales para control de modo
- Eliminada lógica duplicada de control de estado del modo automático

---

### 💡 Technical Improvements
- Diseño orientado a "single source of truth" para el estado del sistema
- Mejora de la robustez del sistema de temporización basado en `Application.OnTime`
- Mejora de mantenibilidad mediante funciones centralizadas de lectura de estado
- Mayor coherencia entre lógica de UI y lógica de negocio

---

## [1.0.0] – 2026‑04‑16
### Added
- Motor completo de examen en Excel
- Sistema de preguntas con aleatoriedad
- Estadísticas por sesión y por pregunta
- Cronómetros de sesión y pregunta
- Documentación integrada y web GitHub Pages

### Fixed
- Sincronización de relojes
- Gestión robusta de Application.OnTime