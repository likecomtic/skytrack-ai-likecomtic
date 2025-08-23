# Backlog inicial — SkyTrack AI

**Fecha:** 2025-08-23

## Épicas
- **E1. Gestión de órdenes de suministro** (SupplyOrder)
- **E2. Trazabilidad operacional** (TrackingEvent)
- **E3. Observabilidad & Operación** (Logs/Métricas/Alertas)
- **E4. Seguridad** (JWT, roles, TLS)

## Historias iniciales
- **H1. Crear Orden de Suministro**
  - *Como* Supervisor, *quiero* registrar una `SupplyOrder` con `flightNumber` e `items`,
    *para* dar trazabilidad al proceso.
  - Criterios: 201 con `id`; validaciones básicas; persistencia.
- **H2. Registrar Evento de Trazabilidad**
  - *Como* Operador, *quiero* anexar un `TrackingEvent` (p.ej., `picked`, `in_transit`, `delivered`)
    *para* actualizar el estado real de la orden.

## Definición de Listo (DoR)
- Aceptación definida (Given/When/Then), dependencias conocidas, diseño C4 vinculado.

## Definición de Hecho (DoD)
- Código + pruebas + documentación mínima + ejemplos en Postman + métricas básicas.
