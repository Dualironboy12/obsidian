# ACID
[[ACID]] es, como en cualquier campo de trabajo con bases de datos, la base de como se deben manejar las transacciones, singifica:
- Atomicidad (Atomicity)
- Consistencia (Consistency)
- Aislamiento (Isolation)
- Durabilidad (Durability)
# Bloqueos (locks)
- Read (lectura compartida): Varios pueden leer al mismo tiempo
- Write (escritura exclusiva): Solo uno puede modificar
- Upgrade: Intención de pasar de lectura a escritura
## Tipos de bloqueo
- Explícitos: el programador puede usar lock() o try_lock() para realizar bloqueos
- Implícitos: se obtienen automáticamente al navegar el grafo de objetos
# Transacciones ODMG ([[ODMG y estandares]])
- begin(): inicia
- commit(): confirma cambios y libera bloqueos activos
- abort(): cancela cambios que esten en curso
- checkpoint(): guarda un estado sin liberar bloqueos
- join() y leave(): asocian o desasocian un hilo con una transaccion
- isOpen(): verifica si una transaccion esta activa
- 