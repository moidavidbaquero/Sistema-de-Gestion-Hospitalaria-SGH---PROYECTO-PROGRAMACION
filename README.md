# 🏥 Sistema de Gestión Hospitalaria (SGH)
Presentado por: 
*Moises David Baquero Daza - 01240371051* y 
*Keyner Steven Garcia Anaya - 01240371013*


---

## 📌 Descripción

El **Sistema de Gestión Hospitalaria (SGH)** es una aplicación desarrollada en Python que permite modelar y gestionar información esencial de una institución de salud, como pacientes, médicos y especialidades.

Este proyecto está orientado a la aplicación de conceptos de **Programación Orientada a Objetos (POO)** en un contexto real.

---

## 🧠 Conceptos aplicados

- Encapsulamiento  
- Abstracción  
- Modularidad  
- Uso de clases y enumeraciones  

---

## 🛠️ Tecnologías utilizadas

- Python 3  
- Google Colab  
- Google Drive  

---

## ⚙️ Configuración

### 1. Montar Google Drive

```python
from google.colab import drive
drive.mount('/content/drive')
```

### 2. Definir ruta base

```python
RUTA_BASE = '/content/drive/MyDrive/SGH/datos/'
```

### 3. Crear directorios

```python
import os
os.makedirs(RUTA_BASE, exist_ok=True)
```

---

## 🧱 Estructura del proyecto

### 🔹 Enumeraciones

#### RegimenEnum
- CONTRIBUTIVO  
- SUBSIDIADO  

---

### 🔹 Clases

#### Especialidad
- Código  
- Nombre  
- Descripción  

#### Paciente
- Documento  
- Nombre  
- Fecha de nacimiento  
- Tipo de sangre  
- Régimen  

#### Medico
- Información del profesional de salud  

---

## 🎯 Objetivos

- Modelar entidades del sistema de salud  
- Aplicar Programación Orientada a Objetos  
- Gestionar información hospitalaria básica  
- Integrar almacenamiento en la nube  

---

## 🚀 Mejoras futuras

- Base de datos (SQLite, PostgreSQL)  
- API REST (Flask / FastAPI)  
- Interfaz gráfica  
- Gestión de citas médicas  
- Sistema de autenticación  

---

## 👨‍💻 Autores

- Moisés David Baquero Daza  
- Keyner Steven Garcia Anaya 

---

## 📄 Licencia

Este proyecto es de uso académico y educativo.

---

## ⭐ Notas

Este sistema representa una base sólida para proyectos más complejos en el sector salud, y puede escalarse fácilmente agregando nuevas funcionalidades.
