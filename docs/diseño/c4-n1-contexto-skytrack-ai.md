# C4 — Nivel 1 (Contexto) · SkyTrack AI
**Fecha:** 2025-08-22

**Objetivo:** Alinear quién usa SkyTrack AI y con qué sistemas interactúa.

```mermaid
flowchart LR
  subgraph Externos
    ERP[ERP / WMS / Excel]
    Flight[Fuente de datos de vuelos]
  end

  Operador[Operador / Proveedor]
  Supervisor[Supervisor / Coordinador]
  Auditor[Auditor / Calidad]

  Sky[SkyTrack AI]

  Operador -->|Registro / Consulta| Sky
  Supervisor -->|Monitoreo| Sky
  Auditor -->|Auditoría| Sky

  ERP <-->|CSV Import/Export| Sky
  Flight -->|Referencia (offline)| Sky
```

**Notas**
- Usuarios interactúan con SkyTrack AI para registrar y consultar.
- Integración MVP por **CSV** (batch/manual).
- Fuente de vuelos como **referencia**, no tiempo real.
