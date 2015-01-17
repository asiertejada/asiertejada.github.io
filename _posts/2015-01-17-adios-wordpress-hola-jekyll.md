---
layout: blog
title: Adiós WordPress. Hola Jekyll.
date: 2015-01-17 11:26:00
categories: blog
tags: github jekyll wordpress 
featured_image: adios-wordpress-hola-jekyll.png
images_folder:
external_url:
---
Nos ha llevado su tiempo pero <strike>de una maldita vez</strike> finalmente se puede considerar que la migración de este blog de *WordPress* a *Jekyll* ha concluido. Pero, ¿por qué nos hemos tomado la molestia?<Sigue Leyendo>

Como no podías ser menos, tras la consabida migración, toca el *post* obligatorio del porqué del cambio a Jekyll. Vayamos por partes.


## El alojamiento: *Netfirms*
Este blog ha estado alojado durante casi dos años en los servidores de [*Netfirms*](http://www.netfirms.com), empresa que, por más que quisiera, no puedo recomendar. Tras un primer año de oferta a un precio más que razonable, una vez pasado dicho año [^1] el precio de su servicio de alojamiento se vuelve desorbitado si comparamos los servicios que ofrecen con [otras alternativas](http://www.stablehost.com) que existen en el mercado actual.

[^1]: Momento en el cual debería haber abandonado *Netfirms*, pero que en el cual, debido a motivos laborales, no tuve el suficiente tiempo para planificar una migración en condiciones.

Así que estaba claro que este año había que cambiar de *hosting* sí o sí. Es decir, tocaba migrar seguro. Lo que aún no se me pasaba por la cabeza era el cambio de plataforma, ya que en un inicio lo planeado era cambiar la instalación de *WordPress* a otro proveedor de alojamiento. Qué ingenuo era.


## La plataforma: *WordPress*
Aquellos que hayáis seguido mínimamente este blog habréis podido deducir que se trataba de una instalación de *WordPress* autoalojada. Siempre he sido un fan de *WordPress* y es que su potencia y su más que asequible curva de aprendizaje son innegables [^2].

[^2]: Ahora es cuando viene la parte del *"Sin embargo...".*

Sin embargo, para un proyecto tan modesto como este blog personal, dicha potencia es un arma de doble filo ya que, mientras por un lado no deja de estar desaprovechada, por el otro, y al mismo tiempo, le resta bastante flexibilidad.

En mi caso la instalación se había convertido en una auténtica momia. La combinación entre el [tema elegido](https://array.is/themes/typable-wordpress-theme/) y los *plugins* empleados no acababa de engrasar perfectamente y la batalla contra el tiempo de carga acabó por suponer demasiados quebraderos de cabeza y escasos réditos.

Pero claro, es lo que tienen los [sitios web dinámicos](http://en.m.wikipedia.org/wiki/Dynamic_web_page) tipo *WordPress* y demás [sistemas de gestión de contenidos](http://es.m.wikipedia.org/wiki/Sistema_de_gesti%C3%B3n_de_contenido) [^3].

[^3]: De las ventajas que nos aporta un sitio web estático frente a los anteriores hablaremos un poco más adelante.

Así que la web andaba un poco patatera pero yo estaba encantado con su estética y con buena parte de su funcionalidad. La encrucijada estaba clara: cambiar de plataforma manteniendo el diseño. Tocaba barajar opciones.


## La nueva plataforma: *Jekyll*
Por lo tanto, a la necesidad de cambiar de proveedor de alojamiento se sumaba también la nueva decisión de buscar una plataforma alternativa a la mastodóntica *WordPress*. Pero, ¿cuál?

Tenía claro que los requisitos mínimos que la plataforma sustituta debía superar tenían que ser, por lo menos, los siguientes:

* **Gratuita**: No estaba por la labor de pasarme a una plataforma de pago para un blog personal. Opciones estilo [*SquareSpace*](http://www.squarespace.com) o [*Ghost*](https://ghost.org) quedaban descartadas desde un inicio [^4].
* **Personalizable**: Si bien esta migración me daba la oportunidad de rediseñar la web, no quería que su diseño cambiara drásticamente, sino más bien todo lo contrario: mantener el diseño actual a la vez que realizaba ciertos cambios/mejoras. Esto dejaba fuera plataformas como [*Medium*](https://medium.com/@asiertejada) [^5], [*Tumblr*](http://asiertejada.tumblr.com), etc.
*  **Estática**: Con *WordPress* ya había aprendido suficiente *PHP* y *SQL* como para sobrevivir durante una temporada más que larga, así que, ya que iba a cambiar de plataforma, ¿por qué no a aprovechar para empezar a gozar de las ventajas de un sitio estático y para mejorar mis conocimientos de *HTML*, *CSS* y *JavaScript*? Alternativas del tipo [*Drupal*](https://www.drupal.org) o [*Joomla*](http://joomla.org) ni se pasaban por la cabeza.
* **Código abierto**: Soy un gran defensor de la [iniciativa del código abierto](http://opensource.org), ya que creo que gracias a ella el aprendizaje de nuevas tecnologías es más sencillo, más cercano y más asequible para cualquier persona. Cualquier sistema propietario quedaba excluido de entrada.

[^4]: Bueno, realmente, *Ghost* fue la otra candidata hasta el final, pero como veremos en breve sucumbió ante las bondades de *Jekyll*.

[^5]: Una auténtica maravilla de plataforma que cada día me gusta más. De hecho el cambio de tipografía y del formato de las entradas de este blog se ha visto parcialmente inspirada por ella.

Por lo tanto, tras esta criba, la única opción que me quedaba era [*Jekyll*](http://jekyllrb.com). 

Veamos: gratuita, *check*, personalizable, *check*, estática, *check*, código abierto, *check*, usada por [*Brett Terpstra*](http://brettterpstra.com), *check*, *check* [^6].

[^6]: Si bien el que escribe no goza de las habilidades del señor Terpstra, y a pesar de que mis conocimientos de *Ruby*, *Phyton* y *Liquid* son bastante escasos, esto no ha servido más que de acicate para empezar a aprender sus rudimentos. De hecho, fue otro de los motivos que inclinó la balanza hacia el lado de *Jekyll*.

Luego *Jekyll* cumplía con creces los requisitos mínimos preestablecidos, especialmente el de la estática lo cual nos iba a aportar las siguientes ventajas [^7]:

* **Simplicidad**:  
	* **Adiós base de datos**: Al contrario que *WordPress* o los demás gestores de contenidos, *Jekyll* no emplea una base de datos sino que todas las entradas y páginas son generadas en *HTML* antes de ser publicadas. Esto es genial para el tiempo de carga de nuestra página web ya que no se realizan llamadas a la base de datos durante la carga.
	* **Adiós sistema de gestión de contenidos**: Simplemente deberemos escribir nuestros textos en *Markdown* y *Jekyll* se encargará de generar nuestro contenido estático. 
	* **Velocidad**: Limitar las funcionalidades a lo básico, carecer de una base de datos y servir sólo contenido estático hará que el número de peticiones *HTTP* de nuestra web sea muy reducido [^8]. Esto se traducirá en mayores velocidades de carga.
	* **Minimalismo**: Nuestro sitio web no incluirá en absoluto ninguna funcionalidad que no estemos usando. Es decir, no desaprovechará ningún recurso.
* **Control del diseño**: Con *Jekyll* gastaremos menos tiempo con plantillas creadas por terceros para en vez de ello crear nuestro propio tema o adaptar sencillos temas base.
* **Seguridad**: La mayoría de amenazas que sufren *WordPress* y los demás gestores no afectan a *Jekyll* ya que este carece de base de datos y tampoco usa *PHP*. Luego nos olvidaremos de actualizaciones de seguridad y de pesados *plugins* de seguridad.

[^7]: **Fuente:** [*Smashing Magazine*](http://www.smashingmagazine.com/2014/08/01/build-blog-jekyll-github-pages/)

[^8]: Tan reducido o no, como nosotros queramos.

## El nuevo alojamiento y algo más: *Github Pages*
La última ventaja, y otro de los factores decisivos del cambio a *Jekyll*, consiste en la posibilidad de alojar nuesta web gratuitamente en [*Github*](http://es.wikipedia.org/wiki/GitHub) a través de su servicio [*Pages*](https://pages.github.com).

Pero no sólo nos ahorraremos el tener que contratar un servicio de *hosting*, sino que a su vez disfrutaremos de un control de versiones [^9] y podremos realizar el desarrollo de nuestro blog en local [^10]. En otras palabras, podremos trastear con nuestro blog en nuestra máquina y, una vez estemos satisfechos con el resultado, lo volcaremos a nuestro repositorio en *Github* con un sólo clic para que sea publicado automáticamente.

[^9]: Y aprenderemos [*Git*](http://es.wikipedia.org/wiki/Git) de paso.

[^10]: Con *WordPress* podíamos hacer algo parecido con [*MAMP*](http://www.mamp.info/en/), pero de nuevo estábamos matando moscas a cañonazos.

## El resultado
Bueno, el resultado son estas líneas que estas leyendo actualmente. Si bien aún no estoy del todo satisfecho con él (hay muchas funcionalidades que he tenido que sacrificar con la migración, y el nuevo diseño aún adolece de mi inexperiencia), sí que creo que por el momento se puede considerar que goza de la viabilidad mínima como para volver a empezar a escribir tras casi dos meses de sequía [^11].

En un futuro no muy lejano volveremos a hablar de los cambios que ha sufrido este blog y de los que tengo en mente, pero por el momento lo dejaremos aquí.

Al igual que aquél, hemos cumplido nuestras peores amenazas. *We're back*.



[^11]: En el fondo, y por más que el viaje también sea muy interesante, de eso se trata… ¿No?