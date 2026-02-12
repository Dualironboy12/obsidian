# ¿Que es el ODMG?
Fue creado en 1991 para definir estándares de las bases de datos orientadas a objetos, asociado al Object Management Group (OMG). Su objetivo es garantizar la portabilidad y estandarizacion de distintos productos, así como normalizar el modelo de datos y los lenguajes de objetos. Generaron 3 especificaciones:
- ODMG - 93
- ODMG 2.0
- ODMG 3.0

# Componentes del estándar ODMG
Los elementos clave del estándar son:
- Object Model
	- Define que es un objeto: atributos + métodos
- ODL (Object Definition Language)
	- Lenguaje para definir interfaces y clases, especifica atributos relaciones y operaciones, similar al esquema relacional , pero orientado a objetos.
- OQL (Object Query Language)
	- Lenguaje de consulta declarativo, similar a SQL-2 pero orientado a objetos, permite selecciona atributos, métodos, y trabajar con colecciones.
- Interfaces con lenguajes de programación
	- Permite que los objetos en la BD se integren directamente con lenguajes de programación como C++, Java, Smalltalk, etc.

# Conceptos clave
Los conceptos clave del modelo ODMG son:
- Objeto
- Clase
- Interfaz
- Literal
- Colecciones
- Relaciones
- Extent

# Importancia del estándar
Permite que distintos sistemas OO DBMS hablen el mismo "idioma", como los sistemas RDBMS, facilita su integración con lenguajes de programación, define como deben de comportarse, manipularse y consultarse los objetos, y es base para entender como funcionan las operaciones, transacciones y consultas en OO DBMS.