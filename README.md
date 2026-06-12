# Proyecto Final: Reporte Histórico ENVIPE (2020-2024)
Este repositorio contiene un análisis exploratorio y descriptivo de gráficas elaboradas con datos de la Encuesta Nacional de Victimización y Percepción sobre Seguridad Pública (ENVIPE) publicada por el INEGI. Aunque las encuestas analizadas corresponden a los levantamientos 2021, 2022, 2023, 2024 y 2025, es importante señalar que estos datos reportan la percepción y experiencias de victimización ocurridas durante los años 2020, 2021, 2022, 2023 y 2024 respectivamente. El estudio identifica tendencias, cambios y patrones en la seguridad pública de México y Querétaro, abordando percepción de inseguridad, incidencia delictiva, confianza en autoridades, medidas de protección adoptadas por la población y experiencias de victimización, así como consecuencias emocionales como miedo, desconfianza, vulnerabilidad y alteraciones en la vida cotidiana.

# Productos generados
El proyecto genera distintos productos analíticos y visuales a partir de los microdatos de la ENVIPE (2021-2025), entre ellos:
- Gráficas de series temporales (barras apiladas y líneas) que muestran la evolución de la percepción ciudadana sobre seguridad pública, victimización y confianza institucional en tres niveles geográficos: nacional, estatal (Querétaro) y municipal (Querétaro, Corregidora y El Marqués).
- Gráficas comparativas por municipio mediante facetas, permitiendo visualizar de manera simultánea el comportamiento de los indicadores en los tres municipios con representatividad estadística dentro del estado de Querétaro.
- Mapas temáticos del estado de Querétaro que ilustran los cambios porcentuales en indicadores clave (como preocupación económica o conocimiento de operativos) entre 2020 y 2024, utilizando escalas de color para identificar mejorías o retrocesos por municipio.
- Reportes reproducibles en formato HTML mediante R Markdown (archivo .Rmd), que integran código, gráficas, mapas y análisis descriptivo en un solo documento autocontenido, facilitando la actualización y replicación del análisis con nuevas ediciones de la ENVIPE.
- Análisis descriptivo estructurado para cada una de las 10 preguntas seleccionadas, incluyendo: planteamiento de la pregunta original, justificación de su importancia, visualización gráfica, interpretación de resultados y conclusiones comparativas entre los tres niveles de análisis.

# Librerias
library(dplyr)

library(ggplot2)

library(tidyr)

library(forcats)

library(scales)

library(stringr)

library(maps)

library(ggrepel)

library(tidyverse)


# Instalacion de Librerias
Copia, pega y corre la siguiente linea en la consola de R antes de correr el codigo:

install.packages(c("dplyr", "ggplot2", "tidyr", "forcats", "scales", "stringr", "maps", "ggrepel", "tidyverse"))

# Requisitos
Software: R 4.2 o superior + RStudio

# Pasos para compilar el codigo en tu propio escritorio
1. Descarga los 5 documentos "bd_envipe_202x_csv.zip" y el documento "mapa.zip".
2. Descomprime los archivos.
3. Obten la direccion de cada una de las carpetas (Ubica la carpeta descomprimida -> Entra en ella -> Haz click derecho y despues izquierdo sobre algun documento -> Propiedades -> Copia el texto que se encuentra en "Ubicación").
4. Descarga el codigo "ProyectoFinal.Rmd".
5. Abrelo y ubica las lineas 18 a 24 dentro del codigo correspondientes al directorio de trabajo.
6. Remplaza la dirección del trabajo con tu propia dirección para cada año (incluido el mapa). 
Ej: Si obtuviste como directorio "C:\Users\user\Downloads" en el codigo deberias tener: directorio2021 <- "C:/Users/user/Dowloads/bd_envipe_2021_csv"
7. Instala las librerias mostradas un poco más atras en este mismo repositorio.
8. Compila el codigo dando click en "Knit" luego en "Knit to Html" (sugerencia).

# Integrantes de Equipo
- Martínez Feregrino José Julián (Repositor)
- Hernández Camacho Carolina
- Espejel Flores Emmanuel
