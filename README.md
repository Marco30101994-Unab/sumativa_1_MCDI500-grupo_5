\# Sumativa 1 MCDI500



\## Integrantes Grupo 5



\- MARCO ÁLVAREZ ARAYA

\- LISHY CORTES ASTUDILLO

\- MARÍA FASSLER NEUMANN

\- RICARDO JARAMILLO PULGAR





\## Descripción del Proyecto



Se está buscando repositorio de acuerdo a lo señalado en clases del día lunes. Cuando se defina el tema, se actualiza este apartado.



\## Datos del Proyecto



\- Fuente: Pendiente

\- Enlace de descarga: Pendiente

\- Ubicación del archivo original: `data/raw/`.

\- Ubicación del archivo procesado: `data/processed/`.



\## Estructura del repositorio



```text

data/raw/        datos originales

data/processed/  datos generados durante el procesamiento de F2

docs/            documentación, metadatos y diccionario de variables

src/             funciones reutilizables del proyecto

F1/notebooks/    notebook de definición del problema y entorno

F2/notebooks/    notebook de obtención y preprocesamiento de datos

F3/              fase posterior del proyecto

F4/              fase posterior del proyecto

```



\## Requisitos



\- Python 3.13

\- Entorno virtual `.venv`

\- Dependencias declaradas en `requirements.txt`



\## Preparación del entorno



```bash

source .venv/Scripts/activate

python -m pip install -r requirements.txt

```



\## Ejecución de los notebooks



```bash

python -m jupyter lab

```



En JupyterLab se ejecutarán los notebooks de F1 y F2 en orden.



\## Reproducibilidad



El proyecto usa rutas relativas y registra las versiones de sus librerías en `requirements.txt`. El entorno virtual no se sube al repositorio porque puede reconstruirse desde ese archivo.



\## Control de versiones



Los commits utilizarán los siguientes prefijos:



\- `docs:` documentación o README.

\- `data:` incorporación o actualización de datos.

\- `feat:` nueva funcionalidad.

\- `fix:` corrección de un error.

