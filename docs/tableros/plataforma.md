# Plataforma & DevOps · Scrumban

CI/CD, cola y workers, observabilidad, entornos y seguridad, ofrecidos a los squads como autoservicio (X-as-a-Service).

## Columnas y límites
Backlog → **Listo para tomar · mín. 3** (punto de pedido) → **En progreso · WIP 3** → **Revisión / PR · WIP 2** → **Verificación en staging · WIP 2** → Hecho (DoD ✔)

**Punto de pedido** = throughput (~1,5 ítems/día) × reposición (2 días) = 3. Cuando "Listo" baja de 3, el Platform Lead repone.

## Clases de servicio
| Clase | Política | Objetivo |
|---|---|---|
| 🔴 Expedite | Carril propio, no respeta WIP, máximo 1 a la vez, enjambre | SEV1: mitigar en < 1 h |
| 🟡 Fixed Date | Se empieza en fecha límite − cycle time p85 − 1 semana | 100 % antes de la fecha |
| 🔵 Standard | Orden del PO | 85 % con cycle time ≤ 7 días |
| ⚪ Intangible | 20 % de la capacidad reservada | ≥ 20 % del throughput |

## Definition of Done (Plataforma)
- [ ] El código se escribió con TDD y tiene tests unitarios y de integración. Cobertura del módulo **≥ 80 %**.
- [ ] Todos los escenarios Gherkin de la historia pasan como tests automáticos (Playwright).
- [ ] El PR fue aprobado por al menos un par (dos si toca pagos, autenticación o migraciones).
- [ ] El pipeline está en verde: lint, tipos, build, tests y SAST **sin vulnerabilidades críticas ni altas**.
- [ ] Si tocó datos de workspaces, hay un test que prueba que una agencia no puede ver datos de otra.
- [ ] La documentación de la API (OpenAPI) y el changelog están actualizados.
- [ ] Está desplegado en producción (con feature flag si todavía no se libera) y el p95 del reporte sigue < 60 s.
- [ ] Tiene métricas o eventos de uso para medir su impacto.
- [ ] El PO la aceptó contra los criterios de aceptación.
- [ ] La infraestructura está definida como código y hay runbook.

---
Políticas completas y pipeline: repositorio **auda-operaciones** (carpeta `docs/politicas`).