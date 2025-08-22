# C4 — Nivel 2 (Contenedores) · SkyTrack AI
**Fecha:** 2025-08-22

**Objetivo:** Descomponer el sistema en contenedores implementables.

```mermaid
flowchart LR
  UI[Web UI (futuro mínimo)] --> API[API Gateway]
  Client[Cliente REST / Postman] --> API

  API --> SVC[Tracking Service]
  SVC --> DB[(Postgres)]
  SVC --> CSV[CSV Import/Export]

  subgraph Futuro
    IDP[Identity Service]
  end

  API -. JWT .-> IDP
```

**Notas**
- **Tracking Service** concentra el dominio: SupplyOrder + TrackingEvent.
- **DB**: Postgres (consultas claras y reportes básicos). *(ADR‑001)*
- **CSV Import/Export**: estrategia MVP con carpetas `csv/in` y `csv/out`. *(ADR‑003)*
- **Identity**: a futuro; MVP con **JWT** simple. *(ADR‑004)*
