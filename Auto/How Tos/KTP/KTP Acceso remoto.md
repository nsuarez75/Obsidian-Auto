---
marca: Siemens
equipo: HMI
howto: True
descripcion: "Configuración del acceso remoto al HMI"
---
[[HMI Siemens]]

Es muy recomendable activar el acceso remoto mediante SM@RTCLIENT al HMI, sobre todo en los que llevan [[safety]] ya que para realizar cualquier modificación es necesario ponerlo en modo transfer y así nos podemos ahorrar levantarnos de la silla cuarenta veces al día. 
De todas formas una vez finalizada la puesta en marcha habría que consultar al cliente si quiere mantenerlo activado o no.

Lo primero es activar el servicio sm@artserver en la configuración de runtime del HMI desde [[TIA]].

Una vez hecho esto cargamos cambios y en los ajustes del HMI, en la pestaña WinCC, aparecerá una opción nueva **Remote**.
Dentro deberemos activar la casilla de iniciar en el arranque automáticamente, y en sus ajustes deberemos personalizar las dos contraseñas que aparecen, tanto la que pone **view only** como la que no, la diferencia es que la que está marcada solo nos permitirá visualizar el HMI una vez realizada la conexión remota y la otra nos permitirá interactuar con ella.
Si ponemos la misma contraseña en ambas casillas cogerá por defecto la opción que nos permite interactuar.

En la pestaña Administration hay que definir una contraseña más, se puede poner la misma que antes.

Cuando acabemos guardamos cambios y arrancamos el servicio, después solo es conectarse utilizando el Sm@rtclient que instala por defecto el [[TIA]].

