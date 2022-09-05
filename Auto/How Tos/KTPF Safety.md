---
marca: Siemens
equipo: HMI
howto: True
descripcion: "Configuración safety KTPxF"
---
[[HMI Siemens]]

Antes de nada hay que ponerle la IP al HMI a mano en los ajustes de sistema entrando en la configuración de red y escogiendo la tarjeta de red correcta.

Cargamos todo el software desde el [[TIA]].
Una vez cargado volvemos al HMI, seguramente aparecerá la ventana de selección del tipo de parada de emergencia, si no se puede acceder a ella desde los ajustes. 
Normalmente se escoge el profisafe e-stop. Hay que escribir el ID que se ha configurado en la [[Connection Box KTP Mobile]] y darle a guardar, nos saltará un aviso diciendo que es necesario crear una contraseña. Si sale un tick verde es que se ha guardado correctamente, de lo contrario significa que el ID introducido no corresponde con el configurado en la [[Connection Box KTP Mobile]] .

A parte de configurar el ID, es necesario que en la config de profinet esté activado el modo IO device, ya que si no no funcionará la seta de emergencia ni el hombre muerto.

En el programa del PLC hay que hacer unos ajustes para que todo funcione correctamente:
- ### [[KTPF Safety TIA]]




