Gracias al gran trabajo de nuestros colaboradores, nos complace anunciar que se ha lanzado Lubuntu 16.04.5 LTS.

# ¿Qué es Lubuntu?
Lubuntu es un sabor oficial de Ubuntu que utiliza el entorno de escritorio Lightweight X11 (LXDE). El objetivo del proyecto es proporcionar una distribución de Linux ligera pero funcional basada en la sólida base de Ubuntu. Lubuntu se dirige específicamente a máquinas antiguas con pocos recursos, pero también funciona muy bien en hardware nuevo. Junto con una interfaz gráfica de usuario sencilla pero fácil de usar, Lubuntu viene con una amplia variedad de aplicaciones seleccionadas por su reducido tamaño para que pueda navegar, enviar correos electrónicos, chatear, jugar y ser productivo.

# ¿Dónde puedo descargarlo?
Puede descargar Lubuntu 16.04.5 LTS en [nuestra página de descargas](https://lubuntu.me/downloads/).

Este anuncio en nuestro sitio web oficial ([Lubuntu.me](https://lubuntu.me/), **NO** en Lubuntu punto net, el cual no está dirigido por nuestros colaboradores de Lubuntu) reemplaza las notas de la versión tradicional que hemos proporcionado en el pasado en la wiki . Hemos omitido algunas notas que son comunes a todos los sabores, por lo que recomendamos que lea [las notas de la versión de Ubuntu](https://wiki.ubuntu.com/XenialXerus/ReleaseNotes).

## ¿Cuál es la diferencia entre Lubuntu 16.04.4 LTS y esta versión?
Lubuntu 16.04.5 es un conjunto de imágenes producidas  convenientemente para que una instalación limpia del último Lubuntu LTS no requiera tantas actualizaciones después de dicha instalación (ya que medida que pasa el tiempo, Lubuntu continúa lanzando Actualizaciones de su Version Estable y correcciones de seguridad para que su experiencia sea lo más fluida posible y para solucionar errores. Si desea ayudarnos con esto, consulte como mas adelante, siempre necesitamos más ayuda), pero no es una nueva versión importante de Lubuntu en sí misma. Si realiza actualizaciones del sistema con regularidad, ya debería estar ejecutando Lubuntu 16.04.5 LTS, y si instala Lubuntu en un sistema usando una imagen Lubuntu 16.04.5 LTS o una versión anterior y realiza actualizaciones del sistema, ese sistema también estará ejecutando Lubuntu 16.04.5 LTS.

# ¿Cómo obtengo ayuda?
Puede obtener soporte para Lubuntu [aquí](https://lubuntu.me/links/).

** Tenga en cuenta que este es el lanzamiento final en la serie 16.04, y solo tiene soporte hasta abril de 2019. **

Si desea soporte comercial o más soporte del que se proporciona en esa página (por un precio bajo), [contacte con Simon Quigley](mailto: tsimonq2@lubuntu.me) y podemos barajar opciones. Tenga en cuenta que esto no está proporcionado por Canonical.

# ¿Cómo ayudo?
¡Siempre necesitamos más ayuda! Siéntase libre de [unirse](https://lubuntu.me/links/) a nuestro canal de desarrollo (que se conecta a tres bandas desde Matrix, Telegram e IRC) y hable con nosotros allí. Ya sea conocedor de otro idioma, tenga algo de tiempo libre para ayudarnos a probar Lubuntu, sea bueno en redactar documentación o simplemente desee mantenerse "informado", ese es el lugar donde debe estar.

De lo contrario, [publicamos un boletín de noticias](https://lubuntu.me/category/newsletter/) generalmente todas las semanas, que detalla el trabajo que se está llevando a cabo actualmente en Lubuntu, incluidos errores y formas en las que puede ayudar.

# Problemas conocidos
Por el momento, las instalaciones LVM encriptadas no funcionan con Lubuntu debido a que Ubiquity no identifica correctamente las particiones zram. Este problema solamente ocurre con las imágenes basadas en 16.04; Las imágenes basadas en 18.04 funcionan correctamente.

[Aquí](https://bugs.launchpad.net/ubuntu/+source/partman-crypto/+bug/1759732) está el informe de errores si desea obtener todos los detalles técnicos.

Como solución alternativa, puede editar la línea 158 de `/ lib / partman / lib / crypto-base.sh` en un sistema de Lubuntu activo reemplazando` Filename *) `con` Filename * | / dev / zram *) `. O bien, puede ejecutar `sudo swapoff -a` antes de la instalación.

Nos disculpamos por las molestias que esto pueda ocasionar; estamos explorando diferentes soluciones para resolver esto.

¿Nos hemos olvidado algo? Por favor [reporte un error](https://bugs.launchpad.net/lubuntu/+filebug) y etiquételo con "lubuntu".

¿No quieres reportar un error? [Háganos saber](https://lubuntu.me/links/) cuál es el problema (con detalle suficiente para que podamos reproducirlo) y además podremos ayudarle a reportar uno.
