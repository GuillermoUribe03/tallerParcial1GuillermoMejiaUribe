**Guía de Ejecución del Notebook OrdenamientoDatasetCausasDeMuerte2024-2**

Realizado Por: Guillermo Mejía Uribe, c.c. 1037643854
Base de Datos Utilizada: Dataset de Causas de Muerte
Nombre del Equipo: Mortal Metrics

Este documento explica el paso a paso necesario para ejecutar y reproducir el notebook, asegurando que se obtengan los resultados esperados en el análisis y comparación de los métodos de ordenamiento implementados.

Este proyecto implementa 15 algoritmos de ordenamiento sobre un dataset con registros de causas de muerte alrededor del mundo. El objetivo es analizar el rendimiento de estos algoritmos en listas de diferentes tamaños, identificando ventajas y desventajas en función de la naturaleza del dataset.

## Tabla de Contenido

1. [Clonar el Repositorio desde GitHub](#1-clonar-el-repositorio-desde-github)
2. [Requisitos Previos](#2-requisitos-previos)
3. [Abrir el Notebook en Google Colab](#3-abrir-el-notebook-en-google-colab)
4. [Descarga del Dataset](#4-descarga-del-dataset)
5. [Exploración del Dataset y Selección de la Columna a Ordenar](#5-exploración-del-dataset-y-selección-de-la-columna-a-ordenar)
6. [Implementación de los Métodos de Ordenamiento](#6-implementación-de--los-métodos-de-ordenamiento)
7. [Pruebas y Medición de Tiempos de Ejecución](#7-pruebas-y-medición-de-tiempos-de-ejecución)
8. [Ejecución de las Pruebas por Tamaño de Muestra](#8-ejecución-de-las-pruebas-por-tamaño-de-muestra)
9. [Visualización Gráfica de los Resultados](#9-visualización-gráfica-de-los-resultados)
10. [Observaciones sobre los Resultados](#10-observaciones-sobre-los-resultados)
11. [Referencias](#11-referencias)

## 1. Clonar El Repositorio desde Github

Para comenzar con la ejecución del proyecto, primero debes clonar el repositorio en tu entorno local.

- Abra Git Bash.

- Cambia el directorio de trabajo actual a la ubicación en donde quieres clonar el directorio.

- Escriba git clone y pegue la dirección URL que ha copiado antes. Como se ve a continuación:

```bash
git clone https://github.com/GuillermoUribe03/tallerParcial1GuillermoMejiaUribe.git
```

Esto descargará todos los archivos del proyecto, incluidos el notebook, las imágenes, y el informe PDF en tu entorno local.

Una vez clonado el proyecto, navega a la carpeta descargada.

## 2. Requisitos Previos

Antes de ejecutar el notebook, asegúrate de tener lo siguiente:

- Acceso a Google Colab (se recomienda este entorno para la ejecución del notebook).
- Cuenta en Kaggle para descargar los datos automáticamente desde la plataforma (opcional).

## 3. Abrir el Notebook en Google Colab

Cargar el archivo del notebook en Colab:

- Sube el archivo OrdenamientoDatasetCausasDeMuerte2024_2.ipynb a Google Colab.
- Una vez cargado, abre el notebook y conecta el entorno presionando el botón "Conectar" en la esquina superior derecha.

* Interactue con el notebook, las cuatro secciones van a tener sus celdas ocultas. Puede abrir o cerrar cada sección ó subsección dando click en '>'

![Estructura del Notebook](/img/notebook.PNG "Estructura notebook")

## 4. Descarga del Dataset

El dataset utilizado se llama "cause_of_deaths.csv" y está disponible en la plataforma Kaggle. Existen dos opciones para importar el dataset:

- Descargar desde Kaggle:

  - En el notebook, ejecuta la celda correspondiente a la descarga automática desde Kaggle.

  ![Seccion descargar desde Kaggle](/img/subirKaggle.PNG "Descargar desde Kaggle")

- Metodo alternativo - Cargar el archivo localmente:

  En caso tal de que la descarga autamitica falle, sube el archivo manualmente desde la carpeta 'data' del proyecto. (Si el paso anterior, es decir la carga de Kaggle, se efectua de manera correcta, ignore esta celda de ejecución.)

  - En el notebook, ejecuta la celda correspondiente a la alternativa de carga manual del archivo, al ejecutarla elige y sube el archivo 'cause_of_deaths.csv' que se encuentra en la carpeta data.

  ![Seccion descarga Alternativa](/img/subirAlternativa.PNG "Descarga Alternativa")

## 5. Exploración del Dataset y Selección de la Columna a Ordenar

Después de cargar exitosamente los datos, encontrarás una sección de información del dataset. Ejecuta todas las celdas de esta sección para cargar librerias necesarias, inspeccionar los datos y seleccionar la columna "Alzheimer's Disease and Other Dementias" como la lista a ordenar en los diferentes métodos.

![Seccion Exploracion del dataset](/img/seccionDataset.PNG "Exploracion Dataset")

## 6. Implementación de los Métodos de Ordenamiento

- Ejecución de los 15 métodos de ordenamiento:

  - En esta sección, cada método se describe y se muestra su implementación en código.
  - Ejecuta las celdas de cada método. Cada uno ordenará una lista con los primeros 2000 registros de la columna seleccionada y mostrará los resultados correspondientes.

  ![Seccion Implementacion de los Métodos de Ordenamiento](/img/SeccionImplementar.PNG "Metodos de ordenamiento")

- Método Exclusivo - Counting Sort:

  El Counting Sort es el método exclusivo de este taller. Es el primer algoritmo presentado en la sección de implementación.

## 7. Pruebas y Medición de Tiempos de Ejecución

En esta sección encontrarás funciones auxiliares para:

- Generación de listas de diferentes tamaños (2000, 3000, 4000, 5000 y 6120 registros). Cada lista se genera aleatoriamente, lo que puede generar variaciones en los tiempos de ejecución entre ejecuciones.
- Medición de tiempos de ejecución para los 15 métodos implementados. Cada método recibe la misma lista de prueba, pero se realizan copias internas para garantizar que la lista original nunca se modifique.

![Seccion Pruebas y Tiempo de Ejecución](/img/SeccionPruebas.PNG "Seccion Pruebas")

## 8. Ejecución de las Pruebas por Tamaño de Muestra

- Ejecuta las secciones de pruebas en orden:

  - Comienza con la prueba para 2000 registros, luego para 3000 registros, y así sucesivamente hasta llegar a la prueba con 6120 registros.
  - Cada sección muestra los tiempos de ejecución de los 15 métodos para cada tamaño, además, muestra la grafica de barras horizontales para comparar visualmente los tiempos de ejecución, y tambien, se observa graficas de disperción de los datos.

## 9. Visualización Gráfica de los Resultados

Al final del notebook, encontrarás una sección de visualización gráfica global que compara los tiempos de ejecución para todos los tamaños de lista y métodos de ordenamiento.

## 10. Observaciones sobre los Resultados

    Es importante tener en cuenta:

    - Variaciones en los tiempos de ejecución: Debido a la generación aleatoria de las listas en cada ejecución, los resultados pueden diferir ligeramente.
    - Reproducir el notebook desde cero: Cada vez que se reinicie el entorno de Colab, deberás ejecutar nuevamente todas las celdas en orden para garantizar la correcta ejecución del notebook.
    - Análisis detallado: Los resultados y análisis completos se encuentran en un informe PDF adjunto.

## 11. Referencias

    - Dataset original: Kaggle - Cause of Deaths
      (https://www.kaggle.com/datasets/iamsouravbanerjee/cause-of-deaths-around-the-world DATA)
    - Informe PDF: Contiene un análisis detallado de los resultados y comparaciones de los métodos implementados.
