# Que es XQuery?
Es un lenguaje de consulta para documentos en [[XML]], basado en [[XPath]], se basa en la esctructura FLWR (For-Let-Where-Return)
- for: recorre nodos
- let: asigna variables
- where: filtra resultados
- return: construye la salida
Por ejemplo:
```XQuery
for $b in //book
where $b/price > 30
return $b/title
```
Devuelve los titulos de libros con precio mayor a 30
# Funciones comunes
- sum(), avg(), count()
- distinct-values()
- string-length()
# Ventajas
Permite construir resultados en XML, es mas expresivo e intuitivo que XPath, y es ideal para transformar y filtrar datos en XML.