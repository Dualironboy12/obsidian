# Data Model

Existen objetos complejos, como tuplas, sets, bags, listas, etc. Cada objeto tiene un identificador único independiente de sus valores.

Hay clases y tipos, las clases tienen atributos, relaciones y métodos, y los tipos definen la estructura de valores.

Existe la herencia, por ejemplo con la especialización de clases.

Las relaciones son binarias y bidireccionales.

Existe una separación entre la lógica y la física de un sistema, es decir, como se define y como se almacena.
# Behavior Model

Existen operaciones y métodos, que definen el comportamiento de los objetos.

Existe encapsulacion, separando la especificación en ODL y la implementacion en PL.

Los comportamientos son heredados, por ejemplo los métodos que son heredados y re-definidos por las subclases, así como también existe la sobrecarga y el polimorfismo.

Existe ligadura dinámica, es decir, el objeto determina su comportamiento en tiempo de ejecución.

Existen las excepciones, las operaciones pueden lanzar errores.
# Name Model

Se accede a la BD mediante nombres únicos.

Cualquier objeto puede recibir un nombre y servir como punto de entrada.

Existen colecciones de instancias de una clase (extent), por ejemplo Persons, Employees, etc.

En comparación con los RDBMS, donde el acceso es por nombre de tabla, en OO DBMS el acceso es por nombre de objeto o colección.
# Persistence Model

Existen dos tipos de objetos, objetos transitorios, que existen únicamente durante la ejecución del programa, y los persistentes, que se almacenan en la BD y persisten tras cerrar el programa.

Un objeto se vuelve persistente si se asocia con un nombre en la BD o si pertenece a un extent.

Las estrategias para determinar la persistencia son al declarar en la clase, por ejemplo "extent Employees", y dinámico, se pueden cambiar los estados usando los comandos persist/unpersist