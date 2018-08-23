Aquí está el segundo número de Esta Semana en el Desarrollo de Lubuntu. Puede leer el número de la semana pasada [aquí](https://lubuntu.me/this-week-in-lubuntu-development-1/).

  

# Cambios

## General

 * Lanzamos la Beta Final 18.04 esta semana. Puede encontrar el anuncio [aquí](https://lubuntu.me/lubuntu-bionic-beaver-final-beta-has-been-released/).
    * El [error de LVM cifrado](https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/+bug/1759732) que describimos la semana pasada se ha corregido (gracias a [Steve Langasek](https : //launchpad.net/~vorlon)!).
    * Todavía estamos trabajando duro para tratar de encontrar qué está causando [el otro error](https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174) que está haciendo que Lubuntu sea imposible de instalar al seleccionar "Instalar Lubuntu" en la pantalla de inicio. Por ahora, puedes seleccionar "Probar Lubuntu", ir al instalador desde allí, y funcionará. ** Por favor, evite presentar errores duplicados, aunque siempre puede marcar ese error como que también le afecta. **
 * Dado que las semillas de Lubuntu son diferentes, necesitamos ajustes en las herramientas para poder soportar la opción de instalación mínima. Esos cambios han llegado ya, y ahora se está utilizando esta opción.
    * [https://code.launchpad.net/~tsimonq2/livecd-rootfs/lubuntu-seed-mangling/+merge/342064](https://code.launchpad.net/~tsimonq2/livecd-rootfs/lubuntu- seed-mangling / + merge / 342064)
    * [https://launchpad.net/ubuntu/+source/livecd-rootfs/2.517](https://launchpad.net/ubuntu/+source/livecd-rootfs/2.517)
    * Gracias a [Iain Lane](https://launchpad.net/~laney)!
    * Esto se agrega a la semilla: [https://github.com/lubuntu-team/lubuntu-seeds/commit/806639acd4f2c1720da06b9cde9a6af11013c07c](https://github.com/lubuntu-team/lubuntu-seeds/commit/806639acd4f2c1720da06b9cde9a6af11013c07c)
 * Se ha emitido una actualización estable de lanzamiento a los usuarios de Lubuntu 16.04 solucionando algunos problemas de LXPanel después de cambiar a un lenguaje de lectura de derecha a izquierda.
    * [https://bugs.launchpad.net/ubuntu/xenial/+source/lxpanel/+bug/1537334](https://bugs.launchpad.net/ubuntu/xenial/+source/lxpanel/+bug/1537334 )
    * [https://launchpad.net/ubuntu/+source/lxpanel/0.8.2-1ubuntu2.1](https://launchpad.net/ubuntu/+source/lxpanel/0.8.2-1ubuntu2.1)

## Lubuntu Next

 * Según el consejo de la Junta técnica de Ubuntu, Lubuntu ha ajustado la duración del soporte de Lubuntu Next a solo nueve meses, oficialmente.
    * [https://code.launchpad.net/~tsimonq2/ubuntu-archive-publishing/lubuntu-next-support-cycle-adjustment/+merge/342475](https://code.launchpad.net/~tsimonq2/ ubuntu-archive-publishing / lubuntu-next-support-cycle-adjustment / + merge / 342475)
    * ¡Gracias a [Steve Langasek](https://launchpad.net/~vorlon)!

## Infraestructura y cambios de proyecto

Se ha [propuesto](https://lists.ubuntu.com/archives/ubuntu-release/2018-April/004387.html) para el Equipo de lanzamiento de Ubuntu y otros sabores (así como los equipos de escritorio y servidor) que debemos suspender las "milestones"  alfa y beta 1 a favor de las pruebas coordinadas mensuales de todos las ISO que enviamos para lanzamiento. Siéntase libre de enviarnos sus comentarios así sea posteando a continuación o en la lista de correo si tiene algo que se deba considerar.

# Hoja de Ruta

Puede encontrar el calendario de lanzamientos de Bionic Beaver [aquí](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule). Esta semana es la fecha límite de traducción para el Kernel Freeze y Bionic.

En términos sencillos, esto significa que a partir del jueves a las 21 UTC, el uso de Linux 4.14 por parte de 18.04 es definitivo, y si desea ayudar con la traducción de cualquiera de los programas [enumerados en la página wiki](https: // wiki. ubuntu.com/NonLanguagePackTranslationDeadline), no hay garantías de que sus traducciones sean incluidas en el lanzamiento (aunque ciertamente se incluirán en el lanzamiento de 18.10 y en adelante, por lo que recomendamos la ayuda para traducir esas aplicaciones independientemente del estado del lanzamiento :)) .

En términos técnicos, esto significa que, si bien el kernel de Linux todavía será ABI (como es habitual con las actualizaciones del kernel, desafortunadamente), no afectará la cadena de versión del parcheado. En cuanto a las traducciones, una exportación manual podría no realizarse desde Rosetta después de esa fecha en los paquetes fuente (lo que probablemente tendría que ocurrir antes del Final Freeze).

La próxima semana, sale el RC, y Final Freeze se pone en marcha. Esto significa que solo las actualizaciones críticas entrarán en la versión de Lubuntu, y las actualizaciones que no se incluyan en las ISO llegarán a través de una actualización. A partir de ahí, Lubuntu 18.04 recibirá puntos de lanzamiento como una LTS normal.

En términos de las versiones LTS, no hay nada inusual en la hoja de ruta. La fecha tentativa para 16.04.5 es el 5 de agosto de 2018, y nuestro soporte para el 16.04 finaliza en abril de 2019.

Una aclaración que debe hacerse es que a partir de la semana pasada Lubuntu Next ** ** envia como versión ISO la 18.04, pero se mantendrá como una ISO diaria. Los paquetes en el archivo (por lo tanto, la pila LXQt) solo se admitirán durante nueve meses. Vea el boletín de la semana pasada para saber por qué.

# En la prensa

Esta sección es para destacar la excepcional cobertura de Lubuntu a lo largo de la semana pasada.

## Inglés

 * [Ubuntu Podcast Season 11 Episode 05 - "High Five"](http://ubuntupodcast.org/2018/04/05/s11e05-high-five/).
 * [Softpedia Linux - "Lubuntu Next adopta el instalador de Calamares, continúa estando en desarrollo" por Marius Nestor](http://news.softpedia.com/news/lubuntu-next-is-adopting-the-calamares-installer- continúa-en-desarrollo-520533.shtml).

## Español

 * [MuyLinux - "Lubuntu Next cambiará el instalador por defecto a Calamares" por Eduardo Medina](https://www.muylinux.com/2018/04/04/lubuntu-next-instalador-calamares/).
 
 
## Varios

Lubuntu estará en LinuxFest NorthWest 2018, ¡ven a saludar! Puede encontrar al Jefe de Lanzamientos Simon Quigley al cargo del stand de Ubuntu, y potencialmente al Líder del Equipo de GC, Walter Lapchynski en su conferencia.

Puede encontrar más detalles sobre la conferencia [aquí](https://linuxfestnorthwest.org/conferences/lfnw18).

# Contáctenos

No dude en ponerse en contacto con nosotros [aquí](https://lubuntu.me/links/) para obtener asistencia, y para fines de prensa / marketing o si tiene una consulta privada, puede ponerse en contacto con el Jefe de Lanzamientos Simon Quigley [aquí](mailto: tsimonq2@lubuntu.me).