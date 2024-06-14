## Acerca de este Repositorio

Este repositorio contiene réplicas de análisis de datos realizados por analistas de datos de políticas públicas, originalmente efectuados en R, stata u otros, pero traducidos a Python. El objetivo es proporcionar una plataforma accesible para analizar y visualizar datos políticos con herramientas de Python, facilitando la comprensión y la reproducibilidad de estos análisis.

Para ello este repositorio proporciona una configuración optimizada y lista para usar de un entorno de desarrollo para Python 3.12.3 enfocado en Ciencia de Datos. Utilizando Docker, facilita la creación de un ambiente aislado y reproducible, eliminando las complicaciones de la configuración manual.

**Conversión de Código:** Traducción de análisis de R a Python.

**Jupyter Notebooks:** Notebooks interactivos con explicaciones detalladas y visualizaciones.

**Comparación de Métodos:** Comparación de los resultados obtenidos con R y Python para validar la replicación.

### Características Principales:

- **Entorno Dockerizado**: Utiliza Docker para encapsular todas las dependencias y configuraciones necesarias, garantizando la portabilidad y consistencia del entorno de desarrollo.
  
- **Integración con Jupyter**: Incluye Jupyter Lab para el análisis interactivo de datos y la creación de documentos reproducibles. 

- **Gestión de Dependencias con Poetry**: Simplifica la gestión de bibliotecas y dependencias de Python con Poetry, facilitando la instalación, actualización y distribución de paquetes.

Este repositorio es ideal para aquellos que desean iniciar rápidamente proyectos de Ciencia de Datos sin preocuparse por la configuración del entorno. ¡Empieza a explorar y desarrollar tus ideas sin obstáculos!


## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes programas:

1. **Docker**: [Guía de instalación de Docker](https://docs.docker.com/engine/install/)
2. **Git**: [Guía de instalación de Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
3. **Visual Studio Code (VSC)**: [Descargar Visual Studio Code](https://code.visualstudio.com/download)

La instalación de Visual Studio Code es opcional, pero se recomienda especialmente si tienes experiencia programando. Si eres principiante, puedes optar por no instalarlo.

## Instrucciones de Instalación

### Clonar el Repositorio

1. Elige una ubicación en tu computadora para clonar el repositorio. Abre tu terminal y ejecuta el siguiente comando:

    ```bash
    git clone https://github.com/cuauhtemocbe/policy-data-analysis-python.git
    ```

    Este comando creará una carpeta llamada **policy-data-analysis-python** en tu máquina.

2. ⚠️**Importante :⚠️** Crear un archivo `.env` dentro de la carpeta **policy-data-analysis-python**

### Configuración con Visual Studio Code (Opción Avanzada)

Si prefieres usar Visual Studio Code para desarrollar o ejecutar los notebooks, sigue estos pasos:

1. Abre Visual Studio Code y selecciona `File > Open Folder`. Luego elige la carpeta **policy-data-analysis-python** para abrir el repositorio.
2. Instala la extensión **Dev Containers** desde el Marketplace de VSC.
3. Abre la Paleta de Comandos (Command Palette) con `Shift + Ctrl + P` y escribe `Dev Containers: Rebuild and Reopen in Container`. Ejecútalo para construir y levantar el contenedor Docker.
4. En el explorador de archivos (`Ctrl + Shift + E`), navega hasta la carpeta `notebooks` y abre el archivo `Hello-Pandas.ipynb`.
5. Ejecuta el notebook; al inicio te solicitará seleccionar un kernel, elige Python 3.12.3.
6. Distruta

### Configuración con Jupyter Lab (Opción Sencilla)

Si prefieres utilizar Jupyter Lab con Docker, sigue estos pasos:

1. Desde la terminal, dentro de la carpeta **policy-data-analysis-python**, ejecuta el siguiente comando para construir y levantar el contenedor:

    ```bash
    docker compose up -d
    ```

2. Luego, ejecuta el siguiente comando para ingresar al contenedor y utilizar la terminal:

    ```bash
    docker exec -it policy-analytics bash
    ```

3. Dentro del contenedor, inicia el servicio de Jupyter Lab con el siguiente comando:

    ```bash
    jupyter lab --ip=0.0.0.0 --port=8888 --no-browser --allow-root --NotebookApp.token=''
    ```

4. Finalmente, abre el siguiente enlace en tu navegador: [http://localhost:8888/lab/tree/notebooks](http://localhost:8888/lab/tree/notebooks)
5. Navega en el explorador a la carpeta notebooks, y abre prueba el notebook `Hello-Pandas.ipynb`.
6. Disfruta.

## Agregando nuevas bibliotecas

Si deseas ampliar las capacidades de tu entorno de desarrollo añadiendo nuevas bibliotecas, sigue estos sencillos pasos:

1. Accede al contenedor ejecutando el siguiente comando en tu terminal:

    ```bash
    docker exec -it policy-analytics bash
    ```

2. Una vez dentro del contenedor, puedes utilizar Poetry para agregar nuevas bibliotecas. Por ejemplo, si deseas agregar la popular biblioteca de visualización de datos, seaborn, simplemente ejecuta:

    ```bash
    poetry add seaborn
    ```

Con estos pasos, podrás expandir rápidamente las funcionalidades de tu entorno de desarrollo para satisfacer tus necesidades específicas.

## Enlaces de Interés

- **Poetry**: [Sitio oficial de Poetry](https://python-poetry.org/)
