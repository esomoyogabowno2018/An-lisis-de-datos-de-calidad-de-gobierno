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
library(readxl)         # Para importar datos de excel a R studio
library(dplyr)          # Para manipulación y transformacion de datos
library(ggrepel)        # Para evitar solapamiento de etiquétas en gráficos
library(ggplot2)        # Para visualizar datos
library(stargazer)      # Para generar tablas en formato Latex, etc
library(factoextra)     # Para visualizar resultados de PCA,clustering, etc
library(FactoMineR)     # Para realizar análisis multivariante PCA,clustering,etc.
```

### **Importación datos**

Para este proyecto utilizaré la base de datos ***QoG Basic Dataset***,
publicada en enero de 2026. Este conjunto de datos de tipo
**transversal** contiene información de las variables más utilizadas de
la base de datos ***QoG Standard Dataset***, donde la unidad de análisis
es el país.

``` r
qog_b26<-read_excel("Datos/qog_bas_cs_jan26.xlsx")
```

``` r
dim(qog_b26)
```

    ## [1] 194 320

El conjunto de datos contiene información sobre ***194*** países y
***320*** variables. Para fines de este proyecto, no se trabajará con la
totalidad de las ***320*** variables, sino que se procederá a filtrar
aquellas más relevantes para el análisis.

### **Limpieza de la base de datos**
