# Productos Equivalentes #

Un producto puede tener asociado una categoria que define sus productos 'Equivalentes' y puede pertenecer SOLO a un grupo (o categoria) de equivalencias. Es decir, el producto "Arroz Blue Patna 1k" puede pertenecer solo al grupo "arroces" (que define arroces que tiene sentido sustiuir si no encuentro la marca deseada) pero no puede *ademas* pertenecer al grupo "hidrocarburos" donde podriamos sugerir que si no hay arroz, podes comprar quiona por decir algo. 

En la definicion de Categorias se puede filtrar por tipo 'Equivalentes' para ver todos los grupos que definen equivalencias. Al agregar un producto a una categoria de Equivalencias, ya no se permitira agregarlo a otro.
Cuando un producto pertenece a una categoria de equivalentes se visualiza en el detalle del producto bajo la etiqueta 'Categoria de Equivalentes'. Notese que alli no se puede editar, lo que hay es un acceso directo a la categoria, desde donde puede quitarse el producto (si se desea cambiar su grupo de equivalentes o no ofrecer ninguno), o pueden agregarse otros productos al mismo grupo.

Cuando un producto no pertenece a ninguna categoria de equivalentes, en los detalles del producto se vera un boton para "Definir Categoria de Equivalentes". Esta opcion simplemente crea la categoria y asocia el producto a la misma.


La descripcion de las categorias de tipo "Equivalentes" no se incluyen en el indice - es decir si buscamos por la descripcion de la categoria equivalentes, no deberiamos encontrar los productos asociadas a la misma. Pero si se indexa, y si quisieramos definir una accion para acceder a ella (es decir, asociar por ejemplo un banner que nos lleve a la lista u ocasion) eso si funciona, necesitamos conocer el ID de la categoria solamente.

Por ejemplo http://trunk.web.imasdev.com/busqueda?2139 aqui se accede a los equivalentes de aceitunas (los productos en la lista no son realmente representativos).
