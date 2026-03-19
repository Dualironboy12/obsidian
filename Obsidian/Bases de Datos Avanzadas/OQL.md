# Que es el OQL (Object Query Language)?
- Tiene una sintaxis similar a SQL-2, pero con características que la hacen orientada a objetos
- Cuenta con acceso declarativo, puede seleccionar objetos y valores sin necesidad de recorrerlos manualmente
- Soporta colecciones:
	- set: conjunto sin duplicados
	- bag: multiconjunto (permite duplicados)
	- list: lista ordenada
- Ejemplo de consultas en OQL: Nos devuelve un `bag<short>` con las edades
```SQL
select p.age from Persons p where p.name = "Pat"
```
- Construcción de objetos y valores:
```SQL
Person(name: "Pat", birthdate: Date "1956-3-8")
```
- Operadores y funciones
	- count(): numero de elementos
	- sum(): suma de valores
	- avg(): promedio 
	- min(), max(): valores extremos
	- union: union de dos conjuntos
	- intersect: intersección de dos conjuntos
	- except: diferencia entre dos conjuntos
	- for all: todos los elementos cumplen una condicion, ejemplo: `for all e in Employees: e.salary > 100000`
	- exists: al menos un elemento cumple la funcion
	- element(): extrae un unico elemento de un conjunto
	- flatten: aplana colecciones anidadas
	- listtoset: convierte lista en conjunto (list to set)
- Usar métodos en consultas
```SQL
select p.oldest_child.address.street 
from Persons p
where p.lives_in("Grenoble")
```
- Agrupamiento:
	- group by y having:
		- Permite dividir los resultados de una consulta segun algun atributo
		- Ejemplo: Este devuelve el numero de personas por edad, se puede usar having para filtrar los grupos tambien
```SQL
select age, count(partition)
from Persons p
group by p.age
```
- Ordenamiento:
	- order by: organiza resultados en listas ordenadas
	- Ejemplo: devuelve una lista de empleados ordenados por edad descendente y nombre ascendente
```SQL
select p from Employees p
order by p.age desc, p.name asc
```
- Tipos de resultados:
- list: cuando se usa order by
- bag: cuando no hay orden explicito y pueden haber duplicados

