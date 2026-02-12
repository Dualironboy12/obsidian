# [[UML]]
Es un lenguaje estandarizado para especificar, visualizar, construir, y documentar los artefactos de un sistema de software.
**No es una metodologia** como Scrum o XP, es una **notacion**, similar a notacion musical
# Diagrama de actividades
Diagrama de comportamiento que muestra flujo de control o flujo de datos a traves de una serie de acciones.
Modela la **lógica procedural**, procesos de negocio y flujos de trabajo
Ejemplo:
![[Pasted image 20260211182745.png]]
## Cuando usarlo?
- Procesos de Negocio
	- Para entender como funciona una organización hoy (As-Is)
- Lógica Compleja
	- Visualizar algoritmos con multiples condiciones
- Casos de Uso
	- Para detallar el flujo de eventos de un caso de uso especifico
## Ejemplo de diagrama en PlantUML
```plantuml
|Guardia|
|Estudiante|
Start
:llega al campus;
|Guardia|
:Solicita credencial;
if (tiene credencial?) then (Si trae credencial)
:Registra el ID;
else (No trae credencial)
:Ejecutar alternativa de ingreso;
	if () then (Acceso Rechazado)
	:Rechaza acceso;
	Stop
	else (Acceso concedido)
	fork
	:Solicita numero ID;
	fork again
	:Solicita identificacion;
	end fork
	|Estudiante|
	:Muestra identificacion y da el ID;
	endif
endif
|Estudiante|
:Ingresar al campus;
Stop
```
# Conceptos importantes
## Identificar el inicio (trigger)
El proceso no siempre empieza cuando el u
## Identificar el fin (Valor)
No termina cuando se imprime el papel. Termina cuando se entrega el **valor** al stakeholder.
**Finales Alternativos**: Recuerden modelar tambien los finales de error o cancelacion.
## Decisiones ocultas
Interrogatorio teórico
- ¿Siempre lo apruebas?
- ¿Que pasa si falta firma?
- ¡Que pasa si el monto es superior a X?