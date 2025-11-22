# api-for-fun

## Descripción

Creación de una **API REST** enfocada en la autenticación y manejo de sesiones.

## Pre requisitos

* Python 3.14.0 [Instalación](https://docs.astral.sh/uv/getting-started/installation/)
* uv 0.9.8 (85c5d3228 2025-11-07) [Instalación](https://www.python.org/downloads/release/python-3140/)

## Quick Start

1. Verifica la instalación de los pre requisitos

    * Verificar la instalación de python 3.14 - Windows y Linux

      ```terminal
      python --version
      ```

    * Verificar la instalación de UV (package manager) - Windows y Linex

      ```terminal
      uv --version
      ```

2. Iniciar el entorno virtual

    * Crear el entorno virtual

      ```terminal
      uv venv
      ```

      Resultado esperado (en windows)

      ```terminal
      Using CPython 3.14.0 interpreter at: C:\Users\tu-usuario\AppData\Local\Programs\Python\Python314\python.exe
      Creating virtual environment at: .venv
      Activate with: .venv\Scripts\activate
      ```

    * Iniciar el entorno virtual

      * En windows

        ```terminal
        .\.venv\Scripts\activate
        ```

      * En linux

        ```terminal
        source .venv/bin/activate
        ```

        Resultado esperado (en Windows)

        ```terminal
        (api-for-fun) C:\Users\tu-usuario\repositories\api-for-fun>
        ```

3. Instalar las dependencias que requiere el proyecto

    * Pre requisio
        * Asegurate de tener el entorno virtual activado
        * Verificar la existencia del archivo `uv-lock`

    * Ejecutar el comando:

      ```terminal
      uv sync
      ```

4. Para iniciar el proyecto se debe ejecutar el comando

    * Ejecutar el comando `fastapi dev main.py`, el resultado esperado es el siguiente

      ```terminal
      (api-for-fun) PS C:\Users\tu-usuario\repositories\api-for-fun> fastapi dev .\main.py
      
         FastAPI   Starting development server 🚀
      
                   Searching for package file structure from directories with __init__.py files
                   Importing from C:\Users\tu-usuario\repositories\api-for-fun
      
          module   🐍 main.py
      
            code   Importing the FastAPI app object from the module with the following code:
      
                   from main import app
      
             app   Using import string: main:app
      
          server   Server started at http://127.0.0.1:8000
          server   Documentation at http://127.0.0.1:8000/docs
      
             tip   Running in development mode, for production use: fastapi run
      
                   Logs:
      
            INFO   Will watch for changes in these directories: ['C:\\Users\\tu-usuario\\repositories\\api-for-fun']
            INFO   Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
            INFO   Started reloader process [11676] using WatchFiles
            INFO   Started server process [2192]
            INFO   Waiting for application startup.
            INFO   Application startup complete.
      ```

      * El servidor se ejecutara en el puerto **8000** del **localhost** de la maquina.
      * Para consultar la autodocumentación de **OPENAPI** ingresa a `http://localhost:8000/docs`.

## Pre requerimientos

...

## To do

- [ ] Configuración del pre commit asegurando el nombramiento y practicas de commits
  - No estoy seguro de si quedo bien configurado, hacer pruebas con los archivos de python cuando se realice commmit.
- [x] Investigar si se debe o no subir el archivo uv.lock y .python-version al repositorio remoto
- [x] Investigar sobre el archivo .python-version que se genera cuando inicio el uv
- [x] Investigar sobre `warning: in the working copy of '.python-version', LF will be replaced by CRLF the next time Git touches it`
- [x] Configurar ruff para que la linea final sea acorde al estandar de LF
- [x] Documentar donde encontrar las reglas de configuración de RUFF
- [x] Realizar commit de base del proyecto
- [x] Documentar la configuración del pre commit
- [x] Actualizar el `README.md` especificando como inicializar el repositorio
