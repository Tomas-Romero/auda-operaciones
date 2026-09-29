# Auda · Manual de operaciones

Repositorio de la estructura operativa de **Auda**, plataforma SaaS de auditoría web, en su etapa de escalado.
Trabajo Práctico Tema 2 de Administración de Sistemas de Información (UTN FRSR, 2026) · Tomás Agustín Romero · Legajo 10289.

## Tableros (GitHub Projects)
Los enlaces a los 5 tableros están en **[TABLEROS.md](TABLEROS.md)**.

| Tablero | Marco | Qué muestra |
|---|---|---|
| Portafolio (maestro) | Niveles de vuelo | Épicas, historias por equipo, vista Roadmap tipo Gantt |
| Squad Auditoría & IA | Scrum + XP | HU-01 a HU-04, BUG-01 (Expedite), FD-01 (Fixed Date), DT-01 (Intangible) |
| Squad Crecimiento | Scrum + XP | HU-05 a HU-08 |
| Plataforma & DevOps | Scrumban | PL-01, PL-02 |
| Soporte & Operaciones | Kanban | BUG-01 (Expedite), SOP-01 |

## Políticas
- [Definition of Ready](docs/politicas/definition-of-ready.md)
- [Definition of Done](docs/politicas/definition-of-done.md)
- [Límites de WIP y columnas](docs/politicas/limites-wip.md)
- [Clases de servicio](docs/politicas/clases-de-servicio.md)
- [Severidades e incidentes](docs/politicas/severidades-incidentes.md)
- [Matriz RACI](docs/politicas/raci.md)
- [Cadencias y ceremonias](docs/politicas/ceremonias.md)
- [Métricas de flujo, DORA y negocio](docs/metricas.md)

## Ingeniería
- Pipeline CI/CD: [.github/workflows/ci-cd.yml](.github/workflows/ci-cd.yml)
- Cómo contribuir, estándares y política de PRs: [CONTRIBUTING.md](CONTRIBUTING.md)
- Plantillas: [historia de usuario](.github/ISSUE_TEMPLATE/historia-de-usuario.md), [bug crítico](.github/ISSUE_TEMPLATE/bug-critico.md), [pull request](.github/pull_request_template.md)
- Decisiones de arquitectura: [docs/adr](docs/adr)

## Backlog
Épicas **EP-1** (motor escalable y resiliente) y **EP-2** (workspaces, colaboración y monetización), con 8 historias de usuario (HU-01 a HU-08) en la pestaña *Issues*. Cada una tiene su chequeo INVEST y sus criterios de aceptación en Gherkin.
