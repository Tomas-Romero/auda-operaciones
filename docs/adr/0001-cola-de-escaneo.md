# ADR 0001 · Cola de trabajos para el motor de escaneo

- **Estado:** aceptada
- **Fecha:** 2026-09-17
- **Participantes:** CTO, Tech Leads, Platform Lead (mesa de arquitectura)

## Contexto

Hoy cada auditoría levanta un Chromium headless dentro del mismo proceso que atiende la web. Con 10 veces más usuarios, los picos de 40–50 escaneos simultáneos agotan CPU y memoria, el p95 del reporte pasa los 60 s y se cae también la web.

## Decisión

Separar el escaneo en **workers** que consumen una **cola de trabajos** (Redis + BullMQ). La web solo encola y muestra el progreso. Plataforma ofrece la cola y el autoescalado de workers como servicio (PL-01). El Squad Auditoría & IA es dueño del código del worker.

## Consecuencias

- (+) La web deja de depender de la carga de escaneo; los workers escalan solos según el largo de la cola.
- (+) Habilita reintentos y reportes parciales (HU-02) y el monitoreo programado (HU-04).
- (−) Suma un componente más para operar y monitorear (Redis).
- (−) Hay que mostrar el estado "En cola" en la interfaz (HU-01).
