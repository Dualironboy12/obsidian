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
	- count, sum, avg, min, max
	- union, intersect, except
	- for all, exists
- Usar métodos en consultas
```SQL
select p.oldest_child.address.street from Persons p
where p.lives_in("Grenoble")
```
- Agrupamiento y ordenamiento:
	- group by y having
	- order by con multiples criterios (asc, desc)

