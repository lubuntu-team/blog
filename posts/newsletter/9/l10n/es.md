Este es el noveno número del Boletín de Desarrollo de Lubuntu. Puede leer el último número [aquí](https://lubuntu.me/this-week-in-lubuntu-development-8/).

# Cambios

## General

Hemos estado puliendo más el escritorio, pero nuestro trabajo todavía está siendo bloqueado por la transición aún en curso de Qt.

¡La actualización de 16.04 a 18.04 ha sido habilitada! Háganos saber si hay algún problema. [Aquí hay](https://www.youtube.com/watch?v=QhdQIzyscGw) un video que hicimos cuando 17.04 llegó al final de su soporte, (End Of Life); las instrucciones siguen siendo válidas.

Nuestro desarrollador principal, Simon Quigley, [se convirtió en  Desarrollador de Ubuntu Core](https://lists.ubuntu.com/archives/ubuntu-devel/2018-August/040436.html) el pasado lunes! Ahora tiene acceso a todo el archivo de Ubuntu.

### Experiencia de escritorio

 - Hemos dividido los complementos de estilo Qt en paquetes binarios separados. Esto eventualmente nos llevará a no ofrecer el estilo de Blackberry roto de forma prederminada, por ejemplo.
 - Para la edición de conexión WiFi por nm-tray, ahora usamos QTerminal. A largo plazo, este será un diálogo nativo de Qt, pero ya se está acercando para este próximo ciclo.
 - El complemento spacer de LXQt Panel ahora tiene una opción de expansión automática, como en LXDE.

### Calamares

 - Escribimos un módulo de Calamares llamado `automirror` que seleccionará automáticamente un espejo Ubuntu basado en su ubicación geográfica. Estamos trabajando en acercarlo para su uso en otras distribuciones.
 - Ahora se pide una fortaleza de contraseña mínima. Esto es para ayudar a promover contraseñas seguras y prevenir ataques de fuerza bruta fáciles. Vamos a establecer de forma mas activa esto a medida que pase el tiempo.
 - Calamares [agrega](https://phab.lubuntu.me/rCALASETTINGSa2e6868a2a61c4e15770cc965c0b4b001c332e81) el usuario a menos grupos de sistema de forma predeterminada. Esto soluciona varios problemas y hace que Lubuntu sea más consistente con otros sabores.
 
# Infraestructura y cambios de proyecto

### Lubuntu está cambiando a Wayland

Lubuntu cambiará a Wayland de manera predeterminada para 20.10.

Haremos esto al portar Openbox para usar [el servidor de pantalla](https://mir-server.io/) Mir, el [QtLayerShell](https://github.com/SirCmpwn/qtlayershell) de  Drew DeVault, y otros componentes asociados.

** P: ** ¿Por qué se está cambiando a Wayland?
** R: ** La implementación de X es antigua y no se actualizará para abordar la forma en que se usa el escritorio de Linux actualmente. Los administradores de ventanas son una idea de última hora, y muchas cosas no se implementan correctamente. Wayland es la versión moderna del sistema de visualización de Linux.

** P: ** ¿Qué pasa con las personas con tarjetas gráficas NVIDIA?
** R: ** Hay muchos detalles por resolver, pero el plan es hacer que todo funcione con esas tarjetas gráficas cuando llegue el momento.

** P: ** ¿Pero Mir no fue deshechado  cuando se abandonó la plataforma Ubuntu Touch?
** R: ** Mir sigue vivo, y todavía tiene un equipo de empleados de Canonical trabajando en él.

Próximamente, mas detalles y noticias; Siéntase libre de dejar sus comentarios a continuación.

### Varios

Como siempre, se agradece el feedback y los comentarios.

## ¿Quiere ayudar?

Una de las maneras más fáciles de involucrarse con Lubuntu y ayudarnos a hacer que este lanzamiento sea el mejor es probar Lubuntu y reportar errores.

Puede aprender a escribir un excelente informe de errores que nos ayude a resolver su problema más rápido al leer [esta guía](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

Se puede encontrar más información sobre las pruebas de Lubuntu [aquí](https://phab.lubuntu.me/w/testing/).

# Traducciones

Tenemos [una instancia de Weblate](https://translate.lubuntu.me/projects/) disponible para traducciones. En este momento no hay muchas cadenas para traducir, pero a medida que pase el tiempo, agregaremos más.

Esta semana, Henrik Christiansen nos ha ayudado a traducir  Calamares al Danés. ¡Gracias!

¿Hablas un idioma que no está disponible para traducir allí? Háganoslo saber en los comentarios o [en otro lugar](https://lubuntu.me/links/) y agregaremos ese idioma.

Aquí están los traductores que han contribuido hasta ahora:

 - Henrik Christiansen (danés)
 - Hans P. Möller (alemán, español)
 - Daniel Absmeier (alemán)
 - Luís Rafael Gomes (portugués)
 - Lucas A. V. Dantas (portugués (Brasil))
 - Marcin Mikołajczak (polaco)
 - Tony Cuesta Escobar (catalán)
 - Einar Mostad (Norwegian Bokmål)

¡Gracias por vuestras valiosas contribuciones!

# Hoja de Ruta

Puede encontrar el ciclo de publicación de Cosmic Cuttlefish [aquí](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule).

Puede dejar de esperar funciones el 23 de agosto de 2018 cuando se active el congelamiento de funciones. La versión beta está programada para el 27 de septiembre de 2018 y la fecha de publicación final para el 18 de octubre de 2018.

Estas son algunas de las principales características específicas de Lubuntu que se puede esperar antes del lanzamiento:

 - Los comienzos de un centro de bienvenida (más detalles próximamente).
 - Mejoras en Calamares, que incluye un módulo adicional para instalar más paquetes.


Nuestro equipo artístico todavía está trabajando en Lenny, y le haremos saber cuándo tendremos a Lenny Cuttlefish. :)

# En la prensa

¿Ha encontrado alguna noticia excepcional sobre Lubuntu? [Háganoslo saber](https://lubuntu.me/links/) y estaremos encantados de incluírla aquí.

# Contáctenos

Síganos en [Twitter](https://twitter.com/LubuntuOfficial) para obtener las últimas actualizaciones de Lubuntu. ¿No usas Twitter porque no es software libre? ¡Sin problema! Síganos en [Mastodon](https://mastodon.technology/@lubuntu) donde se publica el mismo contenido.

No dude en ponerse en contacto con nosotros [aquí](https://lubuntu.me/links/) para obtener asistencia, y para fines de prensa / marketing o si tiene una consulta privada, puede ponerse en contacto con el gerente de lanzamiento Simon Quigley [aquí](mailto: tsimonq2@lubuntu.me).


