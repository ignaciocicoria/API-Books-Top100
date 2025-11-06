# API Libros Top 100

Este proyecto implementa una **API REST con FastAPI** para gestionar una lista de los 100 mejores libros del mundo.  
Permite **consultar, agregar, modificar y eliminar libros** almacenados en un archivo JSON descargado desde GitHub, (https://github.com/benoitvallon/100-best-books/blob/master/books.json).
También incluye un **cliente en consola** que interactúa con la API de manera sencilla.
 
---

## Estructura del repositorio

```
API-Libros-Top100/
│
├── main.py # Servidor FastAPI (API principal)
├── cliente.py # Cliente en consola para interactuar con la API
├── books.json # Base de datos local (descargada automáticamente)
├── requirements.txt # Dependencias del proyecto
└── README.md # Este archivo
```

---


---

##  Instalación y configuración

### 1️⃣ Crear entorno virtual (recomendado)

Desde la raíz del proyecto, ejecutá:

```
python -m venv venv
```

Activar el entorno:

En Windows:
```
venv\Scripts\activate
```

En Linux / macOS:
```
source venv/bin/activate
```
#### 2️⃣ Instalar dependencias

```
pip install -r requirements.txt
```

## Ejecución del proyecto

### 1️⃣ Iniciar el servidor FastAPI

Ejecutá el siguiente comando en la raíz del proyecto:
```
uvicorn main:app --reload
```

Si todo funciona correctamente, verás algo como:

INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)


👉 La URL base del servidor será:
http://127.0.0.1:8000

Podés acceder a la documentación interactiva en:
http://127.0.0.1:8000/docs

### 2️⃣ Ejecutar el cliente de consola

En otra terminal (con el entorno activado), ejecutá:
```
python cliente.py
```

Verás el siguiente menú interactivo:

=== MENÚ DE OPCIONES ===
1. Consultar todos los libros
2. Modificar un libro
3. Verificar si un libro está en la lista
4. Salir


El cliente se conecta automáticamente al servidor en http://127.0.0.1:8000.

## Pruebas recomendadas

Iniciar el servidor con uvicorn main:app --reload

Abrir http://127.0.0.1:8000/docs

Probar los endpoints desde el explorador o usando cliente.py
