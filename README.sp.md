![License: GPLv3](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Platform: Excel](https://img.shields.io/badge/Platform-Microsoft%20Excel-green)
![Language: VBA](https://img.shields.io/badge/Language-VBA-blueviolet)

# Exam‑Excel by Naidel

Sistema de entrenamiento y autoevaluación para exámenes desarrollado en **Microsoft Excel con VBA**.

Exam‑Excel permite practicar preguntas tipo test, simular exámenes reales, registrar estadísticas de aciertos y fallos, y reforzar el estudio mediante retroalimentación y contenido de apoyo.

---

## ✨ Características principales

- ✅ Entrenamiento interactivo tipo examen
- ✅ Selección aleatoria de preguntas
- ✅ Reordenación aleatoria de respuestas
- ✅ Estadísticas de sesión (aciertos, fallos, porcentaje)
- ✅ Estadísticas históricas por pregunta
- ✅ Prioridad para preguntas marcadas en revisión
- ✅ Retroalimentación inmediata
- ✅ Información adicional de estudio
- ✅ Soporte para figuras y gráficos referenciados
- ✅ Glosario de siglas y términos técnicos
- ✅ Interfaz completamente funcional en Excel
- ✅ Sistema de temporizadores persistente entre sesiones  
- ✅ Modos manual y automático de temporización  
- ✅ Comportamiento inteligente de los relojes  
- ✅ Pausa automática al responder en modo automático  
- ✅ Reanudación coherente sin pérdida de contexto temporal 

---

## 🆕 Novedades (v1.1.0)

- ⏱️ Persistencia de temporizadores entre sesiones:
  - Se guarda automáticamente el tiempo total del examen
  - Se conserva el tiempo de cada pregunta
- 🔁 Reanudación de sesiones con recuperación exacta del tiempo
- ⚙️ Modo de temporización Automático / Manual controlado desde la interfaz
  - Selección desde la hoja "Principal"
- ⏸️ Comportamiento automático:
  - El reloj se detiene al responder en modo automático
- ▶️ Lógica inteligente de reanudación:
  - El reloj solo arranca si la pregunta no está respondida
- 💾 Guardado automático del estado al cerrar Excel
- 🛡️ Mejora de robustez:
  - Protección frente a valores de tiempo inválidos o corruptos

---

## 🧭 Flujo de uso básico

1. Abrir el archivo Excel y **habilitar las macros**
2. Ir a la hoja **Principal**
3. Pulsar **Comenzar** para iniciar una nueva sesión
4. Leer la pregunta en la hoja **Pregunta**
5. **Responder haciendo doble clic** sobre la opción deseada
6. Consultar la retroalimentación y continuar con la siguiente pregunta

El modo de temporización puede configurarse como "Manual" o "Automático" desde la hoja Principal.
En modo automático:
- El reloj se detiene automáticamente al responder
- El reloj se reanuda al avanzar a la siguiente pregunta

---

## 🗂️ Estructura del libro

### 📄 Principal
Pantalla inicial del sistema.
Desde aquí se controlan:
- El inicio de sesiones
- La continuación de sesiones existentes
- Los filtros de selección de preguntas

---

### 📄 Pregunta
Pantalla principal del examen.
Muestra:
- Enunciado
- Respuestas posibles
- Indicadores de estado (visto, fallado, revisión)
- Estadísticas de sesión
- Retroalimentación y contenido de estudio

La selección de respuestas se realiza mediante **doble clic**.

---

### 📄 BD (Base de Datos)
Repositorio de preguntas y resultados históricos.

Incluye:
- Enunciado y respuestas
- Respuesta correcta
- Retroalimentación
- Información adicional de estudio
- Estadísticas por pregunta

Esta hoja está pensada para **mantenimiento y edición**, no para uso en examen.

---

### 📄 Sesion
Hoja de uso interno del sistema.

Gestiona:
- Pregunta actual
- Orden aleatorio de respuestas
- Última respuesta seleccionada
- Estado de revisión

Normalmente se encuentra **oculta**.

---

### 📄 Glosario
Relación de siglas y términos técnicos utilizados en las preguntas, con:
- Concepto
- Significado
- Cálculo (si aplica)

---

### 📄 Gráficos
Contiene imágenes, esquemas y gráficos referenciados desde las preguntas mediante textos como:

> “VER FIGURA 1”

---

## 🔀 Aleatoriedad y lógica del sistema

El sistema incorpora varias capas de aleatoriedad:

- Selección aleatoria de preguntas
- Reordenación aleatoria de respuestas
- Prioridad automática para preguntas en revisión
- Respeto de filtros definidos por el usuario

Esto evita la memorización mecánica y mejora el aprendizaje real.

---

## ⚙️ Sistema de temporización

La aplicación incorpora un sistema de doble temporizador:

- Temporizador de sesión → tiempo total del examen
- Temporizador de pregunta → tiempo por pregunta

Características:
- Persistencia automática entre sesiones
- Modos de operación manual y automático
- Gestión inteligente del inicio y pausa

El estado del tiempo se conserva incluso al cerrar el archivo.

---

## 💻 Requisitos

- Microsoft Excel para escritorio
- Macros habilitadas
- No compatible con Excel Online

⚠️ Sin macros habilitadas, la aplicación no funcionará.

---

## 🎯 Casos de uso

Exam‑Excel ha sido diseñado para:

- Preparación de certificaciones
- Estudio técnico
- Oposiciones
- Autoevaluación continuada

Puede adaptarse fácilmente añadiendo nuevas preguntas en la hoja **BD**.

---

## 👤 Autor

**Antonio Teodomiro Márquez Muñoz**  
Alias: **Naidel**  

📧 Contacto: atmarquez@gmail.com

---

## ⚖️ Licencia

Este proyecto se distribuye bajo la licencia:

**GNU General Public License v3 (GPLv3)**

Puedes:
- Usar el software
- Estudiarlo
- Modificarlo
- Redistribuirlo

Siempre que mantengas la misma licencia y respetes sus términos.

El programa se distribuye con la esperanza de que sea útil,  
pero **SIN NINGUNA GARANTÍA**, ni siquiera la implícita de  
COMERCIABILIDAD o ADECUACIÓN PARA UN PROPÓSITO PARTICULAR.

📄 Texto oficial de la licencia:  
https://www.gnu.org/licenses/gpl-3.0.html

---

## 🤝 Contribuciones y feedback

Las sugerencias, mejoras y correcciones son bienvenidas.

- Usa el sistema de *Issues* de GitHub para reportar problemas
- Si adaptas el proyecto a otro tipo de examen, no dudes en compartirlo

---

## ✅ Estado del proyecto

- Versión actual: **1.0.0**
- Estado: **Estable**
- Uso real y probado en entrenamiento de exámenes

---

### 📌 Nota final

Exam‑Excel nació como una herramienta personal y se libera como software libre con el objetivo de compartir una solución práctica, honesta y reutilizable para el estudio y la autoevaluación.

---
