# Clases de servicio

El trabajo circula según su **costo del retraso** (cost of delay).

| Clase | Cuándo aplica | Política | Objetivo de servicio | Ejemplo |
|---|---|---|---|---|
| 🔴 **Expedite** | Caída o degradación en producción, fuga de datos. El costo es inmediato. | Carril propio arriba de todo. No respeta WIP. Máximo 1 a la vez por equipo. Enjambre (*swarming*). | SEV1: mitigar en < 1 h | BUG-01 |
| 🟡 **Fixed Date** | Plazos legales o contractuales. El costo aparece de golpe en una fecha. | Se empieza cuando "fecha límite − cycle time p85 − 1 semana" llega a hoy. | 100 % antes de la fecha | FD-01 |
| 🔵 **Standard** | La mayoría del trabajo. El costo crece de forma lineal. | Orden del PO; primero en entrar, primero en salir dentro del sprint. | 85 % con cycle time ≤ 7 días | HU-01 a HU-08 |
| ⚪ **Intangible** | Deuda técnica, refactor, actualizaciones. Hoy no cuesta, mañana explota. | 20 % de la capacidad de cada sprint, reservado. Se pausa si entra un Expedite. | ≥ 20 % del throughput mensual | DT-01 |

**Reparto de referencia por sprint:** ~70 % Standard · 20 % Intangible · ~10 % colchón para Fixed Date. El Expedite no se planifica.

En el tablero, la clase se ve en el campo **Clase de servicio** (que arma los carriles) y en las etiquetas `expedite`, `fixed-date`, `standard` e `intangible`.
