---
marca: Siemens
equipo: "PNPN Coupler"
howto: True
descripcion: "Configuración safety PN/PN Coupler TIA Portal"
---

[[PNPN Coupler]]

## Intercambio señales Safety PN/PN Coupler

Para realizar intercambio de señales [[safety]] hay que añadir el módulo **IN/OUT** como módulo del dispositivo:

![[inoutpnpn.png]]

En la parte de **X2** se añadiría al revés, **PROFIsafe IN/OUT 6 Byte/ 12 Byte**.

En el programa [[safety]] del PLC hay que utilizar dos FB:

- **SENDDP**: Enviar señales
- **RCVDP**: Recibir señales

La info de [[TIA]] explica bien como utilizar los bloques, solo añadir que en la entrada **DP_DP_ID** de cada uno de ellos debe indicarse el mismo número en ambos proyectos, siendo este único en la red.
En la entrada **LADDR**  hay que indiciar el valor decimal que genera TIA portal para la variable constante asociada al módulo de comunicaciones IN/OUT (cada proyecto tendrá su propio valor, no es necesario que sean indénticas):

![[cosntantepnpn.png]]

El valor de **TIMEOUT** debe ser igual también en ambos bloques (**SENDDP**, **RCVDP**).