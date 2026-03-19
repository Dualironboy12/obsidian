# Que es XPath?
Es un lenguaje para navega y seleccionar partes de un documento [[XML]]. Tiene expresiones de ruta:
- / : raiz
- // : selecciona en cualquier nivel
- . : nodo actual
- .. : nodo padre
# Predicados
Filtran resultados de queries, por ejemplo:
//book\[price>30]
# Funciones comunes
- position(): devuelve la posicion en la lista
- last(): ultimo elemento
- count(): numero de nodos
- contains(): busca texto parcial
Ejemplo:
```XPath
//person[name="Alan"]/email
```
Selecciona el email de la persona cuyo nombre es Alan