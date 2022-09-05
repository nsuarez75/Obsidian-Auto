---
marca: Siemens
equipo: HMI
howto: True
descripcion: "Configuración safety KTPxF en TIA"
---
[[HMI Siemens]]

## Configuración de dispositivo en TIA:
En [[TIA]] hay que configurar la **F-destination address** del HMI:

![[safetyhmi1.png]]

En el apartado **Modo de operación** se ajustan las direcciones del HMI como IO Device, donde se recibirán las señales de sus elementos (hombre muerto, seta de emergencia, botones frontales, llave lateral) que luego se asociarán a los bloques del [[safety]] que tenemos que configurar.

![[modooperacion.png]]

Una vez asignadas estas direcciones es conveniente crear variables para ellas:

Entradas: 

![[entradassafetyHMI.png]]

Salidas:

![[salidassafetyHMI.png]]
## Configuración bloques de comunicación en programa safety:

Para hacer la gestión de la parte [[safety]] del HMI hay que añadir dos bloques en el programa:

- **F_FB_KTP_Mobile**: Encargado de controlar el HMI.
-  **F_FB_KTP_RNG**: Encargado de controlar la [[Connection Box KTP Mobile]]

La explicación de las E/S de estos FB está bien comentada en la ayuda de [[TIA]], solamente apuntar un par de cosas.

En el **F_FB_KTP_Mobile**, en la entrada **MP_DATA** se debe asignar la variable que hayamos creado en el paso anterior para las entradas [[safety]] del HMI y en la salida **MP_DATA_Q** la que hayamos definido para las salidas.

![[variablessafetyhmi.png]]

En el **F_FB_KTP_RNG** en la entrada **ID** se debe asignar el número de ID que hayamos configurado en la [[Connection Box KTP Mobile]] y en las salidas es donde asignaremos las señales de la seta de emergencia y del hombre muerto a las variables que hayamos definido para ello en nuestro proyecto.

![[bloque rng.png]]