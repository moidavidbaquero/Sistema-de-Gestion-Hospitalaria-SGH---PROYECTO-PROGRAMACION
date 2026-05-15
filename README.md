
# 🏥 Sistema de Gestión Hospitalaria (SGH)

## 📌 Descripción del Proyecto

Este proyecto corresponde a un Sistema de Gestión Hospitalaria (SGH) desarrollado en Python bajo el enfoque de Programación Orientada a Objetos (POO).

El sistema está orientado a la administración básica de información hospitalaria, incluyendo:

- Gestión de pacientes
- Gestión de médicos
- Gestión de especialidades médicas
- Persistencia de datos en archivos
- Menús interactivos en consola

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
 ┗ 📜 PROGRAMACION_PROYECTO.ipynb
```

---

# 🔍 Explicación de la Arquitectura

## 🖥️ Menús Consola
Gestionan la interacción con el usuario mediante opciones y navegación del sistema.

## ⚙️ Servicios
Contienen la lógica de negocio:
- Validaciones
- Reglas del sistema
- Procesamiento de información

## 🗂️ Repositorios
Se encargan de:
- Guardar datos
- Leer archivos
- Actualizar registros
- Buscar información

## 💾 Persistencia
La información se almacena usando archivos JSON/TXT para mantener los datos entre ejecuciones.

---

# 🧩 Modelo de Dominio

## Enumeraciones
- Régimen de salud
- Estado de citas
- Especialidades médicas

## 🧍 Paciente
- Número de documento
- Nombre
- Fecha de nacimiento
- Tipo de sangre
- EPS
- Régimen
- Antecedentes médicos

## 👨‍⚕️ Médico
- Identificación
- Nombre
- Especialidad
- Registro profesional

## 🏥 Especialidad
- Código
- Nombre
- Descripción

---

# 🗂️ Repositorios

## Repositorios encontrados
- ArchivoUtil
- EspecialidadRepository
- PacienteRepository
- MedicoRepository

---

# ⚙️ Servicios

## Servicios implementados
- EspecialidadService
- PacienteService
- MedicoService

---

# 🖥️ Interfaz de Usuario

El sistema utiliza una interfaz basada en consola con menús interactivos.

## Menús disponibles
- Menú Principal
- Menú de Especialidades
- Menú de Pacientes
- Menú de Médicos

---

# ▶️ Ejecución del Proyecto

Abrir el notebook en Google Colab y ejecutar todas las celdas.

---

# 🛠️ Tecnologías Utilizadas

- Python
- Programación Orientada a Objetos (POO)
- Google Colab
- Google Drive
- Enumeraciones (Enum)
- Persistencia en archivos JSON

---

# 📚 Conceptos Aplicados

- Encapsulamiento
- Separación por capas
- Persistencia de datos
- Diseño modular
- Reutilización de código
- Arquitectura basada en servicios y repositorios

---

# ✅ Conclusión

El proyecto implementa una arquitectura organizada para la gestión hospitalaria usando Programación Orientada a Objetos.
