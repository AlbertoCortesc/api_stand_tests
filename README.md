# 🧪 Proyecto: Automatización de Pruebas de API (Stand de Usuarios)

## 📌 Descripción del Proyecto

Este proyecto contiene una suite de pruebas automatizadas desarrollada en **Python** 
utilizando el framework **PyTest** y la librería **Requests**.

El objetivo es validar la funcionalidad del *endpoint* de creación de 
usuarios (`/api/v1/users`) en un entorno de prueba (*stand*), asegurando que 
se cumplan las reglas de negocio, incluyendo la correcta validación de todos 
  los campos (longitud, formato, tipo de dato y presencia/ausencia).

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Python 3.x
* **Framework de Pruebas:** PyTest
* **Manejo de Solicitudes:** Requests

## 📂 Estructura del Repositorio

La arquitectura del proyecto está diseñada para ser modular y fácil de mantener:

| Archivo / Carpeta | Propósito |
| :--- | :--- |
| `configuration.py` | Configuración de la URL base y rutas (paths) de los *endpoints*. |
| `data.py` | Contiene los diccionarios (payloads) y datos de prueba utilizados en las solicitudes. |
| `sender_stand_request.py` | Define las funciones para enviar peticiones HTTP (`POST`, `GET`) al *stand* (Capa del Cliente). |
| `create_user_test.py` | Contiene la lógica de las pruebas unitarias y las aserciones (PyTest). |
| `.gitignore` | Reglas para ignorar archivos generados automáticamente (ej: `.venv`, caché de PyCharm). |

## ▶️ Cómo Ejecutar las Pruebas

Para ejecutar la suite de pruebas completa, sigue estos pasos:

1.  **Clonar el Repositorio:** (Una vez que lo subas a GitHub)
    ```bash
    git clone [https://docs.github.com/es/repositories/creating-and-managing-repositories/quickstart-for-repositories](https://docs.github.com/es/repositories/creating-and-managing-repositories/quickstart-for-repositories)
    ```
2.  **Activar el Entorno Virtual:**
    ```bash
    # Para Windows:
    .\.venv\Scripts\activate
    # Para macOS/Linux:
    source .venv/bin/activate
    ```
3.  **Instalar Dependencias:** (Asegúrate de tener un archivo `requirements.txt` con `pytest` y `requests`)
    ```bash
    pip install -r requirements.txt
    ```
4.  **Ejecutar PyTest:**
    ```bash
    pytest
    ```
    El *exit code 0* indica que todas las pruebas pasaron satisfactoriamente.