---
marca: Siemens
equipo: "PNPN Coupler"
howto: True
descripcion: "Configuración PN/PN Coupler TIA Portal"
---

[[PNPN Coupler]]

## Configuración PN/PN Coupler TIA Portal:

El GSD que hay en [[TIA]] para el [[Config PNPN Coupler]] es el que se utiliza cuando ambos controladores están en el mismo proyecto de [[TIA]].

Normalmente los controladores están en proyectos diferentes ya que los usamos (al menos en automoción) para comunicar entre PLCs de nuestra misma línea cuyas redes no se conectan fisicamente o con otras máquinas de otros proveedores.

El GSD que facilita las cosas lo podemos descargar de [[Siemens]]:

[GSD PNPN Coupler](https://support.industry.siemens.com/cs/document/23742537/profinet-gsd-files-gateway?dti=0&lc=en-WW)

![[arbolpnpn.png]]

**X1** Se utiliza en el proyecto donde se conecte al lado izquierdo y **X2** donde se conecte el lado derecho.

Cada lado es completamente independiente, está separado galbánicamente, tiene su propia alimentación de 24V(a veces se les olvida alimentar el lado X2), las IPs no tienen por que estar en la misma subred, **X1** no sabe que existe **X2** y viceversa.

En el hardware se configura el intercambio de datos:

![[modulospnpn.png]]

Lo que se configura en **X1** debe configurarse a la inversa en **X2**, es decir:

**X1 8Bytes IN** ----- **X2 8Bytes OUT**
**X1 8Bytes OUT** ----- **X2 8Bytes IN**
etc.

