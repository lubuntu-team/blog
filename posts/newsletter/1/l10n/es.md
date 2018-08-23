En Lubuntu hemos decidido que era buena idea crear un boletín semanal que detallara el trabajo que ha estado en marcha. Así que, allá vamos. :)



# Cambios

## General

 * Nos estamos preparando para participar en la Beta final. Por el momento, somos conscientes de dos errores destacados que afectan a Lubuntu:
    * [https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174](https://bugs.launchpad.net/ubuntu/+source/ubiquity/+bug/1754174)
        * Esto afecta la instalación de Lubuntu al seleccionar la opción directamente desde el arranque (al seleccionar "Instalar Lubuntu" desde el menú de inicio).
    * [https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/+bug/1759732](https://bugs.launchpad.net/ubuntu/+source/partman-auto-crypto/ + error / 1759732)
        * Esto hace que las instalaciones LVM encriptadas no funcionen debido al hecho de que tenemos compatibilidad zram en la imagen en vivo. Una solución simple es desmontar las particiones zram, pero nos gustaría que esto se arreglara correctamente para cuando llegue a los usuarios.

Esperamos que estos errores sean corregidos antes de lanzar el ISO final, si no antes en la Beta final.

## Lubuntu Next

 * Las imágenes de Lubuntu a partir de 20180401 ya no pide que se seleccione un administrador de ventanas, y aunque todavía se deben establecer algunas configuraciones predeterminadas, ahora se puede usar.
   * Esto se solucionó, pero volvió a surgir cuando los cambios se eliminaron accidentalmente después de introducir SDDM 0.17 en el archivo. Esta carga lo corrige: [https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu2](https://launchpad.net/ubuntu/+source/sddm/0.17.0-1ubuntu2)
   * La nueva versión de Featherpad se sincronizó con Bionic: [https://launchpad.net/ubuntu/+source/featherpad/0.8-1](https://launchpad.net/ubuntu/+source/featherpad/0.8-1)
   * Esto no es lo único que sucedió durante la última semana, tambien hemos realizado algunos cambios en las siguientes ISOs de Lubuntu:
     * Ahora se encuentra de forma predeterminada con Arc como temas de LXQt y Openbox. ¡Gracias al Equipo de Artístico por su duro trabajo!
     * Las aplicaciones predeterminadas que se envían con Lubuntu Next ya están decididas. El objetivo ahora es trabajar en el perfeccionar  la configuración predeterminada con la que se lanzaran dichas aplicaciones, para que se configuren correctamente.
     * Trabajando con Kubuntu y KDE Neon, nos vamos a mover a Calamares como el instalador predeterminado para Lubuntu Next. Creemos que esta es la decisión correcta en el futuro para que se proporcione a los  usuarios un instalador robusto, flexible y modular. Como Lubuntu Next es el primer sabor (en al menos una década, según nuestras estimaciones) que ha cambiado su instalador gráfico (y no es un proyecto liderado por Canonical), esperamos algunos baches en el futuro. El objetivo es, junto con Kubuntu, lanzar 18.10 con Calamares como único instalador gráfico.

## Infraestructura y cambios de proyecto

Como se señaló en anuncios anteriores, ahora tenemos una [instancia de Phabricator](https://phab.lubuntu.me/) que nuestros amigos de Altispeed Technologies hospedaron amablemente, el código principal en el que trabaja Lubuntu ahora está [reflejado en nuestra página oficial de GitHub](https://github.com/lubuntu-team/) (estamos trabajando para duplicar repositorios y hacerlos más útiles, ¡estén atentos!), todas nuestras presencias web oficiales (es decir, Lubuntu.me y subdominios, porque Lubuntu.net ya no está bajo el control del proyecto Lubuntu (no podemos decir más en este momento, excepto que de ninguna manera estamos afiliados a FOSSASIA)) ahora tenemos HTTPS, y tenemos [muchas más formas en las que puede ponerse en contacto nosotros](https://lubuntu.me/links/). Pero, hay más cambios de infraestructura y proyectos que hemos hecho que aún no se han anunciado:

 1. [El CSS](https://github.com/lubuntu-team/cdimage-css) para [las páginas de Lubuntu bajo cdimage.ubuntu.com](http://cdimage.ubuntu.com/lubuntu/daily/ current /) ha sido actualizado con un aspecto renovado, gracias al Equipo Artístico. Hemos documentado este proceso para otros sabores, que está disponible [aquí](https://wiki.ubuntu.com/ReleaseTeam/FlavorCSSChanges).
 1. El logotipo ha cambiado para reflejar el movimiento hacia LXQt. Hay algunos lugares que aún contendrán el logotipo antiguo, pero en general, el logotipo de Lubuntu está cambiando (y ya ha cambiado en muchos lugares) a lo siguiente:

! [Logotipo de Lubuntu](https://pbs.twimg.com/profile_images/965283049968689152/8iy34E_U_200x200.jpg)

Puede encontrar los términos de uso para nuestro nuevo logotipo y marca [aquí](https://github.com/lubuntu-team/lubuntu-identity). Como se explica allí, está licenciado bajo [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/) a menos que reciba permiso explícito de [el equipo de Lubuntu]( https://launchpad.net/~lubuntu-admins).

# Hoja de Ruta

El resto de la hoja de ruta de Bionic está [presentada con bastante claridad](https://wiki.ubuntu.com/BionicBeaver/ReleaseSchedule); participaremos en la Beta final que se lanzará el jueves (asumiendo que los dos errores  sean corregidos), luego en dos semanas obtendremos los candidatos de lanzamiento, y una semana después, se lanzará Lubuntu 18.04.

Lubuntu 18.04 será lanzado como un LTS con tres años de soporte. El escritorio LXDE seguirá siendo el predeterminado durante toda la duración de su ciclo vital, y será lanzado con las mismas aplicaciones que hemos seleccionado en 17.10.

Lubuntu Next continuará siendo una vista previa para "early adopters", porque nuestro enfoque como equipo ahora mismo es pulir Lubuntu 18.04 y convertirlo en una sólida LTS. Si instala Lubuntu Next 18.04 (que puede obtener como una ISO diaria ahora mismo pero no será lanzada), ** muchas cosas no funcionarán bien todavía ** (por supuesto, puede hacerla funcionar con algunas modificaciones, pero no tenemos suficiente confianza en el estado de la ISO ahora mismo para que estemos dispuestos a lanzarla oficialmente). Se mantendrá con soporte ** extraoficialmente **, y los paquetes solo se admitirán en el archivo de Ubuntu durante nueve meses después del lanzamiento. Después de eso, debe actualizar a 18.10 para recibir las últimas actualizaciones.

Frecuentemente recibimos una pregunta en la línea de "¿Por qué no se ha lanzado con LXQt como escritorio predeterminado?" La respuesta a estas preguntas es que, si bien estamos trabajando para lograrlo (y se está progresando), no queremos poner en peligro nuestra base de usuarios lanzando algo que todavía no es del todo perfecto. Agradecemos la ayuda para hacer de Lubuntu Next una experiencia sólida, independientemente de su nivel de experiencia, así que siéntase libre de contactarnos.

# Contáctenos

Siéntase libre de [ponerse en contacto con nosotros](https://lubuntu.me/links/).
