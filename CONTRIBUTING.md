# Cómo trabajamos en el código

## Flujo
1. Tomá una tarjeta de **Sprint Backlog** (pull: nadie te la asigna) y movela a **En progreso**, siempre que haya lugar en el WIP.
2. Creá una rama corta con el ID de la historia: `feat/HU-07-upgrade-pro`. Vive menos de 2 días.
3. TDD: test en rojo → código mínimo en verde → refactor.
4. Abrí un PR chico (< 400 líneas) usando la plantilla. El pipeline tiene que estar en verde.
5. Un par revisa en menos de 4 horas hábiles. Pagos, autenticación, permisos o migraciones: 2 aprobaciones.
6. Merge con *squash* a `main` → deploy automático a staging → E2E → canary en producción.

## Estándares
- TypeScript en modo `strict`, ESLint + Prettier (corren en pre-commit y en CI). El estilo no se discute en el PR.
- [Conventional Commits](https://www.conventionalcommits.org/es/): `feat:`, `fix:`, `refactor:`, `test:`, `chore:`.
- Código y nombres en inglés; textos de la interfaz en español. Glosario del dominio: auditoría (*audit*), reporte (*report*), puntaje (*score*), workspace.
- Decisiones de arquitectura como ADR en `docs/adr` (una página).

## Deuda técnica
- 20 % de cada sprint está reservado para ítems **Intangible** (etiqueta `deuda-tecnica`).
- Regla del boy scout: si tocás un archivo, dejalo un poco mejor.
- Sin tests no hay refactor: primero tests de caracterización.
- Si se agota el error budget del mes, el sprint siguiente se dedica a estabilidad.

## Pair programming
Obligatorio en historias de pagos y seguridad, en incidentes SEV1 y en la primera semana de cada persona nueva.
