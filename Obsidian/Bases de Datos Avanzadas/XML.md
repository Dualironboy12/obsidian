# Introduccion a XML
## Que es XML?
Significa eXtensible Markup Language, es un metalenguaje universal para representar datos en la web, permite intercambio de informacion entre aplicaciones y navegadores, es mas simple que SGML y mas potente que HTML
## Objetivos de XML
- Estandarizar como se procesa la informacion
- Usos tipicos
	- Exchange (XML): intercambio de datos
	- Presentation (XSL): estilos y visualizacion
	- Retrieval (XQuery): consultas
	- Security: cifrado y autenticacion
	- Linking (XLink): enlaces entre documentos
## Elementos de XML
Son la unidad basica de XML, delimitados por etiquetas <...>
Pueden contener texto o sub-elementos
Ejemplo:
```XML
<person>
  <name>Alan</name>
  <age>42</age>
  <email>alan@abc.com</email>
</person>
```
## Atributos
Son propiedades adicionales dentro de una etiqueta, siempre son cadenas de texto, por ejemplo:
```XML
<price currency="Pesos">4200.12</price>
```
## Buenas practicas
Etiquetas correctamente anidadas, atributos únicos, el orden de los sub elementos es relevante.
## Document Type Definition (DTD)
DTD define la gramatica de un documento XML, permite especificar:
- Que elementos existen
- Que atributos pueden tener
- Como se relacionan los elementos entre si
Por ejemplo:
```XML
<!DOCTYPE person [
  <!ELEMENT person (name, age, email)>
  <!ELEMENT name (#PCDATA)>
  <!ELEMENT age (#PCDATA)>
  <!ELEMENT email (#PCDATA)>
]>
```
### Referencias
- ID es un identificador unico
- IDREF referencia a un ID existente
### Limitaciones
No soporta tipos de datos avanzados, unicamente texto, no permite herencia ni validaciones complejas, y usualmente se prefiere usar XML schema en lugar de DTD
## XML Schema
### XSD
Especifica la estructura y tipos de datos de un documento XML, es mas potente que DTD, ya que soporta tipos de datos simples y complejos, ademas se escribe en el propio XML, no en sintaxis especial como DTD.
### Tipos de datos
- Simples: strings, integer, date, boolean, etc.
- Complejos: estructuras con elementos y atributos
Ejemplo:
```XML
<xs:element name="price" type="xs:decimal"/>
<xs:element name="date" type="xs:date"/>
```
### Ventajas sobre DTD
Permite tipos de datos mas ricos, validaciones mas precisas, soporta herencia y reutilizacion de codigo