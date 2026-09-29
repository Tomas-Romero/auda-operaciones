# Squad Crecimiento · Scrum + XP

Onboarding, plan gratuito, pagos, workspaces de agencia y white-label. Sprints de 2 semanas sincronizados con el Squad Auditoría. Objetivos: OBJ-1 (conversión ≥ 5 %) y OBJ-4 (MRR).

## Columnas y límites de WIP
Backlog → Refinado (DoR ✔) → Sprint Backlog → **En progreso · WIP 3** → **Code Review / PR · WIP 2** → **QA / Staging · WIP 2** → Hecho (DoD ✔)

## Clases de servicio (carriles)
| Clase | Política | Objetivo |
|---|---|---|
| 🔴 Expedite | Carril propio, no respeta WIP, máximo 1 a la vez, enjambre | SEV1: mitigar en < 1 h |
| 🟡 Fixed Date | Se empieza en fecha límite − cycle time p85 − 1 semana | 100 % antes de la fecha |
| 🔵 Standard | Orden del PO | 85 % con cycle time ≤ 7 días |
| ⚪ Intangible | 20 % de la capacidad reservada | ≥ 20 % del throughput |

## Definition of Ready
- [ ] Está escrita como "Como [persona], quiero [capacidad], para [beneficio]" y nombra a Lucía o a Martín.
- [ ] Pasa el chequeo INVEST. Si pesa más de 8 puntos, se parte antes de seguir.
- [ ] Tiene al menos 2 escenarios Gherkin: el camino feliz y un caso borde o de error.
- [ ] Está vinculada a una épica y a un OKR o KPI del Módulo 1.
- [ ] Si tiene interfaz, el prototipo fue revisado por el PO y Diseño.
- [ ] Las dependencias con otros equipos están resueltas o tienen fecha acordada en el Scrum of Scrums.
- [ ] El equipo la estimó en puntos y entiende cómo probarla.
- [ ] Tiene clase de servicio y prioridad asignadas en el tablero.

## Definition of Done
- [ ] El código se escribió con TDD y tiene tests unitarios y de integración. Cobertura del módulo **≥ 80 %**.
- [ ] Todos los escenarios Gherkin de la historia pasan como tests automáticos (Playwright).
- [ ] El PR fue aprobado por al menos un par (dos si toca pagos, autenticación o migraciones).
- [ ] El pipeline está en verde: lint, tipos, build, tests y SAST **sin vulnerabilidades críticas ni altas**.
- [ ] Si tocó datos de workspaces, hay un test que prueba que una agencia no puede ver datos de otra.
- [ ] La documentación de la API (OpenAPI) y el changelog están actualizados.
- [ ] Está desplegado en producción (con feature flag si todavía no se libera) y el p95 del reporte sigue < 60 s.
- [ ] Tiene métricas o eventos de uso para medir su impacto.
- [ ] El PO la aceptó contra los criterios de aceptación.

---
Políticas completas y pipeline: repositorio **auda-operaciones** (carpeta `docs/politicas`).