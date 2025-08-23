# 4+1 — Vista de Procesos · SkyTrack AI
**Fecha:** 2025-08-23

**Objetivo:** describir cómo fluyen las solicitudes en los casos clave.

## Crear SupplyOrder
```mermaid
sequenceDiagram
  participant Client
  participant API as API Gateway
  participant SVC as OrderService
  participant DB as Postgres

  Client->>API: POST /supply-orders (payload)
  API->>SVC: validar + delegar
  SVC->>DB: insertar SupplyOrder, items
  DB-->>SVC: id
  SVC-->>API: 201 { id }
  API-->>Client: 201 Created
```

## Registrar TrackingEvent
```mermaid
sequenceDiagram
  participant Client
  participant API as API Gateway
  participant SVC as EventService
  participant DB as Postgres

  Client->>API: POST /tracking-events (orderId, type, at, ...)
  API->>SVC: validar + delegar
  SVC->>DB: insertar evento (idempotencia)
  DB-->>SVC: ok
  SVC-->>API: 201
  API-->>Client: 201 Created
```

## Errores típicos
- **400**: `type` inválido / timestamp mal formado.
- **404**: `orderId` no existe.
- **409**: duplicado por idempotencia.
