flaskpro
# Proyecto Flask - Lista de Tareas 

Este es un proyecto sencillo desarrollado con Flask y SQLAlchemy que permite gestionar una lista de tareas (crear, actualizar, eliminar). La aplicación utiliza una base de datos SQLite para almacenar las tareas y está diseñada con una estructura básica para facilitar su extensión y despliegue.

---

## Características principales

- Crear nuevas tareas con contenido personalizado.
- Listar tareas ordenadas por fecha de creación.
- Actualizar el contenido de tareas existentes.
- Eliminar tareas.
- Interfaz web sencilla con HTML y CSS para una experiencia básica pero funcional.

---

## Instrucciones para ejecutar el proyecto localmente

1. **Clonar el repositorio**

   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd flaskproject
   ```

2. **Crear un entorno virtual e instalar dependencias**

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # En Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Crear la base de datos**

   Ejecuta el siguiente comando para crear las tablas en SQLite:

   ```bash
   python init_db.py
   ```

   *(El archivo `init_db.py` contiene el siguiente código:)*

   ```python
   from app import app, db

   with app.app_context():
       db.create_all()
       print("Base de datos creada correctamente.")
   ```

4. **Ejecutar la aplicación**

   ```bash
   flask run
   ```

   La aplicación estará disponible en `http://127.0.0.1:5000/`

---

## Cambios personalizados realizados

- Estilos CSS personalizados para una apariencia profesional y centrada, mejorando la experiencia de usuario.
- Integración con SQLAlchemy para manejar la base de datos SQLite.
- Modelo `Todo` definido con campos `id`, `content` y `date_created`.
- Implementación de rutas para crear, listar, actualizar y eliminar tareas.
- Separación de la creación de la base de datos en un script externo (`init_db.py`) para facilitar despliegues en servidores como Render.
- Estructura del proyecto con carpetas `templates` y `static` para organizar HTML y CSS.

- Configuración para despliegue en Render, incluyendo archivo `Procfile` y ajuste en dependencias (`requirements.txt`).

---

## Enlace al proyecto desplegado

Puedes ver la aplicación en funcionamiento en:

[https://flaskpro-lm3j.onrender.com/](https://flaskpro-lm3j.onrender.com/)

---
