# Severidades e incidentes

| Severidad | Ejemplo en Auda | Clase de servicio | Primera respuesta | Objetivo |
|---|---|---|---|---|
| **SEV1** | Nadie puede generar reportes, pérdida de datos, fuga de datos entre workspaces | Expedite | 15 min | Mitigar en < 1 h |
| **SEV2** | Degradación: p95 > 60 s, falla la IA o los pagos | Expedite | 30 min | Mitigar en < 4 h |
| **SEV3** | Error con alternativa (el PDF falla en Safari) | Standard (prioridad alta) | 1 día hábil | 5 días hábiles |
| **SEV4** | Consulta, sugerencia, detalle visual | Standard / backlog | 1 día hábil | Según prioridad del PO |

## Circuito

1. **N1 – Soporte:** recibe el ticket o la alerta, clasifica la severidad y resuelve lo que no requiere código.
2. **N2 – Guardia rotativa:** un ingeniero de un squad + uno de Plataforma por semana. Toman SEV1 y SEV2: primero mitigan, después corrigen.
3. **N3 – Squad dueño:** si la corrección de fondo es grande, entra a su backlog.

Después de cada SEV1 o SEV2: **postmortem sin culpables dentro de las 48 h**, con línea de tiempo, causa raíz y acciones.
