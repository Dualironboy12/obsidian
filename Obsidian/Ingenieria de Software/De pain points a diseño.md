Ahora teniendo nuestros pain points y personas, vamos a pasar al diseño de la solucion, **no** del software ni de ninguna tecnologia todavia
Ejemplo:

| Persona                | Dolor validado                    | Evidencia/Dato                    | Decision de Diseño                             |
| ---------------------- | --------------------------------- | --------------------------------- | ---------------------------------------------- |
| Conductor (Estudiante) | Perdida de 15 mins buscando lugar | Nodo B del AS-IS: Recorrido Ciego | Indicador de ocupacion por zona en tiempo real |
| Invitado Externo       | Cuello de botella en acceso       | Fila de 10 personas promedio      | Pre-validacion mediante Token QR dinamico      |
Ahora a debatir generalidades de una solucion al problema planteado:
# Toda decision altera el sistema
## ¿Que elimina?
## ¿Que mejora?
## ¿?
# Modelo conceptual: Estados
## Antes
El sistmea detecta el estado inicial
## Durante
La logica orquesta la transaccion o el cambio de estado
## Despues
El nuevo equilibrio del sistema y la persistencia de datos