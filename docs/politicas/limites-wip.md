# Límites de WIP y columnas

## Squads de producto (Scrum)

| Columna | Qué tiene que cumplir una tarjeta para estar acá | WIP |
|---|---|---|
| Backlog | Título, persona y vínculo a un OKR. Lo ordena el PO. | — |
| Refinado (DoR ✔) | Cumple la [Definition of Ready](definition-of-ready.md). | — |
| Sprint Backlog | El equipo la eligió en la Sprint Planning. | — |
| En progreso | Alguien la tomó (pull, nadie la asigna), rama creada y test en rojo escrito. | **3** |
| Code Review / PR | PR abierto con CI en verde que referencia la historia. | **2** |
| QA / Staging | PR mergeado, desplegado en staging, escenarios Gherkin en ejecución. | **2** |
| Hecho (DoD ✔) | Cumple la [Definition of Done](definition-of-done.md). | — |

## Por qué esos números (Ley de Little)

`Cycle time promedio = WIP promedio ÷ Throughput`

Un squad de 5 personas cierra ~10 historias por sprint de 10 días hábiles, o sea 1 por día. Para un cycle time promedio de 5 días, el WIP promedio tiene que rondar 5. Los límites 3 + 2 + 2 = 7 ponen un techo de ~7 días.

**Regla:** si una columna está llena, nadie empieza nada nuevo. Se ayuda a vaciar la columna llena ("dejar de empezar, empezar a terminar").

## Plataforma (Scrumban)

Backlog → Listo para tomar (**punto de pedido: 3**) → En progreso (**3**) → Revisión / PR (**2**) → Verificación en staging (**2**) → Hecho.

Punto de pedido = throughput (~1,5 ítems/día) × tiempo de reposición (2 días) = 3.

## Soporte (Kanban)

Entrada → Triage (**3**) → Listo para atender → En curso (**3**) → Verificación con el cliente (**2**) → Resuelto.

El carril **Expedite** no cuenta para ningún límite.
