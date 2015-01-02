---
layout: blog
title:  "Descarga Automática de Series y Subtítulos"
date:   2014-05-17 15:00:00
categories: tutoriales
tags: hazel plex subtítulos tv tvshows utorrent
featured_image: descarga-automatica-de-series-y-subtitulos.png
images_folder: descarga-automatica-de-series-y-subtitulos
---
Durante tiempo he buscado la manera de automatizar la descarga de series de TV, que normarmente bajo en V.O., y la de sus correspondientes subtítulos (también en la lengua nativa de la serie). Gracias a herramientas como *TVShows 2* la descarga automática era posible, pero el bajar automáticamente los subtítulos, mediante el uso de la estupenda *Hazel*, era bastante más complicado, requeriendo incluso el uso de complejos *scripts* que no siempre funcionaban. Eso ha llegado a su fin, creo que he encontrado el flujo de trabajo definitivo (al menos para mis necesidades).<Sigue Leyendo>

> Esta entrada toma como base este [artículo](http://albertoperojo.com/post/20710041818/descarga-de-series-tv-shows2-transmission-hazel) de Alberto Pérez Rojo, que a su vez referenciaba a este [otro ya mítico](http://www.nahumgarcia.com/hazel) de Nahúm García.

## Descargar Series de TV Manualmente  
Como siempre me ha gustado seguir las series de TV del momento, generalmente estadounidenses o británicas[^1], la única alternativa para no sucumbir a los *spoilers* omnipresentes en internet y en las redes sociales mientras alguna cadena estatal se dignaba a estrenar la serie en cuestión, no ha sido otra que descargar los capítulos de dichas series en Versión Original (V.O.).  

Gracias a páginas como [*The Pirate Bay*](http://thepiratebay.se/) o [*EZTV*](https://eztv.it) (que a las pocas horas del estreno ya han subido los últimos episodios emitidos en *USA*) y a gestores de descargas mediante [*BitTorrent*](http://es.wikipedia.org/wiki/BitTorrent) como [*uTorrent*](http://www.utorrent.com/) o [*Transmission*](http://www.transmissionbt.com/), esto ha sido siempre bastante sencillo. bastaba con:    

* Abrir *EZTV*.  
* Buscar la serie y capítulo en cuestión.    
* Hacer clic en el [*enlace magnético*](http://es.wikipedia.org/wiki/Enlace_magnetico).  
* Esperar a que nuestro gestor de descargas se bajase el episodio.  

Con estos pequeños pasos, *voilà*, el último episodio de nuestra serie listo para ser visionado en la lengua de la [pérfida Albión](http://es.wikipedia.org/wiki/Pérfida_Albión). 

Teniendo en cuenta la diferencia horaria con los Estados Unidos, la hora de emisión local suele caer de madrugada, a lo que si le sumamos el tiempo que tardan en estar disponibles los nuevos episodios en las mencionadas webs *"piratas"*, lo normal es que hasta bien entrada la madrugada o incluso a primera hora de la mañana no podamos descargarlos. Esto implica que, en caso de tener una jornada laboral al uso, no seremos capaces de descargar ese último episodio (haciendo clic en la página web correspondiente) hasta la tarde/noche del día siguiente a su emisión. Además, habrá que sumarle el tiempo de la descarga en sí mismo que, dependiendo de la calidad del propio vídeo, a la velocidad de de nuestra conexión y a la disponibilidad de [*semillas*](http://es.wikipedia.org/wiki/Seeder), oscilará entre varios minutos a varias horas. En el peor de los casos, la descarga terminará a última hora de la noche o incluso de madrugada, posponiendo el visionado aún más.  

Así que tras 24/48 horas, estaremos listos para ver el capítulo más reciente de nuestra serie favorita. No está mal, pero puede ser mejorado.  

## Descarga de Subtítulos Manualmente  
Obviamente, ver series en V.O. implica tener un cierto nivel en la lengua nativa, generalmente inglés, gozando de un amplio vocabulario, conociendo giros y coloquialismos, y lo que es aún peor, teniendo nuestro oído acostumbrado a los diferentes acentos del habla anglosajona[^2].  
  
Ya cuando aprendí inglés hace años, nuestros profesores nos decían que ver películas en V.O. pero con subtítulos en castellano no servía para nada[^3]. Lo suyo es verlo con subtítulos en inglés. Así que eso es lo que acostumbro, a pesar de que en muchas series ya ni los leo, y para ello suelo utilizar la que para mí es la mejor web de subtítulos: [*Addic7ed*](http://www.addic7ed.com).  

El proceso para descargar los subtítulos manualmente es similar al de buscar el *torrent* para descargar los episodios que he comentado antes: buscar serie, buscar capítulo, tener en cuenta que versión nos hemos bajado (calidad y equipo que la ha [*ripeado*](http://es.wikipedia.org/wiki/Ripear)), clic y descargado[^4].  
  
## Visionado y/u Organización de Episodios Descargados Manualmente
Ahora sólo nos queda renombrar el archivo de subtítulos que hayamos descargado de manera que coincida con el nombre del archivo de vídeo, y así nuestro reproductor de vídeo (para *Mac* yo empleo [*MPlayerX*](http://mplayerx.org/)) detectará automáticamente los subtítulos y podremos disfrutar de ellos sin más quebraderos de cabeza.  

Otra opción es añadir ambos archivos a nuestro *media player system* o *media center* preferido, para que este nos catalogue el episodio, descargue su portada, etc., y desde él mismo poder hacer *streaming* bien a nuestros dispositivos *iOS*, o bien a nuestro dispositivo compatible con [*DLNA*](http://es.wikipedia.org/wiki/Digital_Living_Network_Alliance).  

Simple, sí. Tedioso, también. Hay margen para mejorarlo, y además sustancialmente, y de manera muy simple.  
  
## Descarga Automática de Series y Subtítulos  
Si en vez de tener que hacer todos los pasos anteriormente mencionados a mano, lo que queremos es que nuestro *Mac* se encargue de absolutamente todo, que a la mañana siguiente de la emisión del último capítulo de nuestra serie americana favorita, dicho episodio se encuentre ya procesado por nuestro *media player* con sus subtítulos, su carátula, sus descripciones, etc., y que todo este listo para que nostotros tan sólo debamos sentarnos y darle al *play*, entonces, debemos conseguir automatizar todo el proceso.   
  
Aunque pueda parecer complicado, para conseguir nuestro flujo de trabajo automático tan sólo necesitaremos las siguientes aplicaciones:   

* [***TVShows 2***](http://tvshowsapp.com/):   
	* Gratuita (y desarrollada en España, por cierto).   
	* Se encargará de descargar los archivos *.torrent* cada vez que el *feed RSS* de *EZTV* se actualice con un episodio nuevo de las series a las que nos hayamos suscrito en su panel de preferencias[^5].

* [***uTorrent***](http://www.utorrent.com/):
	* También gratuita. Otro buen gestor de descarga de *torrents* es [*Transmission*](http://www.transmissionbt.com). Yo he usado *uTorrent* desde mis tiempos en *Windows* y simplemente por eso[^6] es el que uso.  
	* Con él conseguiremos descargar el archivo de vídeo del episodio en cuestión.  

* [***Hazel***](http://www.noodlesoft.com/hazel.php):
	* Precio $28.00.
	* Una auténtica navaja suiza para automatizar nuestro *Mac*. Otro día hablaremos más en profundidad de ella.
	* Esta maravilla de aplicación se ocupará de renombrar el archivo de vídeo descargado, de pasarle dicho archivo a la aplicación de descarga de subtítulos, de renombrar el archivo contenedor de los subtítulos, de cerrar las apps y finalmente de mover vídeo y subtítulos a la carpeta de nuestro *media player*.  

* [**Subtítulos**](http://subtitlesapp.com/es):
	* Gratutita.
	* Su función será descargar automáticamente el archivo con los subtítulos correspondientes al episodio que le pasemos.

Veamos más al detalle cómo configurar cada una de las aplicaciones  y cuál es su papel dentro del flujo de trabajo.
  
### **1. *TVShows 2***  
 *TVShows* se instalará en nuestro *Mac* como un panel dentro de Preferencias del Sistema. Una vez instalado, podremos añadir series directamente desde los feeds que la propia app recopila, o bien, añadir otros que hayamos encontrado nosotros.  

<figure markdown="1">
![TVShows 2 - Subscripciones]({{ site.url }}/assets/img/{{ page.images_folder }}/TVShows-Suscripciones.png) 
<figcaption>TVShows 2 - Subscripciones</figcaption>
</figure>  


Así mismo, dentro de cada serie podremos especificar a partir de qué episodio queremos empezar a descargarla, pudiendo elegir entre inicar la subscripción en el próximo episodio que se emita o en un capítulo determinado[^7].  Otra elección es que podremos hacer es si queremos descargar el archivo en versión *HD* ([720p](https://es.wikipedia.org/wiki/720p)) o en una resolución más baja. Obviamente, a mayor calidad más pesado será el archivo de vídeo a descargar.
  
<figure markdown="1">
![TVShows 2 - Añadir serie]({{ site.url }}/assets/img/{{ page.images_folder }}/TVShows-Añadir-Suscripción.png)
<figcaption>TVShows 2 - Añadir serie</figcaption>
</figure>

Por último, desde las preferencias de *TVShows* podremos configurar si queremos que la aplicación aparezca en la barra de menús, el intervalo entre búsquedas, si queremos que la descarga en *HD* esté activada por defecto, notificaciones, etc. Pero sobre todo, la opción a configurar que más nos interesa a nosotros es la elección de la carpeta en que se descargarán los archivos .*torrent*, ya que está debera ser misma carpeta en la que deberá buscar *uTorrent*, para que así inicie las descargas automáticamente.  
  
<figure markdown="1">
![TVShows 2 - Preferencias]({{ site.url }}/assets/img/{{ page.images_folder }}/TVShows-Preferencias.png)
<figcaption>TVShows 2 - Preferencias</figcaption>
</figure>
  
Por lo tanto, como ya dijimos antes, la misión de *TVShows* será revisar periodicámente los *feeds* de nuestras series y cuando en una de esas revisiones encuentre un episodio nuevo, descargar inmediatamente el archivo *.torrent* a la carpeta que le hayamos especificado.  

### **2. *uTorrent***  
El encargado de la descarga del archivo de vídeo a partir del *torrent* descargado por *TVShows* va a ser nuestro gestor de descargas, en mi caso *uTorrent*. Sin embargo, para que la descarga ocurra automáticamente deberemos asegurarnos de configurar correctamente la preferencias de *uTorrent*.  
  
Primero, en la pestaña *General*, la opción *"Iniciar descargas automáticamente"* deberá estar activada, como no podía ser de otra manera. Otro par de opciones que deberemos activar para asegurarnos de que la descarga llegará a buen puerto serán *"Usar uTorrent por defecto de descargas torrents"* y *"Evitar reposar cuando las transferencias están activas"*.  
  
<figure markdown="1">
![uTorrent - Preferencias/General]({{ site.url }}/assets/img/{{ page.images_folder }}/uTorrent-Preferencias-General.png)
<figcaption>uTorrent - Preferencias/General</figcaption>
</figure>
  
Posteriormente, le deberemos decir a *uTorrent* en qué carpeta buscar nuevos archivos *.torrent* para iniciar automáticamente su descarga, la cual deberá ser la misma que configuramos en TVShows, y también en qué carpeta lo descargará, punto importante para que nuestro flujo de trabajo no se detenga.
  
<figure markdown="1">
![uTorrent - Preferencias/Carpetas]({{ site.url }}/assets/img/{{ page.images_folder }}/uTorrent-Preferencias-Carpetas.png)
<figcaption>uTorrent - Preferencias/Carpetas</figcaption>
</figure>
  
De esta manera, *uTorrent* se abrirá automáticamente en cuanto aparezca un nuevo *torrent* en la carpeta especificada, y descargará el archivo de video en la carpeta que le hayamos dicho.

###  **3. *Hazel* y Subtítulos**
Una vez descargado nuestro episodio, el siguiente actor dentro del flujo de trabajo es *Hazel*, que al igual que *TVShows* se instalará como un panel dentro de Preferencias del Sistema.
  
La versatilidad de una aplicación como *Hazel* es enorme, así que en esta entrada tan sólo veremos las reglas que nos interesan para este flujo de trabajo, sin profundizar en demasiados detalles.   
  
El funcionamiento de *Hazel* es muy simple. Nosotros le diremos una carpeta que deberá revisar periódicamente y, a su vez, le definiremos unas reglas que, en caso de cumplirse, desencadenarán una serie de acciones. En el caso de nuestro flujo de trabajo, la carpeta a revisar será aquella que habíamos seleccionado en *uTorrent* en el paso anterior, y las reglas que especificaremos serán las que detallaremos a continuación.

<figure markdown="1">
![Hazel - Reglas]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Reglas.png)
<figcaption>Hazel - Reglas</figcaption>
</figure>

#### **3.1. Limpieza del nombre y renombrado del archivo (opcional)[^8]**
Generalmente la nomenclatura de los archivos de vídeo de series de televisión suele seguir un patrón del tipo:  
  
`Game.of.Thrones.S01E01.HDTV.x264-LOL.mp4`  
  
Donde podemos distinguir varias partes separadas por puntos y/o guiones:  

* **Game.of.Thrones**: La primera parte es el título de la serie, con sus palabras separadas por puntos en vez de espacios.
* **S01E01**: La segunda parte nos indica la temporada (*S* de *Season*, temporada en inglés) y el número de capítulo dentro de esa temporada (*E* del también inglés *Episode*).
* **HDTV**: La tercera parte nos indica de dónde se ha obtenido el vídeo y por tanto su calidad. En caso de series de televisión, lo más normal es que se graben directamente de televisión y en el nombre aparecerá la palabra *HDTV*, pero en ocasiones, los archivos de vídeo se habrán extraído de *DVDs* o de discos *Blu-Ray*, por lo que los términos que aparecerán serán *DVDRip* y *BRip*.
* **x264**: A continuación aparece el [*códec*](http://es.wikipedia.org/wiki/Códec) con el que se ha creado el archivo de vídeo. Los más habituales suelen ser *x264* y *XviD*.
* **LOL**: La última parte del nombre y separado por un guión del *códec* suele aparecer el nombre del equipo que ha grabado y subido el vídeo. Algunos de los más famosos son *LOL*, *FQM*, *KILLERS*, y otros.  
* **.mp4**: Es la extensión del archivo, la cual nos indica que tipo de archivo es. No forma estrictamente parte del nombre del archivo, y por ello siempre va separada de él mediante un punto.
  
Sin embargo, a veces, los nombres de los archivos traen más cosas detrás, generalmente entre corchetes, del estilo:  
		
`Game.of.Thrones.S01E01.HDTV.x264-LOL.[BASURA].mp4`  
  
En mi caso, me gusta que el aspecto final de los nombres sea:  
  
`Game of Thrones - 1x01.HDTV.x264-LOL.mp4`  
  
Para conseguirlo utilizo dos reglas en *Hazel*: la primera para quitar la *"basura"* entre corchetes mediante la cual obtengo el patrón tipo del que hablé al inicio de este punto, y la segunda para, a partir de dicho patrón, obtener el aspecto final a mi gusto.  
  
##### **3.1.1. Quitar basura entre corchetes**  

<figure markdown="1">
![Hazel - Quitar basura entre corchetes]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Quitar-Corchetes.png)  
<figcaption>Hazel - Quitar basura entre corchetes</figcaption>
</figure>
    
En esta primera regla le decimos a *Hazel* que compruebe si se cumplen **todas** las siguientes condiciones:

a) Existe un archivo de vídeo en la carpeta designada.
  
b) Con extensión *.mp4* [^9]. Un detalle importante a tener en cuenta a la hora de escribir nuestras reglas es que *Hazel* considera que el punto de separación entre nombre y extensión no forma parte de ninguno de ellos, ni del nombre ni de la extensión. Así que dicho punto de separación no deberá aparecer en ninguna regla que haga referencia al nombre o a la extensión del archivo.  

c) Cuyo nombre siga el siguiente patrón, con los siguientes ítems:  

* ***Show***: compuesto por cualquier serie de caracteres, y seguido de un punto y la letra mayúscula S.
* ***Season***: compuesto por números, y seguido de un punto y la letra mayúscula E.
* ***Episode***: compuesto por números, y seguido de un punto.
* ***Origin***: compuesto por cualquier serie de caracteres, y seguido de un punto.
* ***Códec***: compuesto por letras y números, y seguido de un guión.
* ***Team***: compuesto por cualquier serie de caracteres, y seguido por un punto.
* ***Basura***: compuesto por cualquier serie de caracteres.
  
d) Cuya extensión esté compuesta por letras y números[^10].   

Es decir, que sea del tipo:  

`Game.of.Thrones.S01E01.HDTV.x264-LOL.[BASURA].mp4`   
  
<figure markdown="1">
![Hazel - Quitar basura entre corchetes - Patrón inicial]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Patrón-Quitar-Corchetes-1.png)
<figcaption>Hazel - Quitar basura entre corchetes - Patrón inicial</figcaption>
</figure> 
  
Y en el caso de que todas las condiciones anteriores se cumplan, le decimos a *Hazel* que elimine la parte llamada basura y mantenga el resto, obteniendo:  

`Game.of.Thrones.S01E01.HDTV.x264-LOL`  
  
<figure markdown="1">
![Hazel - Quitar basura entre corchetes - Patrón final]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Patrón-Quitar-Corchetes-2.png)
<figcaption>Hazel - Quitar basura entre corchetes - Patrón final</figcaption>
</figure>  
  
##### **3.1.2. Renombrar archivo de vídeo**
  
<figure markdown="1">
![Hazel - Renombrar episodios]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Renombrar-Episodios.png) 
<figcaption>Hazel - Renombrar episodios</figcaption>
</figure> 
   
En esta segunda regla, lo que le diremos a *Hazel* es que si encuentra algún archivo de vídeo, con el patrón que hemos obtenido en el paso anterior, lo renombre de manera que el nombre final esté compuesto por los siguientes ítems:
 
 * ***Show***: consistirá en el título de la serie, pero le diremos a *Hazel* que sustituya los puntos que separan las diferentes palabras por espacios. Irá seguido de un espacio, un guión y otro espacio.
* ***Season***: que serán los números obtenidos en el paso anterior, seguidos de una equis minúscula (x).
* ***Episode***:  que también serán los números obtenidos en el paso anterior, seguidos de un punto.
* ***Origin***: compuesto por la serie de caracteres de la regla anterior, y seguido de un punto.
* ***Códec***: compuesto por las mismas letras y números de la regla anterior, y seguido de un guión.
* ***Team***: compuesto por la misma serie de caracteres obtenida con anterioridad.
* ***Extension***: que sigue siendo la original.
  
Resultando el nombre final:  
  
`Game of Thrones - 1x01.HDTV.x264-LOL.mp4`  

Una vez renombrado el archivo, le diremos a *Hazel* que le añada una etiqueta de color rojo. Esta etiqueta nos servirá para identificar que el archivo está renombrado, pero que todavía no se ha bajado su subtítulo. 
  
<figure markdown="1">
![Hazel - Renombrar episodios - Patrón]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Patrón-Renombrar-Episodios.png)
<figcaption>Hazel - Renombrar episodios - Patrón</figcaption>
</figure>  
  
#### **3.2. Descarga y renombrado del archivo de subtítulos[^11]**
Con nuestro archivo de vídeo ya listo, es turno de descargar sus subtítulos de manera automática gracias a la última versión de la aplicación Subtítulos (puesto que anteriormente no descargaba siempre los subtitulos correctos al seguir este flujo de trabajo). Una vez descargados, le añadiremos al nombre del archivo de subtítulos el identificador del lenguaje en el que están escritos[^11] y cerraremos la aplicación Subtítulos.  
  
En este paso emplearemos 3 reglas en *Hazel*:  
  
#### **3.2.1. Descarga de subtítulos**  
Para descargar los subtítulos automáticamente, lo único que le diremos a *Hazel* es que cada vez que encuentre un archivo de vídeo etiquetado de color rojo, lo abra dos veces con la aplicación Subtítulos (no sé por qué narices si sólo lo abre una vez no descarga el archivo), y que posteriormente etiquete nuestro archivo de vídeo en verde, es decir, como archivo renombrado y con subtítulos descargados.  
  
El archivo que obtendremos de la aplicación Subtítulos siempre tendrá el mismo nombre que el archivo de vídeo que le hayamos pasado, pero su extensión será *.srt*, es decir:   
  
`Game of Thrones - 1x01.HDTV.x264-LOL.srt` 

<figure markdown="1">
![Hazel - Descargar subtítulos]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Descargar-Subtítulos.png)
<figcaption>Hazel - Descargar subtítulos</figcaption>
</figure>  
  
##### **3.2.2. Renombrar archivo de subtítulos (opcional)[^111]**
La segunda regla que ejecutaremos en este paso es una muy sencilla y que tiene como objeto añadir el fragmento *.en* al nombre del archivo de subtítulos (*.srt*). De manera que nuestro archivo de subtítulos tras esta regla será:  
  
`Game of Thrones - 1x01.HDTV.x264-LOL.en.srt`  
  
<figure markdown="1">
![Hazel - Añadir idioma a nombre de subtítulos]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Añadir-Idioma-a-Nombre-de-Subtítulos.png)
<figcaption>Hazel - Añadir idioma a nombre de subtítulos</figcaption>
</figure>

##### **3.2.3. Cerrar la aplicación Subtítulos**
Por último, y en paralelo a la anterior, haremos que *Hazel* ejecute una última regla, en la que le diremos que cada vez que encuentre un archivo de vídeo etiquetado en verde, ejecute un pequeño *script* que cerrará automáticamente la aplicación Subtítulos.  
  
<figure markdown="1">
![Subtítulos]({{ site.url }}/assets/img/{{ page.images_folder }}/Subtítulos.png)
<figcaption>Subtítulos</figcaption>
</figure>
  
<figure markdown="1">
![Hazel - Cerrar aplicación Subtítulos]({{ site.url }}/assets/img/{{ page.images_folder }}/Hazel-Cerrar-App-Subtítulos.png)
<figcaption>Hazel - Cerrar aplicación Subtítulos</figcaption>
</figure>

El código del script será el siguiente:  

{% highlight bash %}  
tell application "Subtitles" to quit  
{% endhighlight %}

El funcionamiento de esta parte del flujo de trabajo se puede observar en el siguiente *screencast*:  

<p class='embed-container'><iframe src="//player.vimeo.com/video/94922596?portrait=0" width="720" height="405" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></p>
     
### **4. *Plex***
Así, con nuestro episodio renombrado y subtítulado, lo único que nos quedaría hacer es mover ambos archivos a nuestro *media center* favorito, que para mí es *Plex*.  
  
  
  
Lo que conseguimos con *Plex*, además de que nos organice las series y nos descargue carátulas, descripciones, etc. (que no es poco), es crear un servidor en nuestro ordenador, nuestro [*NAS*](http://es.wikipedia.org/wiki/Network-attached_storage/) o incluso en un *Apple TV* que nos permitirá hacer *streaming* a multitud de dispostivos (*iOS*, *DLNA*, etc.)[^12].
  
<figure markdown="1">
![Plex - Series TV - Game of Thrones]({{ site.url }}/assets/img/{{ page.images_folder }}/Plex-GoT.png)
<figcaption>Plex - Series TV - Game of Thrones</figcaption>
</figure>  

<figure markdown="1">
![Plex - Series TV - Game of Thrones - Season 4]({{ site.url }}/assets/img/{{ page.images_folder }}/Plex-GoT-S04.png)
<figcaption>Plex - Series TV - Game of Thrones - Season 4</figcaption>
</figure>    
  
<figure markdown="1">
![Plex - Series TV - Game of Thrones - Season 4 - Episode 5]({{ site.url }}/assets/img/{{ page.images_folder }}/Plex-Got-S04E05.png)
<figcaption>Plex - Series TV - Game of Thrones - Season 4 - Episode 5</figcaption>
</figure>     
  
Automatizar este movimiento se podría conseguir fácilmente con *Hazel*. Tan sólo habría que añadir un par de reglas más para que, a partir del nombre de los archivos de vídeo y de subtítulos, o a partir de unas ciertas etiquetas de color, *Hazel* traslade dichos ficheros a dentro de la carpeta que supervisa *Plex*.

Sin embargo, en mi caso, como las series las llevo en un disco externo que no está siempre conectado a mi *MacBook*, no lo tengo implementado **aún**.   
  
Además, esta entrada está saliendo bastante larga, por lo que, seguramente, lo mejor será dejarlo para otro día. Volveremos a hablar de *Hazel* y de *Plex* no dentro de mucho.

[^1]: Lo siento, Cuéntames, Serranos y demás comunidades de vecinos.   
[^2]: No tiene nada que ver el inglés británico que nos enseñan en escuelas y academias, con el inglés americano (que se pronuncia diferente en cada estado, o incluso en las diferentes zonas de cada estado), eso está claro. Pero incluso dentro de las islas, nada tiene que ver cómo pronuncia un escocés con un inglés. Ni tampoco habla igual un doctor universitario de Pasadena que el camello más famoso de Alburquerque.  
[^3]: Salvo que no tengas idea de inglés y no te interese aprenderlo.  
[^4]: En este caso los subtítulos son meros archivos de texto que apenas pesan varios KB, por lo que, por muy mala conexión que tengamos, la descarga es inmediata.
[^5]: Últimamente *TVShows* no descarga bien algunos *feeds*, en mi caso el de Juego de Tronos, debido a que, al parecer, la app funciona con dos *feeds* por serie, uno con los diez últimos episodios de cada serie y otro *"full"* con todos los episodios de todas las temporadas. Parece que este último no se está actualizando correctamente, y a pesar de que el primero si está actualizado, la app parece escoger el *feed* más desactualizado (que de los dos, siempre es la versión *"full"*). A pesar de que sólo afecta a un número reducido de series, esperemos que se solucione pronto.
[^6]: Por eso y por la ya difunta visualización [*3D Globe*](https://www.youtube.com/watch?v=V35K67xK75I).
[^7]: En el caso de elegir iniciar la subscripción en otro capítulo que no sea el próximo a emitir, *TVShows* descargará todos los capítulos desde el elegido como inicial hasta el último emitido.  
[^8]: Si no sóis unos maniáticos del orden y **no váis a usar** [***Plex***](https://support.plex.tv/hc/en-us/articles/200220687-Naming-Series-Based-TV-Shows), no necesitaréis estas reglas de limpieza y cambio de nombre de nuestros archivos de vídeo, y el resultado será el mismo.  
[^9]: Yo siempre bajo las series en este formato y esta regla redundante me asegura que *Hazel* nunca va a procesar una película. Si vosotros descargáis en varios formatos, esta condición sobraría.  
[^10]: Otra regla redundante (ya que todas las extensiones de archivos sólo pueden estar formadas por letras y números, y no símbolos), pero que ayuda a *Hazel* a no equivocarse cuando se usan puntos en los nombres de los archivos.
[^11]: De nuevo, la parte de renombrar los archivos de subtítulos es opcional, en función de vuestras manías, y **siempre y cuando no vayáis a usar** [***Plex***](https://support.plex.tv/hc/en-us/articles/200471133-Adding-local-Subtitles-to-your-media).   
[^111]: De nuevo, la parte de renombrar los archivos de subtítulos es opcional, en función de vuestras manías, y **siempre y cuando no vayáis a usar** [***Plex***](https://support.plex.tv/hc/en-us/articles/200471133-Adding-local-Subtitles-to-your-media).  
[^12]: Eso y poder usar el *iPhone* como mando a distancia, que siempre queda resultón.
