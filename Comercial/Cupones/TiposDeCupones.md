# Tipos de Cupones

## Cupones del Ecommerce.

Los cupones pueden ser 'al portador' o para un cliente especifico. 
Los cupones personales (es decir, asignados a un cliente) son visibiles en la seccion 'mis-cupones' de cada cliente - y en caso de tener cupones personales aplicables a una compra, el boton 'aplicar cupones' se visualiza destacado.

Los cupones al portador en cambio, son un codigo que tiene que ingresar el cliente en el momento de la compra. 

## Cupones Externos

Es posible definir cupones externos (Fielo, PromoThor) que se asocian con cupones del ecommerce de diferentes maneras:

### Cupones de Aplicacion Automatica 

#### Clientes definidos por Fielo
Estos corresponden a las campanhas de upsell y afines. Se define un segmento en Fielo a los cuales se les ofrecera un descuento. El segmento en Fielo se representa en el Ecommerce como un Grupo de tipo Segmento de Fielo (y se indica los segmentos de Fielo correspondientes). De esta manera el ecommerce sabra que clientes se encuentran asociados al grupo. 
A la hora de aplicar el descuento en caja se puede dejar en manos del ecommerce asociando un codigo de caja al grupo, el cual se envia a la caja junto con la compra. Este codigo de caja debe corresponder con la promocion (GeoPromotion) que aplica el descuento.
En este caso el codigo de caja se aplica en cada compra que haga el cliente, mientras que la promocion este activa en caja, el grupo este activo en el ecommerce y el cliente este asociado a los segmentos en Fielo.

#### Clientes definidos en el Ecommerce
Estos corresponden a Grupos de tipo Dinamico en el Ecommerce. En este caso, es el ecommerce quien define - segun reglas del grupo - que clientes participan en el mismo.
La aplicacion del cupon es tambien automatica en cada compra del cliente - mientras el grupo este activo y el cliente se encuentre asociado al mismo -, aunque es posible limitar la cantidad de aplicaciones del cupon, configurando un tope de compras en el grupo.



