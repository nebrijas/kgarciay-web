## Actividad Dirigida 4

Esta es la actividad dirigida 4 que consiste en hacer un ejercicio de programación literaria donde se debe conectar a una API de Covid19 por medio de la url https://api.covid19api.com/countries para obtener los datos de países que fueron necesarios para el desarrollo de esta actividad utilizando el notebook de Jupyter

## Código fuente

El código fue implementado en Jupyter y fue generado como un archivo .ipynb ya cargado en la página principal de este github, por lo tanto, se realizará el ejercicio de programación literaria usando como base el archivo mencionado

## Programación literaria

Cómo es común se realizará la respectiva documentación en este caso de la actividad número 4 tal y como lo dice el enunciado

## Librerías 

 - **pandas:** Es una biblioteca de Sotware escrita como extensión de NumPy para manipulación y análisis de datos en Python 
 - **numpy:** Es una biblioteca que permite crear vectores y matrices de forma multidimensional, junto con varias funciones matemáticas

## Implementación de código

Para realizar correctamente esta actividad se tenía obligatoriamente que observar el funcionamiento del código, para esto, se tuvo que descargar anaconda que es una distribución libre y abierta de los lenguajes R y Phyton, se utilizó Anaconda Navigator donde está incluido el programa Jupyter el cual fue de gran uso como entorno de desarrollo para observar la impresión del código.

## Importación de librerías

Al realicar el código en Jupyter, ya que para entenderlo mejor se realizó paso a paso como lo indicó el profesor en cada clase. Se importó una librería original de Python, en este caso no hubo necesidad de cambiar o adicionar alguna ya que funcionaba correctamente. Esta es:

-**import pandas as pd** para poder hacer el correcto funcionamiento de la librería pandas

## Variables

A continuación se explicarán las variables que fueron necesarias para la realización del código, donde se explicará que contiene cada una y para que han sido utilizadas: 

 - **url:** Esta variable fue usada para guardar la URL principal ya que para conectarse con la API de Covid19 
 - **df:** Esta variable guarda la información generada por el archivo de la url que es tipo json
 - **url_rt_es:** Guarda la url que contiene los datos de España
 - **df_rt_es:** Esta variable guarda la información generada por el archivo de url_rt_es
 - **casos_es:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_es 
 - **url_rt_pa:** Guarda la url que contiene los datos de Panamá
 - **df_rt_pa:** Esta variable guarda la información generada por el archivo de url_rt_pa
 - **casos_pa:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_pa 
 - **pa_vs_es:** Guarda la unión de casos que ocurrieron en la misma fecha entre España y Panamá
 - **url_rt_cr:** Guarda la url que contiene los datos de Costa Rica
 - **df_rt_cr:** Esta variable guarda la información generada por el archivo de url_rt_cr
 - **casos_cr:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_cr
 - **url_rt_nc:** Guarda la url que contiene los datos de Nicaragua
 - **df_rt_nc:** Esta variable guarda la información generada por el archivo de url_rt_nc
 - **casos_nc:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_nc
 - **url_rt_gu:** Guarda la url que contiene los datos de Guatemala
 - **df_rt_gu:** Esta variable guarda la información generada por el archivo de url_rt_gu
 - **casos_gu:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_gu
 - **url_rt_sal:** Guarda la url que contiene los datos de El Salvador
 - **df_rt_sal:** Esta variable guarda la información generada por el archivo de url_rt_sal
 - **casos_sal:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_sal
 - **url_rt_hon:** Guarda la url que contiene los datos de Honduras
 - **df_rt_hon:** Esta variable guarda la información generada por el archivo de url_rt_hon
 - **casos_hon:** Esta variable permite guardar solamente los casos y las fechas cuando ocurrieron esos casos del archivo df_rt_hon
 - **cenA_vs:** Guarda la unión de casos que ocurrieron en la misma fecha entre Panamá, Costa Rica, Nicaragua, Guatemala, El Salvador y Honduras, el nombre de la                       variable representa centro América

## Explicación del código

A continuación se explicará paso a paso el código que se realizó.

### Código

```
!pip install pandas
```

Se realizó la instalación de la librería de pandas

### Código 

```
pip install numpy
```

Se instaló la librería de numpy

### Código 

```
import pandas as pd
```

Se generó el import de pandas para poder hacer uso de la respectiva librería}

### Código 

```
url = 'https://api.covid19api.com/countries'
url
```

Se guardó la url mencionada al principio de la actividad que contiene la información de los países como el nombre, el slug y el ISO2 que se refiere al código de dirección de cada país. Luego, se realizo la respectiva impresión del archivo de la variable url 

### Código 

```
df = pd.read_json(url)
df
```

En la variable df por medio de pd.read se lee el archivo json que contiene la url ya mencionada guardando la información de los paises, esta función es generada por pandas que es capaz de leer el json que ofrece la API. Luego, se genera la impresión del dataframe desde el inicio hasta el final

### Código 

```
df[df['Country'] == 'Spain']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a España por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código 
```
url_rt_es = 'https://api.covid19api.com/country/spain/status/confirmed/live'
df_rt_es = pd.read_json(url_rt_es)
df_rt_es
```

Se puede ver los casos diarios de España desde la dirección https://api.covid19api.com/country/spain/status/confirmed/live definiendo una nueva variable url_rt_es y creando el objeto df_rt_es que lee la información de la url

### Código 
```
df_rt_es.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_es.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_es = df_rt_es.set_index('Date')['Cases']
casos_es.plot(title="Casos de Covid19 en España")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/espa%C3%B1a.png">

### Ahora con Panamá

Se repite el mismo proceso con España pero cambiando el país a Panamá para luego realizar el ploteo de ambos países 

### Código
```
df[df['Country'] == 'Panama']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Panama por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_pa = 'https://api.covid19api.com/country/panama/status/confirmed/live'
df_rt_pa = pd.read_json(url_rt_pa)
```

Se puede ver los casos diarios de Panamá desde la dirección https://api.covid19api.com/country/panama/status/confirmed/live definiendo una nueva variable url_rt_pa y creando el objeto df_rt_pa que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_pa = df_rt_pa.set_index('Date')['Cases']
casos_pa.plot(title="Casos de Covid19 en Panamá")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/panama.png">

### Proceso para realizar la gráfica que demuestre la diferencia entre España y Panamá en casos de Covid19

### Código 
```
casos_pa
casos_es
```

Se genera la impresión del contenido de las variables de los casos de España y de Panamá

### Código 
```
pa_vs_es= pd.concat([casos_es, casos_pa], axis=1)
pa_vs_es
```

En este caso se concatena, es decir se combina lo que se encuentre en casos_es y casos_pa y se guarda todo eso en una sola variable llamada pa_vs_es

### Código 
```
pa_vs_es.columns = ('España', 'Panamá')
pa_vs_es
```

Se agrega el nombre de las columnas para definir los datos clasificados a cual de los dos países corresponde

### Resultado de la concatenación

<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/concatenacion.PNG">

### Código 
```
pa_vs_es.plot(title= "Comparativa Covid19 España-Panama")
```

Se ha establecido que en el dataframe hay un un "index" que son las fechas y dentro de ese archivo sólo se quieren conocer los valores del número de casos. Para esto, se crea una visualización por medio de la función plot. Se utilizará el gráfico creando un titulo, se crea la variable title seguido del = para establecer la equivalencia y entre comillas porque es texto literal.

El resultado es un gráfico de línea en el cual el eje x es el "index" establecido, las fechas; y el eje y son los valores extraídos del número de casos 

### Gráfico resultante

<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/grafico_es_pa.png">

## Se realiza el mismo proceso con países de Centro América

### Panamá

Se empieza el proceso con Panamá repitiendo exactamente el mismo proceso que ya se ha escrito anteriormente

### Código
```
df[df['Country'] == 'Panama']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Panama por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_pa = 'https://api.covid19api.com/country/panama/status/confirmed/live'
df_rt_pa = pd.read_json(url_rt_pa)
```

Se puede ver los casos diarios de Panamá desde la dirección https://api.covid19api.com/country/panama/status/confirmed/live definiendo una nueva variable url_rt_pa y creando el objeto df_rt_pa que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_pa = df_rt_pa.set_index('Date')['Cases']
casos_pa.plot(title="Casos de Covid19 en Panamá")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/panama.png">

### Costa Rica

### Código
```
df[df['Country'] == 'Costa Rica']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Costa Rica por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_cr = 'https://api.covid19api.com/country/costa-rica/status/confirmed/live'
df_rt_cr = pd.read_json(url_rt_cr)
```

Se puede ver los casos diarios de Costa Rica desde la dirección https://api.covid19api.com/country/costa-rica/status/confirmed/live definiendo una nueva variable url_rt_cr y creando el objeto df_rt_cr que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_cr = df_rt_cr.set_index('Date')['Cases']
casos_cr.plot(title="Casos de Covid19 en Costa Rica")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/costa%20rica.png">

### Nicaragua

### Código
```
df[df['Country'] == 'Nicaragua']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Nicaragua por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_nc = 'https://api.covid19api.com/country/nicaragua/status/confirmed/live'
df_rt_nc = pd.read_json(url_rt_nc)
```

Se puede ver los casos diarios de Nicaragua desde la dirección https://api.covid19api.com/country/nicaragua/status/confirmed/live definiendo una nueva variable url_rt_nc y creando el objeto df_rt_nc que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_nc = df_rt_nc.set_index('Date')['Cases']
casos_nc.plot(title="Casos de Covid19 en Nicaragua")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/nicaragua.png">

### Guatemala

### Código
```
df[df['Country'] == 'Guatemala']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Guatemala por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_gu = 'https://api.covid19api.com/country/guatemala/status/confirmed/live'
df_rt_gu = pd.read_json(url_rt_gu)
```

Se puede ver los casos diarios de Nicaragua desde la dirección https://api.covid19api.com/country/guatemala/status/confirmed/live definiendo una nueva variable url_rt_gu y creando el objeto df_rt_gu que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_gu = df_rt_gu.set_index('Date')['Cases']
casos_gu.plot(title="Casos de Covid19 en Guatemala")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/guatemala.png">

### El Salvador

### Código
```
df[df['Country'] == 'El Salvador']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a El Salvador por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_sal = 'https://api.covid19api.com/country/el-salvador/status/confirmed/live'
df_rt_sal = pd.read_json(url_rt_sal)
```

Se puede ver los casos diarios de El Salvador desde la dirección https://api.covid19api.com/country/el-salvador/status/confirmed/live definiendo una nueva variable url_rt_sal y creando el objeto df_rt_sal que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_sal = df_rt_gu.set_index('Date')['Cases']
casos_sal.plot(title="Casos de Covid19 en El Salvador")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/salvador.png">

### Honduras

### Código
```
df[df['Country'] == 'Honduras']
```

Se utiliza 'Country' para que en el archivo se identifique que se está en la sección de países y ademas se iguala a Honduras por medio de los signos == que permite que la variable df busque el páis correspondiente en la sección correspondiente y eso crea una máscara sobre los datos guardandolo en la variable

### Código
```
url_rt_hon = 'https://api.covid19api.com/country/honduras/status/confirmed/live'
df_rt_hon = pd.read_json(url_rt_hon)
```

Se puede ver los casos diarios de Honduras desde la dirección https://api.covid19api.com/country/honduras/status/confirmed/live definiendo una nueva variable url_rt_hon y creando el objeto df_rt_hon que lee la información de la url

### Código 
```
df_rt_pa.head()
```

Permite observar la información que tiene la cabecera del archivo

### Código 
```
df_rt_pa.tail()
```

Permite observar la información que tiene la cola del archivo

### Código 
```
casos_hon = df_rt_hon.set_index('Date')['Cases']
casos_hon.plot(title="Casos de Covid19 en Honduras")
```

Se crea una nueva variable que permite guardar la información filtrada de casos y fechas del archivo.
Luego se utiliza la funcion plot que es la encargada de realizar la respectiva gráfica generada.

### Gráfica
<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/honduras.png">

### Proceso para realizar la gráfica que demuestre la diferencia entre los países de Centro América en casos de Covid19

### Código 
```
casos_pa
casos_cr
casos_nc
casos_gu
casos_sal
casos_hon
```

Se genera la impresión del contenido de las variables de los casos de Panamá, Costa Rica, Nicaragua, Guatemala, El Salvador, Honduras

### Código 
```
cenA_vs= pd.concat([casos_pa, casos_cr, casos_nc, casos_gu, casos_sal, casos_hon], axis=1)
cenA_vs
```

En este caso se concatena, es decir se combina lo que se encuentre en casos_pa, casos_cr, casos_nc, casos_gu, casos_sal, casos_hon y se guarda todo eso en una sola variable llamada cenA:vs

### Código 
```
cenA_vs.columns = ('Panamá', 'Costa Rica', 'Nicaragua', 'Guatemala', 'El salvador', 'Honduras')
cenA_vs
```

Se agrega el nombre de las columnas para definir los datos clasificados a cual de los dos países corresponde

### Resultado de la concatenación

<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/concatenacion_Cen_A.PNG">

### Código 
```
cenA_vs.plot(title= "Comparativa Covid19 Panama-Costa Rica-Nicaragua-Guatemala-El Salvador-Honduras")
```

Se ha establecido que en el dataframe hay un un "index" que son las fechas y dentro de ese archivo sólo se quieren conocer los valores del número de casos. Para esto, se crea una visualización por medio de la función plot. Se utilizará el gráfico creando un titulo, se crea la variable title seguido del = para establecer la equivalencia y entre comillas porque es texto literal.

El resultado es un gráfico de línea en el cual el eje x es el "index" establecido, las fechas; y el eje y son los valores extraídos del número de casos 

### Gráfico resultante

<img src = "https://github.com/nebrijas/kgarciay-web/blob/main/grafica_cen_A.png">


-----------------------------------

Clic **[aquí](https://github.com/nebrijas/kgarciay-web/blob/main/AD1.md)** para volver a *la Actividad Dirigida 1*

Clic **[aquí](https://github.com/nebrijas/kgarciay-web/blob/main/AD2.md)** para volver a *la Actividad Dirigida 2*

Clic **[aquí](https://github.com/nebrijas/kgarciay-web/blob/main/AD3.md)** para volver a *la Actividad Dirigida 3*

Clic **[aquí](https://github.com/nebrijas/kgarciay-web/blob/main/README.md)** para volver a *README*

