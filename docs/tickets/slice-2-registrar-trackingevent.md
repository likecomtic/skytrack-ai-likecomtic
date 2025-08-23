# Vertical Slice 2 — Registrar TrackingEvent

**Fecha:** 2025-08-23

## Objetivo
Exponer `POST /tracking-events` para anexar eventos a una orden.

## Tareas
- OpenAPI `POST /tracking-events` (campos: `orderId`, `type`, `at`).
- `TrackingEventController` + `TrackingService` + `EventRepository`.
- Regla: un `delivered` cierra la orden.
- Migración SQL (`tracking_events`).
- Pruebas (unitarias y de integración).
- Ejemplos en Postman / curl.
