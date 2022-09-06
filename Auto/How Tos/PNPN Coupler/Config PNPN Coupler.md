---
marca: Siemens
equipo: "PNPN Coupler"
howto: True
descripcion: "Configuración PN/PN Coupler TIA Portal"
---

[[PNPN Coupler]]

## Configuración PN/PN Coupler TIA Portal:

Si ambos [[PLC]] a conectar están en el mismo proyecto se utilizan ambas bocas del [[PNPN Coupler]] de las dos tarjetas de red, cada una conectada a su controlador con su IP correspondiente.

Normalmente los [[PLC]] están en proyectos diferentes ya que los usamos (al menos en automoción) para comunicar entre [[PLC|PLCs]] de nuestra misma línea cuyas redes no se conectan fisicamente y cada uno tiene su propio proyecto de TIA o con otras máquinas de otros proveedores.

Si están en distinto proyecto hay que activar esta opción:

![[ajustecoupler1.png]]


El controlador del proyecto donde esté fisicamente(el que lo tenga en su armario eléctrico) el [[PNPN Coupler]] lo conectaremos a su puerto **X1**:

![[Pasted image 20220906123253.png]]
El puerto **X2** no hace falta configurarlo, se puede dejar la IP y nombre sin asignar.

Después hay que definir el mapeado de señales:

![[Pasted image 20220906122500.png]]

En el otro proyecto habría que conectar el controlador al **X2** en vez de a **X1** y configurar el mapeado teniendo en cuenta que la zona a configurar es la **X2**, donde deberá ser un espejo de **X1**.

Ej:
**X1 8Bytes IN** ----- **X2 8Bytes OUT**
**X1 8Bytes OUT** ----- **X2 8Bytes IN**
etc.


## ## Configuración PN/PN Coupler fabricante externo:

Si la otra máquina no es Siemens y utiliza otro entorno de programación, deberá descargar de [[Siemens]] el GSDML correcto.

[GSDML PNPN Coupler](https://support.industry.siemens.com/cs/document/23742537/profinet-gsd-files-gateway?dti=0&lc=en-WW)

![[arbolpnpn.png]]

Hay que añadir **X1** o **X2**, depende de donde esté conectado el cable de red del equipo y configurar el mapeado igual que se hacía en TIA Portal pero con el orden de señales en espejo.

Lo que se configura en **X1** debe configurarse a la inversa en **X2**, es decir:

![[modulospnpn.png]]

**X1 8Bytes IN** ----- **X2 8Bytes OUT**
**X1 8Bytes OUT** ----- **X2 8Bytes IN**
etc.