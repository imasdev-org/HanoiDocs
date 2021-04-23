# Ubicaciones

Las ubicaciones permiten definir un mapa del local y ordena la picklist en funcion de la estructura definida para ubicaciones.

Se puede definir un mapa de ubicaciones a nivel de Centro-de-Armado o a nivel de Sucursal.

El mapa de ubicaciones tiene varias ubicaciones ordenadas, y cada una de ellas tiene varias posiciones. Tanto las ubicaciones como las posiciones tienen un nombre y un orden.
Dentro de cada posicion se pueden asignar:
 - productos
 - categorias (del arbol).

# Ubicacion de un Producto

Un producto se puede ubicar de forma directa - es decir, asignar el producto a una posicion especifica de una ubicacion especifica - o de forma indirecta a traves de su categoria pricipal (es decir, aquella que llega a la raiz del arbol mercadotecnico).
En dicho caso se buscan las categorias de forma de ubicar al producto por la categoria mas especifica primero, y mas generica al final. Por ejemplo si un producto tiene la siguiente categorizacion: "Oliva">"Aceites y Vinagres">"Almacen", se va a ubicar en aquella posicion asociada a la categoria "Oliva", en caso de no haber ninguna, se buscara la ubicacion de "Aceites y Vinagres", y en caso que no se encuentre se buscara la categoria 'Almacen'.
Si no se encuentra ninguna ubicacion de esta forma, se asignara a una ubicacion especial al final (Productos sin Ubicacion).
