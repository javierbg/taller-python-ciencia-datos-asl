# Introducción a la Ciencia de Datos con Python
Este breve tutorial explica algunos de los conceptos relacionados con las librerías NumPy, Matplotlib, `pandas` y `scikit-learn` de Python.

Basado en el material de la asignatura Introducción a los Métodos Computacionales de 4º Curso del Grado en Ingeniería Informática (Universidad de Córdoba) [(repositorio)](https://github.com/ayrna/tutorial-scikit-learn-IMC).

## Instalación del entorno de trabajo

Para instalar el entorno de trabajo tenemos dos opciones: usar directamente el gestor de paquetes `pip` o utilizar la herramienta `conda`.

### Instalación con `pip`

Si ya dispones de Python en una versión >=3.7 puedes usar este método. Crearemos un entorno virtual donde instalaremos las versiones de los paquetes necesarios, especificadas en el fichero [`requirements.txt`](requirements.txt).

```bash
# Creamos un entorno en el directorio "venv"
# Si usas Ubuntu/Debian necesitarás instalar el paquete "python3-venv"
# En otras distros viene incluído con Python>=3.7
python3 -m venv venv

# Activamos el entorno de manera que los paquetes que
# instalemos se instalen sólo para éste
source venv/bin/activate

# Instalamos los paquetes especificados en el fichero "requirements.txt"
pip install -r requirements.txt
```

El entorno virtual permanecerá activo hasta que cerremos la terminal o ejecutemos el comando `deactivate`.

### Instalación con `conda`

Si dispones de la herramienta `conda` (instrucciones de instalación en Linux [aquí](https://conda.io/projects/conda/en/latest/user-guide/install/linux.html), recomiendo instalar la versión reducida "`miniconda`") la instalación es algo más sencilla. `conda` podrá instalar automáticamente una versión de Python compatible si tu distribución no la ofrece.

```bash
# Esto creará el entorno virtual especificado en "requirements.yml"
# de nombre "sklearn-env"
conda env create -f requirements.yml

# Puedes activar este entorno en la terminal desde cualquier lugar
# usando el siguiente comando
conda activate sklearn-env
```

El entorno virtual permanecerá activo hasta que cerremos la terminal o ejecutemos el comando `conda deactivate`.

## Abrir el cuaderno con Jupyter

Una vez instalado y activado el entorno de ejecución podemos lanzar el servidor Jupyter para trabajar con el cuaderno del tutorial.

```bash
jupyter notebook
```

Este comando abrirá automáticamente una pestaña en nuestro navegador donde podremos navegar por el sistema de archivos y abrir cuadernos de Jupyter (`.ipynb`). Podemos cerrar el servidor cuando queramos pulsando Ctrl+C.

### Trabajar directamente desde Visual Studio Code

Las versiones recientes de VS Code son capaces de abrir cuadernos de Jupyter directamente si instalamos la extensión de Python de Microsoft. Podremos seleccionar el entorno virtual (tanto si lo hemos creado de forma manual o con `conda`) y abrir el fichero `.ipynb` directamente.