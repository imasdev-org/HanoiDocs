# Collecionables #
Es un tipo de promocion que permite implementar un descuento en la compra de productos al utilizar stickers.

Los clientes pueden juntar stickers virtuales o fisicos. Si juntan stickers virtuales pueden usarlos en el web para obtener un descuento al comprar los productos coleccionables (aquellos productos definidos en la promo).

Las promos coleccionables permiten definir:
- La cantidad de stickers por cartilla (esta informacion se usa solo para tener una relacion entre las cartillas fisicas y la acumulacion de stickers virtuales, pero no tiene efecto en la funcionalidad). Hay veces que los stickers se presentan agrupados por cartilla para mantener esa relacion con el mundo fisico.
- El mensaje de producto se muestra SOLO a clientes que no juntan stickers virtuales, de forma de poder poner un mensaje que los impulse a acumular stickers virtuales (por ejemplo: "Si juntaras stickers podrias comprar este productos online con descuento!")
- A nivel de cada producto coleccionable se indica el precio al canjear una cartilla y el precio al canjear media cartilla. Esta informacion se muestra en la pagina de producto. En carruseles y resultados de la busqueda solo se muestra el precio al canejar 1 cartilla completa.

## Funcionamiento de la Promo ##
### Carrito ###
Al agregar productos coleccionables al carrito se agregan con el precio de lista. 
Si el cliente junta stickers virtuales se aplican los stickers de forma de descontar primero los productos de mayor precio (es decir, si el cliente tiene 45 stickers, la cartilla tiene 28 stickers y compra 2 productos coleccionables, se aplicara una cartilla (28 stickers) al producto mas caro, y media cartilla (14 stickers) al siguiente. Completando 42 stickers y le sobran 3.
En cada producto va a ver los stickers que se le aplican y en los descuentos aparece el descuento total obtenido al canjear los stickers.

### Checkout ###
En el checkout el descuento se ve como todos los demas descuentos como parte del summary. 
A la misma vez, debajo del summary se muestra la informacion de cartillas canjeadas - para asemejar el proceso al mundo fisico y porque podria existir una mejor aplicacion de las cartillas a la que resuelve el algoritmo y al menos se da visibilidad de lo que va a hacer el sistema. Si al usuario no le gusta es libre de no comprar y realizar su compra fisica con mas control de la aplicacion de los stickers.

## Integraciones ###
Por ahora la aplicacion de los stickers en la caja se hara de forma manual, por lo cual en la picklist se mostrara una seccion con informacion del canje, para que se pueda ingresar en la caja a mano.





