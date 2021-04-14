# Consideraciones para la Busqueda

Hay varios elementos de los productos que afectan como los mismos rankean en los resultados de las busqueds - cuando se ordenan por relevancia.
Los atributos importantes son:

- *Nombre* : El nombre del producto es una parte clave en cuanto a su efecto en los resultados. La primera palabra del nombre deberia ser aquella palabra mas buscada/representativa. En la busqueda lo que tiene mas fuerza es el match de la primera palabra buscada con la primera palabra del nombre del producto. Por tanto, si un cliente busca 'Coca' tiene igual relevancia 'Refresco Coca Cola' que 'Jamon Doña Coca'. Si queremos darle mas fuerza a la coca cola, el nombre del producto deberia ser 'Coca Cola Refresco' (si es que queremos poner la palabra Refresco en el nombre). 
- *Keywords* : Las keywords ayudan a ubicar un producto asignandole posibles palabras de busqueda que no sean parte del titulo / nombre de la categoria / descripcion, etc. Las keywords se analizan como una bolsa de palabras, es decir, las frases no son relevantes ('dulce de leche') crea 3 palabras que se usaran en la busqueda 'dulce' 'de' y 'leche'. 
- *Cantidad de Hits de primera palabra* : Hay un efecto de ponderacion por la cantidad de veces que el termino buscado se repite en nombre del producto (no asi en el resto de los datos). Si tenemos un producto que se llama 'Leche saborizada, sabor Duce de Leche' y un cliente busca 'Leche' este producto va a rankear mas alto que otros que por ahi pueden tener mas ventas.
- *Impulso*: El impulso funciona como parte del ponderador que permite incrementar o bajar la relevancia. Es un multiplicador por tanto deberia ir de 0 a n.  En caso de asignarle 0 el ponderador de ventas se elimina.
- *Datos*: Los datos de producto indexados son primera-palabra-del-nombre, nombre, codigo-de-producto, descripcion, primeras 3 categorias del arbol (por ejemplo Bebidas/Bebidas con Alcohol/Espumantes), Marca, categorias de tipo lista (visibles) 
 
## Busquedas x Texto
### Usuario Anonimo
- Que haya stock
- Hit en 1a palabra ponderado por frecuencia de la 1a palabra
- Disponibilidad (cosa que sin stock y alternativos queden al final)
- Ventas totales ponderadas por Impulso

### Usuario Logueado
- Que haya stock
- Que el cliente haya comprado
- Hit en 1a palabra ponderado por frecuencia de la 1a palabra
- Disponibilidad (cosa que sin stock y alternativos queden al final)
- Ventas totales ponderadas por Impulso

## Navegar por Categoria (Menu)
### Usuario Anonimo
- Que haya stock
- Ventas totales ponderadas por Impulso
- Disponibilidad (cosa que sin stock y alternativos queden al final)

### Usuario Logueado
- Que haya stock
- Que el cliente haya comprado
- Ventas totales ponderadas por Impulso
- Disponibilidad (cosa que sin stock y alternativos queden al final)

