---
layout: blog
title:  "El Flujo de Trabajo (I) - Markdown para WordPress"
date:   2014-01-05 15:00:00
categories: blog
tags: markdown wordpress
featured_image: flujo-trabajo-markdown-para-wordpress.png
---
En la anterior (y primera) entrada de este blog hablé sobre cómo dar con el flujo de trabajo adecuado ha sido causa fundamental en mi decisión de comprometerme a escribir más asiduamente. Veamos por qué y descubramos qué es *Markdown*.<Sigue Leyendo>

## La Plataforma: *WordPress*
Algo que obvié (por motivos obvios, valga la redundancia) en mi anterior entrada es que la plataforma elegida para este blog es [*WordPress*](http://es.wordpress.org). La base de esta elección frente a otras plataformas más recientes como puedan ser [*Ghost*](http://ghost.org/) o [*Jekyll*](http://jekyllrb.com/), es precisamente la más que consolidada trayectoria de *WordPress* y el hecho de que si bien las nuevas plataformas de *blogging* acaban siendo más simples de usar y más eficientes, requieren de un período de aprendizaje inicial que, para alguien ya acostumbrado a los mimbres de *WordPress*, no compensa en el corto plazo.  

Es decir, que de inicio resultan más complicadas, a pesar de que en el fondo son menos complejas, e incluso más enfocadas al *blogging*, al prescindir de muchas de las opciones de *WordPress*[^1].  

[^1]: Suena paradójico, pero tiene sentido. Tal vez en otra entrada dé tiempo a profundizar algo más.  

## *Markdown*
Sin embargo, a pesar de esta curva de aprendizaje más asequible para el usuario medio, escribir un blog con textos medianamente ricos puede pasar rápidamente de algo motivador a algo tedioso en cuanto nos enfrentamos a la tarea de escribir código. Es un hecho, tarde o temprano deberemos dejar el editor visual de *WordPress* y adentrarnos en el no tan amigable código *HTML*[^2].  

[^2]: *HyperText Markup Language* o [lenguaje de marcas de hipertexto](http://es.wikipedia.org/wiki/HTML).  

Es aquí donde entra en juego esa pequeña maravilla que es el *Markdown*[^3], invención de [John Gruber](http://daringfireball.net/) y del malogrado [Aaron Swartz](http://es.wikipedia.org/wiki/Aaron_Swartz), que no es otra cosa que un lenguaje de marcas ligeras o simples que nos permite evitar la complejidad de las etiquetas *HTML* aportándonos muchas ventajas a la vez:

* **Simplificar el código**: es su principal virtud y de la que derivan el resto. En vez de poner ejemplos aquí, lo mejor es echar un ojo a la [sintáxis de *Markdown*](http://daringfireball.net/projects/markdown/syntax), donde el señor Gruber la explica muy bien.  
* **Permitir una escritura continua del código**: dado que no es necesario hacer clics de ratón para dar formato, que las listas, numeradas o no, se generan al *"estilo Word"*, o que en el caso de los enlaces, las direcciones *URL* se pueden insertar todas al final una vez terminada la redacción del texto.  
* **Incrementar la legibilidad del código**: al prescindir de etiquetas y sustituirlas por caracteres de texto plano, el código resultante es muy parecido al texto que se va a generar con él.  
* **Disminuir el tamaño de nuestros archivos de texto**: por la misma razón anterior, los archivos de texto contendrán menos caracteres, lo cual a priori puede no parecer gran cosa, pues los archivos de texto ya son reducidos de por sí. Sin embargo, en perspectiva, el ahorro de ancho de banda a lo largo de un período de tiempo prologando es más que interesante.
* **Aumentar la productividad a la hora de publicar textos enriquecidos**: en definitiva, por todos los motivos anteriores, la creación y publicación de textos enriquecidos es mucho más eficiente.  

En la actualidad, existen varios desarrollos que añaden nuevas funcionalidades (tablas, notas al pie[^4], etc…) a *Markdown* como son [*MultiMarkdown*](http://fletcherpenney.net/multimarkdown/) o [*Markdown Extra*](http://michelf.ca/projects/php-markdown/extra/), y cuyo soporte ha sido implementado en las principales aplicaciones que usan *Markdown*.  

[^3]: En contraposición a *Markup*, que como hemos visto anteriormente, viene a significar marcas *"pesadas"* o *"de alto nivel"*.      

[^4]: Esta nota está hecha con *MultiMarkdown*, por ejemplo. Adoro las notas al pie.

## *Markdown* para *WordPress*
Vale. Ya sabemos lo que es *Markdown* y qué ventajas nos aporta, pero, ¿cómo podemos integrarlo en *WordPress*?  

Personalmente, creo que la mejor manera es recurrir a un editor de texto aparte, con soporte para *Markdown* que nos genere el *HTML*, y posteriormente subir la entrada a *WordPress*. Sin embargo, si estamos acostumbrados a utilizar el editor nativo de *WordPress*, o si queremos editar borradores de entradas que hayamos subido con otra aplicación previamente, directamente desde el navegador, puede ser interesante modificarlo para trabajar con *Markdown*.  

Para ello, la mejor opción es el *plugin* [*Markdown QuickTags*](http://brettterpstra.com/code/markdown-quicktags), creación de otro de los grandes gurús de la productividad en general y del *Markdown* en particular, el señor [Brett Terpstra](http://brettterpstra.com). Este plugin realiza una serie de cambios en el editor de texto nativo de *WordPress* que nos resultarán de gran ayuda.

Para empezar, sustituye la barra de herramientas clásica por otra con los formatos y atajos más utilizados en *Markdown*.  

Así mismo, incluye un par de botones justo a la izquierda de la mecionada barra de herramientas: *Full Screen Editor* y *Preview* (Editor a Pantalla Completa y Previsualización, respectivamente):

* El primero, de nombre desafortunado, habilitará una especie de de modo *focus* en una estrecha franja emergente dentro del navegador, oscureciendo el resto de la ventana, algo interesante y muy de moda últimamente, pero en ningún caso ocupará la pantalla completa.  
	  
* El segundo nos generará una previsualización en la misma área de edición. Pero, al menos en mi caso, la altura de dicha área de edición se ve disminuida a poco más de línea y media, dificultando la visualización cómoda del artículo, por lo que no es de mucha utilidad.  
	
Por último, añade una fila de 4 enlaces en la parte inferior del cuadro de texto del editor, siendo los 2 primeros los enlaces de *Undo* (Deshacer) y *Redo* (Rehacer), cuyo funcionamiento es el habitual a este tipo de botones. Los otros 2 enlaces son la chicha de este plugin:  

* ***Render***: nos convertirá el texto en *Markdown* presente en el área de edición a *HTML*, para así poder pulsar el botón de Publicar (si no nuestra entrada será una copia del código *Markdown*, es decir, texto plano).  
	
* ***Markdownify***: convertirá un texto en *HTML* a *Markdown*, lo cual puede ser muy útil a la hora de editar entradas antiguas. Hay que tener en cuenta, que traducirá todo lo que pueda a *Markdown*, por lo que si es un *HTML* muy complejo que incluya funciones no soportadas por *Markdown*, el resultado dejará mucho que desear.  

Y por hoy creo que ya es más que suficiente, tampoco vamos a volvernos locos el primer día. En caso de que queráis profundizar más, creo que con la cantidad de enlaces que hay en este artículo tenéis material de sobra para un buen rato.  

En la próxima entrada hablaré sobre las aplicaciones que incorporo en mi flujo de trabajo para escribir *Markdown* y publicar en *WordPress*. Hasta la próxima.