# Métricas

## Flujo

| Métrica | Desde → hasta | Meta |
|---|---|---|
| Lead time | Creación del ítem → en producción | p85 ≤ 15 días hábiles (Standard) · Expedite ≤ 4 h |
| Cycle time | "En progreso" → cumple DoD | p85 ≤ 7 días hábiles · promedio ≤ 5 |
| Throughput | Ítems en "Hecho" por semana | Squads ~5 · Plataforma ~7 |
| WIP | Ítems entre "En progreso" y "QA" | Dentro de los límites 3 / 2 / 2 |

El CFD se mira en *Insights* del tablero (gráfico histórico por estado): bandas paralelas = flujo estable; una banda que se ensancha = cuello de botella.

## DORA

| Indicador | Hoy (estimado) | 6 meses | 12 meses |
|---|---|---|---|
| Frecuencia de despliegue | ~1 por semana | 1 por día por squad | varias por día |
| Lead time for changes | 3–5 días | < 1 día | < 4 h |
| Change failure rate | ~25 % | ≤ 15 % | ≤ 10 % |
| MTTR | ~4 h | < 2 h | < 1 h |

SLO: 99,9 % de disponibilidad → error budget de ~43 min/mes.

## Negocio (outcomes)

MAU · DAU/MAU · activación (primer reporte en < 5 min) · retención a 30 días · conversión freemium→pago ≥ 5 % · MRR · churn < 5 % · NPS ≥ 50 · CSAT de soporte ≥ 90 %.
