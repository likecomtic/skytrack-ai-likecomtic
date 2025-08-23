# Vista de Procesos por Rol · SkyTrack AI — QA / Testing
**Fecha:** 2025-08-23
**Rol:** QA / Testing
**Objetivo:** Probar flujos con **rutas felices** y **rutas de error** verificables.

## Swimlanes (sistemas y checks)
```mermaid
flowchart LR
  subgraph Cliente
    A[POST /supply-orders]
  end
  subgraph API_GW[API Gateway]
    B[Validar formato y auth]
  end
  subgraph Servicio[OrderService]
    C[Validaciones de negocio]
    D[Crear orden + ítems]
  end
  subgraph DB[Postgres]
    E[(Persistir)]
  end

  A --> B --> C
  C -->|válido| D --> E
  C -->|inválido| X[(400 Bad Request)]
  E --> R[201 { id }]
  R --> A
```
## Puntos de prueba
- 201 con `id` cuando el payload es válido.
- 400 cuando `payload` tiene errores.
- (Si aplica) 409 por duplicado / idempotencia.
