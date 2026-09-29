# Definition of Done (DoD)

Lista no negociable. Una tarjeta pasa a **Hecho (DoD ✔)** solo si se cumple todo.

- [ ] El código se escribió con TDD y tiene tests unitarios y de integración. Cobertura del módulo **≥ 80 %**.
- [ ] Todos los escenarios Gherkin de la historia pasan como tests automáticos (Playwright).
- [ ] El PR fue aprobado por al menos un par (dos si toca pagos, autenticación o migraciones).
- [ ] El pipeline está en verde: lint, tipos, build, tests y SAST **sin vulnerabilidades críticas ni altas**.
- [ ] Si tocó datos de workspaces, hay un test que prueba que una agencia no puede ver datos de otra.
- [ ] La documentación de la API (OpenAPI) y el changelog están actualizados.
- [ ] Está desplegado en producción (con feature flag si todavía no se libera) y el p95 del reporte sigue < 60 s.
- [ ] Tiene métricas o eventos de uso para medir su impacto.
- [ ] El PO la aceptó contra los criterios de aceptación.

## Variantes por equipo

- **Plataforma & DevOps:** además, la infraestructura está definida como código y existe un runbook.
- **Soporte & Operaciones:** un ticket está resuelto cuando el cliente lo confirma o pasan 72 h sin respuesta. Si fue SEV1 o SEV2, cuando además el postmortem está publicado.

**Dueño de la política:** Tech Lead de cada equipo. Se revisa en las retrospectivas.
