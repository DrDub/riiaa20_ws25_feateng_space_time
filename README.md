# Source code for RIIAA'20 workshop 25: Feature Engineering for Spatial and Temporal Data

This workshop consists of three notebooks working on three datasets but the last notebook is FYI, the hands-on bits are within the first two notebooks.

The theory part (in Spanish) is available here: 

[![Theory](https://img.youtube.com/vi/0ev3UfA1fo4/hqdefault.jpg)](https://youtu.be/0ev3UfA1fo4)

## Spatial Data: African cuckoos in Nigeria

We will be using the migration data through satellite telemetry for
African cuckoos in Nigeria, kindly released by Iwajomo SB et al, 2018
as part of the movebank.org data repository. It contains 12,563
tracking points for six individuals, from May 29th, 2013 until Jun
28th, 2017.

We will look into the problem of predicting whether a bird will move
in the next two hours.

## Time Series: World Population by Country

Population prediction using data provided by the World Bank and the
number of links a Wikipedia for the country receives. Exemplifies
using previous values of the target feature.

## Historical Data: City Population

Using data derived from the DBpedia graph for different versions, we
will look into imputing large number of missing historical data.



## Instrucciones para estudiantes

(basada en las instrucciones provistas por la organización de RIIAA'20, el instructor no usa Conda ni Anaconda)

Cosas para preparar
* Una laptop.
* Este repositorio de GitHub clonado y actualizado antes del taller.
* Un sentido aventurero en los datos.
* Un ambiente Python 3.7+ con Anaconda (ver opciones 1 y 2 abajo).

Los talleres serán impartidos usando *notebooks* de Jupyter, documentos con código ejecutable, texto, ecuaciones, visualizaciones, imágenes y demás material. Los *notebooks* se pueden crear y ejecutar en la nube vía Google Colab (opción 1) o de manera local en tu computadora a través de [Jupyter Notebooks](https://jupyter.org/) (opción 2).

### Opcion 1: Google Colab
[Colab](https://colab.research.google.com) es un servicio de Google para ejecutar *notebooks* en la nube. Provee ambientes de Python 2 y 3 con CPUs, GPUs y TPUs. Solo necesitas tener una cuenta de Google o crear una.

Recomendamos que elijas un ambiente con Python 3 y GPU. Para activarlo:
* Abre el menú `Entorno de ejecución`
* Elige la opción `Restablecer todos los entornos de ejecución...` .
* Vuelve a abrir `Entorno de ejecución`
* Elige `Cambiar tipo de entorno de ejecución`
* Selecciona Python 3 como `Tipo de ejecución` y GPU de la lista de `Acelerador por hardware`

La siguiente captura de pantalla ilustra este proceso.

![](media/escoge_acelerador.png)

En [Colab](https://colab.research.google.com) puedes crear un nuevo *notebook*, subir uno existente desde tu computadora o importarlo de Google Drive o GitHub.

### Opcion 2: Ambiente local
Para tener la versión de Python 3.7+ y todas las bibliotecas instaladas en cualquier plataforma, la organización de RIIAA'20 recomienda que uses [**Anaconda**](https://www.anaconda.com/) y generes un ambiente con el archivo `environment.yml` de este repositorio usando una terminal y el comando:

```
conda env create -n riiaa20 -f environment.yml
```

Cambia el nombre `riia20` por tu nombre favorito para el ambiente.

Para activar el ambiente que creaste, en una terminal ingresa el comando

```
conda activate riiaa20
```

Una vez activado, puedes ejecutar la aplicación de Jupyter Notebook

```
jupyter notebook
```

Este comando abrirá una pestaña o ventana en tu navegador web, como se muestra en la siguiente captura de pantalla:

![](media/jupyter_notebook.png)

Al igual que en Google Colab, puedes crear un nuevo *notebook* seleccionando el botón `New` y posteriormente `Python 3`. De forma alternativa, puedes abrir uno existente seleccionando el archivo del *notebook* (con extensión `.ipynb`) dentro del directorio donde ejecutaste Jupyter Notebook. Con el botón `Upload` agregas archivos que se encuentran en otra parte de tu computadora a este directorio. Para cerrar Jupyter Notebook, presiona el botón `Quit` y posteriormente cierra la pestaña o ventana de tu navegador web.

Para desactivar el ambiente `riiaa20` de Anaconda simplemente haz

```
conda deactivate
```

### Opcion 2': Ambiente local usando environments

Siguiendo el [README](https://github.com/DrDub/artfeateng/blob/master/README.md) del código del [libro](http://artoffeatureengineering.com/).

python3 -m venv feateng
source ./feateng/bin/activate



## General dependencies

pip3 install jupyter
pip3 install ipykernel
pip3 install scikit-learn
pip3 install lxml
pip3 install numpy
pip3 install scipy
pip3 install matplotlib
pip3 install graphviz

pip3 install geopy
pip3 install folium


## Launch Jupyter with the feateng environment

python -m ipykernel install --user --name feateng
jupyter notebook --no-browser .
