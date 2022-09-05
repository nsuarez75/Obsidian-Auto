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

En el apartado **Modo de operación** se ajustan las direcciones del HMI como IO Device, donde se recibirán las señales de sus elementos (hombre muerto, seta de emergencia, botones frontales, llave lateral) que luego se asociarán a los bloques del safety que tenemos que configurar.

![[modooperacion.png]]

## Configuración bloques de comunicación en programa safety:

Para hacer la gestión de la parte safety del HMI hay que añadir dos bloques en el programa:

- a