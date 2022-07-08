## Actividad Dirigida 3

Esta es la actividad dirigida 3 que consiste en hacer un ejercicio de programación literaria aprovechando el código que hemos usado en programación con Python donde realizamos Web Scrapping. A continuación pongo el código fuente.

# Código fuente


```
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored

resultados = []

req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')

tags = soup.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)


os.system("clear")

print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))

print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```


## Programación literaria

Cómo es común se realizará la respectiva documentación en este caso de la actividad número 3 tal y como lo dice el enunciado. Se harán las respectivas explicaciones de:
- [Librerias](#Librerias)
- Librerías especiales para web scraping
- Implementación de código
- Importación de librerías
- Instalación de librerías
- [Variables](#Variables)
- Funcionamiento

## Librerías 

 - **requests:** Es el estándar para realizar solicitudes HTTP en Phyton, abstrae las solicitudes detrás de una API para que pueda concentrarse en interactuar con los                  servicios y consumir los datos de su aplicación.
 - **time:** El modulo time de la biblioteca estándar de Python proporciona un conjunto de funciones para trabajar con fechas y/o horas de distintos relojes para                    obtener información relacionada con nuestro horario
 - **csv:** Es el formato más común de importación y exportación de hojas de cálculo y bases de datos. Implementa clases para leer y escribir datos tabulares en                   formato CSV, permite leer datos desde un archivo de Excel
 - **os:** Permite utilizar funcionalidades independientes como el open(), si se quiere manipular alguna ruta se utiliza os.path y, si se quiere leer un archivo en su            totalidad se utiliza fileinput
 - **re:** Es un paquete integrado que permite trabajar con expresiones regulares
 - **colored:** Biblioteca de Python muy simple que permite enviar color y formato a la terminal

## Librerías especiales para web scraping

 - **pandas:** Es una biblioteca de Sotware escrita como extensión de NumPy para manipulación y análisis de datos en Python 
 - **BeautifulSoup:** Crea un árbol con todos los elementos de un documento y permite la extracción de información

## Implementación de código

Para realizar correctamente esta actividad se tenía obligatoriamente que observar el funcionamiento del código, para esto, se tuvo que descargar anaconda que es una distribución libre y abierta de los lenguajes R y Phyton, se utilizó Anaconda Navigator donde está incluido el programa Spyder el cual fue de gran uso como entorno de desarrollo para observar la impresión del código. Luego, como ya se había clonado el repositorio se utilizó del archivo llamado ad3.md sólo el código

## Importación de librerías

Al abrir el código en Spyder se importaron varias librerias que son originales de Python, en este caso no hubo necesidad de cambiar o adicionar algo a estas librerías ya que todas funcionaban correctamente. Estas son:
1. **import requests**
2. **import time**
3. **import csv**
4. **import re**
5. **import os**

## Instalación de librerías

En este caso al implementar el código se presentaron varios errorres porque no se tenían instaladas algunas librerías que se necesitaban para que a lo largo del código este funcionara y corriera de forma correcta. En este caso se utilizaron los siguientes comandos que fueron escritos en la terminal del programa Spyder y que fueron instalados por el mismo medio, como por ejemplo:

1. **from bs4 import BeautifulSoup** se utilizó el comando: **pip install beautifulsoup4**
2. **import pandas as pd** se utilizó el comando: **pip install pandas**
3. **from termcolor import colored** se utilizó el comando: **pip install termcolor**

## Variables

A continuación se explicarán las variables que fueron necesarias para la realización del código, donde se explicará que contiene cada una y para que han sido utilizadas: 

 - **resultados:** Esta variable está inicializada como un arreglo o vector que va guardando al final del vector la conversión de los códigos de html a un texto     l                    legible generada por .text, esa conversión se genera gracias a la libreria de BeautifulSoup
 - **req:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este caso             es https://resultados.elpais.com, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req y es de tipo bs4.
 - **tags:** Esta variable genera que dentro de la variable soup agregando un findAll se busquen todas las etiquetas h2 de la página web que se encuentra                            dentro de la variable req, y esto devolverá una lista con todas las etiquetas encontradas
 - **req2:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/internacional, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup2:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req2 y es de tipo bs4.
 - **req3:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/opinion, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup3:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req3 y es de tipo bs4.
 - **req4:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/espana/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup4:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req4 y es de tipo bs4.
 - **req5:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/economia/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup5:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req5 y es de tipo bs4.
 - **req6:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/sociedad/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup6:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req6 y es de tipo bs4.
 - **req7:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/educacion/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup7:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req7 y es de tipo bs4.
 - **req8:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/clima-y-medio-ambiente/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup8:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req8 y es de tipo bs4.
 - **req9:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/ciencia/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup9:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req9 y es de tipo bs4.
 - **req10:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/cultura/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup10:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req10 y es de tipo bs4.
 - **req11:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/babelia/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup11:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req11 y es de tipo bs4.
 - **req12:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/deportes/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup12:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req12 y es de tipo bs4.
 - **req13:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/tecnologia/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup13:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req13 y es de tipo bs4.
 - **req14:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/tecnologia/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup14:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req14 y es de tipo bs4.
 - **req15:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/gente/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup15:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req15 y es de tipo bs4.
 - **req16:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/television/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup16:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req16 y es de tipo bs4.
 - **req17:** Esta variable utiliza el método get que hace parte de la libreria requests, permite enviar un get request es decir una solicitud a una URL que en este                  caso es https://elpais.com/eps/, la variable guarda lo que devuelve un objeto Requests.Response
 - **soup17:** Utiliza la librería BeautifulSoup que permite realizar el Web Scrapping de la página web que ha sido definida en la variable req17 y es de tipo bs4.
 - **str_match:** Esta variable es utilizada por la librería pandas y permite determinar si lo que está en la variable resultados coincide con el objeto "feminismo",                     "igualdad", "mujeres", "mujer", "brecha salarial", "machismo", "violencia", "maltrato", "homicidio", "género", "asesinato", "Sexo" que esté en la                       variables. Devuelve un valor booleano que indica si fue o no encontrado el objeto

## Ciclos

En esta sección se explicará el uso de los ciclos en cada parte del código.

### Código

```
req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')

tags = soup.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
    
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena resultados esas etiquetas de tipo h2. Este ciclo imprime:

```
Al menos seis muertos por un tiroteo en un desfile del Día de la Independencia en EE UU
La entrega de la nueva Constitución sella el inicio de una nueva era en Chile
El desmarque de la derecha y la caótica inauguración marcan el cierre de la Convención constitucional 
La primera Constitución paritaria y con perspectiva de género
Trump, al desnudo
Se busca oposición
Una democracia agonizante
¿Es posible disentir de esta retórica belicista?
Los equipos de rescate buscan al menos a 13 desaparecidos del desprendimiento de un glaciar en Italia sin casi esperanzas de hallarlos vivos
Una cúpula adversa y guerrerista: los retos de Petro con los militares
Patricia Ariza, la dramaturga que será la nueva ministra de Cultura en Colombia
Condenada a 50 años de prisión una joven que perdió un embarazo en El Salvador
Acribillados a balazos siete miembros de una familia en el Estado mexicano de Veracruz
Los Ángeles se convierte en la tercera ciudad de EE UU con una oficina contra el calor extremo
Flores nocturnas: las trabajadoras sexuales de Uruguay reclaman derechos
El hígado necesita tres días semanales sin alcohol

De reina de las criptomonedas a cabeza de “los más buscados”
La investigación de EE UU sobre la muerte de la periodista palestina se cierra en falso por el mal estado de la bala 
El voto extranjero se atasca en Nueva York
Ucrania presenta un ambicioso plan de reconstrucción de 720.000 millones
Turquía retiene un buque ruso con 4.500 toneladas de trigo presuntamente robado de Ucrania
Alberto Fernández cede al kirchnerismo la gestión de la economía argentina
Un juez ordena la detención de uno de los arquitectos de la verdad histórica del ‘caso Ayotzinapa’ en México
La expareja de Juan Carlos I blindó su casa, ordenadores y teléfonos por temor a ser espiada por la inteligencia española
Los primeros poemas de Severo Sarduy, una joya inédita
Barat, de The Libertines: “Había algo muy bonito en mi amistad con Doherty”
Un siglo de canciones, 1.500 artistas
Residente reivindica la América que no es Estados Unidos

Ron Carter, 85 años, todavía un coloso del contrabajo 
En un mundo inestable y pospandémico, ¿para qué sirve la moda?
Britney Spears acusa a sus exgerentes de haberse apropiado de más de  17 millones de dólares de su patrimonio
¿Por qué los mosquitos pican más a unas personas que a otras?
El ‘influencer’ del momento parodia la moda desde una de las islas más pobres del mundo
¡Qué bueno es tener a mano una madre alfa para organizar una fiesta masiva!
Solo y sin oxígeno artificial en la cima del Everest: cada paso es una agonía   
El Nadal fulminante eleva el vuelo
Halep, un mal trago para Paula Badosa
Nunca hay paz para Ferrari: “¡Dejad de inventar, chicos!”
El Barcelona oficializa los fichajes de Kessié y Christensen
Pedro Sánchez: “El régimen de Putin es una autocracia dominada por una oligarquía corrupta y ultracapitalista”
Francisco de Roux: “Si no se acaba con el narco, Colombia no tendrá paz”
Especial | Análisis de la nueva estrategia de la Alianza punto por punto
La economía mundial se desinfla: así es la crisis que viene
The war against abortion in the US: A state-by-state battle
Four hours inside a sweltering truck: The migrant dream that ended in tragedy
US police kill unarmed Black man in rain of bullets, video shows
Russia says it has taken Lysychansk, key city in battle for eastern Ukraine
Rescuers search for missing climbers after deadly glacier collapse in Italian Alps
Is Mexico trailblazing a new development model for the world?
Letras Americanas: la actualidad literaria de un continente vista por el escritor Emiliano Monge
Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
Toda la actualidad científica en el boletín de Materia
Ideas: reportajes y entrevistas para entender el mundo
El Tribunal Supremo de Trump marca la agenda política de Biden
El derecho al aborto no es político
“No necesito que me deje bañada en sangre para ver que lo que me hacía no estaba bien”  
Texas es la nueva China para  Elon Musk
El ministro de Economía de Argentina cede a la presión del kirchnerismo y presenta su renuncia
Locos, cobardes y el golpe de Donald Trump
Las batallas del exmarine que sufrió abusos sexuales en un internado religioso en Zamora
El toreo en Colombia se alista para la embestida de la presidencia de Petro
El caso de la artista Paula Bonet destapa a nuevas víctimas de su acosador
Antony Beevor, historiador militar: “La guerra de Ucrania puede desatar una catástrofe global”
Adele vuelve a escena cinco años después en un concierto ante un público entregado
Residente reivindica la América que no es Estados Unidos en su regreso a Madrid
Thierry Philip: “Si los europeos menores de 20 años dejasen mañana de fumar, la mortalidad por cáncer se reduciría a la mitad en 50 años”
Disfunciones sexuales: todo lo que la fisiosexología puede hacer por ti 
Celos, suegras y uso de Tinder: el complicado emparejamiento de los monos entre zoos
La culpa fue de Tsitsipas
Sinner aborta la rebelión tardía de Alcaraz
Y una florentina para ordenar a tantos hombres en el Tour
Los peores incendios forestales de España: cómo se están intensificando los monstruos de fuego
Alud de solicitudes de vecinos de Barcelona para instalar placas solares
Golpe a la credibilidad internacional de EE UU en el reto climático
Herramientas y trucos para recordar la ubicación del coche gracias al móvil
Las tres amigas que quieren revolucionar los materiales de construcción con fibras de hongos
Dall-E, el popular generador automático de imágenes que hace dibujos sexistas y racistas 
Cádiz entrega una calle a sus divas trans La Petróleo y La Salvaora
Corinna Larsen blindó su casa, ordenadores y teléfonos por temor a ser espiada por el CNI
Feijóo se sentará en el escaño del jefe de la oposición para buscar el foco en el debate sobre el estado de la nación
‘Mi vida con 300 kilos’: un diamante entre la mierda’, por Jimina Sabadú
La voz de los más inocentes
Las actrices de ‘Intimidad’: “Si una mujer no es complaciente en esta profesión, llegan las amenazas”
Juanes: “Me siento maduro, interesante y seguro, y eso me encanta”
Emitida una orden de alejamiento contra Ricky Martin por violencia doméstica 
La última exnovia de Berlusconi se casa con una cantante italiana
Volver a la escuela tras dos años de pandemia
La discriminación contra las minorías sexuales limita el desarrollo de Latinoamérica
República Dominicana, donde la vida fluye por el río infinito
'Cuento de Catherine del Biombo 5', por Javier Marías 
Marta Segarra: “Quien diga que el hombre es el único animal que viola se equivoca”
‘Los marxistas nos están lavando el cerebro’: la teoría de la conspiración que cala en cierta derecha 
Manual para sobrevivir al calentón del euríbor
La carrera por las oposiciones ha empezado: en juego hay 45.000 trabajos para toda la vida
Los primeros poemas de Severo Sarduy, una joya inédita
Libros para el verano: 80 novedades recomendadas para estas vacaciones
Una estrategia de desinformación amenaza la estabilidad y la convivencia en República Centroafricana
El poder creativo de los migrantes
Una ruta por la crónica negra de las calles de Barcelona
En el restaurante Compartir de Barcelona los aciertos alternan con propuestas que aguardan su puesta a punto
Las 10 modelos que consiguieron ser las mejor pagadas del momento
Courtney Love: «Los filtros de Instagram están destruyendo nuestras vidas»
A-ha: cómo tres tipos que no se soportan sobrevivieron a la canción pop más grande de los ochenta 
Una granja llena de armas y dos denuncias por secuestro: ¿cómo ha llegado Ezra Miller hasta aquí?
Menú semanal de El Comidista (4 a 10 de julio)
Parejas con restaurante: seis historias de amor y cuchillos
Adiós al consumidor, llega el ‘yosumidor’
Un camarero busca empleo en Málaga: “En once entrevistas me han ofrecido contrato de media jornada y el resto sin declarar“
Ponte a prueba con nuestros crucigramas, sopas de letras, sudokus y juegos arcade
Pasan a la historia de ‘First Dates’ con esta escena que lleva 7.000 retuits y 54.000 me gusta
El PSG encuentra un ‘9’ para Mbappé
‘¿Y si China controlara la televisión en España? El verdadero problema con TikTok’, por Antonio Ortiz
```

### Código
```
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
    
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req2 que es utilizada por la variable soup2 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Ucrania presenta en Suiza un ambicioso plan de reconstrucción de 720.000 millones 
Al menos seis muertos a las afueras de Chicago por un tiroteo en un desfile del Día de la Independencia
Turquía retiene un buque ruso con 4.500 toneladas de trigo presuntamente robado de Ucrania
Las otras fronteras de Rusia: entre el miedo (al imperio) y los intereses nacionales
El lenguaje que Putin entiende
En busca de un lugar para la Unión Europea en el mundo 
De Ucrania a las vallas espinosas de Melilla
Macron y las consecuencias del amor
La entrega de la nueva Constitución sella el inicio de una nueva era en Chile
La investigación de EE UU sobre la muerte de la periodista palestina se cierra en falso por el mal estado de la bala 
El laborismo británico se reconcilia con el Brexit y promete que el Reino Unido no regresará a la UE
Los equipos de rescate buscan al menos a 13 desaparecidos del desprendimiento de un glaciar en Italia sin casi esperanzas de hallarlos vivos
Arrestada en Mariupol y encarcelada por las fuerzas rusas: los 83 días de horror de una española
Kaliningrado no teme a la OTAN
Rusia avanza posiciones en el este de Ucrania al controlar la ciudad clave de Lisichansk
Macron remodela su Gobierno mes y medio después de constituirlo
Una cúpula adversa y guerrerista: los retos de Petro con los militares
Alberto Fernández cede al kirchnerismo la gestión de la economía argentina
Tres muertos y varios heridos graves en un tiroteo en un centro comercial de Copenhague
La entrega de la nueva Constitución sella el inicio de una nueva era en Chile
Del Estado social de derecho al fin del Senado: claves del nuevo texto constitucional chileno
Isidro Solís: “La propuesta de Constitución es extraordinariamente mala y dañina para la democracia en Chile”
Fernando Atria:  “Espero que el proceso constituyente chileno sea refundacional”
El voto extranjero se atasca en Nueva York
```

### Código
```
req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
    
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req3 que es utilizada por la variable soup3 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Una memoria democrática más inclusiva y plural
Trump, al desnudo
Ese cuerpo
El Tribunal Constitucional: entre el Derecho y el no Derecho
‘Mi casa, mi árbol’
Hambre: las muertes que sí podemos evitar
Gobiernos rojos y glóbulos blancos
Vulnerables
Si son negros, vienen a delinquir 
Selenita
Santa Bárbara y la cultura de la defensa
El mundo que viene
Las humanidades lo petan
El Roto
Peridis
Flavita Banana
Riki Blanco
Sciammarella
Planeta de Plástico, por Malagón
Envía tu carta
Salud y mentiras
Reconocimiento al Gobierno
Jóvenes brillantes, educación pública y poder 
En la calle circulan rumores
Opinar sin insultar
Contra el conflicto de intereses, transparencia
El defensor del lector contesta
```

### Código

```
req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req4 que es utilizada por la variable soup4 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Sánchez acelera y aprueba este martes un crédito extra de 1.000 millones en Defensa pese a las críticas de Podemos
El PP desplaza al PSOE del primer puesto tras las elecciones andaluzas
“Esto es una tortura psicológica”
¿Es posible disentir de esta retórica belicista?
Los trajes del presidente Sánchez
Panegírico del voto
Perder el sentido de la oportunidad
La búsqueda de seguridad vence al cabreo
Solo uno de cada cuatro españoles valora las medidas del Gobierno
Bruselas considera “inaceptable” la muerte de personas en la frontera de Melilla 
ERC se mueve a la abstención para seguir negociando la Ley de Memoria Democrática
El Gobierno acusa al PP de ejercer una estrategia “de conspiración” y “trumpista”
Consulte todos los datos internos de la encuesta de EL PAÍS de julio: cuestionarios, cruces y respuestas
Un niño de siete años, grave tras intoxicarse por una fuga de cloro en la piscina de un hotel de Mallorca
Drones submarinos para el narco ‘made in Cádiz’
Feijóo se sentará en el escaño del jefe de la oposición para buscar el foco en el debate sobre el estado de la nación
El conductor que desencadenó el accidente múltiple de Granada asegura que se le cruzó un animal
El Tribunal Superior catalán plantea llevar al Constitucional la ley del Govern que rechaza fijar el 25% del castellano en las aulas
El tiempo de la semana: de las tormentas al calor intenso y generalizado
Un paraíso en el que avistar más de 20 especies de cetáceos
El secreto de Fuerteventura se hace viral: la ‘playa de las palomitas’
Un vino para triunfar entre los mileniales
Artesanía y cultura que conquista a las ‘influencers’
Más allá de la capital. El triunfo de la vida rural madrileña
```

### Código

```
req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req5 que es utilizada por la variable soup5 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
La creación de empleo se acelera en el inicio del verano: la afiliación sube en 115.000 trabajadores y el paro baja en 42.000 personas
Los grandes bancos españoles se centran en fidelizar a sus clientes ante el alza de los tipos de interés
Gobierno y Junta se comprometen a salvar las filiales de Abengoa que sean rentables
Auge y caída de Gamesa: un puntal de la industria vasca pasa a manos alemanas
Carlos Jiménez Villarejo: un hombre contra la desesperanza
IPC: de la negación al riesgo de sobrerreacción
Criptoactivos y protección del inversor
Texas es la nueva China para  Elon Musk
A Unilever se le indigesta el helado 
Alemania registra su primer déficit comercial desde 1991  
El gas duplica su precio en un mes y complica la temporada de llenado de depósitos en Europa
El Supremo compensa la cotización a madres solicitantes de subsidio por paro
Detenido un empresario de Alicante por ocultar el accidente laboral de un operario que trabajaba sin contrato 
El tranvía de Cádiz llega con diez años de retraso
El gasto de los turistas extranjeros se dispara hasta 8.023 millones en mayo y casi iguala el nivel prepandemia
La Audiencia rebaja de seis millones a 50.000 euros una multa de la CNMC a Telefónica
Belén Garijo (Merck): “El poder no me interesa. Mi objetivo es tener impacto”
Las Bolsas caen, la inflación arruina mis depósitos... y ahora, ¿qué hago yo con mis ahorros?
La inflación aprieta y a las familias no les salen las cuentas
La economía mundial se desinfla: así es la crisis que viene
La carrera por las oposiciones ha empezado: en juego hay 45.000 trabajos para toda la vida
Los jueces se ponen de parte de las víctimas de ‘phishing’ bancario
Texas es la nueva China para  Elon Musk
IPC: de la negación al riesgo de sobrerreacción
A Unilever se le indigesta el helado 
Créditos para comprar un coche: cuáles son las mejores ofertas de los bancos
Los expertos vaticinan el fin de la guerra en Ucrania aunque con cesiones territoriales
Telefónica dispara un 30% su área logística con el tirón del ‘ecommerce’ y los nuevos negocios
Meliá, Barceló, RIU y NH arrancan el verano con subidas de precios del 10%
Líos en la piscina comunitaria: normas y sentencias para un chapuzón seguro
Parir en casa, educarlo por mi cuenta… ¿Qué puedo decidir sobre mi hijo y qué no?
Saltarse un paso a nivel de camino a la oficina es accidente laboral
El futuro probable de una sociedad insostenible
Francisco Javier Blasco: “Llevamos años sin mejorar la eficacia de las políticas activas de empleo”
¿Es esta la edad dorada del emprendimiento universitario?
Cancerberos del bienestar de la empresa
Salud a golpe de clic con la cercanía del médico de cabecera
Cómo garantizar la seguridad en un mundo de amenazas híbridas
¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
Las aventuras de un par de calcetines que dan empleo a todo un pueblo
Cultura financiera como punto de partida para volver a empezar
Por qué digitalizar una pyme aporta más empleo
Logística a bajas temperaturas, la revolución que vino del frío
‘Coopetir’: la actitud DFactory
Así serán las ciudades de la (nueva) última milla
Cinco errores habituales al digitalizar un negocio 
PERTE Agroalimentario: ¿cómo acceder a los fondos europeos?
Fondos soberanos: ¿Cómo funcionan las cajas fuertes de los estados más ricos?
¿Crisis de deuda mundial a la vista?
El método Muñoz para triunfar en cada reto que se propone
Gloria Ramos, cuando el afán de superación acaba en la alfombra roja 
Hotmart y su plataforma 360 para creadores de contenidos
Una aplicación para presentar la declaración desde casa y conseguir los máximos beneficios
```

### Código

```
req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req6 que es utilizada por la variable soup6 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Mensaje de los hepatólogos para cuidar el hígado: tres días seguidos a la semana sin probar el alcohol (al menos)
Retrato del putero en España: “Vas, pasas un rato con los amigos, follas y para casa. Y no es carísimo”
La historia de Mika C., de un centro de menores hasta la universidad: “Creces sin referentes”
El control del cuerpo de las mujeres
No se gobierna con el catecismo romano
Un día muy triste para todas las mujeres
El Supremo de Estados Unidos destruye un derecho fundamental de las mujeres
La guerra contra el aborto en EE UU se libra Estado a Estado 
El caso de la artista Paula Bonet destapa a nuevas víctimas de su acosador
José Manuel Bar, secretario de Estado de Educación: “Los docentes de secundaria deben empezar a estudiar pedagogía en su carrera”
Las batallas del exmarine que sufrió abusos sexuales en un internado religioso en Zamora
La nueva ley impedirá que un sanitario esté más de tres años trabajando sin ser funcionario
Lombardía pide que se decrete el estado de emergencia en toda Italia por la sequía
Vacaciones, ola de covid y saturación en urgencias: la sanidad se enfrenta a un verano “desastroso y desalentador”
Los peores incendios forestales de España: cómo se están intensificando los monstruos de fuego
Tímidos avances en la minería submarina, las áreas protegidas o los corales: estos son los acuerdos de la Conferencia de los Océanos de Lisboa
El duelo de Parla por Cristina, asesinada por su expareja en vísperas de celebrar su 19º cumpleaños
Patricia Espinosa: “El cambio climático no se ve como la emergencia que es”
Se buscan profesionales en economía circular
La economía circular llega a la ciudad. Te contamos dónde se encuentra 
Mitos, falsedades, bulos y realidades sobre el VIH 40 años después
Educadores con VIH para minimizar el impacto tras el primer diagnóstico
Qué son las evidencias científicas y por qué están revolucionando la educación
Munic, el joven redimido por el trap
El tremendo peso de la obesidad en España
Interactivo | Los 14 cambios en los aeropuertos españoles que no ves y que ya están ocurriendo
Encontrar empleo pese a los obstáculos. Por dónde empezar la búsqueda
La fórmula de Carboneros para evitar el éxodo rural: trabajar cuidando a los vecinos 
Consejos y cuidados para el primer verano con un gatito o un perrito
¿Qué tienen en común perros y gatos cuando son cachorros?
La guía definitiva para alimentarnos mejor (y cuidar nuestra salud y la del planeta)
El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
La salud mental de los refugiados: cómo abrirse para cerrar las heridas
Yogures con menos azúcar, paso firme hacia la alimentación infantil del futuro
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Conectada con el mercado laboral y tecnológica: así es la universidad del presente
```

### Código

```
req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req7 que es utilizada por la variable soup7 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
José Manuel Bar, secretario de Estado de Educación: “Los docentes de secundaria deben empezar a estudiar pedagogía en su carrera”
Ayuso se apunta ahora el tanto de la bajada de tasas universitarias, pese a que las llevó a los tribunales para no reducirlas
Notas de Selectividad 2022 por comunidades: los aprobados rozan el 96%
Becas públicas en centros privados de Madrid para familias que ganan más de 100.000 euros
La oposición a Ayuso ve “un atraco” que familias que ganan 100.000 euros puedan lograr una beca
El control de las becas a las que optan incluso familias que ganan más de 100.000 euros está en manos de una empresa privada
El futuro probable de una sociedad insostenible
Una historia en la que caben Alaska, García Lorca, Suárez y Popper: la Universidad Internacional Menéndez Pelayo cumple 90 años 
La ONU alerta de una “crisis global de educación” de mayor magnitud de lo que calculaba
El caso del profesor que debe ir escoltado en la Universidad del País Vasco por el acoso de compañeros: “Tengo miedo de que me tiren por las escaleras”
El techo de cristal del grado medio de FP: candidatos demasiado preparados se quedan con los puestos
Sin currículos
La escuela concertada ante las desigualdades: el debate pendiente
La equidad frente a las políticas educativas de privatización en Andalucía
No hay lunes al sol en la Universidad
Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
Una fórmula para que la escuela pública compita mejor con la concertada
La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
El Ayuntamiento de Madrid guarda en un cajón una herramienta ya pagada para ver los datos de contaminación al detalle 
La implantación del nuevo Bachillerato general fracasa pese a su demanda potencial: “Creímos que lo pedirían seis alumnos y lo han hecho 27”
Toni Solano, director de instituto: “Veo mal a los niños, necesitan muchísima ayuda”
Niños, Administraciones y redes sociales: prohibir su uso con una mano y enseñar a crear contenidos con la otra
El Gobierno aprueba el decreto de bachillerato: los alumnos podrán terminar con un suspenso y desembocará en una nueva Selectividad
La ley del silencio dentro y fuera del aula
Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
Golpe a la temporalidad en las universidades: 25.000 profesores asociados serán indefinidos a tiempo parcial
Antonio Abril: “Yo le decía a Castells: ‘Tienes que aguantar la presión, tienes que hacer la reforma universitaria”
Los universitarios extranjeros podrán quedarse un año en España automáticamente al terminar la carrera
```
### Código

```
req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req8 que es utilizada por la variable soup8 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
El anticiclón de las Azores se está expandiendo e intensificando
Los peores incendios forestales de España: cómo se están intensificando los monstruos de fuego
Lombardía pide que se decrete el estado de emergencia en toda Italia por la sequía
Tímidos avances en la minería submarina, las áreas protegidas o los corales: estos son los acuerdos de la Conferencia de los Océanos de Lisboa
Golpe a la credibilidad internacional de EE UU en el reto climático
Patricia Espinosa: “El cambio climático no se ve como la emergencia que es”
El Tribunal Supremo socava la lucha de Estados Unidos contra el cambio climático
Los 500 cadáveres del ‘vampiro’ de perros
¿Por qué hace más calor ahora mismo en Escandinavia que en España?
El PSOE andaluz vira de posición sobre el aumento de regadíos en Doñana: de la abstención al “no absoluto”
Conservacionistas demuestran el uso de redes de pesca ilegales por parte de embarcaciones marroquíes en el Mediterráneo 
Crisis energética y precios del carbono
La lección del martín pescador para afrontar la crisis ecológica
Estocolmo+50: mirar atrás para tomar impulso
El verano ya no es lo que era 
Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
La UE abraza las renovables para romper la dependencia de Rusia
La lucha en un pueblo de Teruel para salvar su última montaña
¿Qué aire respiran los niños de Madrid y Barcelona? En el 46% de los colegios se supera la contaminación permitida
```

### Código

```
req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req9 que es utilizada por la variable soup9 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
El anticiclón de las Azores se está expandiendo e intensificando
Josep Maria Trigo, astrónomo: “Si se descubre que viene un cometa, da igual dónde nos resguardemos”
Bosón de Higgs: diez años del descubrimiento del siglo (hasta ahora)
Celos, suegras y uso de Tinder: el complicado emparejamiento de los monos entre zoos
Hallado en Egipto el fósil de un gran dinosaurio “con cara de bulldog” de hace 98 millones de años
Alrededor de la mesa
Cristóbal Blanco: “Los ajedrecistas desarrollan más una gran parte del cerebro”
Una inmunoterapia con virus obtiene resultados prometedores contra el cáncer más letal en niños
Molinos y gigantes, adelantos tecnológicos y el síndrome bicicleta
El festival Starmus celebra 50 años de exploración de Marte 
Los animales de sangre fría parece que no envejecen
“No tenemos otra opción que creer que podemos hacer lo necesario para que la humanidad sobreviva” 
¿Dónde hay civilizaciones extraterrestres?
Toreros, trenes voladores y ovaciones a Franco: las películas inéditas del ingeniero José Hernández Santorcuato
Las personas que comparten el mismo olor tienen más probabilidades de forjar una amistad
Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer
¿Dónde hay civilizaciones extraterrestres?
Matemáticas para describir los remolinos, los taxis del océano
Reaparece la tesis de María Wonenburger, la pionera matemática española que permaneció décadas en el olvido
Técnicas criptográficas que se fundamentan en lo impredecible
Las matemáticas de los juegos malabares
Fracciones egipcias
El problema del huerto
Números McNugget
Molinos y gigantes, adelantos tecnológicos y el síndrome bicicleta
El síndrome del hombre lobo y la realidad lógica de su fábula
La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
El andar del borracho, las huellas del azar y el juego de dados en algunos libros malditos
El campo vibratorio y las fronteras de la ciencia desde un punto de vista científico
¿Son mejores las hormonas bioidénticas?
¿Qué surgió antes, el ARN o el ADN?
¿Por qué se sabe que los núcleos de la Tierra rotan?
¿Qué son los mini reactores nucleares?
Invitados indeseables por Navidad: el muérdago y otras plagas que evitar durante las fiestas
Las ‘apps’ nutricionales o cómo comer bien no debería depender de uno mismo
Malnutrición invisible: el impacto de la pobreza en la salud infantil
El óxido de etileno, la sustancia cancerígena que ha obligado a retirar miles de alimentos en la UE
Que no te líen con los ingredientes: aceites y grasas de mala calidad nutricional
```
### Código

```
req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req10 que es utilizada por la variable soup10 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Peter Brook, el gran árbol del teatro
El fotógrafo que ayudó a que el Paisaje de la Luz de Madrid sea Patrimonio Mundial
El tremendo espectáculo de la desnudez
Un siglo de canciones, 1.500 artistas
Peter Brook, el gran árbol del teatro
Planes de señoras
Un horizonte sin límites en el parabrisas
Muere a los 97 años Peter Brook, el gigante del teatro de nuestro tiempo
La ‘Operación Triunfo’ del Cante de las Minas, el festival más importante de flamenco
Ron Carter, 85 años, todavía un coloso del contrabajo 
Muere el historiador Fernando García de Cortázar a los 79 años
El festival Grec de Barcelona vibra en su primer fin de semana con Israel Galván y Thomas Ostermeier 
Antony Beevor, historiador militar: “La guerra de Ucrania puede desatar una catástrofe global”
Adele vuelve a escena cinco años después en un concierto ante un público entregado
Residente reivindica la América que no es Estados Unidos en su regreso a Madrid
Susan Meiselas, una vida de fotógrafa entre la industria del sexo y las guerras de Centroamérica
Belle and Sebastian intensifican en Madrid su quimérica busca de la canción perfecta
Últimos cartuchos: nueva entrega de las crónicas de Emmanuel Carrère desde el juicio por los atentados de París
Colm Tóibín: “Las discusiones trans son tan intensas que la conversación sobre la homosexualidad en el pasado no interesa”
Cómo sobrevive un tranquilo pueblo gallego a la invasión de 140.000 ‘metaleros’
El último atardecer de Europa se ve solo desde este lugar. Un viaje hacia el infinito por el Camino de Fisterra-Muxía
Un paseo fluvial con museos y otro lleno de piscinas termales. Las sorpresas de la Vía de la Plata
Lorca, en la ciudad al margen
El Pirineo oscense, para entrar a vivir
Toda la lectura del verano, en el bolsillo
Libros que enganchan aún más que las series de televisión que los adaptan
Harry Potter cumple 25 años: libros para revivir la magia de Hogwarts
Disfruta de 'Los paseos musicales del Real Jardín Botánico'
Sistema Europe Youth Orchestra
Preestreno de 'Entre la vida y la muerte'
El Ballet de Kiev en Madrid y Barcelona
Aroma de buen toreo
Ángel Téllez, la única novedad de las Corridas Generales de Bilbao
La feria de Albacete apuesta por los toreros manchegos
El Instituto Juan Belmonte celebrará un curso de verano en la Universidad Rey Juan Carlos sobre tauromaquia y animalismo
```

### Código

```
req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req11 que es utilizada por la variable soup11 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Los primeros poemas de Severo Sarduy, una joya inédita
Libros para el verano: 80 novedades recomendadas para estas vacaciones
Rigoberta Bandini, Jordi Évole, Rosa Montero, Juan Diego Botto, Albert Serra y otros nombres de la cultura proponen sus lecturas estivales
‘The Murder of Crows’: por qué el arte sonoro es más poderoso que el visual
El regreso de Perrate: fiesta, linaje y ocho gozosos minutos de bulerías
Raíces y alas del flamenco: seis discos entre tradición y evolución
Tres veces Calderón: variaciones sobre la tortura en una obra sugestiva e imaginativa
Diego Luna, un actor magnético para una obra mediocre
Trampantojo: Planazo
Lo nuevo de Gorillaz, Pixies, Beyoncé, Christina Rosenvinge, Drake y otras canciones de junio
‘Eppur si muove’: el avance imparable de los videojuegos
No eran marcianos, eran humanos
El desafío de Frida Kahlo
Lo que siento (no se olviden de Ucrania) 
Otros turismos (lejos y aquí cerca)
‘Horas muertas’, en un Dublín hipnótico
‘Prometeo’, trío de ases
‘La memoria del alambre’, ese algo misterioso que daba miedo
‘Tarradellas. Una cierta idea de Cataluña’: manual de resistencia
Antoni Muntadas: “Supe que me dedicaría al arte cuando dejé de pintar”
Manuel Estrada: “Me agrada que una portada guste más después de leer el libro”
Óscar Esquivias: “No hace falta ser creyente para leer la Biblia”
Amelia Castilla: “Los ritos nos ayudan a hacer viable el trance de la muerte”
Shuarma: “Me gusta de la poesía el silencio que encierra”
```

### Código

```
req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req12 que es utilizada por la variable soup12 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Nadal se reafirma hacia Fritz
Halep, un mal trago para Paula Badosa
Nunca hay paz para Ferrari: “¡Dejad de inventar, chicos!”
Aquí Pablo Laso, aquí su obra
La culpa fue de Tsitsipas
Wimbledon, el aroma británico de la tradición
Fútbol moderno, prohibido pensar
El Real Madrid aparta a Pablo Laso del banquillo
Niepómniashi, un retador tan fuerte como inestable
El Barcelona oficializa los fichajes de Kessié y Christensen
Rodrygo amplía su contrato con el Madrid hasta 2028 y entra en el club de los 1.000 millones de cláusula
España se proclama campeona del mundo de waterpolo en una final agónica 
Solo y sin oxígeno artificial en la cima del Everest: cada paso es una agonía   
Sinner aborta la rebelión tardía de Alcaraz
Sainz: “No dejé de creer, a la espera de algo que finalmente pasó”
Argentina es demasiado para España
Y una florentina para ordenar a tantos hombres en el Tour
La selección femenina de fútbol sala vuelve a conquistar Europa
El Torneo de Candidatos de ajedrez de Madrid
Cuando Linares era el Wimbledon del ajedrez
“La pasión que genera el fútbol es inigualable”
“Nunca acepto un no por respuesta”
La mayor fábrica de baloncesto de Europa
Crónica de dos ciudades moldeadas por la misma pasión 
Amarillo Tour
Alcaraz se despide de Wimbledon tras caer ante Sinner (6-1, 6-4, 6-7, 6-3)
Victoria y catarsis de Dylan Groenewegen en la tercera etapa del Tour de Francia
La victoria de Carlos Sainz, en imágenes
Sainz: “No dejé de creer, a la espera de algo que finalmente pasó”
Judit fulmina a Carlsen
Carlsen negocia si renuncia al título o lo defiende en 2023 contra Niepómniashi
Carlos Sainz gana en Silverstone su primera carrera de Fórmula 1 
```
### Código

```
req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req13 que es utilizada por la variable soup13 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
Regina Barzilay: “Tenemos que aprender a vivir en un mundo en el que la tecnología toma decisiones que no podemos supervisar”
Herramientas y trucos para recordar la ubicación del coche gracias al móvil
Las tres amigas que quieren revolucionar los materiales de construcción con fibras de hongos
El Constitucional afianza el derecho al olvido en internet
Dall-E, el popular generador automático de imágenes que hace dibujos sexistas y racistas 
Por qué el algoritmo de Google no es una persona
Comunidades de energía: una fórmula barata, limpia y segura
“Queremos que la programación sea el inglés del siglo XXI”
Imágenes sexuales que destruyen y matan
Tres cosas que hacemos mal con el teléfono móvil (y no sirven para nada)
Christopher Mims: “Amazon sabe cómo bajar el ritmo de trabajo para prevenir lesiones. Pero quizá dejaría de ganar dinero” 
¿Sigue siendo imprescindible tener un antivirus? 
Google News vuelve a España ocho años después de su cierre
Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
Instagram, el mejor de los mundos posibles
Del terrorismo youtuber al influencer rabioso: el odio inunda la red
Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
Cinco razones por las que este ‘smartphone’ es sencillamente tentador
La cámara de este ‘smartphone’ es pura magia
Por qué los nuevos coches ya no los diseñarán las personas
Una catapulta para el talento de ‘kilómetro cero’
```

### Código

```
req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2.Este ciclo imprime:

```
Regina Barzilay: “Tenemos que aprender a vivir en un mundo en el que la tecnología toma decisiones que no podemos supervisar”
Herramientas y trucos para recordar la ubicación del coche gracias al móvil
Las tres amigas que quieren revolucionar los materiales de construcción con fibras de hongos
El Constitucional afianza el derecho al olvido en internet
Dall-E, el popular generador automático de imágenes que hace dibujos sexistas y racistas 
Por qué el algoritmo de Google no es una persona
Comunidades de energía: una fórmula barata, limpia y segura
“Queremos que la programación sea el inglés del siglo XXI”
Imágenes sexuales que destruyen y matan
Tres cosas que hacemos mal con el teléfono móvil (y no sirven para nada)
Christopher Mims: “Amazon sabe cómo bajar el ritmo de trabajo para prevenir lesiones. Pero quizá dejaría de ganar dinero” 
¿Sigue siendo imprescindible tener un antivirus? 
Google News vuelve a España ocho años después de su cierre
Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
Instagram, el mejor de los mundos posibles
Del terrorismo youtuber al influencer rabioso: el odio inunda la red
Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
Cinco razones por las que este ‘smartphone’ es sencillamente tentador
La cámara de este ‘smartphone’ es pura magia
Por qué los nuevos coches ya no los diseñarán las personas
Una catapulta para el talento de ‘kilómetro cero’
```

### Código

```
req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req15 que es utilizada por la variable soup15 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
En un mundo inestable y pospandémico, ¿para qué sirve la moda?
Los premios Princesa de Girona, en imágenes
‘Fiebre del sábado noche’ en tu salón: el curioso caso de las bolas de discoteca en la decoración del hogar
Britney Spears acusa a sus exgerentes de haberse apropiado de 17 millones de euros de su patrimonio durante la tutela
En el corazón del surrealismo: Leonor y Sofía visitan el Museo de Dalí en su primer acto solitario en Cataluña
Shakira cambia de estrategia para evitar el juicio por fraude fiscal tras separarse de Gerard Piqué
Emitida una orden de alejamiento contra Ricky Martin por violencia doméstica 
Rocío Jurado ya tiene su templo en Chipiona
La última exnovia de Berlusconi se casa con una cantante italiana
Juanes: “Me siento maduro, interesante y seguro, y eso me encanta”
Tom Cruise cumple 60 años: una celebración de su vida y su carrera en 12 fotos  
Cómo Julia Fox, actriz de una sola película, dominatrix y ‘obra maestra’ de internet, se convirtió en meme (e icono) de la generación TikTok
Lindsay Lohan se casa en una boda secreta
Entre Sevilla, Ascot, el pasado y el futuro: Mans condensa su universo en una colección sin miedo a los contrastes
La colección de Palomo Spain para Correos: cómo la moda unió a una empresa centenaria y a otra rabiosamente joven
Archie Alled-Martínez, el barcelonés que continúa el legado de Lagerfeld: “No hace falta llevar un arco iris para ser tú mismo”
Victorio & Lucchino, 40 años de moda en su museo de Córdoba, en imágenes
Vídeo | Eugenia Silva: “El estilismo de Britney Spears no hay por dónde cogerlo”
Trece aperitivos
Vende menos comer que correr
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
Breve guía de los mejores vinos blancos italianos para descubrir este verano
```

### Código

```
req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req16 que es utilizada por la variable soup16 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
¿Quién demonios votó a Podemos en La Moraleja?
La voz de los más inocentes
Las actrices de ‘Intimidad’: “Si una mujer no es complaciente en esta profesión, llegan las amenazas”
Publicidad convertida en lírica y humanismo 
La voz de los más inocentes
‘Mi vida con 300 kilos’: un diamante entre la mierda
¿Hay demasiadas series a la vez?
Crecer dentro del fenómeno global ‘Stranger Things’: “Lo llevamos bien, con terapia”
La televisión también quiere ser verde: cómo ‘Servir y proteger’ disminuyó la contaminación en su rodaje
Las 10 mejores series sobre intrigas políticas para ver después de la cumbre de la OTAN 
Por qué los bisexuales, el colectivo no heterosexual más numeroso de España, siguen siendo invisibles en televisión
La ‘venganza’ de William Levy: “De joven, en Cuba, viví demasiadas injusticias”
Qué ver en televisión para celebrar el Orgullo LGTBI+ 2022
La ilustradora española que se asoma a las ventanas de Nueva York en ‘Solo asesinatos en el edificio’
24 series para este verano
Muere la actriz Mary Mara (’Urgencias’ y ‘Ray Donovan’) ahogada en un río de Nueva York
‘La clave’ de Balbín, gloria y caída del programa que cambió la televisión española
¿Qué ver hoy en TV? Lunes 4 de julio de 2022
Nueve capítulos para recordar ‘The Wire’ en su 20º aniversario
Harry Palmer: el tercer vértice del mágico triángulo de espías británicos
Las series de junio de 2022: ‘The Boys’ en Amazon Prime Video; ‘Peaky Blinders’ en Netflix y otras
La fuerza acompaña a ‘Obi-Wan Kenobi’, una serie deslumbrante
```

### Código

```
req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```
En esta sección se tiene un ciclo utilizando for donde si h2 está dentro de la variable tags, entonces genera una impresión de una cadena de etiquetas y se agrega a la cadena el resultado de esas etiquetas de tipo h2. En este caso se utiliza una URL distinta definida en req17 que es utilizada por la variable soup17 donde permite  evidenciar el cambio en la variable tags. Este ciclo imprime:

```
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
En busca de la huella de Camarón de la Isla, leyenda viva del flamenco
República Dominicana, donde la vida fluye por el río infinito
Oliviero Toscani: “El fascismo resulta muy cómodo porque no te exige razonar”
La importancia del respeto para sentirnos bien
El placer de lo rancio y otros gustos y aromas que recuerdan la niñez
Un misterio en el Real Madrid y un fantasma en Gales: ¿quién diablos es Gareth Bale?
España entra en la ruta del lujo mundial: fiestas, palacios y joyas valoradas en millones de euros
Así es el barrio de Pekín donde hay “robotaxi” y la compra llega en vehículo sin conductor
Saborear el momento
Lorena Jaume-Palasí: “Crear principios éticos universales para  la inteligencia artificial es una iniciativa cosmética”
Así es el primer campo de golf de España convertido en una reserva natural
Aprendizaje continuo para un mundo en cambio
Los coches más vendidos en la primera mitad de 2022
La palabra médico
El cuerpo
Cuento de Catherine del Biombo 5
Vende menos comer que correr
Harina enriquecida para acabar con el “hambre oculta”
Lugares de esperanza para salvar los océanos
Los guardianes del clima que llevan medio siglo leyendo las advertencias de los glaciares
Epidemia de violencia: claves del negocio de las armas en Estados Unidos
Los ejecutivos voladores y la ética medioambiental
Ibiza, entre la noche desenfrenada y el turismo tranquilo 
Luz Casal: “Tengo el alma rockera. Nada ha doblegado mi rebeldía”
Rashid Johnson: “Los pensadores y creadores negros estamos cansados de que nos nieguen un espacio autónomo”
Sergio Hernández: “En el mundo, la gente ya no quiere verdades, quiere mentiras”
Elvira Sastre: “No hay que perdonarlo todo”
La trinidad del taco perfecto: “Buena tortilla, delicioso relleno y una salsa sabrosa”
La casa de Nina Urgell Cloquell, un piso en el que las paredes hablan
Garbanzos verdes y puchero
Bikôkô y Julio Peña, dos estrellas en ebullición  
Cuando Chufy encontró a Rossy: dos amigas, una isla y una colección de moda
Retrato Robot 
Ilusiones hipnóticas
El poder del hormigón
Maulévrier, Japón a la francesa
‘Fantasías en el Prado’, por Alberto García-Alix
```
### Adicional
#### Código

```
os.system("clear")
```

Esta línea se utiliza para limpiar la pantalla a medida que va pasando por los ciclos mencionados anteriormente, todo esto es gracias a el import os de Python

## Excepciones
### Código

```
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
```
Esta excepción utiliza un condicional donde dependiendo el estado de las variables req, ya sea 1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16 o 17 si no es igual a 200 se generará una excepción ya que se toma como fuera del código de estado de respuesta en HTTP; por lo tanto, se mostrará en pantalla "No se puede hacer Web Scraping en" la URL asignada por cada variable req. Esta excepción se encuentra dentro de cada ciclo ya que si se sale del código no se permite realizar ninguna operación.

## Impresiones
### Código

```
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))
```
Para realizar las impresiones se utiliza la función print, donde se llama una función de la librería termcolor la función colored que permite imprimir el texto de color azul enviandole por parametro 'blue' y además que el texto se muestre en negrilla por medio de attrs=['bold']. Imprime también la palabra Feminismo en color verde por medio del parametro 'green'

### Código

```
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
print(colored("Igualdad", 'green', attrs=['bold']))
```
Imprime la palabra Igualdad en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']


### Código

```
str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))
print(colored("Mujeres", 'green', attrs=['bold']))
```
Imprime la palabra Mujeres en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']


### Código

```
str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

```
Imprime la palabra Mujer en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

```
Imprime la palabra Brecha salarial en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

```
Imprime la palabra Machismo en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))
```
Imprime la palabra Violencia en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))
```
Imprime la palabra Maltrato en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))
```
Imprime la palabra Homicidio en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))
```
Imprime la palabra Género en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))
```
Imprime la palabra Asesisnato en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']

### Código

```
str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))

```
Imprime la palabra Sexo en color verde por medio del parametro 'green' y el texto en negrilla por medio de attrs=['bold']. 
Termina también la lista de impresiones

## Impresión final

En esta sección se mostrará la impresión final con la ejecución del código completo. Teniendo en cuenta uqe evidentemente en la terminal de Spyder que es el programa que se utilizó a lo largo de esta actividad si se imprime el texto con los colores correspondientes por cada impresión y además, la negrilla añadida al texto a lo largo del código

```
Flavita Banana
Riki Blanco
Sciammarella
Planeta de Plástico, por Malagón
Envía tu carta
Salud y mentiras
Reconocimiento al Gobierno
Jóvenes brillantes, educación pública y poder 
En la calle circulan rumores
Opinar sin insultar
Contra el conflicto de intereses, transparencia
El defensor del lector contesta
Una memoria democrática más inclusiva y plural
Trump, al desnudo
Ese cuerpo
El Tribunal Constitucional: entre el Derecho y el no Derecho
‘Mi casa, mi árbol’
Hambre: las muertes que sí podemos evitar
Gobiernos rojos y glóbulos blancos
Vulnerables
Si son negros, vienen a delinquir 
Selenita
Santa Bárbara y la cultura de la defensa
El mundo que viene
Las humanidades lo petan
El Roto
Peridis
Flavita Banana
Riki Blanco
Sciammarella
Planeta de Plástico, por Malagón
Envía tu carta
Salud y mentiras
Reconocimiento al Gobierno
Jóvenes brillantes, educación pública y poder 
En la calle circulan rumores
Opinar sin insultar
Contra el conflicto de intereses, transparencia
El defensor del lector contesta
Sánchez acelera y aprueba este martes un crédito extra de 1.000 millones en Defensa pese a las críticas de Podemos
El PP desplaza al PSOE del primer puesto tras las elecciones andaluzas
“Esto es una tortura psicológica”
¿Es posible disentir de esta retórica belicista?
Los trajes del presidente Sánchez
Panegírico del voto
Perder el sentido de la oportunidad
La búsqueda de seguridad vence al cabreo
Solo uno de cada cuatro españoles valora las medidas del Gobierno
Bruselas considera “inaceptable” la muerte de personas en la frontera de Melilla 
ERC se mueve a la abstención para seguir negociando la Ley de Memoria Democrática
El Gobierno acusa al PP de ejercer una estrategia “de conspiración” y “trumpista”
Consulte todos los datos internos de la encuesta de EL PAÍS de julio: cuestionarios, cruces y respuestas
Un niño de siete años, grave tras intoxicarse por una fuga de cloro en la piscina de un hotel de Mallorca
Drones submarinos para el narco ‘made in Cádiz’
Feijóo se sentará en el escaño del jefe de la oposición para buscar el foco en el debate sobre el estado de la nación
El conductor que desencadenó el accidente múltiple de Granada asegura que se le cruzó un animal
El Tribunal Superior catalán plantea llevar al Constitucional la ley del Govern que rechaza fijar el 25% del castellano en las aulas
El tiempo de la semana: de las tormentas al calor intenso y generalizado
Un paraíso en el que avistar más de 20 especies de cetáceos
El secreto de Fuerteventura se hace viral: la ‘playa de las palomitas’
Un vino para triunfar entre los mileniales
Artesanía y cultura que conquista a las ‘influencers’
Más allá de la capital. El triunfo de la vida rural madrileña
La creación de empleo se acelera en el inicio del verano: la afiliación sube en 115.000 trabajadores y el paro baja en 42.000 personas
Los grandes bancos españoles se centran en fidelizar a sus clientes ante el alza de los tipos de interés
Gobierno y Junta se comprometen a salvar las filiales de Abengoa que sean rentables
Auge y caída de Gamesa: un puntal de la industria vasca pasa a manos alemanas
Carlos Jiménez Villarejo: un hombre contra la desesperanza
IPC: de la negación al riesgo de sobrerreacción
Criptoactivos y protección del inversor
Texas es la nueva China para  Elon Musk
A Unilever se le indigesta el helado 
Alemania registra su primer déficit comercial desde 1991  
El gas duplica su precio en un mes y complica la temporada de llenado de depósitos en Europa
El Supremo compensa la cotización a madres solicitantes de subsidio por paro
Detenido un empresario de Alicante por ocultar el accidente laboral de un operario que trabajaba sin contrato 
El tranvía de Cádiz llega con diez años de retraso
El gasto de los turistas extranjeros se dispara hasta 8.023 millones en mayo y casi iguala el nivel prepandemia
La Audiencia rebaja de seis millones a 50.000 euros una multa de la CNMC a Telefónica
Belén Garijo (Merck): “El poder no me interesa. Mi objetivo es tener impacto”
Las Bolsas caen, la inflación arruina mis depósitos... y ahora, ¿qué hago yo con mis ahorros?
La inflación aprieta y a las familias no les salen las cuentas
La economía mundial se desinfla: así es la crisis que viene
La carrera por las oposiciones ha empezado: en juego hay 45.000 trabajos para toda la vida
Los jueces se ponen de parte de las víctimas de ‘phishing’ bancario
Texas es la nueva China para  Elon Musk
IPC: de la negación al riesgo de sobrerreacción
A Unilever se le indigesta el helado 
Créditos para comprar un coche: cuáles son las mejores ofertas de los bancos
Los expertos vaticinan el fin de la guerra en Ucrania aunque con cesiones territoriales
Telefónica dispara un 30% su área logística con el tirón del ‘ecommerce’ y los nuevos negocios
Meliá, Barceló, RIU y NH arrancan el verano con subidas de precios del 10%
Líos en la piscina comunitaria: normas y sentencias para un chapuzón seguro
Parir en casa, educarlo por mi cuenta… ¿Qué puedo decidir sobre mi hijo y qué no?
Saltarse un paso a nivel de camino a la oficina es accidente laboral
El futuro probable de una sociedad insostenible
Francisco Javier Blasco: “Llevamos años sin mejorar la eficacia de las políticas activas de empleo”
¿Es esta la edad dorada del emprendimiento universitario?
Cancerberos del bienestar de la empresa
Salud a golpe de clic con la cercanía del médico de cabecera
Cómo garantizar la seguridad en un mundo de amenazas híbridas
¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
Las aventuras de un par de calcetines que dan empleo a todo un pueblo
Cultura financiera como punto de partida para volver a empezar
Por qué digitalizar una pyme aporta más empleo
Logística a bajas temperaturas, la revolución que vino del frío
‘Coopetir’: la actitud DFactory
Así serán las ciudades de la (nueva) última milla
Cinco errores habituales al digitalizar un negocio 
PERTE Agroalimentario: ¿cómo acceder a los fondos europeos?
Fondos soberanos: ¿Cómo funcionan las cajas fuertes de los estados más ricos?
¿Crisis de deuda mundial a la vista?
El método Muñoz para triunfar en cada reto que se propone
Gloria Ramos, cuando el afán de superación acaba en la alfombra roja 
Hotmart y su plataforma 360 para creadores de contenidos
Una aplicación para presentar la declaración desde casa y conseguir los máximos beneficios
Mensaje de los hepatólogos para cuidar el hígado: tres días seguidos a la semana sin probar el alcohol (al menos)
Retrato del putero en España: “Vas, pasas un rato con los amigos, follas y para casa. Y no es carísimo”
La historia de Mika C., de un centro de menores hasta la universidad: “Creces sin referentes”
El control del cuerpo de las mujeres
No se gobierna con el catecismo romano
Un día muy triste para todas las mujeres
El Supremo de Estados Unidos destruye un derecho fundamental de las mujeres
La guerra contra el aborto en EE UU se libra Estado a Estado 
El caso de la artista Paula Bonet destapa a nuevas víctimas de su acosador
José Manuel Bar, secretario de Estado de Educación: “Los docentes de secundaria deben empezar a estudiar pedagogía en su carrera”
Las batallas del exmarine que sufrió abusos sexuales en un internado religioso en Zamora
La nueva ley impedirá que un sanitario esté más de tres años trabajando sin ser funcionario
Lombardía pide que se decrete el estado de emergencia en toda Italia por la sequía
Vacaciones, ola de covid y saturación en urgencias: la sanidad se enfrenta a un verano “desastroso y desalentador”
Los peores incendios forestales de España: cómo se están intensificando los monstruos de fuego
Tímidos avances en la minería submarina, las áreas protegidas o los corales: estos son los acuerdos de la Conferencia de los Océanos de Lisboa
El duelo de Parla por Cristina, asesinada por su expareja en vísperas de celebrar su 19º cumpleaños
Patricia Espinosa: “El cambio climático no se ve como la emergencia que es”
Se buscan profesionales en economía circular
La economía circular llega a la ciudad. Te contamos dónde se encuentra 
Mitos, falsedades, bulos y realidades sobre el VIH 40 años después
Educadores con VIH para minimizar el impacto tras el primer diagnóstico
Qué son las evidencias científicas y por qué están revolucionando la educación
Munic, el joven redimido por el trap
El tremendo peso de la obesidad en España
Interactivo | Los 14 cambios en los aeropuertos españoles que no ves y que ya están ocurriendo
Encontrar empleo pese a los obstáculos. Por dónde empezar la búsqueda
La fórmula de Carboneros para evitar el éxodo rural: trabajar cuidando a los vecinos 
Consejos y cuidados para el primer verano con un gatito o un perrito
¿Qué tienen en común perros y gatos cuando son cachorros?
La guía definitiva para alimentarnos mejor (y cuidar nuestra salud y la del planeta)
El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
La salud mental de los refugiados: cómo abrirse para cerrar las heridas
Yogures con menos azúcar, paso firme hacia la alimentación infantil del futuro
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Conectada con el mercado laboral y tecnológica: así es la universidad del presente
José Manuel Bar, secretario de Estado de Educación: “Los docentes de secundaria deben empezar a estudiar pedagogía en su carrera”
Ayuso se apunta ahora el tanto de la bajada de tasas universitarias, pese a que las llevó a los tribunales para no reducirlas
Notas de Selectividad 2022 por comunidades: los aprobados rozan el 96%
Becas públicas en centros privados de Madrid para familias que ganan más de 100.000 euros
La oposición a Ayuso ve “un atraco” que familias que ganan 100.000 euros puedan lograr una beca
El control de las becas a las que optan incluso familias que ganan más de 100.000 euros está en manos de una empresa privada
El futuro probable de una sociedad insostenible
Una historia en la que caben Alaska, García Lorca, Suárez y Popper: la Universidad Internacional Menéndez Pelayo cumple 90 años 
La ONU alerta de una “crisis global de educación” de mayor magnitud de lo que calculaba
El caso del profesor que debe ir escoltado en la Universidad del País Vasco por el acoso de compañeros: “Tengo miedo de que me tiren por las escaleras”
El techo de cristal del grado medio de FP: candidatos demasiado preparados se quedan con los puestos
Sin currículos
La escuela concertada ante las desigualdades: el debate pendiente
La equidad frente a las políticas educativas de privatización en Andalucía
No hay lunes al sol en la Universidad
Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
Una fórmula para que la escuela pública compita mejor con la concertada
La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
El Ayuntamiento de Madrid guarda en un cajón una herramienta ya pagada para ver los datos de contaminación al detalle 
La implantación del nuevo Bachillerato general fracasa pese a su demanda potencial: “Creímos que lo pedirían seis alumnos y lo han hecho 27”
Toni Solano, director de instituto: “Veo mal a los niños, necesitan muchísima ayuda”
Niños, Administraciones y redes sociales: prohibir su uso con una mano y enseñar a crear contenidos con la otra
El Gobierno aprueba el decreto de bachillerato: los alumnos podrán terminar con un suspenso y desembocará en una nueva Selectividad
La ley del silencio dentro y fuera del aula
Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
Golpe a la temporalidad en las universidades: 25.000 profesores asociados serán indefinidos a tiempo parcial
Antonio Abril: “Yo le decía a Castells: ‘Tienes que aguantar la presión, tienes que hacer la reforma universitaria”
Los universitarios extranjeros podrán quedarse un año en España automáticamente al terminar la carrera
El anticiclón de las Azores se está expandiendo e intensificando
Los peores incendios forestales de España: cómo se están intensificando los monstruos de fuego
Lombardía pide que se decrete el estado de emergencia en toda Italia por la sequía
Tímidos avances en la minería submarina, las áreas protegidas o los corales: estos son los acuerdos de la Conferencia de los Océanos de Lisboa
Golpe a la credibilidad internacional de EE UU en el reto climático
Patricia Espinosa: “El cambio climático no se ve como la emergencia que es”
El Tribunal Supremo socava la lucha de Estados Unidos contra el cambio climático
Los 500 cadáveres del ‘vampiro’ de perros
¿Por qué hace más calor ahora mismo en Escandinavia que en España?
El PSOE andaluz vira de posición sobre el aumento de regadíos en Doñana: de la abstención al “no absoluto”
Conservacionistas demuestran el uso de redes de pesca ilegales por parte de embarcaciones marroquíes en el Mediterráneo 
Crisis energética y precios del carbono
La lección del martín pescador para afrontar la crisis ecológica
Estocolmo+50: mirar atrás para tomar impulso
El verano ya no es lo que era 
Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
La UE abraza las renovables para romper la dependencia de Rusia
La lucha en un pueblo de Teruel para salvar su última montaña
¿Qué aire respiran los niños de Madrid y Barcelona? En el 46% de los colegios se supera la contaminación permitida
El anticiclón de las Azores se está expandiendo e intensificando
Josep Maria Trigo, astrónomo: “Si se descubre que viene un cometa, da igual dónde nos resguardemos”
Bosón de Higgs: diez años del descubrimiento del siglo (hasta ahora)
Celos, suegras y uso de Tinder: el complicado emparejamiento de los monos entre zoos
Hallado en Egipto el fósil de un gran dinosaurio “con cara de bulldog” de hace 98 millones de años
Alrededor de la mesa
Cristóbal Blanco: “Los ajedrecistas desarrollan más una gran parte del cerebro”
Una inmunoterapia con virus obtiene resultados prometedores contra el cáncer más letal en niños
Molinos y gigantes, adelantos tecnológicos y el síndrome bicicleta
El festival Starmus celebra 50 años de exploración de Marte 
Los animales de sangre fría parece que no envejecen
“No tenemos otra opción que creer que podemos hacer lo necesario para que la humanidad sobreviva” 
¿Dónde hay civilizaciones extraterrestres?
Toreros, trenes voladores y ovaciones a Franco: las películas inéditas del ingeniero José Hernández Santorcuato
Las personas que comparten el mismo olor tienen más probabilidades de forjar una amistad
Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer
¿Dónde hay civilizaciones extraterrestres?
Matemáticas para describir los remolinos, los taxis del océano
Reaparece la tesis de María Wonenburger, la pionera matemática española que permaneció décadas en el olvido
Técnicas criptográficas que se fundamentan en lo impredecible
Las matemáticas de los juegos malabares
Fracciones egipcias
El problema del huerto
Números McNugget
Molinos y gigantes, adelantos tecnológicos y el síndrome bicicleta
El síndrome del hombre lobo y la realidad lógica de su fábula
La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
El andar del borracho, las huellas del azar y el juego de dados en algunos libros malditos
El campo vibratorio y las fronteras de la ciencia desde un punto de vista científico
¿Son mejores las hormonas bioidénticas?
¿Qué surgió antes, el ARN o el ADN?
¿Por qué se sabe que los núcleos de la Tierra rotan?
¿Qué son los mini reactores nucleares?
Invitados indeseables por Navidad: el muérdago y otras plagas que evitar durante las fiestas
Las ‘apps’ nutricionales o cómo comer bien no debería depender de uno mismo
Malnutrición invisible: el impacto de la pobreza en la salud infantil
El óxido de etileno, la sustancia cancerígena que ha obligado a retirar miles de alimentos en la UE
Que no te líen con los ingredientes: aceites y grasas de mala calidad nutricional
Peter Brook, el gran árbol del teatro
El fotógrafo que ayudó a que el Paisaje de la Luz de Madrid sea Patrimonio Mundial
El tremendo espectáculo de la desnudez
Peter Brook, el gran árbol del teatro
Un siglo de canciones, 1.500 artistas
Planes de señoras
Un horizonte sin límites en el parabrisas
Muere a los 97 años Peter Brook, el gigante del teatro de nuestro tiempo
La ‘Operación Triunfo’ del Cante de las Minas, el festival más importante de flamenco
Ron Carter, 85 años, todavía un coloso del contrabajo 
Muere el historiador Fernando García de Cortázar a los 79 años
El festival Grec de Barcelona vibra en su primer fin de semana con Israel Galván y Thomas Ostermeier 
Antony Beevor, historiador militar: “La guerra de Ucrania puede desatar una catástrofe global”
Adele vuelve a escena cinco años después en un concierto ante un público entregado
Residente reivindica la América que no es Estados Unidos en su regreso a Madrid
Susan Meiselas, una vida de fotógrafa entre la industria del sexo y las guerras de Centroamérica
Belle and Sebastian intensifican en Madrid su quimérica busca de la canción perfecta
Últimos cartuchos: nueva entrega de las crónicas de Emmanuel Carrère desde el juicio por los atentados de París
Colm Tóibín: “Las discusiones trans son tan intensas que la conversación sobre la homosexualidad en el pasado no interesa”
Cómo sobrevive un tranquilo pueblo gallego a la invasión de 140.000 ‘metaleros’
El último atardecer de Europa se ve solo desde este lugar. Un viaje hacia el infinito por el Camino de Fisterra-Muxía
Un paseo fluvial con museos y otro lleno de piscinas termales. Las sorpresas de la Vía de la Plata
Lorca, en la ciudad al margen
El Pirineo oscense, para entrar a vivir
Toda la lectura del verano, en el bolsillo
Libros que enganchan aún más que las series de televisión que los adaptan
Harry Potter cumple 25 años: libros para revivir la magia de Hogwarts
Disfruta de 'Los paseos musicales del Real Jardín Botánico'
Sistema Europe Youth Orchestra
Preestreno de 'Entre la vida y la muerte'
El Ballet de Kiev en Madrid y Barcelona
Aroma de buen toreo
Ángel Téllez, la única novedad de las Corridas Generales de Bilbao
La feria de Albacete apuesta por los toreros manchegos
El Instituto Juan Belmonte celebrará un curso de verano en la Universidad Rey Juan Carlos sobre tauromaquia y animalismo
Los primeros poemas de Severo Sarduy, una joya inédita
Libros para el verano: 80 novedades recomendadas para estas vacaciones
Rigoberta Bandini, Jordi Évole, Rosa Montero, Juan Diego Botto, Albert Serra y otros nombres de la cultura proponen sus lecturas estivales
‘The Murder of Crows’: por qué el arte sonoro es más poderoso que el visual
El regreso de Perrate: fiesta, linaje y ocho gozosos minutos de bulerías
Raíces y alas del flamenco: seis discos entre tradición y evolución
Tres veces Calderón: variaciones sobre la tortura en una obra sugestiva e imaginativa
Diego Luna, un actor magnético para una obra mediocre
Trampantojo: Planazo
Lo nuevo de Gorillaz, Pixies, Beyoncé, Christina Rosenvinge, Drake y otras canciones de junio
‘Eppur si muove’: el avance imparable de los videojuegos
No eran marcianos, eran humanos
El desafío de Frida Kahlo
Lo que siento (no se olviden de Ucrania) 
Otros turismos (lejos y aquí cerca)
‘Horas muertas’, en un Dublín hipnótico
‘Prometeo’, trío de ases
‘La memoria del alambre’, ese algo misterioso que daba miedo
‘Tarradellas. Una cierta idea de Cataluña’: manual de resistencia
Antoni Muntadas: “Supe que me dedicaría al arte cuando dejé de pintar”
Manuel Estrada: “Me agrada que una portada guste más después de leer el libro”
Óscar Esquivias: “No hace falta ser creyente para leer la Biblia”
Amelia Castilla: “Los ritos nos ayudan a hacer viable el trance de la muerte”
Shuarma: “Me gusta de la poesía el silencio que encierra”
Nadal se reafirma hacia Fritz
Halep, un mal trago para Paula Badosa
Nunca hay paz para Ferrari: “¡Dejad de inventar, chicos!”
Aquí Pablo Laso, aquí su obra
La culpa fue de Tsitsipas
Wimbledon, el aroma británico de la tradición
Fútbol moderno, prohibido pensar
El Real Madrid aparta a Pablo Laso del banquillo
Niepómniashi, un retador tan fuerte como inestable
El Barcelona oficializa los fichajes de Kessié y Christensen
Rodrygo amplía su contrato con el Madrid hasta 2028 y entra en el club de los 1.000 millones de cláusula
España se proclama campeona del mundo de waterpolo en una final agónica 
Solo y sin oxígeno artificial en la cima del Everest: cada paso es una agonía   
Sinner aborta la rebelión tardía de Alcaraz
Sainz: “No dejé de creer, a la espera de algo que finalmente pasó”
Argentina es demasiado para España
Y una florentina para ordenar a tantos hombres en el Tour
La selección femenina de fútbol sala vuelve a conquistar Europa
El Torneo de Candidatos de ajedrez de Madrid
Cuando Linares era el Wimbledon del ajedrez
“La pasión que genera el fútbol es inigualable”
“Nunca acepto un no por respuesta”
La mayor fábrica de baloncesto de Europa
Crónica de dos ciudades moldeadas por la misma pasión 
Amarillo Tour
Alcaraz se despide de Wimbledon tras caer ante Sinner (6-1, 6-4, 6-7, 6-3)
Victoria y catarsis de Dylan Groenewegen en la tercera etapa del Tour de Francia
La victoria de Carlos Sainz, en imágenes
Sainz: “No dejé de creer, a la espera de algo que finalmente pasó”
Judit fulmina a Carlsen
Carlsen negocia si renuncia al título o lo defiende en 2023 contra Niepómniashi
Carlos Sainz gana en Silverstone su primera carrera de Fórmula 1 
Regina Barzilay: “Tenemos que aprender a vivir en un mundo en el que la tecnología toma decisiones que no podemos supervisar”
Herramientas y trucos para recordar la ubicación del coche gracias al móvil
Las tres amigas que quieren revolucionar los materiales de construcción con fibras de hongos
El Constitucional afianza el derecho al olvido en internet
Dall-E, el popular generador automático de imágenes que hace dibujos sexistas y racistas 
Por qué el algoritmo de Google no es una persona
Comunidades de energía: una fórmula barata, limpia y segura
“Queremos que la programación sea el inglés del siglo XXI”
Imágenes sexuales que destruyen y matan
Tres cosas que hacemos mal con el teléfono móvil (y no sirven para nada)
Christopher Mims: “Amazon sabe cómo bajar el ritmo de trabajo para prevenir lesiones. Pero quizá dejaría de ganar dinero” 
¿Sigue siendo imprescindible tener un antivirus? 
Google News vuelve a España ocho años después de su cierre
Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
Instagram, el mejor de los mundos posibles
Del terrorismo youtuber al influencer rabioso: el odio inunda la red
Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
Cinco razones por las que este ‘smartphone’ es sencillamente tentador
La cámara de este ‘smartphone’ es pura magia
Por qué los nuevos coches ya no los diseñarán las personas
Una catapulta para el talento de ‘kilómetro cero’
Regina Barzilay: “Tenemos que aprender a vivir en un mundo en el que la tecnología toma decisiones que no podemos supervisar”
Herramientas y trucos para recordar la ubicación del coche gracias al móvil
Las tres amigas que quieren revolucionar los materiales de construcción con fibras de hongos
El Constitucional afianza el derecho al olvido en internet
Dall-E, el popular generador automático de imágenes que hace dibujos sexistas y racistas 
Por qué el algoritmo de Google no es una persona
Comunidades de energía: una fórmula barata, limpia y segura
“Queremos que la programación sea el inglés del siglo XXI”
Imágenes sexuales que destruyen y matan
Tres cosas que hacemos mal con el teléfono móvil (y no sirven para nada)
Christopher Mims: “Amazon sabe cómo bajar el ritmo de trabajo para prevenir lesiones. Pero quizá dejaría de ganar dinero” 
¿Sigue siendo imprescindible tener un antivirus? 
Google News vuelve a España ocho años después de su cierre
Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
Instagram, el mejor de los mundos posibles
Del terrorismo youtuber al influencer rabioso: el odio inunda la red
Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
El impacto de la tecnología en la hostelería: de la comanda digital al pago con código QR
Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
Cinco razones por las que este ‘smartphone’ es sencillamente tentador
La cámara de este ‘smartphone’ es pura magia
Por qué los nuevos coches ya no los diseñarán las personas
Una catapulta para el talento de ‘kilómetro cero’
En un mundo inestable y pospandémico, ¿para qué sirve la moda?
Los premios Princesa de Girona, en imágenes
‘Fiebre del sábado noche’ en tu salón: el curioso caso de las bolas de discoteca en la decoración del hogar
Britney Spears acusa a sus exgerentes de haberse apropiado de 17 millones de euros de su patrimonio durante la tutela
En el corazón del surrealismo: Leonor y Sofía visitan el Museo de Dalí en su primer acto solitario en Cataluña
Shakira cambia de estrategia para evitar el juicio por fraude fiscal tras separarse de Gerard Piqué
Emitida una orden de alejamiento contra Ricky Martin por violencia doméstica 
Rocío Jurado ya tiene su templo en Chipiona
La última exnovia de Berlusconi se casa con una cantante italiana
Juanes: “Me siento maduro, interesante y seguro, y eso me encanta”
Tom Cruise cumple 60 años: una celebración de su vida y su carrera en 12 fotos  
Cómo Julia Fox, actriz de una sola película, dominatrix y ‘obra maestra’ de internet, se convirtió en meme (e icono) de la generación TikTok
Lindsay Lohan se casa en una boda secreta
Entre Sevilla, Ascot, el pasado y el futuro: Mans condensa su universo en una colección sin miedo a los contrastes
La colección de Palomo Spain para Correos: cómo la moda unió a una empresa centenaria y a otra rabiosamente joven
Archie Alled-Martínez, el barcelonés que continúa el legado de Lagerfeld: “No hace falta llevar un arco iris para ser tú mismo”
Victorio & Lucchino, 40 años de moda en su museo de Córdoba, en imágenes
Vídeo | Eugenia Silva: “El estilismo de Britney Spears no hay por dónde cogerlo”
Trece aperitivos
Vende menos comer que correr
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
Breve guía de los mejores vinos blancos italianos para descubrir este verano
¿Quién demonios votó a Podemos en La Moraleja?
La voz de los más inocentes
Las actrices de ‘Intimidad’: “Si una mujer no es complaciente en esta profesión, llegan las amenazas”
Publicidad convertida en lírica y humanismo 
La voz de los más inocentes
‘Mi vida con 300 kilos’: un diamante entre la mierda
¿Hay demasiadas series a la vez?
Crecer dentro del fenómeno global ‘Stranger Things’: “Lo llevamos bien, con terapia”
La televisión también quiere ser verde: cómo ‘Servir y proteger’ disminuyó la contaminación en su rodaje
Las 10 mejores series sobre intrigas políticas para ver después de la cumbre de la OTAN 
Por qué los bisexuales, el colectivo no heterosexual más numeroso de España, siguen siendo invisibles en televisión
La ‘venganza’ de William Levy: “De joven, en Cuba, viví demasiadas injusticias”
Qué ver en televisión para celebrar el Orgullo LGTBI+ 2022
La ilustradora española que se asoma a las ventanas de Nueva York en ‘Solo asesinatos en el edificio’
24 series para este verano
Muere la actriz Mary Mara (’Urgencias’ y ‘Ray Donovan’) ahogada en un río de Nueva York
‘La clave’ de Balbín, gloria y caída del programa que cambió la televisión española
¿Qué ver hoy en TV? Lunes 4 de julio de 2022
Nueve capítulos para recordar ‘The Wire’ en su 20º aniversario
Harry Palmer: el tercer vértice del mágico triángulo de espías británicos
Las series de junio de 2022: ‘The Boys’ en Amazon Prime Video; ‘Peaky Blinders’ en Netflix y otras
La fuerza acompaña a ‘Obi-Wan Kenobi’, una serie deslumbrante
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
En busca de la huella de Camarón de la Isla, leyenda viva del flamenco
República Dominicana, donde la vida fluye por el río infinito
Oliviero Toscani: “El fascismo resulta muy cómodo porque no te exige razonar”
La importancia del respeto para sentirnos bien
El placer de lo rancio y otros gustos y aromas que recuerdan la niñez
Un misterio en el Real Madrid y un fantasma en Gales: ¿quién diablos es Gareth Bale?
España entra en la ruta del lujo mundial: fiestas, palacios y joyas valoradas en millones de euros
Así es el barrio de Pekín donde hay “robotaxi” y la compra llega en vehículo sin conductor
Saborear el momento
Lorena Jaume-Palasí: “Crear principios éticos universales para  la inteligencia artificial es una iniciativa cosmética”
Así es el primer campo de golf de España convertido en una reserva natural
Aprendizaje continuo para un mundo en cambio
Los coches más vendidos en la primera mitad de 2022
La palabra médico
El cuerpo
Cuento de Catherine del Biombo 5
Vende menos comer que correr
Harina enriquecida para acabar con el “hambre oculta”
Lugares de esperanza para salvar los océanos
Los guardianes del clima que llevan medio siglo leyendo las advertencias de los glaciares
Epidemia de violencia: claves del negocio de las armas en Estados Unidos
Los ejecutivos voladores y la ética medioambiental
Ibiza, entre la noche desenfrenada y el turismo tranquilo 
Luz Casal: “Tengo el alma rockera. Nada ha doblegado mi rebeldía”
Rashid Johnson: “Los pensadores y creadores negros estamos cansados de que nos nieguen un espacio autónomo”
Sergio Hernández: “En el mundo, la gente ya no quiere verdades, quiere mentiras”
Elvira Sastre: “No hay que perdonarlo todo”
La trinidad del taco perfecto: “Buena tortilla, delicioso relleno y una salsa sabrosa”
La casa de Nina Urgell Cloquell, un piso en el que las paredes hablan
Garbanzos verdes y puchero
Bikôkô y Julio Peña, dos estrellas en ebullición  
Cuando Chufy encontró a Rossy: dos amigas, una isla y una colección de moda
Retrato Robot 
Ilusiones hipnóticas
El poder del hormigón
Maulévrier, Japón a la francesa
‘Fantasías en el Prado’, por Alberto García-Alix
A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:
Feminismo
Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
Igualdad
La escuela concertada ante las desigualdades: el debate pendiente
Mujeres
El control del cuerpo de las mujeres
Un día muy triste para todas las mujeres
El Supremo de Estados Unidos destruye un derecho fundamental de las mujeres
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
Mujer
Las actrices de ‘Intimidad’: “Si una mujer no es complaciente en esta profesión, llegan las amenazas”
El control del cuerpo de las mujeres
Un día muy triste para todas las mujeres
El Supremo de Estados Unidos destruye un derecho fundamental de las mujeres
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
Las actrices de ‘Intimidad’: “Si una mujer no es complaciente en esta profesión, llegan las amenazas”
La rebelión de las cocineras de España: “Hay mujeres, falta reconocimiento”
Brecha salarial

Machismo

Violencia
Emitida una orden de alejamiento contra Ricky Martin por violencia doméstica 
Emitida una orden de alejamiento contra Ricky Martin por violencia doméstica 
Epidemia de violencia: claves del negocio de las armas en Estados Unidos
Maltrato

Homicidio

Género
La primera Constitución paritaria y con perspectiva de género
Americanas: Reportajes y noticias sobre feminismo e historias con enfoque de género de la región
Asesinato
La ilustradora española que se asoma a las ventanas de Nueva York en ‘Solo asesinatos en el edificio’
Sexo
Susan Meiselas, una vida de fotógrafa entre la industria del sexo y las guerras de Centroamérica

```

## Fin de la actividad

En esta sección se finaliza la actividad después de evidenciar el buen funcionamiento del código, las explicaciones de cada función, ciclo, excepción y condicional que se encontrara. También, se logró comprender un poco mejor el uso del Web Scrapping, el uso de las URL por medio de los estados activos de HTTP, se aprendieron nuevas técnicas de programación y se instalaron nuevos programas que permitieron un mejor entendimiento.

------------------------
Clic **[aquí]** (https://github.com/nebrijas/kgarciay-web/blob/main/AD1.md)** para volver a *la Actividad Dirigida 1*

Clic **[aquí]** (https://github.com/nebrijas/kgarciay-web/blob/main/AD2.md) para volver a *la actividad dirigida 2*

Clic **[aquí]** (https://github.com/nebrijas/kgarciay-web/blob/main/AD3.md) para volver a *la actividad dirigida 3*

Clic **[aquí]** (https://github.com/nebrijas/kgarciay-web/blob/main/AD4.md) para volver a *la actividad dirigida 4*

Clic **[aquí]** (https://github.com/nebrijas/kgarciay-web/blob/main/README.md) para volver a *README.md*


