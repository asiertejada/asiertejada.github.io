---
layout: blog
title:
date: 2014-07-24 23:55:00
categories: blog
tags: apple mac osx yosemite beta
featured_image: la-beta-de-os-x-yosemite-ya-esta-disponible-solucion-de-problemas.jpeg
images_folder: la-beta-de-os-x-yosemite-ya-esta-disponible-solucion-de-problemas
---
La beta pública de *OS X Yosemite* ya está disponible, sin embargo, su proceso de descarga no está exento de problemas. También, como era de esperar, empiezan a aparecer los primeros bugs. Si quieres probarla, lo mejor es tener paciencia y preparar tu *Mac* antes de proceder.<Sigue Leyendo>  
  
Tal y cómo se anunció ayer en muchos de los medios especializados, la descarga de la beta pública de [*OS X Yosemite*](http://www.apple.com/es/osx/preview/) ya se encuentra disponible para aquellos usuarios que se dieron de alta en el mencionado programa.   
  
## Requisitos  
* *OS X Mavericks* 10.9 o posterior instalado en nuestro *Mac*.  
* Al menos 2 GB de memoria.
* Por lo menos 8 GB disponibles en nuestro disco duro[^1].  
  
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Requisitos-Beta-Yosemite.png)
  
## Descargando la Beta Pública 1 de *OS X Yosemite*  
Para proceder con la descarga, tan sólo deberemos hacer *login* en la [web del programa](https://appleseed.apple.com/sp/betaprogram) (o darnos de alta si aún no lo hemos hecho).   
  
Una vez dentro, y tras pulsar en el enlace *Get Yosemite* recibiremos un código que podremos canjear en la *Mac App Store* para así iniciar la descarga del instalador.      
  
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Código-Beta-Yosemite.png)
  
## Errores en la Descarga y Solución  
Dada la gran expectativa creada por la primera (en la historia de *OS X*)  beta pública de *OS X Yosemite*, no es de extrañar que se estén dando algunas incidencias en este primer día. Algunas de los problemas más comunes están siendo:  
  
### La Web del Programa de Betas está Caída
Enhorabuena, acabas de tirar abajo la web de *Apple*. Bueno, tú y los miles de usuarios que están intentando descargar la beta.  
    
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Yosemite-Beta-Site-Down.jpg)  

**Solución:**    
Paciencia. Respira hondo y aprovecha para realizar los pasos previos que te garantizarán una [instalación segura de *OS X Yosemite*]({{ site.url }}/como-probar-os-x-yosemite-beta/).  
  
### *"Este código ya se ha canjeado"*  
Algunos usuarios están reportando que a la hora de introducir el código para iniciar la descarga se estan encontrando con este error, que parece ser un *bug* de la web de *Apple*. En mi caso no me ha pasado, pero el problema tiene fácil solución.    
  
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Código-Canjeado-Beta-Yosemite.png)
  
**Solución:**    

1. Ve a la pestaña *Comprado* de la *Mac App Store*.   
2. Pulsa ⌘+R para refrescar la pantalla y que aparezca *OS X Yosemite Beta 1* en la parte superior.   
3. Pulsa en el botón *Instalar* y la descarga comenzará.   
  
### *"No se ha podido descargar la aplicación*  
Si la descarga (de aproximadamente 5 GB) se interrumpe bien por culpa de *Apple*, bien por culpa de nuestro proveedor de servicios de internet, no debe cundir el pánico, podremos reanudar la descarga de forma muy sencilla.  
  
**Solución:**  
[Cómo Reanudar Descargas Interrumpidas](http://support.apple.com/kb/HT4485?viewlocale=es_ES&locale=en_US)

## ACTUALIZACIÓN (25/07/2014):
Al parecer, la solución proporcionada por Apple no funciona en numerosos casos, en los que la descarga se interrumpe por problemas de DNS.

La solución que están sugiriendo algunos usuarios es cambiar las DNS por 114.114.114.114 o por 8.8.8.8. En el siguiente video podéis encontrar un tutorial acerca del proceso:

<div class='embed-container'><iframe src="//www.youtube.com/embed/kgHX_2cMTKg" frameborder="0" allowfullscreen></iframe></div>

Otra solución que están reportando como válida es utilizar alguna VPN para realizar la descarga.

## Problemas Conocidos de la Beta  
Como cabría de esperar, a pesar de que esta primera beta pública es la misma que la cuarta beta del programa de desarrolladores, existen algunos *bugs* ya identificados que deberíamos conocer antes de proceder con la instalación. La propia *Apple* nos avisa de los siguientes:  
  
> ### *Safari*  
* *Safari* puede colgarse durante la reproducción de cierto contenido de *Netlflix*.  
>  
> ### *iPhoto* y *Aperture*  
* Las versiones de *iPhoto* 3.5.1 y *Aperture* 3.5.1 son las únicas soportadas por *OS X Yosemite*. En caso, de querer usarlas habrá que actualizarlas gratuitamente vía *Mac App Store*.
* Al entrar en el modo de *Edición* en *iPhoto* puede que se muestre una pantalla en negro en vez de la fotografía que queríamos editar.
* Las funcionalidad de *Photo Stream* y la compartición de fotos vía *iCloud* puede  que no funcionen correctamente si tenemos instaladas *iPhoto* y/o *Aperture*.  
> 
> ### *iCloud*  
* La página con el historial de compras compartidas está deshabilitada para las cuentas [*En Familia*](https://www.apple.com/es/ios/ios8/family-sharing/).  
* [*iCloud Drive*](https://www.apple.com/es/ios/ios8/icloud-drive/) puede aparecer vacío en el *Finder* tras la primera configuración. Para solucionar este problema, reinicia tu *Mac*.  
  
Yo añadiría que si queremos probar la nueva [*Spotlight*]({{ site.url }}/spotlight-alfred-y-launchbar-lanzadores-de-aplicaciones-para-mac/), deberemos configurar el idioma del *Mac* como inglés americano, ya que si lo dejamos en español no disfrutaremos de las nuevas sugerencias.     
  
## Instalación Segura  
Antes de lanzarnos a instalar deberemos tomar algunas precauciones lógicas. Lo primero de todo es hacer una copia de seguridad de nuestro *Mac*, bien con [*Time Machine*](https://www.apple.com/es/support/timemachine/), bien con nuestra aplicación de creación de *backups* favorita.    
  
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Time-Machine-Yosemite-Beta.png)
  
Una vez realizada nuestra copia de seguridad, lo recomendable es [instalar la beta de *Yosemite* en una partición separada de nuestra instalación de *Mavericks*]({{ site.url }}/como-probar-os-x-yosemite-beta/). De esta manera no sobrescribiremos nuestro sistema operativo funcional y evitaremos tener que restaurarlo si encontramos que alguna aplicación sin la que no podemos sobrevivir no funciona en *Yosemite*.    
  
## Probando *Yosemite*  
Una vez finalizado el proceso de instalación, podremos disfrutar de *OS X Yosemite Beta 1* así como de las futuras betas públicas[^2]. Así que sólo queda disfrutar de esta vista previa del futuro sistema operativo de *Apple*, y si nos topamos con algún *bug* reportarlo mediante la aplicación *Feedback Assistant*.  
  
![]({{ site.url }}/assets/img/{{ page.images_folder }}/Feedback-Assistant-Yosemite-Beta.png)  

## ACTUALIZACIÓN (19/10/2014)

Ahora que la versión definitiva ya está disponible, os recomiendo que leáis el siguiente artículo sobre [cómo instalar *OS X Yosemite* de forma segura](asiertejada), en el que explico, entre otras cosas, cómo recuperar el espacio de la partición que hemos usado para probar la beta.
  
  
[^1]: Si vamos a hacer un uso más o menos continuado de la beta es recomendable disponer de entorno unos 15-25 GB libres.  
  
[^2]: Que al parecer se publicarán con menor frecuencia que las betas del programa de desarrolladores. 