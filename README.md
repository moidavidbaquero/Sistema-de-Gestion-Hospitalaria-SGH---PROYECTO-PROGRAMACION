# 🏥 Sistema de Gestión Hospitalaria (SGH)

## 📌 Descripción del Proyecto

Este proyecto corresponde a un **Sistema de Gestión Hospitalaria (SGH)** desarrollado en Python bajo el enfoque de **Programación Orientada a Objetos (POO)**.

El sistema permite administrar de forma integral la información hospitalaria mediante una arquitectura modular basada en modelos, repositorios, servicios e interfaz gráfica interactiva dentro de Google Colab.

### Funcionalidades principales

* Gestión de especialidades médicas
* Gestión de pacientes
* Gestión de médicos y consultorios
* Agendamiento y cancelación de citas médicas
* Registro de evolución clínica (consultas y tratamientos)
* Historial clínico por paciente
* Módulo analítico con métricas y auditoría general
* Persistencia de datos en archivos de texto plano
* Interfaz gráfica interactiva con `ipywidgets`
* Validaciones del sistema en cada módulo
* Organización modular por capas

---

## 👨‍💻 Autores

* **MOISES DAVID BAQUERO DAZA**
* **KEYNER STEVEN GARCIA ANAYA**

---

## 🧱 Estructura del Proyecto

```
📦 Sistema_Gestion_Hospitalaria
 ┣ 📂 datos/                          ← Persistencia en Google Drive
 ┃ ┣ 📜 pacientes.txt
 ┃ ┣ 📜 medicos.txt
 ┃ ┣ 📜 especialidades.txt
 ┃ ┣ 📜 citas.txt
 ┃ ┣ 📜 consultas.txt
 ┃ ┗ 📜 tratamientos.txt
 ┃
 ┣ 📂 Sección 1 — Modelo (Dominio)
 ┃ ┣ 📜 RegimenEnum
 ┃ ┣ 📜 EstadoCitaEnum
 ┃ ┣ 📜 Especialidad
 ┃ ┣ 📜 Paciente
 ┃ ┣ 📜 Medico
 ┃ ┣ 📜 Cita
 ┃ ┣ 📜 Consulta
 ┃ ┗ 📜 Tratamiento
 ┃
 ┣ 📂 Sección 2 — Repositorios
 ┃ ┣ 📜 ArchivoUtil
 ┃ ┣ 📜 EspecialidadRepository
 ┃ ┣ 📜 PacienteRepository
 ┃ ┣ 📜 MedicoRepository
 ┃ ┣ 📜 CitaRepository
 ┃ ┗ 📜 RegistroClinicoRepository
 ┃
 ┣ 📂 Sección 3 — Servicios
 ┃ ┣ 📜 EspecialidadService
 ┃ ┣ 📜 PacienteService
 ┃ ┣ 📜 MedicoService
 ┃ ┣ 📜 CitaService
 ┃ ┣ 📜 RegistroClinicoService
 ┃ ┗ 📜 AnalisisService
 ┃
 ┣ 📂 Sección 4 — Interfaz Gráfica (ipywidgets)
 ┃ ┣ 📜 Pestaña 1: Especialidades
 ┃ ┣ 📜 Pestaña 2: Pacientes
 ┃ ┣ 📜 Pestaña 3: Médicos
 ┃ ┣ 📜 Pestaña 4: Citas Médicas
 ┃ ┣ 📜 Pestaña 5: Evolución Clínica
 ┃ ┗ 📜 Pestaña 6: Métricas y Auditoría
 ┃
 ┣ 📂 Sección 5 — Ejecución Principal
 ┃ ┗ 📜 Renderizado de interfaz completa
 ┃
 ┗ 📜 PROGRAMACION_PROYECTO_FINAL.ipynb
```

---

## 🔍 Explicación de la Arquitectura

### 🖥️ Interfaz Gráfica (ipywidgets)
Gestiona la interacción con el usuario mediante pestañas, formularios y botones interactivos directamente en Google Colab. Incluye validaciones visuales, tablas HTML y retroalimentación en tiempo real.

### ⚙️ Servicios
Contienen la lógica del negocio:

* Validaciones de datos y reglas del sistema
* Procesamiento de operaciones clínicas
* Análisis estadístico y generación de reportes

### 🗂️ Repositorios
Se encargan de:

* Persistencia y lectura de archivos `.txt`
* Escritura y actualización de registros
* Búsquedas por clave única (documento, código, registro)

### 💾 Persistencia
La información se almacena en **archivos de texto plano** (`.txt`) separados por el carácter `|` (pipe), ubicados en **Google Drive** bajo la ruta `/content/drive/MyDrive/SGH/datos/`.

---

## 🧩 Modelo de Dominio

### Enumeraciones
El sistema implementa enumeraciones para representar:

* **RegimenEnum** — Régimen de aseguramiento en salud (CONTRIBUTIVO, SUBSIDIADO)
* **EstadoCitaEnum** — Estado de una cita médica (PROGRAMADA, ATENDIDA, CANCELADA, NO_ASISTIO)

### 🧍 Paciente
Representa un paciente del hospital. Incluye:

* Número de documento
* Nombre completo
* Fecha de nacimiento (formato `YYYY-MM-DD`)
* Tipo de sangre
* EPS
* Régimen de afiliación
* Antecedentes médicos

### 👨‍⚕️ Médico
Representa un médico del hospital. Incluye:

* Número de registro (ej: `MED-001`)
* Nombre completo
* Código de especialidad
* Número de consultorio
* Horario de atención

### 🏥 Especialidad
Representa una especialidad médica. Incluye:

* Código (ej: `ESP-001`)
* Nombre
* Descripción

### 📅 Cita
Representa una cita médica programada. Incluye:

* Código único autogenerado
* Documento del paciente
* Registro del médico
* Fecha y hora (formato `DD-MM-YYYY` / `HH:MM`)
* Motivo de la cita
* Estado (`PROGRAMADA`, `ATENDIDA`, `CANCELADA`, `NO_ASISTIO`)

### 📋 Consulta
Registro clínico de una consulta médica realizada. Incluye:

* Código de la cita asociada
* Descripción del diagnóstico
* Código CIE-10
* Síntomas
* Signos vitales: presión arterial, temperatura, frecuencia cardíaca
* Observaciones clínicas

### 💊 Tratamiento
Formulación médica asociada a una cita atendida. Incluye:

* Código de la cita asociada
* Medicamento
* Dosis
* Frecuencia
* Duración en días

---

## 🗂️ Repositorios

| Repositorio | Responsabilidad |
|---|---|
| `ArchivoUtil` | Lectura, escritura, reescritura y generación de códigos únicos |
| `EspecialidadRepository` | CRUD de especialidades médicas |
| `PacienteRepository` | CRUD de pacientes con actualización de datos |
| `MedicoRepository` | CRUD de médicos, filtrado por especialidad y horario |
| `CitaRepository` | CRUD de citas, actualización de estados |
| `RegistroClinicoRepository` | Persistencia de consultas y tratamientos clínicos |

---

## ⚙️ Servicios

| Servicio | Responsabilidad |
|---|---|
| `EspecialidadService` | Registro y listado de especialidades con validaciones |
| `PacienteService` | Alta, actualización y consulta de pacientes |
| `MedicoService` | Registro y consulta de médicos |
| `CitaService` | Agendamiento, cancelación y búsqueda de citas por rango de fechas |
| `RegistroClinicoService` | Registro de consultas, tratamientos e historial clínico |
| `AnalisisService` | Promedio de consultas por médico, diagnósticos frecuentes, medicamentos más prescritos |

---

## 🖥️ Interfaz de Usuario

El sistema utiliza **pestañas interactivas** construidas con `ipywidgets`, organizadas de la siguiente manera:

| Pestaña | Descripción |
|---|---|
| **Especialidades** | Registro y listado de especialidades médicas |
| **Pacientes** | Alta, actualización y búsqueda de pacientes |
| **Médicos** | Registro y listado de médicos por especialidad y horario |
| **Citas Médicas** | Agendamiento, cancelación y búsqueda por rango de fechas |
| **Evolución Clínica** | Registro de consultas, formulación de tratamientos e historial clínico |
| **Métricas** | Promedio de consultas, diagnósticos frecuentes, medicamentos prescritos y auditoría general |

---

## ▶️ Ejecución del Proyecto

1. Abrir el notebook `PROGRAMACION_PROYECTO_FINAL.ipynb` en **Google Colab**.
2. Ejecutar **todas las celdas** en orden (Entorno de ejecución → Ejecutar todo).
3. Autorizar el montaje de **Google Drive** cuando se solicite.
4. Navegar por las **pestañas** de la interfaz gráfica interactiva.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3**
* **Programación Orientada a Objetos (POO)**
* **Google Colab**
* **Google Drive** (persistencia de datos)
* **ipywidgets** (interfaz gráfica interactiva)
* **IPython.display** (renderizado HTML en notebook)
* **Archivos de texto plano** (`.txt` separado por `|`)
* **Enumeraciones** (`Enum`)
* **Expresiones regulares** (`re`)

---

## 📚 Conceptos Aplicados

* Encapsulamiento y abstracción
* Modularidad y separación de responsabilidades
* Arquitectura por capas (Modelo → Repositorio → Servicio → Vista)
* Persistencia de datos con archivos de texto
* Enumeraciones para control de estados
* Generación de códigos únicos por timestamp
* Serialización y deserialización de objetos (pipe-delimited)
* Interfaz gráfica reactiva con widgets
* Análisis de datos y generación de reportes en HTML

---

## 🚀 Mejoras Implementadas en la Versión Final

* Adición del módulo completo de **Citas Médicas** con agendamiento, cancelación y búsqueda por rango de fechas
* Módulo de **Evolución Clínica** con registro de consultas (signos vitales, CIE-10, diagnóstico) y formulación de tratamientos
* **Historial clínico** consultable por número de documento del paciente
* **Módulo Analítico** con promedio de consultas por médico, diagnósticos frecuentes y medicamentos más prescritos
* **Auditoría General** con distribución por EPS/Régimen y tasa de ocupación por especialidad
* Interfaz gráfica completamente renovada con pestañas, tablas HTML y validaciones visuales
* Filtrado de médicos por especialidad y horario
* Botón global de limpieza de pantalla

---

## ✅ Conclusión

El proyecto implementa una solución integral para la **gestión hospitalaria** usando Programación Orientada a Objetos en Python.

La arquitectura por capas (Modelo → Repositorio → Servicio → Interfaz) garantiza la separación clara de responsabilidades, facilitando el mantenimiento, la escalabilidad y la reutilización del código. La incorporación del módulo clínico y analítico eleva el sistema a un nivel funcional cercano a un sistema de **Historia Clínica Electrónica (HCE)** real.
