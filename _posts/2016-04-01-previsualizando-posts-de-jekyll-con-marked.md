---
layout: blog
title: Previsualizando Posts de Jekyll con Marked
date: 2016-04-01 10:00:00
categories: blog
tags: byword jekyll marked ruby
featured_image: previsualizando-posts-de-jekyll-con-marked.png
images_folder: previsualizando-posts-de-jekyll-con-marked
---
Al final va a ser que el tener un blog no es sino una excusa para cacharrear porque, visto lo visto, aún no le he cogido el ritmo a lo de escribir. En este enésimo retorno por fin he logrado conseguir algo que tenía pendiente desde que di el salto a *Jekyll*.<Sigue Leyendo>

Y es que al final uno pasa más tiempo perfilando flujos de trabajo y automatizando cosas que realmente escribiendo. Recientemente, por fin he acabado mi flujo en movilidad para poder *postear* en el blog desde el *iPhone* o el *iPad* gracias al maravilloso cliente de [*Git*](https://git-scm.com) llamado [*Working Copy*](https://itunes.apple.com/es/app/working-copy/id896694807?mt=8&uo=4&at=1l3v5kR&ct=blog) [^1]. Pero eso es harina de otro costal, y espero (y cruzo los dedos) que pronto aparezca otra entrada por aquí acerca del tema.

[^1]: Un auténtico *powerhorse* para trabajar con repositorios *Git*, por lo que es idóneo para blogs servidos por *Jekyll* y alojados en [*GitHub Pages*](https://pages.github.com/), alojamiento que por cierto es gratuito para nuestra primera web.

Pero lo que realmente me ha traído frente el teclado esta vez ha sido el poder conseguir visualizar de una manera más o menos fiel los textos escritos [*Markdown*](https://daringfireball.net/projects/markdown/) y [*Liquid*](https://github.com/Shopify/liquid/wiki/ES-Home) en [*Marked*](https://itunes.apple.com/es/app/marked-2/id890031187?ls=1&mt=12&uo=4&at=1l3v5kR&ct=blog) [^2], algo que me había traído de cabeza más de una vez y que tras varias intentonas tenía medio aparcado.

[^2]: Esta última se encuentra descontada al 50% en el momento de escribir esta entrada. Una gran oportunidad para apoyar al bueno de Brett Terpstra (y de paso a este blog, *léase* enlace afiliado). 

No volveré hablar otra vez sobre *Markdown*, [*Byword*](https://itunes.apple.com//es/app/byword/id420212497?mt=12&uo=4&at=1l3v5kR&ct=blog) y *Marked* pues lo hice hace ya un buen tiempo en este mismo blog. Si alguien estuviese interesado en saber más, [no tiene pérdida](http://www.asiertejada.com/el-flujo-de-trabajo-ii-byword-y-marked/).

Sí que me permitiré volver a hablar un poco sobre [*Jekyll*](https://jekyllrb.com/) y no para ahondar sobre sus bondades como excelente generador de páginas web estáticas, si no para hacerlo acerca de su uso de *Liquid* y de cómo dejarme de [*CMS*](https://es.wikipedia.org/wiki/Sistema_de_gestión_de_contenidos)s *a la* *WordPress* y remangare con *Jekyll* ha hecho que por el camino haya tenido que aprender *Git*, me haya tenido que poner las pilas con la[ Interfaz de Línea de Comandos](https://es.wikipedia.org/wiki/Interfaz_de_l%C3%ADnea_de_comandos) e incluso haya hecho mis pinitos en [*Ruby*](https://www.ruby-lang.org/es/).

La cuestión es que [*Jekyll* utiliza plantillas o etiquetas en *Liquid*](https://jekyllrb.com/docs/templates/) de manera que tareas como enlazar imágenes son mucho más sencillas[^3], ya que, en vez de tener que enlazar toda la *URL* de cada imagen que queramos usar, bien en *HTML*:

{% highlight html %} {% raw %}
<img src="http://www.asiertejada.com/assets/img/mi-imagen.png" alt="" width="" height="" border="" align="" />
{% endraw %} {% endhighlight %}
	
bien en Markdown:

{% highlight text %} {% raw %}
![](http://www.asiertejada.com/assets/img/mi-imagen.png)
{% endraw %} {% endhighlight %}

podemos emplear etiquetas de *Liquid* y tan sólo referenciar el nombre de cada imagen cada vez:

{% highlight text %} {% raw %} 
![]({{ site.url }}/assets/img/{{ page.images_folder }}/mi-imagen.png)
{% endraw %} {% endhighlight %}

Donde `site.url` hace referencia a la etiqueta `url` que hayamos especificado en el archivo de configuración *YAML* de nuestro blog:

<script src="https://gist.github.com/asiertejada/ca520cccd50cf961324503d1a93a1271.js"></script>

Y `page.images.folder` a la carpeta donde subimos nuestras imágenes y que especificamos en el [*Front Matter*](https://jekyllrb.com/docs/frontmatter/) también en [*YAML*](https://es.wikipedia.org/wiki/YAML) de cada una de nuestras entradas, es decir de cada archivo en *Markdown* que creamos:

<script src="https://gist.github.com/asiertejada/5a4028e80527de37c4b09f0e9b60386e.js"></script>

[^3]: No digamos ya si empleamos un software como [*TextExpander*](http://www.asiertejada.com/textexpander/).

Maravilloso, pero el problema que suponía esto en mi flujo de trabajo era que, a la hora de previsualizar las entradas de mi blog en *Marked* mientras las escribía en *Byword*, las etiquetas de *Liquid* no eran correctamente procesadas por lo que las imágenes no se mostraban más que como una línea de código [^4]. 

[^4]: Problemas del primer mundo, o del primer mundo *geek* para ser más precisos. Lo sé.

En mi caso, suelo usar *Marked* también para enviar una copia en *PDF* del artículo terminado a mi *iPad* [^5] y revisarlo y anotarlo para, en caso necesario, corregirlo antes de publicarlo.

[^5]: Este artículo se revisará en un *iPad Pro* que recibí como regalo por mi cumpleaños. Pero de él, de *cachofones* y demás compras de *iCacharros* posteriores a la anterior entrada de este blog hablaremos en otra momento. Crucemos los dedos para que no sea dentro de meses cuando hayamos renovado los juguetes.

Sabía que el desarrollador de *Marked*, Brett Terpstra, se habría topado con este problema también y que por tanto, como buen *hacker*, habría tenido que buscar una solución. Y efectivamente así era. Buceando por su blog encontré la correspondiente entrada [*Previewing Jekyll posts with Marked*](http://brettterpstra.com/2013/01/04/previewing-jekyll-posts-with-marked/) [^6] como no podía ser de otra forma.

[^6]: A la cual hemos copiado el título sin miramiento alguno.

En ella Brett explica que, para poder conseguir nuestro objetivo, es necesario preprocesar nuestro archivo en *Markdown* para transformar así las etiquetas de *Liquid* antes de ser procesadas por *Marked* y, para ello, comparte el *script* en *Ruby* que emplea para su blog. 

Obviamente, el *script* necesita ser modificado para cada blog en cuestión, en estas cosas cada maestrillo tiene su librillo, pero la idea de Brett era que este ejemplo nos sirva para enterarnos de por dónde iban los tiros. 

En mis primeras intentonas no fui capaz de conseguir que el *script* funcionara y, como tampoco tenía muchas ganas (ni tiempo) para dar mis primeros pasos con *Ruby*, pues acabé por dejar la tarea en el apartado *Algún día* de [mi gestor de tareas favorito](http://www.asiertejada.com/things-se-actualiza-para-yosemite/).

Sin embargo, esta Semana Santa, y dado que había decido poner fin mi ausencia en este blog, decidí ponerme manos a la obra una vez más. 

Así que, ni corto ni perezoso, fui destripando concienzudamente el *script* línea por línea mientras que a su vez iba consultando en [*Dash*](https://itunes.apple.com/es/app/dash/id449589707?ls=1&mt=12&uo=4&at=1l3v5kR&ct=blog) [^7] la documentación oficial de *Ruby* e iba destripando las [*Expresiones Regulares*](https://es.wikipedia.org/wiki/Expresión_regular) con la ayuda de esa gran herramienta llamada [*RegExr*](http://regexr.com).

[^7]: Otra aplicación indispensable si estás tocando código en un *Mac*.

Y así, mediante prueba y error [^8], por fin conseguí de una manera más que aceptable la meta que me había propuesto, obteniendo como resultado algo parecido a lo que se puede ver en la figura que sigue a estas líneas. Todo gracias a la preciosidad de *script* que adjunto al final de esta entrada. Misión cumplida.

<figure markdown="1">
![]({{ site.url }}/assets/img/{{ page.images_folder }}/jekyll-post-from-byword-to-jekyll.png)
<figcaption><em>Byword</em>, <em>Marked</em> sin preprocesador y <em>Marked</em> con preprocesador</figcaption>
</figure>

<script src="https://gist.github.com/asiertejada/8432cbc74e5acb9004fb.js"></script>

[^8]: Prueba, error, fallo, fallo, arreglado, cuatro fallos más, vaya si resulta que los cajetines de código también los tengo con *Liquid*, prueba, error, etc.