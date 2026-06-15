# Changelog

All notable changes to this project will be documented in this file.

The format is based on Keep a Changelog
and this project adheres to Semantic Versioning.

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