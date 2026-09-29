# Soporte & Operaciones · Kanban

Tickets de usuarios (N1), incidentes y coordinación de la guardia N2. Trabajo no planificable: flujo continuo con clases de servicio.

## Columnas y límites
Entrada → **Triage · WIP 3** → Listo para atender → **En curso · WIP 3** → **Verificación con cliente · WIP 2** → Resuelto

## Severidades
| Severidad | Clase | Primera respuesta | Objetivo |
|---|---|---|---|
| SEV1 | Expedite | 15 min | Mitigar en < 1 h |
| SEV2 | Expedite | 30 min | Mitigar en < 4 h |
| SEV3 | Standard | 1 día hábil | 5 días hábiles |
| SEV4 | Standard | 1 día hábil | Según prioridad |

## Clases de servicio
| Clase | Política | Objetivo |
|---|---|---|
| 🔴 Expedite | Carril propio, no respeta WIP, máximo 1 a la vez, enjambre | SEV1: mitigar en < 1 h |
| 🟡 Fixed Date | Se empieza en fecha límite − cycle time p85 − 1 semana | 100 % antes de la fecha |
| 🔵 Standard | Orden del PO | 85 % con cycle time ≤ 7 días |
| ⚪ Intangible | 20 % de la capacidad reservada | ≥ 20 % del throughput |

## Definition of Done (Soporte)
- [ ] El cliente confirmó la solución o pasaron 72 h sin respuesta.
- [ ] Si fue SEV1 o SEV2: postmortem sin culpables publicado dentro de las 48 h.
- [ ] Si hubo causa en el código: issue creado en el backlog del squad dueño.

---
Políticas completas y pipeline: repositorio **auda-operaciones** (carpeta `docs/politicas`).