---
layout: blog
title: Cómo Instalar OS X Yosemite de Forma Segura
date: 2014-10-19 07:15:00
categories: tutoriales
tags: apple mac osx yosemite
featured_image: como-instalar-os-x-yosemite.jpg
images_folder: como-instalar-os-x-yosemite
---
La versión final de *OS X* 10.10 vio la luz el pasado jueves 16 de octubre. Como siempre que toca actualizar el sistema operativo de nuestros *Macs*, nunca está de más seguir un procedimiento seguro a la hora de instalar *OS X* *Yosemite*.<Sigue Leyendo>

Después de meses de versiones betas tras ser anunciada en la pasada [conferencia de desarrolladores](https://developer.apple.com/wwdc/), por fin nos ha sido publicada la versión final de *OS X Yosemite*, repleta no sólo de cambios en la interfaz y demás elementos gráficos, sino también de gran cantidad de  funcionalidades nuevas que acercan el sistema operativo de nuestros *Mac* a *iOS*, consiguiendo que ambos se integren de maravilla.

No es de extrañar que con todo el *hype* que ha creado esta última iteración de *OS X* nos lancemos de cabeza e impacientes a actualizar nuestros *Mac*. Sin embargo, si queremos evitar numerosos problemas, deberemos planificar esta actualización y realizarla de una manera segura.

## Pasos Previos

### Comprobar que Cumplimos los Requisitos del Sistema
Antes de empezar a volvernos locos, lo primero que deberemos comprobar es que nuestro *hardware* cumple con los requisitos mínimos para instalar *OS X Yosemite* en él. 

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Macs.png)

Si vas a actualizar desde *Mavericks*, puedes estar tranquilo ya que los requisitos son los mismos. Si tu sistema operativo es *Mountain Lion* o anterior, entonces tu dispositivo deberá encontrarse en la siguiente lista:

* *iMac* (*Mid-2007* o posterior)
* *MacBook* (13" Aluminio *Late 2008* o posterior), (13" *Early 2009* o posterior)
* *MacBook Pro* (13", *Mid-2009* o posterior), (15" *Mid/Late 2007* o posterior), (17" *Late 2007* o posterior)
* MacBook Air (*Late 2008* o posterior)
* Mac Mini (*Early 2009* o posterior)
* Mac Pro (*Early 2008* o posterior)
* Xserve (*Early 2009*)

En cuanto a la *RAM*, *Apple* nos avisa de que el mínimo necesario será de 2 GB, aunque instalar *Yosemite* en un dispositivo con tan poca memoria no es en absoluto recomendable y tal vez sea buen momento para incrementarla.

Igualmente, si bien el mínimo de espacio disponible en disco debe ser de 8 GB, deberíamos asegurarnos de disponer de por lo menos 30 GB libre sólo para el sistema operativo, si queremos un comportamiento fluido.

### Obtener una ID de Apple
Sería muy extraño que estés leyendo estas líneas y no dispongas de una *ID* de *Apple*, requisito fundamental para descargar gratuitamente *OS X Yosemite* de la *Mac App Store*, pero por si acaso lo dejamos caer aquí.

### Actualizar las Aplicaciones *(Opcional)*
Este es un paso opcional pero, dado que muchos desarrolladores ya habían actualizado sus aplicaciones antes incluso del lanzamiento de la versión final de *Yosemite*, seguro que muchas de ellas ya estarán disponibles en la pestaña de actualizaciones de la *Mac App Store*. Cuanto más actualizado esté nuestro *Mac* antes de actualizar el sistema operativo mejor.

### Realizar una Copia de Seguridad
A pesar de que las actualizaciones de *Mac OS X* no suelen dar problemas, <span class="highlight">**SIEMPRE**</span> deberemos hacer al menos una copia de seguridad de nuestras máquinas. Y digo al menos porque en mi caso, además de usar *Time Machine*, hago otra copia extra en otro disco aparte que es un clon exacto de mis discos duros. Para ello utilizo la maravillosa [*Carbon Copy Cloner*](https://bombich.com/), si bien otra alternativa por la que también optan muchos usuarios es [*Super Duper*](http://www.shirt-pocket.com/SuperDuper/). Más vale prevenir que curar.

### Decidir Qué Tipo de Instalación Vamos a Hacer
Dependiendo de lo que pretendamos, podemos elegir entre varios tipos de actualización, y en función de nuestra elección deberemos seguir unos un otros pasos.

1. **Realizar una instalación limpia:** si el sistema operativo de nuestro *Mac* lleva tiempo sin ser actualizado, o si hemos estado trasteando con la versión beta en nuestro disco duro principal (no en una partición), o simplemente si el rendimiento de nuestra máquina ha bajado sustancialmente, esta puede ser la mejor opción. 

2. **Actualizar encima de nuestro antiguo sistema operativo:** si no se da ninguno de los casos anteriores, podemos optar por realizar un simple *upgrade*, ya que en la mayoría de los casos no suele dar problemas. En mi caso, esta vez he elegido actualizar y tan sólo me he encontrado con un problema, debido a haber tenido las betas de *OS X Yosemite* instaladas en una partición. 

3. **Instalar *OS X Yosemite* en una partición:** si crees que el nuevo aspecto gráfico no es para ti, o intuyes que el rendimiento de tu *Mac* puede empeorar con *Yosemite*, o, en definitiva, piensas que vas a tener que volver a *Mavericks* en breve, esta es tu mejor opción. 

## Descargar el instalador de *OS X Yosemite*
Una vez realizados los anteriores pasos previos, que son comunes para cualquiera que sea el tipo de instalación que hayamos decidido realizar, llega la hora de descargarse el instalador de *OS X Yosemite*.

Encontrarlo no será difícil en la *Mac App Store*, lo que si que será harina de otro costal será descargarlo, ya que el archivo pesa más de 5 GB, por lo que deberemos ser pacientes mientras se descarga [^1].

[^1]: Si estás leyendo esto, al menos habrás evitado el cuello de botella de los primeros días, con lo que posiblemente tu descarga será más ágil.

Sin embargo, una vez descargado el instalador, todavía deberemos realizar algunos pasos extra antes de proceder con la instalación.

### Poner una Copia del Instalador a Buen Recaudo
Sea cual sea la opción de actualización que vayamos a seguir, siempre es buena idea realizar una copia del instalador fuera de la carpeta *Aplicaciones* ya que una vez terminada la instalación con éxito *OS X Yosemite* el instalador se autoborra de dicha carpeta.

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Instalador-a-Buen-Recaudo.jpg)

Así, si queremos actualizar otros *Macs* o queremos crear un disco de arranque no tendremos que volver a descargarnos los 5 GB. 

## Realizando una Instalación Limpia
Si elegimos esta opción, debemos tener claro que <span class="highlight">el disco en el que vayamos a instalar *OS X Yosemite* será **borrado y perderemos todos sus datos**, por lo que es de vital importancia realizar una copia de seguridad previa.</span>

A continuación los principales pasos a seguir.

### Crear un Disco de Arranque con el Instalador
Igualmente, para este tipo de instalación, necesitaremos crear un disco de arranque con el instalador de *OS X Yosemite*.

Los requisitos para crearlo serán los siguientes:

* Disponer de una copia del instalador de *OS X Yosemite*.
* Disponer de un disco con al menos 8 GB y con formato *Mac OS Plus (con registro)* y con esquema de particiones *GUID*. <span class="highlight">**Importante:** Aunque el disco que tengamos ya esté en este formato, el disco **será formateado** durante el proceso de creación del disco de arranque.</span>
* Disponer de privilegios de administrador en el *Mac* que vayamos a usar para crearlo.

Para crearlo seguiremos los siguientes pasos:

1. Formatear el disco, si es necesario, y renombrarlo como *Untitled* [^2].
2.  Asegurarse de que el instalador está en la carpeta *Aplicaciones* [^21].
3. Copiar el siguiente comando para *Terminal*:
		
		sudo /Applications/Install\ OS\ X\ Yosemite.app/Contents/Resources/createinstallmedia --volume /Volumes/Untitled --applicationpath /Applications/Install\ OS\ X\ Yosemite.app --nointeraction
		
4. Abrir una ventana de *Terminal* (que se encuentra en *Aplicaciones/Utilidades*).
5. Pegar y ejecutar el anterior comando.
6. Escribir nuestra contraseña de administrador.

Si hemos seguido los pasos al pie de la letra, empezarán a salir una lista de tareas en la ventana del *Terminal*:

	Erasing disk: 0%... 10%... 20%...
	Copying installer files to disk… 
	Copy complete. Making disk bootable… 
	Copying boot files… 
	Copy complete. 
	
Una vez aparezca *Copy complete.* tendremos nuestro disco de arranque listo.

**Nota:** Realizar este paso resulta más que interesante aunque no vayamos a realizar una instalación limpia. Yo lo recomiendo hacer siempre, ya que disponer de un disco de arranque nos puede sacar de más de un apuro.

[^2]: Realmente estos dos pasos sólo son necesarios si queremos usar el mismo código del paso 3. El disco duro podrá llamarse como quiera y el instalador podrá estar donde sea, pero en ese caso deberemos modificar las rutas del comando apropiadamente.

[^21]: Realmente estos dos pasos sólo son necesarios si queremos usar el mismo código del paso 3. El disco duro podrá llamarse como quiera y el instalador podrá estar donde sea, pero en ese caso deberemos modificar las rutas del comando apropiadamente.

### Reiniciar Usando el Disco de Arranque con el Instalador
Con nuestro disco de arranque conectado dispondremos dos alternativas:

1. Reiniciar como siempre y mantener pulsada la tecla *Opción* (⌥) y, una vez reiniciado nuestro *Mac*, elegir el disco de arranque con el instalador.
2. Ir a Preferencias del Sistema/Disco de Arranque y seleccionar nuestro disco de arranque con el instalador.

### Borrar Nuestro Disco Principal
Una vez que arranquemos con este disco estaremos en el [modo de recuperación](https://support.apple.com/kb/HT4718?viewlocale=es_ES&locale=es_ES), desde el cual podremos usar las utilidades *OS X*.

Así, lo primero que haremos será acceder a la *Utilidad de Discos* y borrar nuestro disco principal, ya que habremos realizado una copia de seguridad de él anteriormente. Con él borrado, volveremos al menú de utilidades y estaremos listos para instalar *OS X Yosemite*.

##  Actualizando Encima de una Versión Anterior de OS X
En caso de realizar directamente un *upgrade*, habrá que realizar algunas tareas previas que nos ayudarán a realizar un instalación lo más limpia posible.

### Verificar y Reparar Nuestro Disco y sus Permisos
Una buena práctica antes de realizar una actualización de nuestro sistema operativo es abrir la *Utilizad de Discos* (en *Aplicaciones/Utilidades*) y verificar, y en caso necesario reparar posteriormente, tanto el disco desde el que corre nuestro sistema como sus permisos. Cuanto más tiempo haya pasado sin que hayamos hecho esta simple operación, más recomendable es hacerla. De esta manera el instalador no encontrará problemas extraños. [^3]

[^3]: Este paso puede ser incluido en el siguiente (*Recuperar el Espacio de la Partición Usada para Probar la Beta*) si nos encontramos en el supuesto que en él se menciona.

###  Recuperar el Espacio de la Partición Usada para Probar la Beta
Si [probaste la beta de *Yosemite* en una partición]({{ site.url }}/como-probar-os-x-yosemite-beta/), ahora ya no la necesitarás más y deberías borrarla y recuperar su espacio. Sin embargo, esto no es tan sencillo como parece y hay que entrar en modo de recuperación para conseguirlo:

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Recuperar-Espacio-Partición.png)

1. Reiniciar nuestro *Mac*, manteniendo la combinación `⌘+R` durante el reinicio.
2. Abrir la *Utilidad de Discos*.
3. Seleccionar el disco que contiene la partición a borrar.
4. Pulsar sobre la pestaña *Particiones.*
5. Seleccionar la partición a borrar.
6. Eliminarla pulsando sobre el botón con el símbolo `—`.
7. Seleccionar la partición restante.
8. Redimensionar la partición original bien mediante la casilla tamaño [^4], o bien arrastrando su contorno en el mapa de particiones.
9. Pulsar el botón *Aplicar*.

[^4]: Si no sabemos el tamaño exacto del disco bastará con poner un número mayor y aparecerá el valor exacto en la casilla.

De esta manera evitaremos mensajes de error y recuperaremos el espacio de nuestro disco antes de realizar la actualización.

### Vaciar la Carpeta usr/local *(Sólo Desarrolladores)* 
En el caso de usar nuestro *Mac* para desarrollo con otro software distinto a *Xcode*, deberemos quitar de la carpeta *usr/local* todo aquello que no sea de *Apple*. En caso contrario, tal y como comenta [Jim Lindley en su blog](https://jimlindley.com/blog/yosemite-upgrade-homebrew-tips/), nos arriesgamos a sufrir pausas durante la actualización de hasta 12 horas.

## Instalar *OS X Yosemite* en una partición
Si has tomado la vía más precavida te recomiendo que visites este artículo sobre [cómo instalar *Yosemite* en una partición]({{ site.url }}/como-probar-os-x-yosemite-beta/), y este otro sobre [*RebootToHDD*]({{ site.url }}/reboottohdd-como-cambiar-rapidamente-entre-mavericks-y-la-beta-de-yosemite/), una utilidad que te permitirá "saltar" entre particiones de una manera ágil.

## Instalar *OS X Yosemite*
Y por fin, y tras una buena cantidad de pasos previos y precauciones estamos listos para instalar *OS X Yosemite*. 

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Instalar-OS-X-Yosemite.png)

## ACTUALIZACIÓN (23/10/2014): Desactivar Trim Enabler o similares

Como bien explican los desarrolladores de *Trim Enabler* en su [web](http://www.cindori.org/trim-enabler-and-yosemite/), *Apple* ha introducido en *Yosemite* un nuevo requerimiento de seguridad llamado *kext signing*, que viene activado por defecto.

Si dicha extensión se encuentra activa, y nuestro disco principal (donde vamos a instalar el sistema operativo) es un disco *SSD* al que le hemos activado el [*TRIM*](http://es.wikipedia.org/wiki/TRIM) mediante software (*Trim Enabler*, etc.), podemos encontrarnos con que al iniciar nuestro *Mac* aparece el fatídico signo de prohibido sobre fondo gris y no podemos avanzar más allá de él.

![]({{ site.url }}/assets/img/{{ page.images_folder }}/Signo-de-Prohibido.png)

A partir de la versión 3.3 de *Trim Enabler* cuando arranquemos la aplicación nos avisará de la problemática y nos pedirá permiso para desactivar *kext signing*, con lo que en futuros arranques no habrá problemas, antes de activar el *TRIM*.

Así la sequecia más segura sería actualizar a la versión 3.3 y desactivar *Trim Enabler* antes de instalar *OS X Yosemite*, y una vez actualizados el sistema volver a activar el *TRIM*.

Sin embargo, hay que tener en cuenta que *kext signing* se encuentra alojado en la memoria *NVRAM/PRAM*, por lo que aunque esté desactivado, si reseteamos por cualquier motivo dicha memoria lo volveremos a activar.

