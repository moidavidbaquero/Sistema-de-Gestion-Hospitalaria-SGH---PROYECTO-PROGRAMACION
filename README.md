
# 🏥 Sistema de Gestión Hospitalaria (SGH) - Avance 3

## 📌 Descripción del Proyecto

Este proyecto corresponde a un Sistema de Gestión Hospitalaria (SGH) desarrollado en Python bajo el enfoque de Programación Orientada a Objetos (POO).

El sistema permite administrar información hospitalaria mediante una arquitectura modular basada en modelos, servicios y repositorios.

### Funcionalidades principales

- Gestión de pacientes
- Gestión de médicos
- Gestión de especialidades médicas
- Persistencia de datos
- Menús interactivos
- Validaciones del sistema
- Organización modular por capas

---

# 👨‍💻 Autores

- MOISES DAVID BAQUERO DAZA
- KEYNER STEVEN GARCIA ANAYA

---

# 🧱 Estructura del Proyecto

```txt
📦 Sistema_Gestion_Hospitalaria
 ┣ 📂 data
 ┃ ┣ 📜 pacientes.json
 ┃ ┣ 📜 medicos.json
 ┃ ┗ 📜 especialidades.json
 ┃
 ┣ 📂 models
 ┃ ┣ 📜 paciente.py
 ┃ ┣ 📜 medico.py
 ┃ ┗ 📜 especialidad.py
 ┃
 ┣ 📂 repositories
 ┃ ┣ 📜 paciente_repository.py
 ┃ ┣ 📜 medico_repository.py
 ┃ ┗ 📜 especialidad_repository.py
 ┃
 ┣ 📂 services
 ┃ ┣ 📜 paciente_service.py
 ┃ ┣ 📜 medico_service.py
 ┃ ┗ 📜 especialidad_service.py
 ┃
 ┣ 📂 utils
 ┃ ┗ 📜 archivo_util.py
 ┃
 ┣ 📜 main.py
 ┣ 📜 README.md
 ┗ 📜 PROGRAMACION_PROYECTO_3.ipynb
```

---

# 🔍 Explicación de la Arquitectura

## 🖥️ Menús Consola
Gestionan la interacción con el usuario mediante opciones y navegación.

## ⚙️ Servicios
Contienen la lógica del negocio:
- Validaciones
- Reglas del sistema
- Procesamiento de datos

## 🗂️ Repositorios
Se encargan de:
- Persistencia
- Lectura de archivos
- Escritura de datos
- Búsquedas

## 💾 Persistencia
La información se almacena utilizando archivos JSON/TXT.

---

# 🧩 Modelo de Dominio

## Enumeraciones
El sistema implementa enumeraciones para representar:

- Especialidades médicas
- Régimen de salud
- Estados del sistema

---

## 🧍 Paciente

Representa un paciente del hospital.

### Incluye:
- Documento
- Nombre
- Fecha de nacimiento
- EPS
- Régimen
- Tipo de sangre
- Antecedentes médicos

---

## 👨‍⚕️ Médico

Representa un médico del hospital.

### Incluye:
- Identificación
- Nombre
- Especialidad
- Registro profesional

---

## 🏥 Especialidad

Representa una especialidad médica.

### Incluye:
- Código
- Nombre
- Descripción

---

# 🗂️ Repositorios

## Repositorios encontrados

- ArchivoUtil
- PacienteRepository
- MedicoRepository
- EspecialidadRepository

---

# ⚙️ Servicios

## Servicios implementados

- PacienteService
- MedicoService
- EspecialidadService

---

# 🖥️ Interfaz de Usuario

El sistema utiliza menús interactivos en consola.

## Menús disponibles

- Menú principal
- Gestión de pacientes
- Gestión de médicos
- Gestión de especialidades

---

# ▶️ Ejecución del Proyecto

1. Abrir el notebook en Google Colab.
2. Ejecutar todas las celdas.
3. Navegar por el menú principal.

---

# 🛠️ Tecnologías Utilizadas

- Python
- Programación Orientada a Objetos (POO)
- Google Colab
- Google Drive
- JSON
- Enumeraciones (`Enum`)

---

# 📚 Conceptos Aplicados

- Encapsulamiento
- Modularidad
- Persistencia de datos
- Arquitectura por capas
- Separación de responsabilidades
- Reutilización de código

---

# 🚀 Mejoras Implementadas en el Avance 3

- Mejor organización del código
- Separación de capas
- Validaciones adicionales
- Persistencia optimizada
- Menús más estructurados
- Reutilización de componentes

---

# ✅ Conclusión

El proyecto implementa una solución organizada para la gestión hospitalaria usando Programación Orientada a Objetos.

La arquitectura modular facilita el mantenimiento, escalabilidad y reutilización del código.
