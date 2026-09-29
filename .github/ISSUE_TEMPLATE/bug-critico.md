---
name: Bug crítico / Incidente (Expedite)
about: Caída o degradación en producción (SEV1 o SEV2). Entra al carril Expedite.
title: "[BUG-XX] "
labels: bug, bug-critico, expedite
---

**Severidad:** SEV1 / SEV2 (ver `docs/politicas/severidades-incidentes.md`)
**Detectado por:** alerta / tickets / usuario
**Impacto:** qué no funciona, desde cuándo y a cuántos usuarios afecta

## Qué se hace
- [ ] La guardia N2 toma la tarjeta (primera respuesta: 15 min SEV1, 30 min SEV2)
- [ ] Mitigación aplicada
- [ ] Soporte comunica en la página de estado cada 30 min
- [ ] Corrección definitiva con test que reproduce el problema
- [ ] Postmortem sin culpables publicado (máximo 48 h)
