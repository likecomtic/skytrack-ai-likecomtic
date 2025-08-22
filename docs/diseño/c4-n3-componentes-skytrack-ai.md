# C4 — Nivel 3 (Componentes) · SkyTrack AI
**Fecha:** 2025-08-22

**Objetivo:** Descomponer el Tracking Service en componentes.

```mermaid
flowchart LR
  subgraph API[API Gateway]
    OC[OrderController]
    EC[EventController]
  end

  subgraph Dominio[Tracking Service]
    OS[OrderService]
    ES[EventService]
    V[Validators]
    M[Mappers]
  end

  subgraph Infra[Infra]
    OR[OrderRepository]
    ER[EventRepository]
    DB[(Postgres)]
    CSV[CSV Import/Export]
  end

  OC --> OS
  EC --> ES
  OS --> OR
  ES --> ER
  OR --> DB
  ER --> DB
  OS --> V
  ES --> V
  M --> OR
  M --> ER
  CSV --> OS
```

**Notas**
- Estado proyectado por eventos: `requested → picked → in_transit → delivered → verified`.
- Idempotencia por clave natural `orderId + type + at`.
- Errores típicos: `400` (type inválido), `404` (orderId no existe), `409` (duplicado idempotente).
