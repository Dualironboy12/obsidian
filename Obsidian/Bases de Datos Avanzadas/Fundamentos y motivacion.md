# DBMS Relacionales
## Historia y Madurez
Los RDBMS (DBMS Relacionales) llevan mas de 40 años en la industria, han habido prototipos desde los años 70s, con productos comerciales a partir de los años 80s.
## Fortalezas
Es una tecnología madura, optimizada y eficiente, tiene concurrencia con las propiedades [[ACID]], es segura ya que permite diseñar bases de datos resistentes y persistentes.
Adicionalmente, el estándar de los lenguajes basados en SQL permite que haya bastante soporte y distribución, con multiples y robustos DBMS.

## Limitaciones de los RDBMS
El modelo relacional es plano, no cuenta con estructuras complejas, solamente maneja datos básicos, no existen métodos ni comportamientos, únicamente contando con procedimientos almacenados.
Adicionalmente los lenguajes basados en SQL no son lenguajes de programación, son lenguajes de consulta (Query), lo que limita sus características, no cuentan con modularidad, herencia, polimorfismo, etc. Esto mismo provoca impedancia al interactuar con lenguajes de programación, especialmente los lenguajes basados en paradigma orientado a objetos.

# PL vs. DML

## Lenguajes de programación (PL)
Integran datos y programas, suelen estar optimizados, hoy en día cuentan con garbage collectors, aun que la persistencia de la información esta limitada a información guardada en variables y bloques.

## Lenguajes de Manipulación de Datos (DML)
Tienen integrada persistencia sistemática de los datos en el disco. Todas las transacciones están diseñadas para ser gobernadas por el concepto de [[ACID]]. Están diseñados para manipular únicamente datos, no tienen capacidades o comportamientos mas alla de eso.

## Problema
Dos tipos y paradigmas de lenguajes distintos implican tener constantes conversiones entre datos y objetos para realizar operaciones y consultar datos.

## Solución
Una forma de solucionar esto es usando OO DBMS, es decir, bases de datos diseñadas para operar con objetos que viajan "del disco a la pantalla" sin requerir conversiones.

# Bases de Datos Orientadas a Objetos
## Conceptos OO aplicados a las BDs
En las OO DBMS contamos con objetos con atributos y métodos, con identidad única y relaciones mas complejas.

## Origen
Los OO DBMS responden a necesidades creadas por tecnologías y flujos de trabajo modernos:
- Inteligencia Artificial
- Lenguajes Orientados a Objetos

## Modelos Semanticos
En el caso de las OO DBMS contaremos con muchas características que trae el paradigma orientado a objetos, como clases, herencia, composición, generalización, etc.

# "Golden Rules" de los OO DBMS
Los sistemas que existen en OO DBMS deben contar con:
- Persistencia confiable
- Seguridad y recuperacion
- Compartir datos
- Consultas ad-hoc
- Soporte para objetos complejos
- Tipos y Clases
- Encapsulacion y herencia
- Ligadura dinamica
- DBMS completo y extensible

# El [[ODMG y estandares]] (Object Database Management Group)
Creado en 1991 para estandarizar los OO DBMS, ha tenido multiples versiones (ODMG-93, ODMG 2.0, ODMG 3.0), con el objetivo de dar potabilidad y normalizacion a los OO DBMS.

Definieron las siguientes especificaciones:
- Object Model
- ODL (Object Definition Language)
- OML (Object Manipulation Language)
- OQL (Object Query Language)
- Interfaces para lenguajes orientados a objetos