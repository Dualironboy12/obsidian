# ¿Que es UML?
Es un lenguaje grafico estandar para modelar sistemas de software, que permite representar desde la fase de concepción hasta la implementacion, es interpretado tanto por humados como por herramientas CASE (Computer Aided Software Engineering)

# Los [[Diagramas de clases]]
Cuentan con algunos elementos principales:
- Clases
- Visibilidad
- Estereotipos
- Relaciones
# [[UML aplicado a OODBs]]
Cada clase UML persistente se convierte a una clase de la base de datos, los atributos en columnas o propiedades, las relaciones en asociaciones en la BD, y la herencia se traduce en especialización/generalización en el modelo EER y luego en tablas según las opciones de mapeo.

# Ejemplo basico

```plantuml
class Empleado <<persistent>> {
	-idEmpleado: int
	-nombre: string
	-sueldo: float
	
}
class Departamento <<persistent>>{
	-idDepartamento: int
	-nombre: string
}
Empleado "N" -- "1" Departamento : trabaja_en
Departamento "1" -- "1" Empleado : administra
```