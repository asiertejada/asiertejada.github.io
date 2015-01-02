---
layout: blog
title:  "SearchLink - Una Gema para Enlazar en Markdown"
date:   2014-05-24 13:00:00
categories: tutoriales
tags: markdown searchlink
featured_image: searchlink-una-gema-para-enlazar-en-markdown.png
---
En esta entrada me gustaría hablar sobre *SearchLink*, un servicio del sistema para *Mac OS X* que nos permitirá generar enlaces *"al vuelo"* en *Markdown* de una manera muy ágil, y mediante distintas fuentes de búsqueda. Toda una joya creada por el genial Brett Terpstra.<Sigue Leyendo>
  
## ¿Qué es *SearchLink?*  
Como ya dijimos en la introducción, [*SearchLink*](http://brettterpstra.com/projects/searchlink/) es un servicio del sistema para *Mac OS X*, cuya función principal es facilitar la tarea de añadir enlaces *HTML* a nuestros textos compuestos con *Markdown*.  
  
## ¿Cómo funciona?  
Para utilizar *SearchLink* deberemos escribir dentro nuestro texto algún patrón como el siguiente[^1]:  

	[texto a enlazar](!algo "texto opcional a buscar") 
    
Donde:  
  
* **[texto a enlazar]**: será el texto que mostrará el enlace, y a la vez será el texto que *SearchLink* usará para buscar el enlace.
* **!algo**: nos definirá el tipo de búsqueda que realizará *SearchLink*.
* **"texto opcional a buscar"**: nos permitirá añadir téminos extra a la búsqueda pero que no aparecerán en el texto del enlace[^2]. 
  
Posteriormente, deberemos seleccionar el texto que incluya el patrón anterior en nuestro texto, y ejecutar *SearchLink*, bien desde el menú Servicios que aparecerá sobre el texto resaltado al hacer clic derecho, bien mediante un atajo de teclado que hayamos definido previamente.  
  
Sin embargo, esto no implica que haya que repetir esta operación para cada enlace que introduzcamos. *SearchLink* está diseñado de tal manera que podremos seleccionar todo nuestro texto en *Markdown* una vez creado, y el propio servicio se encargará, al ejecutarse, de distinguir los diferentes enlaces y si estos han sido ya procesados o no.  
  
Precisamente por eso mismo, [definir un atajo de teclado](http://support.apple.com/kb/PH10837?viewlocale=es_ES)  para *SearchLink* cobra gran sentido, ya que así mediante dos combinaciones de teclado (⌘+A para seleccionar todo nuestro texto, y aquel que hayamos definido para ejecutar *SearchLink*) habremos generado todos los enlaces de nuestro texto de una manera rápida y sencilla.

## Búsquedas disponibles  
Como hemos dicho anteriormente, tendremos diferentes búsquedas disponibles, siendo las más destacadas[^3]:  
  
* **!mas**: buscará una aplicación en la *Mac App Store*.  
* **!itu**: buscará una aplicación en la *App Store* de *iTunes*.  
* **!s**: buscará en la categoría de software en *Google*.
* **!g**: realizará una búsqueda general en *Google*. 
* **!wiki**: buscará en la versión inglesa de la *Wikipedia*.
* **!ipod**: buscará un podcast en *iTunes*.
* **!a**: buscará un producto en la página americana de *Amazon*.
* **!@t**: buscará un perfil de *Twitter*.
* **!@adn**: buscará un perfil de [*App.net*](https://alpha.app.net).  
  
## Opciones de configuración    
Por si fuera poco, *SearchLink* también nos permite configurar ciertas opciones que resultan más que interesantes. Entre otras:  
      
1. Utilizar enlaces *"en línea"* o *"referenciados"*[^1].
2. Buscar en *Google* si la búsqueda en *iTunes* no da ningún resultado.
3. Especificar el país para nuestras búsquedas en *iTunes* y *Mac App Store* (de momento no funciona con *Wikipedia* o *Amazon*).
4. Añadir nuestros códigos de afiliado a los enlaces de *iTunes*, *Mac App Store* y *Amazon*.
5. Añadir códigos personalizados para realizar búsquedas dentro de un sitio específico con *Google Sites* (por ejemplo, **!bt** buscaría en [www.brettterpstra.com](http://brettterpstra.com/)).  
  
Para configurar estas opciones será necesario crear un archivo `.searchlink` en nuestra [carpeta de inicio](http://support.apple.com/kb/PH10939?viewlocale=es_ES), que siga la estructura del [archivo ejemplo](https://gist.github.com/ttscoff/9064738/raw/.searchlink) que nos proporciona el propio Brett en su blog. Lo más sencillo es descargarlo directamente en la carpeta de inicio y editarlo[^4].  
  
## Descarga e instalación  
Actualmente *SearchLink* va por la versión 2.1.3, que puede ser descargada desde la propia [web de Brett Terpstra](http://brettterpstra.com/2014/02/18/searchlink-2-dot-1/), o bien desde este [enlace](http://cdn3.brettterpstra.com/downloads/SearchLink2.1.3.zip).  
  
Desde esta última versión, la [instalación de *SearchLink* no necesita de ejecutar nada en el Terminal](http://brettterpstra.com/2014/05/08/install-searchlink-without-the-terminal-hassle/), y se reduce simplemente a descomprimir y hacer doble clic. 
    
Si todavía no os hacéis exactamente una idea de la potencia de *SearchLink*, lo mejor es ver un pequeño *screencast*:  

<p class='embed-container'><iframe src="//player.vimeo.com/video/96294065?portrait=0" width="720" height="405" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe></p>


[^1]: Recordatorio de [cómo se crean enlaces en *Markdown*](http://daringfireball.net/projects/markdown/syntax#link).  
[^2]: Otra opción es dejar en blanco la parte del texto a enlazar y especificar los términos de búsqueda en la parte opcional, es decir: `[]("texto opcional a buscar")`. En este caso, el título de la primera búsqueda será el que se útilice como el texto del enlace.  
[^3]: El listado completo de búsquedas disponibles se puede consultar en la propia [página del proyecto en el blog de Brett Terpstra](http://brettterpstra.com/projects/searchlink/#available-searches).  
[^4]: Se trata de un archivo oculto, por lo que para trabajar con él deberemos de [haberle dicho a nuestro *Mac* que nos muestre los archivos ocultos.](http://www.applesfera.com/os-x/muestra-archivos-ocultos-en-os-x-de-forma-rapida)