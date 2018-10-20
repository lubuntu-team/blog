Gracias a todo el trabajo duro de nuestros colaboradores, Lubuntu 18.10 ha sido lanzado! Con el nombre en clave Cosmic Cuttlefish, Lubuntu 18.10 es la 15ª versión de Lubuntu y la primera versión de Lubuntu con LXQt como entorno de escritorio predeterminado, con soporte hasta julio de 2019.

<div style="position:relative;height:0;padding-bottom:56.25%"><iframe src="https://www.youtube.com/embed/CRgcsTQGvwU?ecver=2" width="640" height="360" frameborder="0" allow="autoplay; encrypted-media" style="position:absolute;width:100%;height:100%;left:0" allowfullscreen></iframe></div>

NOTICE

# ¿Qué es Lubuntu?

Lubuntu es un sabor oficial de Ubuntu que utiliza el Lightweight Qt Desktop Environment (LXQt). El objetivo del proyecto es proporcionar una distribución Linux ligera pero funcional basada en una base Ubuntu sólida como una roca. Lubuntu proporciona una interfaz gráfica de usuario simple pero moderna y potente, y viene con una amplia variedad de aplicaciones para que pueda navegar, enviar correo electrónico, chatear, jugar y ser productivo.

# Bienvenido a LXQt

<img style="float: center; width: 500em;" src="https://phab.lubuntu.me/file/data/zwng7o6qanhvvucgajdc/PHID-FILE-djx4vzahriz23c5622vu/Screenshot_20181007_Desktop.png" />

Esta es la primera versión de Lubuntu con LXQt como entorno de escritorio principal. El proyecto Lubuntu, en 18.10 y versiones sucesivas, ya no será compatible con el entorno de escritorio LXDE ni con las herramientas del archivo Ubuntu sino que se centrará en el entorno de escritorio LXQt. Puede encontrar las siguientes aplicaciones y conjuntos de herramientas principales instalados de forma predeterminada en esta versión:

 - LXQt 0.13.0, con muchas correcciones y mejoras soportadas desde la versión anterior.
 - Qt 5.11.1, que es el primer lanzamiento de punto en la serie Qt 5.11.
 - Mozilla Firefox 62, que recibirá actualizaciones del equipo de seguridad de Ubuntu durante todo el ciclo de soporte de la versión.
 - La suite LibreOffice 6.1.2, con la interfaz Qt 5.
 - VLC 3.0.4, para ver medios y escuchar música.
 - Featherpad 0.9.0, para la edición de notas y códigos.
 - Discover Software Center 5.13.5, para una manera fácil y gráfica de instalar y actualizar el software.
 - El potente y rápido cliente de correo electrónico Trojitá 0.7 para llegar a la bandeja de entrada cero en un abrir y cerrar de ojos.

Usted puede encontrar una variedad de otras aplicaciones instaladas que tienen como objetivo mejorar su experiencia mientras se mantiene fuera del camino de su flujo de trabajo normal.

## Calamares

Lubuntu ha pasado a utilizar el instalador del sistema [Calamares](https://calamares.io/) en lugar del instalador de Ubiquity que utilizan otros sabores. Calamares es un marco de instalación universal que pretende ser fácil, usable, bello, pragmático, inclusivo y agnóstico para la distribución.

En este ciclo nuestro principal objetivo era resolver cualquier problema que surgiera del cambio en el instalador, especialmente en torno a la herramienta Ubuntu que está orientada al uso de Ubiquity, por lo que carece de características como la instalación mínima, pero en el próximo ciclo vamos a poner un énfasis en la mejora de la paridad de características.

Desafortunadamente, tuvimos problemas con los sistemas EFI y los sistemas LUKS encriptados que configuraban GRUB correctamente. Mientras tanto, le animamos a que utilice la experiencia de particionamiento manual mejorada y fácil de usar proporcionada por Calamares. De lo contrario, el equipo de control de calidad de Lubuntu ha estado trabajando duro probando muchas combinaciones de instalaciones para asegurarse de que todo lo demás funciona como se esperaba. Puede encontrar una tabla completa de las instalaciones probadas [aquí](https://phab.lubuntu.me/T107).

Gracias a Adriaan de Groot y a muchos otros miembros del equipo de Calamares; sin ti, Calamares no habría funcionado tan bien como lo hace para nosotros.

## Manual de Lubuntu

El equipo de Lubuntu ha trabajado arduamente en el pulido de un Manual de Lubuntu para facilitar a los usuarios nuevos y experimentados el uso más productivo de su sistema. El libro se puede encontrar en [manual.lubuntu.me](https://manual.lubuntu.me/).

Eventualmente lo enviaremos en la instalación por defecto de Lubuntu, pero por ahora nuestro objetivo es pulirlo y recibir comentarios de la comunidad, por lo que permanecerá publicado como un sitio web sólo por ahora.

El manual está construido usando [Sphinx](http://www.sphinx-doc.org/en/stable/), y la fuente se puede encontrar en nuestra instancia de Phabricator [aquí](https://phab.lubuntu.me/source/lubuntu-manual/), o si prefieres usar GitHub para contribuir, también se refleja [allí](https://github.com/lubuntu-team/manual).

Queremos agradecer a Lyn Perrine por todo el arduo trabajo que ha puesto en el Manual de Lubuntu recientemente, porque la mayor parte del texto en el manual ahora mismo es lo que ella ha escrito. ¡Gracias!

## La comunidad española de Lubuntu

A lo largo de este ciclo, Lubuntu ha iniciado una comunidad española para hispanohablantes (ya sea como lengua materna o como lengua secundaria) para hablar y contribuir al Lubuntu y a GNU/Linux en general. El grupo ha crecido en tamaño y ahora es más grande que nuestro grupo de desarrollo.

Si hablas español y quieres unirte a una comunidad amigable de gente de Linux con todos los niveles de experiencia técnica, la comunidad española de Lubuntu es para ti. Puedes unirte al grupo Telegram en [telegram.lubuntu.me/español](https://telegram.lubuntu.me/español) o al canal IRC en #lubuntu-es en freenode.

Gracias a [Wolfenprey](https://twitter.com/Wolfen48K), [GatoOscuro](https://gatooscuro7.wordpress.com/), [Hans Möller](https://twitter.com/hpmoller), y muchos, muchos otros grandes miembros de la comunidad que lo hacen posible.

# ¿Dónde puedo descargarlo?

Puede descargar Lubuntu 18.10 en [nuestra página de descargas](https://lubuntu.me/downloads/).

# Problemas conocidos y soluciones alternativas

## Problemas con los métodos alternativos

El problema más importante y notable es que al actualizar Lubuntu de 18.04 a 18.10 causa una buena cantidad de problemas. Por lo tanto,no estamos apoyando oficialmente este camino de actualización en este momento, sin embargo, hemos preparado [una página en el Manual de Lubuntu](https://manual.lubuntu.me/D/upgrading.html) que puede ayudar a resolver los problemas que surgen después de la actualización.

LXQt trata todos los monitores como uno solo cuando pinta el fondo de escritorio. Planeamos resolver esto de una manera más nativa para la versión 19.04, pero mientras tanto, el colaborador de Lubuntu Hans Möller ha escrito [un script](https://git.launchpad.net/~hmollercl/stitchwp/tree/stitchWP.sh) que puede ser usado como una solución para tratar todos los fondos de forma diferente.

No hemos transferido la pestaña «Controladores adicionales» de software-properties-gtk a software-properties-qt, que puede utilizarse para instalar controladores adicionales de CPU y gráficos. Como solución provisional, puede utilizar la herramienta de línea de comandos «ubuntu-drivers».

## Problemas con las correcciones

El tema LibreOffice predeterminado que se incluye en las ISO es el tema predeterminado de Adwaita, que no es coherente con el tema del sistema. Esto se arreglará en la versión 1:6.1.2-0ubuntu2.

Trojitá tiene problemas de visualización con algunos correos electrónicos relacionados con un problema de QtWebkit. Esto será fijado en la versión 5.212.0~alpha2-12ubuntu2.

Ambos de los arreglos anteriores deben venir como actualizaciones dentro de la próxima semana.

## Problemas conocidos

Trojitá se cae si es ordenado y reordenado varias veces de manera sucesiva (LP: #[1797665](https://bugs.launchpad.net/ubuntu/+source/trojita/+bug/1797665)).

La tecla de acceso directo del menú desplegable de QTerminal no cambia constantemente la visibilidad (LP: #[1795998](https://bugs.launchpad.net/ubuntu/+source/qterminal/+bug/1795998)).

El único problema no relacionado con Ubiquity que afecta a todos los sabores de Ubuntu (y al principal Ubuntu) es que los DNS dejan de funcionar después de desconectarse de una VPN debido a la resolución del sistema (LP: #[1797415](https://bugs.launchpad.net/ubuntu/+source/systemd/+bug/1797415)).

# Contribuyendo a Lubuntu

¡Siempre necesitamos más ayuda! No importa tu nivel de habilidad o tu experiencia técnica, hay algo en lo que puedes ayudar que puede hacer una gran diferencia en Lubuntu. [Únete](https://lubuntu.me/links/) en nuestro chat que está puenteado de tres maneras a Matrix, Telegrama, e IRC y hablar con nosotros allí. Ya sea que conozcas otro idioma, tengas tiempo libre para ayudarnos [test](https://phab.lubuntu.me/w/testing/) Lubuntu, seas bueno escribiendo documentación, o simplemente quieras mantenerte «al tanto», ese es el lugar en el que debes estar.

Otro gran método para involucrarse es el reporte de errores. Si observa un problema, por favor, rellene el formulario de error usando [las instrucciones en el Wiki de Lubuntu](https://phab.lubuntu.me/w/bugs/).

¿No quieres reportar un error? [Háganos saber](https://lubuntu.me/links/) cuál es el problema (en detalle, lo suficiente como para que podamos reproducirlo) y podemos ayudarlo a presentar uno o hacerlo nosotros mismos.

## La infraestructura cambia en este ciclo

Lubuntu se ha mudado de GitHub y sobre todo de Launchpad para el flujo de trabajo del proyecto. Hemos decidido optar por [Phabricator](https://phacility.com/phabricator/), que es una plataforma de alojamiento de proyectos con todas las características principales que se esperan de competidores como GitLab. Puede encontrar nuestra instancia de Phabricator [aquí](https://phab.lubuntu.me/).

Además, para las traducciones, siempre que sea posible utilizamos una instancia de [Weblate](https://weblate.org), que se puede encontrar [aquí](https://translate.lubuntu.me/languages/). También puede encontrar la instancia de LXQt Weblate [aquí](https://weblate.lxqt.org/); animamos a las personas que conocen más de un idioma con fluidez a que traduzcan Lubuntu y LXQt para que todos se beneficien.

# Nuevos colaboradores

 - [Simon Quigley](https://twitter.com/tsimonquigley2)
 - [Walter Lapchynski](https://soc.ialis.me/@wxl)
 - [Lyn Perrine](https://phab.lubuntu.me/p/lynorian/)
 - Rafael Laguna, que ha dimitido del proyecto. Gracias por sus innumerables contribuciones al proyecto!
 - [Wendy Hill](https://www.wendyhillphoto.com/)
 - [Samuel Banya](http://www.musimatic.net/)
 - [Hans Möller](https://twitter.com/hpmoller)
 - [Tony Cuesta Escobar (Wolfenprey)] (https://twitter.com/Wolfen48K)
 - [Dan Simmons](https://mastodon.technology/@kc2bez)
 - Muchos más contribuyentes!

No es posible donar a Lubuntu como proyecto en este momento, pero si se siente generoso y le gustaría donar a contribuyentes individuales, aquí hay personas que han hecho públicos los enlaces de donación:

 - [Simon Quigley](https://www.patreon.com/tsimonq2)
 - [Walter Lapchynski](https://www.paypal.com/donate/?token=XhZBN4w32pnCuTbIjGnsxPn7pAk_a5_FMofe_9MN8Mzqsx9Nji-OVU4ImAqoekPhScCSoW&country.x=US&locale.x=US)

# ¡Manténgase conectado!

[Publicamos un boletín de noticias](https://lubuntu.me/category/newsletter/) de vez en cuando que detalla el trabajo que está ocurriendo actualmente en Lubuntu, incluyendo errores corregidos y formas adicionales en las que puede ayudar.

Para obtener la información y los anuncios más recientes de Lubuntu, síganos en [Twitter](https://twitter.com/LubuntuOfficial), [Mastodon](https://mastodon.technology/@lubuntu), o [Telegram](https://t.me/LubuntuOfficial). Tenemos otras páginas de medios sociales y formas de mantenerse conectado que se pueden encontrar [aquí](https://lubuntu.me/links/).

# Capturas de pantalla

Como se prometió [en Twitter](https://twitter.com/LubuntuOfficial/status/1050068447000973312), los usuarios que probaron Lubuntu y nos enviaron sus capturas de pantalla serán acreditados en el anuncio. Aquí están las presentaciones:

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="und" dir="ltr">❤️ <a href="https://t.co/lNBgQQD9kH">pic.twitter.com/lNBgQQD9kH</a></p>&mdash; GnuXero (@GnuXero26) <a href="https://twitter.com/GnuXero26/status/1050071135054905351?ref_src=twsrc%5Etfw">October 10, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Learning to customize Lubuntu &lt;3 <a href="https://t.co/5sVYbG0B2R">pic.twitter.com/5sVYbG0B2R</a></p>&mdash; Leandro Ramos (@leandroembu) <a href="https://twitter.com/leandroembu/status/1051495186054991872?ref_src=twsrc%5Etfw">October 14, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="und" dir="ltr"> <a href="https://t.co/gmleH5b6nw">pic.twitter.com/gmleH5b6nw</a></p>&mdash; N0um3n0 (@Cryptodata) <a href="https://twitter.com/Cryptodata/status/1051536066421944330?ref_src=twsrc%5Etfw">October 14, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Marneu, uno de nuestros nuevos moderadores [r/Lubuntu](https://www.reddit.com/r/Lubuntu/) que usa Lubuntu 18.10 con el gestor de ventanas i3, envió tres capturas de pantalla: [uno](https://i.imgur.com/ObmUloF.jpg), [dos](https://i.imgur.com/r7yj5Wh.png), [tres](https://i.imgur.com/A5WNmIM.png).

Y por supuesto, aunque no cuenta, Dustin Krysak nos dio una captura de pantalla [Ubuntu Budgie](https://ubuntubudgie.org/blog/2018/10/18/18-10-ubuntu-budgie-released):

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Here is the best screenshot yet..... ha ha <a href="https://t.co/WanVi9IZNv">pic.twitter.com/WanVi9IZNv</a></p>&mdash; Dustin 🤖 Krysak (@Bashfulrobot) <a href="https://twitter.com/Bashfulrobot/status/1050254685498560512?ref_src=twsrc%5Etfw">October 11, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

¡Gracias a todos los que enviaron capturas de pantalla!
