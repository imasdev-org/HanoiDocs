# Estados de un Pedido - Flujo

Los pedidos avanzan desde que son creados hasta que son entregados por un flujo que tiene diversos pasos (configurables). 

## Visibilidad
No todos los estados son visibles para el cliente - por ello en la lista de estados vemos el estado en si, y una columna adicional que indica el "Estado xa Cliente". Los estados visibles por el cliente son los que se ven en el avance del pedido cuando vemos los detalles de un pedido en el web o en la app.

## Orden
Cada estado tiene un orden asociado - que define el flujo -, o puede ser definido como una excepcion en cuyo caso el orden no importa. 

## Condiciones
El flujo de avance - desde creado hasta entregado - puede tener ciertas diferencias segun el tipo de sucursal. Por ejemplo en las sucursales de tipo pickup (Click & Go) no tiene sentido el estado "Enviado a Domicilio" y por tanto se puede saltear en este tipo de sucursales - esto puede hacerse en la pestanha de configuracion avanzada del estado. 
De esta forma, pueden definirse diferentes flujos segun los tipos de entrega, compartiendo la definicion de los estados en comun.

## Notificaciones
Asociado a cada estado, se puede asociar una o mas notificaciones que se disparan cuando el pedido entra en dicho estado.
Las notificaciones tienen un medio asociado que define la forma en que la notificacion sera enviada al cliente (nota: no todos los medios estan habilitados, hoy en dia Whatasapp aun no esta configurado para produccion). Se pueden elegir 'todos los medios' tambien y notificar al cliente por todos los medios disponibles. Notese que NO hay forma ahora mismo para que un cliente evite dichas notificaciones o elija un medio particular por tanto es importante ser selectivo para no atomizar al cliente con notificaciones por todos los medios.  
En caso que una notificacion tenga habilitado el medio 'Email' se asocia con una plantilla de email que define el contenido/formato del mismo. Las planillas estan definidas en Mandrill y por ello no es posible agregar una nueva sin programar la plantilla nueva y asociarla a las posibles plantillas. 
Las notificaciones pueden tener una accion asociada que agregaran un link (o una accion en la app) para poder abrir una pagina especifica cuando el cliente hace click en la notificacion o en el link (tipicamente para acceder a la pagina de detalles del pedido en este tipo de notificaciones).
