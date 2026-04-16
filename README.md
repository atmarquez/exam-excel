![License: GPLv3](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Platform: Excel](https://img.shields.io/badge/Platform-Microsoft%20Excel-green)
![Language: VBA](https://img.shields.io/badge/Language-VBA-blueviolet)

# Exam‑Excel by Naidel

An interactive training and self‑assessment system for exams, developed in **Microsoft Excel with VBA**.

Exam‑Excel allows users to practice multiple‑choice questions, simulate real exam scenarios, track correct and incorrect answers, and reinforce learning through feedback and study notes.

---

## ✨ Key Features

- ✅ Interactive exam‑style training
- ✅ Random question selection
- ✅ Randomized answer order
- ✅ Session statistics (attempted, correct, incorrect, percentage)
- ✅ Historical statistics per question
- ✅ Priority handling for questions marked for review
- ✅ Immediate feedback after answering
- ✅ Additional study information when available
- ✅ Support for figures and referenced graphics
- ✅ Glossary for technical terms and acronyms
- ✅ Fully functional Excel‑based interface

---

## 🧭 Basic Usage Flow

1. Open the Excel file and **enable macros**
2. Go to the **Principal** sheet
3. Click **Start** to begin a new session
4. Read the question on the **Pregunta** sheet
5. **Answer by double‑clicking** on the desired option
6. Review the feedback and continue with the next question

---

## 🗂️ Workbook Structure

### 📄 Principal
Main entry point of the system.
Used to:
- Start new sessions
- Resume previous sessions
- Configure question filters

---

### 📄 Pregunta
Main exam interface.
Displays:
- Question text
- Answer options
- Status indicators (seen, failed, review)
- Session statistics
- Feedback and study content

Answers are selected via **double click**.

---

### 📄 BD (Database)
Repository of all questions and historical data.

Includes:
- Question text and answers
- Correct answer
- Feedback explanations
- Study information
- Per‑question statistics

This sheet is intended for **editing and maintenance**, not for exam use.

---

### 📄 Sesion
Internal system sheet (runtime data).

Manages:
- Current question
- Randomized answer order
- Last selected answer
- Review state

This sheet is usually **hidden**.

---

### 📄 Glosario
Glossary of technical terms and acronyms used in the questions, including:
- Term
- Meaning
- Formula or calculation (when applicable)

---

### 📄 Gráficos
Contains images, diagrams, and figures referenced in questions using texts such as:

> “SEE FIGURE 1”

---

## 🔀 Randomization Logic

The system applies multiple layers of randomization:

- Random question selection
- Random answer positioning
- Priority selection for review‑marked questions
- Respect for user‑defined filters

This avoids memorization patterns and improves effective learning.

---

## 💻 Requirements

- Microsoft Excel (desktop version)
- Macros enabled
- Not compatible with Excel Online

⚠️ The application will not work if macros are disabled.

---

## 🎯 Use Cases

Exam‑Excel is suitable for:

- Certification preparation
- Technical studies
- Competitive exams
- Continuous self‑assessment

It can be easily adapted by adding new questions to the **BD** sheet.

---

## 👤 Author

**Antonio Teodomiro Márquez Muñoz**  
Alias: **Naidel**

📧 Contact: atmarquez@gmail.com

---

## ⚖️ License

This project is distributed under the terms of the:

**GNU General Public License v3 (GPLv3)**

You are free to:
- Use the software
- Study how it works
- Modify it
- Redistribute it

Provided that you comply with the terms of the GPLv3.

This program is distributed in the hope that it will be useful,  
but **WITHOUT ANY WARRANTY**, without even the implied warranty of  
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

📄 Official license text:  
https://www.gnu.org/licenses/gpl-3.0.html

---

## 🤝 Contributions and Feedback

Suggestions, improvements, and bug reports are welcome.

- Use GitHub *Issues* to report problems or request enhancements
- If you adapt the project to another type of exam, feel free to share it

---

## ✅ Project Status

- Current version: **1.0.0**
- Status: **Stable**
- Actively used and proven in real exam training scenarios

---

### 📌 Final Note

Exam‑Excel started as a personal study tool and is released as free software to share a practical, transparent, and reusable solution for exam preparation and self‑assessment.

---
