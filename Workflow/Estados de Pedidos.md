# Estados de un Pedido 

Los pedidos avanzan desde que son creados hasta que son entregados por un flujo que tiene diversos pasos (configurables).
No todos los estados son visibles para el cliente - por ello en la lista de estados vemos el estado en si, y una columna adicional que indica el "Estado xa Cliente". Los estados visibles por el cliente son los que se ven en el avance del pedido cuando vemos los detalles de un pedido en el web o en la app.

Cada estado tiene un orden asociado - que define el flujo -, o puede ser definido como una excepcion en cuyo caso el orden no importa. 

El flujo de avance - desde creado hasta entregado - puede tener ciertas diferencias segun el tipo de sucursal. Por ejemplo en las sucursales de tipo pickup (Click & Go) no tiene sentido el estado "Enviado a Domicilio" y por tanto se puede saltear en este tipo de sucursales - esto puede hacerse en la pestanha de configuracion avanzada del estado. 
De esta forma, pueden definirse diferentes flujos segun los tipos de entrega, compartiendo la definicion de los estados en comun.
