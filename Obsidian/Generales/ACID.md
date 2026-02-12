# Propiedades ACID en Bases de Datos

Las transacciones en un DBMS deben cumplir con las propiedades **ACID** para garantizar confiabilidad y seguridad.

| Propiedad | Significado | Ejemplo práctico |
|-----------|-------------|------------------|
| **Atomicity (Atomicidad)** | Una transacción es *todo o nada*. Si alguna operación falla, se revierte todo el conjunto. | Transferencia bancaria: si se descuenta dinero de una cuenta, debe acreditarse en la otra. Si falla, ninguna operación se aplica. |
| **Consistency (Consistencia)** | La transacción lleva la base de datos de un estado válido a otro estado válido, respetando reglas y restricciones. | No se puede registrar una venta si el inventario queda en negativo. |
| **Isolation (Aislamiento)** | Las transacciones concurrentes no interfieren entre sí; se ejecutan como si fueran secuenciales. | Dos usuarios comprando el último boleto de avión: el sistema asegura que solo uno lo obtenga. |
| **Durability (Durabilidad)** | Una vez confirmada (commit), la transacción es permanente, incluso si ocurre un fallo del sistema. | Si se guarda un pedido y luego se apaga el servidor, el pedido sigue registrado al reiniciar. |

