---
layout: blog
title: Cómo Probar OS X Yosemite Beta
date: 2014-06-08 12:00:00
categories: tutoriales
tags: apple beta mac osx yosemite
featured_image: como-probar-os-x-yosemite-beta.png
images_folder: como-probar-os-x-yosemite-beta
---
Probar la primera beta de *OS X Yosemite* es un proceso sencillo, pero siempre habrá que tomar algunas precauciones, siendo la más básica de todas el no instalar la beta en la misma partición en la que tengamos instalado nuestro sistema operativo principal.<Sigue Leyendo>

En la [*keynote* principal de la pasada *WWDC*](http://www.apple.com/apple-events/june-2014/) *Apple* presentó la que será la versión décima de su sistema operativo para *Mac*: [*OS X Yosemite*](https://www.apple.com/osx/preview/).   

Tanto si eres desarrollador, como si te has unido al nuevo programa de prueba de betas de *OS X* que ha abierto recientemente *Apple*, el [*OS X Beta Program*](https://appleseed.apple.com/sp/betaprogram/), en este *post* encontrarás una manera segura de instalar *Yosemite* en tu *Mac* habitual (si dispones de otro *Mac* dedicado exclusivamente al desarrollo, no necesitarás este tutorial).  

##  Requisitos previos    
Antes de embarcarse a probar *OS X Yosemite Beta*, habrá que cumplir los siguientes requisitos:  

* **Descargar *OS X Yosemite***: para ello será necesario estar registrado en el programa de desarrolladores *Mac* de *Apple*, [*Mac Developer Program*](https://developer.apple.com/programs/mac/), cuya cuota es de $99/año. Esto nos permitirá descargar el instalador de la *OS X Yosemite Dev Preview* desde la *Mac App Store*[^1].  

[^1]: Si no habrá que buscar una manera alternativa de poder conseguir dicho instalador. Y hasta ahí puedo leer.  

* **Comprobar que nuestro *Mac* cumple los requisitos de sistema**: lo primero será chequear en qué *Mac* pretendemos instalar *Yosemite*.  Es tan sencillo como pulsar en el menú de *Apple* (el que tiene como icono el logo de *Apple*) de la barra de menús, posteriormente seleccionar *Acerca de este Mac*, y finalmente pulsar el botón *Más información...* para obtener una imagen como la siguiente:  

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Acerca-de-este-Mac.png)    

Una vez sepamos exactamente con qué *Mac* estamos trabajando, deberemos compararlo con el listado de *Mac* compatibles con *OS X Yosemite Beta*, que según [*ArsTechnica*](http://arstechnica.com/apple/2014/06/psa-the-idevices-and-macs-that-will-support-ios-8-and-os-x-10-10/) es el siguiente:  

> * *iMac* (Mediadios 2007 o posterior)
>	* *MacBook* (13 pulgadas *Aluminum*, finales 2008), (13 pulgadas, principios 2009 o posterior)
>	* *MacBook Pro* (13 pulgadas, mediados 2009 o posterior), (15 pulgadas, mediados/finales 2007 o posterior), (17 pulgadas, finales 2007 o posterior)
>	* MacBook Air (Finales 2008 o posterior)
>	* Mac Mini (Principios 2009 o posterior)
>	* Mac Pro (Principios 2008 o posterior)
>	* Xserve (Principios 2009)  

* **Disponer de al menos 25GB disponibles de disco duro**: el mínimo requerido son 15GB, pero para que no haya ninguna merma de rendimiento siempre es mejor disponer de un extra de espacio.  

* **Hacer una copia de seguridad de nuestro *Mac***: en teoría nada debería salir mal, pero como vamos a andar tocando las particiones de nuestros discos, nunca está de más hacer una copia de seguridad con [*Time Machine*](http://support.apple.com/kb/HT1427?viewlocale=es_ES)[^2], por si las moscas.  

[^2]: O con vuestro programa de copias de seguridad favorito, o con varios, dependiendo del nivel de paranoia de cada uno.    

## Crear una partición para *OS X Yosemite*  
Antes de proceder con la instalación de *OS X Yosemite*, habrá qe realizar una partición exclusiva para él, de manera que nos aseguremos que nuestra instalación principal de *OS X* queda preservada. De esta manera conseguiremos un arranque dual de nuestro *Mac*, donde podremos elegir qué sistema operativo queremos arrancar, y también podremos desinstalar *Yosemite* de una manera segura.  

Para crear una partición utilizaremos la *Utilidad de Discos* y, una vez abierta (se encuentra dentro de *Aplicaciones*, en la carpeta *Utilidades*), seguiremos los siguientes pasos:  

1. Elegir el disco en el que queremos crear la partición, en el caso de que nuestro *Mac* disponga de varias unidades[^3].
2. Pulsar en la pestaña *Particiones*.
3. Hacer clic en el botón *+* debajo del diagrama de disposición de particiones.
4. Seleccionar la nueva partición creada.
5. Cambiarle el nombre y especificar el tamaño (25GB).
6. Pulsar el botón *Aplicar*.    

[^3]: Es posible instalar *OS X Yosemite* en un disco duro extraíble o una memoria *flash* de tamaño suficiente. Sin embargo, el rendimiento del sistema operativo bajará sensiblemente. En caso de optar por esta última opción, obviamente, sólo podremos ejecutar *Yosemite* cuando la unidad externa esté conectada.

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Utilidad-de-Discos.png)  

## Instalar *OS X Yosemite* en la nueva partición  
Una vez hecha nuestra copia de seguridad, con el instalador de *Yosemite* descargado y con su partición creada, es hora de instalar *OS X 10.10*.  

Para ello los pasos a seguir son muy sencillos:  

1. Buscar el instalador que hemos descargado en la carpeta *Aplicaciones* y ejecutarlo.
2. Elegir como destino la partición que hemos creado anteriormente.
3. Esperar a que se instale completamente. Nuestro *Mac* se reiniciará automáticamente en *Yosemite* una vez finalizado el proceso de instalación y ya podremos disfrutar de *OS X Yosemite*.

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Instalar-OS-X-10.10.png)

## Arranque dual *Mavericks-Yosemite*  
Con el anterior proceso acabado, dispondremos tanto de *Yosemite* como de *Mavericks* instalados en nuestro *Mac*.   

Para elegir qué sistema operativo deberá iniciarse, deberemos dejar pulsada la tecla *Opción* (⌥) durante el arranque, y posteriormente elegir la partición adecuada.  

De esta manera, podremos continuar trabajando con nuestro *Mac* a la vez que probamos el último sistema operativo de *Apple*, mientras seguimos a la espera de que se publique su versión definitiva.

## Desinstalando *Yosemite* (en un futuro)    
Una vez nos hayamos cansado de probarlo, o bien estemos en disposición de actualizar nuestro sistema operativo a la versión definitiva de *OS X 10.10*, para desinstalar la beta de *Yosemite*, lo único que deberemos hacer es borrar la partición desde la *Utilidad de Discos* y redimiensionar nuestro disco duro para así recuperar el espacio. Un proceso simple y seguro.   

## ACTUALIZACIÓN (19/10/2014)
Ahora que la versión definitiva ya está disponible, os recomiendo que leáis el siguiente artículo sobre [cómo instalar *OS X Yosemite* de forma segura]({{ site.url }}/como-instalar-os-x-yosemite/), en el que explico, entre otras cosas, cómo recuperar el espacio de la partición que hemos usado para probar la beta.

**Fuente:** [*OSXDaily*](http://osxdaily.com/2014/06/05/install-os-x-yosemite-separate-partition/)
