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

A parte de configurar el ID de la [[Connection Box KTP Mobile]], es necesario que en la config del HMI esté activado el modo IO device en los ajustes [[PROFINET]], ya que si no no funcionará la seta de emergencia ni el hombre muerto.

Debemos también indicar la dirección [[safety]] del HMI que configuramos en [[TIA]]  ([[KTPF Safety TIA]]) en el apartado [[PROFIsafe]] del HMI.




