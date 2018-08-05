Aquí está el octavo número de Esta Semana en el Desarrollo de Lubuntu. Puede leer el último número [aquí](https://lubuntu.me/this-week-in-lubuntu-development-7/).

<! - más ->

# Cambios

## General

Esta semana se ha centrado en pulir la experiencia del instalador y el escritorio en general. Aquí están los cambios realizados, con enlaces a los detalles completos.

#### Experiencia de escritorio

  - [LXPanel-Qt: no reinicia automáticamente el volumen cuando se modifica.](Https://phab.lubuntu.me/rLXQTPANELPACKAGING9635deb67b79e0483f89baa61b855428b688913b)
     - [Cometido de Upstream.](https://github.com/lxqt/lxqt-panel/commit/41259bb4a9c58876e68337a287d968b4ed9fb7e4)
     - [Informe de errores de Upstream.](Https://github.com/lxqt/lxqt/issues/1520)
     - Si algo está sonando demasiado alto en su ordenador, ahora puede silenciar el volumen, cambiarlo y activarlo, sin que el volumen se mantenga en silencio mientras lo está cambiando.

## Infraestructura y cambios de proyecto

### Lubuntu Blog

El Blog oficial de Lubuntu ahora está  [siendo mantenido](https://phab.lubuntu.me/source/blog/) bajo Git en nuestra instancia de Phabricator. Todos los post del  blog desde ahora serán escritos en Markdown y serán publicados usando los scripts que tenemos ahí.

### Phabricator

### Varios

Como siempre, se agradecen los comentarios.

# Errores

## Nuevos / Arreglo Necesario

  - [Lubuntu 18.10 lxqt-panel - 2 notificaciones al iniciar sesión: 2 accesos directos "no se pueden registrar"](https://pad.lv/1781511)
  - [xdg user-dirs no se lee / almacena correctamente para el icono de escritorio en el panel izquierdo](https://pad.lv/1768961)
     - Archivado en Upstream: [Error al utilizar un disco que no se inicia para la ubicación de los archivos personales.](Https://github.com/lxqt/lxqt/issues/1389)
  - [La opción de edición de la partición "Format" aparece para seguir volviendo a "Keep"](https://pad.lv/1773610)
  - [Punto de montaje de partición personalizado no guardado con "OK"; guardado con <Enter>](https://bugs.launchpad.net/ubuntu/+source/calamares/+bug/1773608)
  - [sddm no iniciará correctamente el escritorio lxqt](https://pad.lv/1781392)
  - [Calamares falla en modo UEFI después de un comando externo en Lubuntu Cosmic](https://pad.lv/1781015)

## Resuelto / Marcado como inválido / duplicado

- [Dos opciones de instalación habituales pueden haber estado ausentes](https://pad.lv/1773613)
     - Estamos tomando una nueva dirección con el instalador que no implica necesariamente estas opciones directamente.
  - [lubuntu no se puede instalar en hardware real con uefi](https://pad.lv/1781539)
     - Marcado como duplicado de: [Calamares falla en el modo UEFI después del comando externo en Lubuntu Cosmic](https://pad.lv/1781015)

## Resuelto
  - [Lubuntu Cosmic no puede determinar mi ubicación](https://pad.lv/1781310)
  - [Lubuntu Cosmic tiene un "Instalar Lubuntu 18.10" en el escritorio](https://pad.lv/1781309)
  - [Calamares falla después de un comando externo (no se puede eliminar el archivo no existente) en Lubuntu Cosmic](https://pad.lv/1780977)
  - [Calamares falla después de que el comando externo verifique el modo UEFI en Lubuntu Cosmic](https://pad.lv/1780875)

## ¿Quiere ayudar?

Una de las maneras más fáciles de involucrarse con Lubuntu y ayudarnos a hacer que este lanzamiento sea el mejor es probar Lubuntu y reportar errores.

Puede aprender a escribir un excelente informe de errores que nos ayude a resolver su problema más rápido al leer [esta guía](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

Se puede encontrar más información sobre las pruebas de Lubuntu [aquí](https://phab.lubuntu.me/w/testing/).

# Traducciones

Tenemos [una instancia de Weblate](https://translate.lubuntu.me/projects/) disponible para traducciones. En este momento no hay muchas cadenas para traducir, pero a medida que pase el tiempo, agregaremos más.

¿Hablas un idioma que no está disponible para traducir allí? Háganoslo saber en los comentarios o [en otro lugar](https://lubuntu.me/links/) y agregaremos ese idioma.

Aquí están los traductores que han contribuido hasta ahora:
 - Henrik Christiansen (danés)
 - Hans P. Möller (alemán, español)
 - Daniel Absmeier (alemán)
 - Luís Rafael Gomes (portugués)
 - Lucas A. V. Dantas (portugués (Brasil))
 - Marcin Mikołajczak (polaco)
 - Tony Cuesta Escobar (catalán)

¡Gracias por vuestras valiosas contribuciones!

# Hoja de Ruta

Puede encontrar el ciclo de publicación de Cosmic Cuttlefish [aquí](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

Puede dejar de esperar funciones el 23 de agosto de 2018 cuando se active el congelamiento de funciones. La versión beta está programada para el 27 de septiembre de 2018 y la fecha de publicación final para el 18 de octubre de 2018.

Estas son algunas de las principales características específicas de Lubuntu que se puede esperar antes del lanzamiento:

  - Los comienzos de un centro de bienvenida (más detalles por venir).
  - Mejoras en Calamares, que incluye un módulo adicional para instalar más paquetes.
  - Un plan para reemplazar Openbox, el administrador de ventanas actual usado en Lubuntu.

Nuestro equipo artístico todavía está trabajando en Lenny, y le haremos saber cuándo tendremos a Lenny Cuttlefish. :)

# En la prensa

Esta sección es para resaltar la cobertura excepcional de Lubuntu desde el último número.

- [Lubuntu 18.10 podría admitir PC de 32 bits si hay la suficiente demanda, así es cómo puede ayudar](https://news.softpedia.com/news/lubuntu-18-10-may-support-32-bit-pcs-if -all-s-demand-here-s-how-you-can-help-521998.shtml)

¿Encontraste alguna otra historia excepcional sobre Lubuntu? [Háganoslo saber](https://lubuntu.me/links/) y estaremos encantados de incluirlos aquí.

# Contáctenos

No dude en ponerse en contacto con nosotros [aquí](https://lubuntu.me/links/) para obtener asistencia, y para fines de prensa / marketing o si tiene una consulta privada, puede ponerse en contacto con el Jefe de Lanzamientos Simon Quigley [aquí](mailto: tsimonq2@lubuntu.me).