# Generar un diagrama UML de clases a partir de un caso
## Leer y analizar el caso
Es vital identificar las entidades principales; personas, objetos, conceptos clave, etc.

Por ejemplo: “Una empresa tiene empleados, departamentos y proyectos. Los empleados trabajan en proyectos y cada departamento tiene un director.”

En este caso, nuestras entidades son Empleado, Departamento, Proyecto.
## Definir las clases UML
Cada entidad identificada se convierte en una clase UML, con atributos relevantes, identificar los que haya mencionados en el caso, por ejemplo:
- Empleado -> id, nombre, sueldo
- Departamento -> idDepartamento, nombre
- Proyecto -> idProyecto, nombre, ubicacion
Las clases persistentes deben marcarse con el estereotipo persistent
## Definir las relaciones
Definir relaciones entre clases y sus características:
- Asociación
	- Empleado - Departamento (N:1) -> trabaja en
	- Departamento - Empleado (1:1) -> dirige
	- Empleado - Proyecto (M-N) -> trabaja en
- Multiplicidad
	- Indica cuantas instancias participan entre si
- Roles
	- Da una descripción del nombre de la relación
## Definir la herencia
Revisar si los casos requieren de relaciones de herencia, por ejemplo de especialización, representa la relación de herencia a una superclase con la flecha de herencia.
## Representar las restricciones
Usa la notacion UML para restricciones:
- {disjoint}
- {overlapping}
- {mandatory}
- {complete}
- {incomplete}
```plantuml
' Clase Empleado (superclase)
class Empleado <<persistent>> {
  +dni: string
  +nombre: string
  +sueldo: float
}

' Subclases de Empleado
class Tecnico <<persistent>> {
  +especialidad: string
}

class Ingeniero <<persistent>> {
  +area: string
}

' Clase Departamento
class Departamento <<persistent>> {
  +numero: int
  +nombre: string
}

' Clase Proyecto
class Proyecto <<persistent>> {
  +numProyecto: int
  +nombre: string
  +ubicacion: string
}

' Relaciones
Empleado "N" -- "1" Departamento : trabaja_en
Departamento "1" -- "1" Empleado : administra
Empleado "M" -- "N" Proyecto : trabaja_en

' Herencia
Tecnico --|> Empleado
Ingeniero --|> Empleado
```