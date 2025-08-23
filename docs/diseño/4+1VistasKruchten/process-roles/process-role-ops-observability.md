# Vista de Procesos por Rol · SkyTrack AI — Operaciones / DevOps
**Fecha:** 2025-08-23
**Rol:** Operaciones / DevOps
**Objetivo:** Ubicar **puntos de instrumentación** (logs, métricas, trazas).

## Flujo con observabilidad
```mermaid
flowchart TD
  A[POST /supply-orders] --> B[API Gateway\nlog: request_id, status]
  B --> C[OrderService\nmetric: orders_created_total]
  C --> D[Postgres\ntrace: db_insert_span]
  D --> E[Respuesta 201 { id }\nlog: latency_ms]
```
## Instrumentación sugerida
- **Logs** con `request_id`, `status`, `latency_ms` en gateway y servicio.
- **Métricas**: `orders_created_total`, `db_write_errors_total`.
- **Trazas**: spans para API, servicio y DB (propagar `trace_id`). 
