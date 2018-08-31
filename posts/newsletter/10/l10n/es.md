Este es el décimo número del Boletín de Desarrollo de Lubuntu. Puede leer el último número [aquí](https://lubuntu.me/lubuntu-development-newsletter-9/).



# Cambios

## General

Como siempre, ¡Continuamos puliendo el escritorio!

Muchos de los cambios que habíamos realizado, incluida una nueva versión de SDDM, han migrado hacia Qt 5.11.1 hace unos días. ¡Gracias a todos los involucrados en llevar dicha transición!

### Experiencia de escritorio

 - Todos los paquetes que no son esenciales han sido [ahora degradados](https://phab.lubuntu.me/rSEEDfc9c1389cf0e9928a7bd2cf1b460d18a3264b605) hacia los recomendados para nuestro metapaquete.
 - En LXQt Sudo, [el texto ya no está cortado](https://phab.lubuntu.me/rLXQTSUDOPACKAGING196967406935b3d8e0aafb32968bb73b96778dcb).
 - Ahora puede (opcionalmente) [anular](https://phab.lubuntu.me/rLXQTPANELPACKAGINGcac77df97847bc4008fae01446f121e68275e248) el tema de iconos para el panel. Esto ha sentado las bases para que podamos elegir un tema de iconos que se vea mejor visualmente para el panel.
 - Network Manager Tray, la implementación pura de Qt de un ícono de indicador NM que utilizamos en Lubuntu, ha [sido incluida en la lista negra](https://phab.lubuntu.me/rDEFAULTSETTINGS9e192e55224221d4d01b0ceeb9575699d54c0d5a) del menú. Esto evita que los usuarios se confundan y comiencen con varias sesiones duplicadas de nm en la bandeja.
 - Hemos [arreglado](https://phab.lubuntu.me/rDEFAULTSETTINGS51d5e2fa96937089ee8e39b56bf1224f48f5e8f4) la ejecución de comandos como root con la opción PCManFM-Qt incorporada.

### Calamares

 - El soporte de XFS ahora se ha [habilitado](https://phab.lubuntu.me/rSEED8a2e4b0be76619f93dc78b27bfb56970dd5e171a) con Calamares.
 - Arreglamos la función de autologin para el instalador de Lubuntu. Si instaló una iso "daily" con autologin habilitado antes del 21 de agosto, le recomendamos que reinstale.
    - [Dicha solución necesita nuestra configuración.](Https://phab.lubuntu.me/rCALASETTINGS4f328dc3d72a509463c368ef1514ac5080e87977)
    - [La corrección necesaria de Calamares en Upstream.](Https://phab.lubuntu.me/rCALAPACKAGING4ef8ded762c93b8b797802cb3abf02c8b7d92b0b)
 - Antes del último boletín, habilitamos la verificación de contraseñas. Después de algunos comentarios vocales, [preguntamos a la comunidad](https://lists.ubuntu.com/archives/lubuntu-devel/2018-August/001221.html) en [nuestra lista de correo de desarrollo](https: // lists. ubuntu.com/mailman/listinfo/lubuntu-devel) para ver qué pensaban al respecto, y una abrumadora mayoría tenía la misma opinión; se debería advertir, pero aún así se debería poder establecer una contraseña débil. Si bien el equipo de Lubuntu ** recomienda encarecidamente elegir una contraseña segura al instalar Lubuntu **, hemos [deshabilitado](https://phab.lubuntu.me/rCALASETTINGSfcc2036633b31b2ebb4dca6d41421aacfbef7265) la comprobación de contraseñas.
 
## Infraestructura y cambios de proyecto

### Nueva documentación

Hemos comenzado con varios fragmentos de documentación en nuestra instancia de Phabricator que detallan más cómo contribuir a Lubuntu. Como muestra, algo en lo que estamos trabajando:

 - [Tutorial de Empaquetado](https://phab.lubuntu.me/w/packaging-tutorial/)
 - [Documento de política de empaquetado](https://phab.lubuntu.me/w/packaging/)

También tenemos una [Guía General de Colaboradores](https://phab.lubuntu.me/w/contributor-guide/) que se ha iniciado. Todos estos documentos son un trabajo en progreso, y se actualizarán a medida que tengamos mano de obra.

### Cambios en las redes sociales

Lubuntu ha tenido recientemente [nuestra cuenta de Twitter](https://twitter.com/LubuntuOfficial) (que ahora se refleja en forma bidireccional en [nuestra cuenta de Mastodon](https://mastodon.technology/@lubuntu)) como la principal fuente de informar a los usuarios de los cambios y promover información positiva. Aunque diferentes miembros tienen cuentas en diferentes lugares, también mantenemos presencias en [Reddit](https://www.reddit.com/r/Lubuntu), [Google+](https://plus.google.com/communities/102737741860934586009 ), e [Instagram](https://www.instagram.com/lubuntu_os/) entre otros.

A saber, tenemos varios grupos de Facebook: [Oficial de Lubuntu](https://www.facebook.com/groups/lubuntu.official/), [QA de Lubuntu](https://www.facebook.com/groups/LubuntuQA/ ), y [Lubuntu Offtopic](https://www.facebook.com/groups/lubuntu.offtopic/) así como [nuestra única página oficial](https://www.facebook.com/Lubuntu.Official.Page /) (hay uno no oficial que no controlamos nosotros, sino las mismas personas que controlan la red de Lubuntu DOT, pero no recomendamos seguirlos).

Estamos buscando personas con un interés particular en mantener e inspirar la discusión en nuestros grupos de Reddit, Facebook y Google+. En este momento, estos tienen solicitudes de soporte o solo son enlaces a estas publicaciones del blog. Si está interesado, por favor [envíe un correo electrónico a Simon Quigley](mailto: tsimonq2@lubuntu.me) con el tema "Deseo ayudar a mantener la presencia del SITIO de Lubuntu" (donde "SITIO" es Reddit, Facebook o Google+) .

Si nadie interviene para ayudar a administrar estos grupos, es probable que los cerremos dentro del próximo mes más o menos. Estaremos encantados de entrenar a quien esté interesado.

Además, estamos abriendo al público nuestro soporte y grupos de Telegram "Offtopic". ** Tenga en cuenta que los siguientes enlaces son temporales y pueden cambiar en cualquier momento; no dude en consultarnos en el canal principal de desarrollo para los actualizados si estos enlaces cambian. ** [Soporte](https://t.me/joinchat/DH6s1ELAZusx_9mFamoScg), [offtopic](https://t.me/ joinchat / DH6s1EKjxEYc6M3YGRGt-Q). Estos enlaces estarán disponibles en [nuestra página principal de enlaces](https://lubuntu.me/links/) en los próximos días.

### Respondiendo preguntas sobre Wayland

En el último boletín informativo anunciamos que vamos a cambiar a Wayland vía Mir para 20.10. Aquí hay algunas preguntas comunes que hemos recibido y algunas respuestas para ellas.

** P: ** ¿Por qué elegisteís 20.10? ¿Por qué no antes?
** R: ** Algunas personas especularon que esto era porque el trabajo para portar Openbox tomaría mucho tiempo. Es probable que tome mucho menos tiempo, pero la verdadera razón para esperar tanto es porque 20.04 es la primera LTS que enviaremos con LXQt. Al enviar una LTS con una pila X ya probada y verificada, es una cosa menos por la que debemos preocuparnos antes de saber que está lista. Por lo tanto, es probable que tengamos una sesión alternativa con Wayland una vez esté lista y la enviemos a la LTS, pero no la respaldemos como ** predeterminada ** hasta la llegada de 20.10.

** P: ** ¿Por qué elegir Mir en lugar de wlroots?
** R: ** Mir es compatible con tarjetas gráficas NVIDIA, mientras que wlroots no. Un principio principal de Lubuntu es no romper el sistema operativo si podemos evitarlo. Eso también sirve para dar soporte a una marca de tarjetas gráficas muy popular. Aquí hay un comentario que Chris Halse Rogers del equipo Mir dejó en la última publicación del blog que vale la pena destacar:

> Acerca del soporte de NVIDIA: [este PR](https://github.com/MirServer/mir/pull/415) acaba de fusionarse, arreglando la plataforma 
eglstream-kms (que es compatible con NVIDIA, cuando se activa el soporte de modos en el controlador NVIDIA).
>
> Todavía no admite clientes GL, pero las extensiones están en su lugar y esa es una de    las siguientes cosas en mi lista.

Además, Alan Griffiths del equipo Mir respondió a un comentario que preguntaba sobre escritorios remotos, diciendo:

> Esto es algo a lo que cada compositor de Wayland tiene que enfrentarse, 
sucederá y se consensuará.
>
> Desde la perspectiva de Mir, el equipo principal aún no ha llegado a esto. Sin embargo, conozco un par de esfuerzos de la comunidad en ese aspecto:
> https://github.com/MirServer/mir/issues/467
> https://forums.ubports.com/topic/1389/reverse-convergence-view-control-your-phone-from-computer-like-vnc-rdp
>
> Lo lograremos.

Si bien hemos estado en conversaciones con Drew DeVault desde el boletín anterior, y planeamos utilizar algunos de los estándares en los que él y otros han trabajado, como salvaguarda, aún creemos que para un futuro inmediato, Mir es la mejor opción .

** P: ** ¿Qué pasa con el proyecto Waybox ya existente?
** R: ** No sabíamos que existía antes de afirmar que íbamos a portar Openbox a Mir, y actualmente estamos en conversaciones con el autor de ese código para utilizarlo en lugar de duplicar el trabajo, si es posible.

### Varios

Como siempre, se agradecerá feedback.

# ¿Quiere ayudar?

Una de las maneras más fáciles de involucrarse con Lubuntu y ayudarnos a hacer que este lanzamiento sea el mejor es probar Lubuntu y reportar errores.

Puede aprender a escribir un excelente informe de errores que nos ayude a resolver su problema más rápido al leer [esta guía](https://www.chiark.greenend.org.uk/~sgtatham/bugs.html).

Se puede encontrar más información sobre las pruebas en Lubuntu [aquí](https://phab.lubuntu.me/w/testing/).

# Traducciones

Tenemos [una instancia de Weblate](https://translate.lubuntu.me/projects/) disponible para traducciones. En este momento no hay muchas cadenas para traducir, pero a medida que pase el tiempo, agregaremos más.

¿Habla un idioma que no está disponible para traducir allí? Háganoslo saber en los comentarios o [en otro lugar](https://lubuntu.me/links/) y agregaremos ese idioma.

Esta semana, Wolfenprey tradujo varias publicaciones del blog de Lubuntu al español. ¡Gracias!

También hemos agregado soporte para coreano después de un comentario en nuestra última publicación.

Aquí están los traductores que han contribuido hasta ahora:

 - Henrik Christiansen (danés)
 - Hans P. Möller (alemán, español)
 - Daniel Absmeier (alemán)
 - Luís Rafael Gomes (portugués)
 - Lucas A. V. Dantas (portugués (Brasil))
 - Marcin Mikołajczak (polaco)
 - Tony Cuesta Escobar (catalán)
 - Einar Mostad (Bokmål noruego)
 - Emanuele Antonio Faraone (italiano)
 - Carl Schwan (francés)
 
 ¡Gracias por tus valiosas contribuciones!

# Hoja de Ruta

Puede encontrar el ciclo de publicación de Cosmic Cuttlefish [aquí](https://wiki.ubuntu.com/CosmicCuttlefish/ReleaseSchedule). La versión beta está programada para el 27 de septiembre de 2018 y la fecha de publicación final para el 18 de octubre de 2018.

En lugar de seguir enumerando nuestros objetivos aquí, hemos creado [una tarea en nuestra instancia de Phabricator](https://phab.lubuntu.me/T53) con todos los bloqueadores en las versiones de Lubuntu y las características esperadas. Además, ahora tenemos [una página wiki](https://phab.lubuntu.me/w/lubuntu_2/) que detalla el trabajo que vamos a hacer para el final del siguiente ciclo de desarrollo.

Nuestro equipo artístico todavía está trabajando en Lenny, y le haremos saber cuándo tenemos a Lenny Cuttlefish. :)

# En la prensa

Esta sección es para resaltar la cobertura excepcional de Lubuntu desde el último número.

## Inglés

 - [Después de adoptar LXQt, Lubuntu está cambiando a Wayland por defecto para Ubuntu 20.10](https://news.softpedia.com/news/after-adopting-lxqt-lubuntu-is-switching-to-wayland-by-default- for-ubuntu-20-10-522370.shtml)
 - [Cambio de Lubuntu hacia Wayland, portando Openbox a Mir](https://www.phoronix.com/scan.php?page=news_item&px=Lubuntu-Openbox-Mir-Wayland)

El Jefe de Lanzamiento, Simon Quigley, estuvo en un episodio de un hangout semanal en vivo sobre Linux, muy informal, llamado [BigDaddyLinux](https://www.youtube.com/channel/UCtZRKfyvx7GUEi-Lr7f4Nxg) (Rocco) Live. Hablaron sobre nuestra llamada para realizar pruebas en [su episodio hace una semana](https://www.youtube.com/watch?v=e-OmgNAiif4) y lo convirtieron en su desafío de distribución semanal. Simon se unió al [último episodio](https://www.youtube.com/watch?v=AoCy98PIM1o) que le dio al equipo de Lubuntu algunos comentarios valiosos sobre la dirección tomada para el futuro.

Siéntase libre de [unirse al grupo Destination Linux en Telegram](https://t.me/joinchat/DH6s1EJ4bp9iKemtBhgf5A) (el lugar principal de chat para BDLL) y dígales que vienen de nuestra parte.

## Español

 - [Lubuntu usará Wayland pero no será hasta 2020](https://ubunlog.com/lubuntu-utilizara-wayland-pero-no-sera-hasta-el-2020/)
 - [Lubuntu optara por el servidor grafico Wayland para sus próximas versiones](https://www.linuxadictos.com/lubuntu-optara-por-el-servidor-grafico-wayland-para-sus-proximas-versiones.html)

¿Encontraste alguna otra historia excepcional sobre Lubuntu? [Háganoslo saber](https://lubuntu.me/links/) y estaremos encantados de incluirla aquí.

# Contáctenos

Síganos en [Twitter](https://twitter.com/LubuntuOfficial) para obtener las últimas actualizaciones de Lubuntu. ¿No usas Twitter porque no es software libre? ¡No problemo! Síganos en [Mastodon](https://mastodon.technology/@lubuntu) donde se publica el mismo contenido.

No dude en ponerse en contacto con nosotros [aquí](https://lubuntu.me/links/) para obtener asistencia, y para fines de prensa / marketing o si tiene una consulta privada, puede ponerse en contacto con el Jefe de Lanzamiento Simon Quigley [aquí](mailto: tsimonq2@lubuntu.me).