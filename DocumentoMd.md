Proyecto de análisis de datos de calidad de gobierno
================
Gabino Owono Esomoyo
2026-05-31

### **Introducción**

La calidad de la administracíon pública es una factor determinante para
el desarollo económico,social y político de caulquier nación.Gobiernos
competentes y libres de corrupción generan confienza ciudadana,reducen
las desigualdades y mejoran la provisión de servicios esenciales como la
salud,educación,etc.Comprender y medir la calidad gubernamental permite
identificar fortalezas y debilidades institucionales,diseñar políticas
más efectiva,etc.

Este proyecto tiene como principal objetivo introducir en el manejo y
exploración de bases de datos con <span style="color:blue;">***R
studio***</span>.Para ello,utilizaremos el conjunto de datos de la
***Encuesta a Expertos sobre la calidad de la administracíon pública
(QoG Expert Survey)***, elaborada por el Instituto de Calidad de
Gobierno de la Universidad de Gotemburgo.

Este conjunto de datos contiene información sobre la calidad de
gobernanza,la transparencia y la eficiencia del sector público en los
paises del mundo.

En este proyecto aprenderás a:

- Importar bases de datos a R studio

- limpiar bases de datos

- Manipular y explorar bases de datos

- Realizar análisis descriptivos básicos

- Visualizar datos para comparar la calidad de gobierno en diferentes
  paises

- Intrepretar datos

### **Installación de packages**

Para realizar este proyecto, utilizaré principalmente los siguientes
librerías:

``` r
library(haven)          # Para importar datos de formato .dta a R studio
library(dplyr)          # Para manipulación y transformacion de datos
library(ggrepel)        # Para evitar solapamiento de etiquétas en gráficos
library(ggplot2)        # Para visualizar datos
library(stargazer)      # Para generar tablas en formato Latex, etc
library(factoextra)     # Para visualizar resultados de PCA,clustering, etc
library(FactoMineR)     # Para realizar análisis multivariante PCA,clustering,etc.
```

### **Importación datos**
