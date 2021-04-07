# Productos Agotados

En una promocion, se puede definir un numero maximo de productos a vender, despues de lo cual el producto pasa a estar 'agotado'.

## Como se agota un producto?
Un producto se agota cuando se llega a un numero de ventas mayor al tope definido en la promo. Las ventas se calculan desde el inicio de de la promocion.
El calculo se hace en tiempo real (al completar cada compra que contenga productos con tope) de forma 'temporal'

El proceso de migracion evalua - para todas las promociones activas que tengan algun producto con tope - las ventas desde la fecha de inicio de la promo y actualiza el estado de agotado o no del producto.
Esta evaluacion es necesaria porque podria haber cancelaciones en ventas, o cambios en la configuracion de la promocion que dejen los valores previos obsoletos.

La marca de agotado se controla por sucursal / mundo. Es decir, si la promocion estaba restringida a ciertas sucursales la marca de agotado se aplica solo para dichas sucursales.

## Como se des-agota un producto?
Cuando la promo se desactiva, se desagota automaticamente.
Si se aumenta el tope a un numero mayor de las ventas registradas, se desagota automaticamente (el proceso de migracion lo re-evaluara).

Cuando se desagota un producto en el backend (es decir, se aumenta el tope o se deshabilita el producto en la promo) se deshagota SOLO para aquellas marcas que hayan sido generadas por la promocion afectada
Cuando se desagota un producto desde migracion porque se termino la promocion, se deshabilita el producto para todas las sucurales donde la promocion estaba activa - en este caso NO se controla promocion. Esto es porque la marca de agotado puede estar definida solo para 1 promocion, pero podrian haber definiciones solapadas de promociones que no sabemos bien el efecto. Del mismo modo se realiza para todos los mundos donde aplica la promocion.

## Que efecto tiene que un producto se marque como Agotado?
En el sitio el producto pasa a no ser comprable y muestra una etiqueta 'En Sucursales'. 
En las busquedas el producto pierde relevancia quedando para el final junto con los productos sin stock.

Si bien el cambio a 'agotado' se hace en tiempo real en la compra que agota el producto, en las busquedas el producto no se vera como agotado hasta que corra el proceso de migracion. Pero si veremos el producto agotado en la pagina de producto o el carrito de compras.

