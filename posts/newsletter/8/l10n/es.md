Aquí está el octavo número de Esta Semana en el Desarrollo de Lubuntu. Puedes leer el último número [aquí](https://lubuntu.me/this-week-in-lubuntu-development-7/).

<! - más ->

# Cambios

## General

[¡Se ha lanzado Lubuntu 18.04.1!](Https://lubuntu.me/bionic-1-released/)

[¡Se ha lanzado Lubuntu 16.04.5!](Https://lubuntu.me/xenial-5-released/)

[Estamos tomando un nuevo rumbo.](Https://lubuntu.me/taking-a-new-direction/)

Las últimas semanas nos hemos centrado en pulir la experiencia de escritorio y en algunos cambios importantes en la infraestructura del proyecto.

Desafortunadamente, muchas de las correcciones en las que hemos estado trabajando están siendo bloqueadas por la transición a Qt 5.11.1 que está en curso. Se ha subido todo a cosmic-proposed, donde se esperan pruebas automatizadas antes de que sea generalmente instalable. Más detalles técnicos sobre ese proceso están disponibles [aquí](https://wiki.ubuntu.com/ProposedMigration).

Esta transición también se está haciendo en Debian Sid.

¡Estamos enormemente agradecidos a [UBports](https://ubports.com/) por su contribución financiera para permitir a los colaboradores de Lubuntu dedicar tiempo a esto! Puede ayudar a patrocinar su trabajo (y, por lo tanto, parte de nuestro trabajo) [aquí](https://ubports.com/donate).


#### Experiencia de escritorio

 - [LXPanel-Qt: no reinicia automáticamente el volumen cuando se modifica.](Https://phab.lubuntu.me/rLXQTPANELPACKAGING9635deb67b79e0483f89baa61b855428b688913b)
    - [Cometido de Upstream.](https://github.com/lxqt/lxqt-panel/commit/41259bb4a9c58876e68337a287d968b4ed9fb7e4)
    - [Informe de errores de Upstream.](Https://github.com/lxqt/lxqt/issues/1520)
    - Si algo está sonando demasiado alto en su ordenador, ahora puede silenciar el volumen, cambiarlo y activarlo, sin que el volumen se mantenga en silencio mientras lo está cambiando.

- Configuración por defecto:
    - [Quitar / usr / compartir / aplicaciones; estos archivos son nativos en LXQt.](https://phab.lubuntu.me/rDEFAULTSETTINGS758e4746525465c15c1cc7cfec2ba7c38b182d90)
    - [No inicie un gestor de archivos con Ctrl + Alt + D, porque eso ya muestra el escritorio en LXQt.](Https://phab.lubuntu.me/rDEFAULTSETTINGS804d49dfc6350f0c16fd19ec2b44f5b9964191db)
    - [Quitar los accesos directos del botón de volumen ya que están integrados en LXQt.](Https://phab.lubuntu.me/rDEFAULTSETTINGS5209b412656d71f5ecb6296c6a9dc941e9460665)
    - [Duplicada la posición del divisor para el panel PCManFM-Qt Places.](Https://phab.lubuntu.me/rDEFAULTSETTINGSc58864779695ded62d70e34e13c756133a45588b)
    - [gksu -> pkexec en PCManFM-Qt.](https://phab.lubuntu.me/rDEFAULTSETTINGSaaa50f079236906a8f8ac97d96b37c281fcd9d4e)
 - [QTerminal: Recordar el estado de maximización de la ventana.](Https://phab.lubuntu.me/rQTERMINALPACKAGING6a643cd600a187bf472232b0d41ecfa7c932d1f9)
    - [Informe de error de Launchpad.](Https://pad.lv/1754496)
    - [Informe de errores de Upstream (enviado por nosotros).](Https://github.com/lxqt/qterminal/issues/450)
    - [Solicitud de pull en Upstream (enviada por nosotros).](Https://github.com/lxqt/qterminal/pull/451)
    - [Cometido de Upstream](https://github.com/lxqt/qterminal/commit/14b1ee093b6712c4d3e1b6fe832ba353afa3d35a)
 - Mover el cuadro de diálogo de archivo desde LXQt Qt Plugin a LibFM-Qt para una mejor integración de la plataforma.
    - LibFM-Qt:
       - [Solicitud de pull en Upstream.](Https://github.com/lxqt/libfm-qt/pull/243)
       - [Cometido de Upstream](https://github.com/lxqt/libfm-qt/commit/da5966a5f36bd927cffdfc790da4a96cd5568083)
       - [Confirmación de empaquetado](https://phab.lubuntu.me/rLIBFMQTPACKAGING19fd5f3c8be72f799ddb966f68e84bb5521b416c)
    - LXQt Qt Plugin:
       - [Solicitud de pull en Upstream.](Https://github.com/lxqt/lxqt-qtplugin/pull/39)
       - [Cometido de Upstream](https://github.com/lxqt/lxqt-qtplugin/commit/73d20ab01995ca869f8d967535d4969409b22ec3)
       - [Confirmación de empaquetado](https://phab.lubuntu.me/rLXQTQTPLUGINPACKAGING0144765ce2217c62aa69d170369c980e6d9e8e26)
 - Agregar la capacidad de establecer temas GTK desde la configuración de apariencia LXQt.
   - [Solicitud de pull en Upstream.](Https://github.com/lxqt/lxqt-config/pull/244)
   - [Confirmación de empaquetado](https://phab.lubuntu.me/rLXQTCONFIGPACKAGINGae2282e219fa929077a3ebddf9aa79f8df023bff)

### Calamares

  - Hemos [reemplazado](https://phab.lubuntu.me/rCALASETTINGS88e201e0c82eda4438f78ad949b25a43409556a2) algunas líneas terriblemente complejas por otras mejores, gracias a KDE Neon.
    - Esto también solucionó un problema de Calamares, por lo que ahora se puede instalar en BIOS, UEFI en modo no seguro y en modo UEFI seguro, algo que antes no era posible.
  - [Predeterminado](https://phab.lubuntu.me/rCALASETTINGSec8d1863c8ae49a73cff15547aa773e02d953dfa), GRUB ahora está instalado en `/boot/efi/EFI/ubuntu` en lugar de `/boot/efi/EFI/lubuntu`.
  - [Hacer](https://phab.lubuntu.me/rCALASETTINGS912a94ead53188a2f222e3d72a2f8d5e553b7373) `/bin/bash` el shell predeterminado.

### Lubuntu Seed

- [Eliminar ship; ya no se usa.](https://phab.lubuntu.me/rSEEDd8529092ee6708b0c2693eb338d508c45cf8cba8)
  - [Hacer de vim una recomendación, no una dependencia difícil.](Https://phab.lubuntu.me/rSEED1b4ee934da65a22550f43e54725c7d68af75e713)
  - [Se recomienda zsync de manera predeterminada.](Https://phab.lubuntu.me/rSEED2df3b53a1fccffb4bdafa86297189954cb455ccd)

### Varios

  - [SDDM 0.18.0](https://github.com/sddm/sddm/releases/tag/v0.18.0) se ha subido a Debian Sid y Ubuntu Cosmic.
    - Se realizaron cambios en el empaquetado para facilitar su uso en otros sabores y derivados de Ubuntu. En lugar de codificar de forma rígida el tema Breeze, ahora tenemos un sistema de tematización en Ubuntu muy similar al de Debian, donde un paquete puede instalar su tema SDDM en el directorio ubuntu-theme en un script postinst.
    - Esto corrige CVE-2018-14345; estamos estudiando la posibilidad de seleccionar este parche en lanzamientos de Ubuntu estables anteriores.
  - Gracias a [Nate Graham](https://pointieststick.wordpress.com/) por [la indicación](https://phabricator.kde.org/T9244), incorporamos la solución para [un error](https: / /bugreports.qt.io/browse/QTBUG-66036) que afectaba visualmente a los programas basados en KDE bajo pantallas HiDPI.

## Infraestructura y cambios del proyecto

### Blog Lubuntu

El blog oficial de Lubuntu ahora [se mantiene](https://phab.lubuntu.me/source/blog/) bajo Git en nuestra instancia de Phabricator. Todas las publicaciones del blog de ahora en adelante se escribirán en formato Markdown y luego se publicarán utilizando los scripts que se encuentran allí.

Estamos (lentamente) trabajando en convertir todas las publicaciones en formato Markdown y mantenerlas allí.

Las traducciones de cada publicación se guardan en el directorio `l10n` de cada publicación (el nombre del archivo es` LANG_CODE.md`) y el código de localización se coloca en una lista YAML en info.yaml (consulte el anuncio del lanzamiento de 16.04.5 para tomar un ejemplo). Esto se debe a que Weblate no admite traducciones para Markdown de momento.

### Lugito

 - En los repositorios seleccionados, Lugito [automáticamente](https://phab.lubuntu.me/rLUGITOf91111a1807701daf1c3cdb4ee7bd2db7b57fc6a) comentará los informes de errores que están en los mensajes de confirmación con un mensaje de que la solución está en progreso.

### Varios

Como siempre, se agradecerán comentarios.

# Errores

## Nuevo / Arreglo necesario

 - [xdg user-dirs no se lee / almacena correctamente para el icono de escritorio en el panel izquierdo](https://pad.lv/1768961)
    - Archivado en upstream: [Error al utilizar un disco no iniciable para la ubicación de los archivos personales.](Https://github.com/lxqt/lxqt/issues/1389)
 - [La opción de edición de la partición "Format" aparece para seguir volviendo a "Keep"](https://pad.lv/1773610)
 - [Punto de montaje de una partición personalizada no se guarda con "OK"; se guarda con Enter](https://bugs.launchpad.net/ubuntu/+source/calamares/+bug/1773608)
 - [sddm no se inicia correctamente en el escritorio lxqt](https://pad.lv/1781392)

## Resuelto

 - [Lubuntu 18.10 lxqt-panel - 2 notificaciones al iniciar sesión: 2 accesos directos "no se pueden registrar"](https://pad.lv/1781511)
 - [Calamares falla en modo UEFI después de un comando externo en Lubuntu Cosmic](https://pad.lv/1781015)

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

¡Esta semana hemos agregado "Norwegian Bokmål"! Gracias a Einar Mostad por traducir.

¡Gracias por vuestras valiosas contribuciones!

## Grupo español

¡Tenemos [un grupo Oficial de Lubuntu en español en Telegram](https://t.me/lubuntues) que tiene tantos miembros como [nuestro grupo de desarrollo (en inglés)](https://t.me/lubuntudevel) en el momento de escribir esto!

Este es un grupo de lubuntu de propósito general, solo para españoles, y para entusiastas y contribuyentes por igual. ¡Siéntase libre de unirse!

¡Gracias a [Wolfenprey](https://twitter.com/Wolfen48K), el recién nombrado jefe del equipo español de Lubuntu, por conducirlo!

# Hoja de Ruta

Puede encontrar el ciclo de publicación de Cosmic Cuttlefish [aquí](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

Puede dejar de esperar funciones el 23 de agosto de 2018 cuando se active el congelamiento de funciones. La versión beta está programada para el 27 de septiembre de 2018 y la fecha de publicación final para el 18 de octubre de 2018.

Estas son algunas de las principales características específicas de Lubuntu que se puede esperar antes del lanzamiento:

 - Los comienzos de un centro de bienvenida (más detalles próximamente).
 - Mejoras en Calamares, que incluye un módulo adicional para instalar más paquetes.
 - Un plan para reemplazar Openbox, el administrador de ventanas actual usado en Lubuntu.

Nuestro equipo artístico todavía está trabajando en Lenny, y le haremos saber cuándo tendremos a Lenny Cuttlefish. :)

# En la prensa

Esta sección es para resaltar la cobertura excepcional de Lubuntu desde el último número.

## En inglés

 - [Lubuntu 18.10 podría admitir PC de 32 bits si hay la suficiente demanda, así es cómo puede ayudar](https://news.softpedia.com/news/lubuntu-18-10-may-support-32-bit-pcs-if -all-s-demand-here-s-how-you-can-help-521998.shtml)
 - [Los futuros lanzamientos de Lubuntu no se enfocarán en PC obsoletos, ofrecerán un sistema operativo Linux modular](https://news.softpedia.com/news/future-lubuntu-releases-won-t-focus-on-old-pcs -will-offer-a-modular-linux-os-522141.shtml)
 - [Lubuntu basado en Ubuntu Linux ya no se centrará en el hardware obsoleto después de mudarse a LXQt](https://betanews.com/2018/07/30/ubuntu-linux-lubuntu-old-lxqt/)
 - [Destination Linux EP81 - Canonical Fanboys (la cobertura comienza a las 26:24)](https://www.youtube.com/watch?v=7xlY0GQ-XvY)

## En español

 - [Lubuntu cambia de rumbo: los “equipos obsoletos” ya no son el objetivo](https://www.muylinux.com/2018/07/30/lubuntu-cambia-rumbo/)
 - [Lubuntu ya no será una distro para PCs antiguos](https://www.computekni.com/2018/08/lubuntu-ya-no-sera-una-distro-para-pcs.html)

¿Encontraste alguna otra historia excepcional sobre Lubuntu? [Háganoslo saber](https://lubuntu.me/links/) y estaremos encantados de incluirlas aquí.

# Contáctenos

Síganos en [Twitter](https://twitter.com/LubuntuOfficial) para obtener las últimas actualizaciones de Lubuntu. Estamos trabajando para que los tweets aparezcan automáticamente en [nuestra cuenta de Mastodon](https://mastodon.technology/@lubuntu) para las personas que prefieran no usar Twitter.

No dude en ponerse en contacto con nosotros [aquí](https://lubuntu.me/links/) para obtener asistencia, y para fines de prensa / marketing o si tiene una consulta privada, puede ponerse en contacto con el jefe de lanzamientos Simon Quigley [aquí](mailto: tsimonq2@lubuntu.me).
