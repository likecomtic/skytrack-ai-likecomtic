# Vertical Slice 1 — Crear SupplyOrder

**Fecha:** 2025-08-23

## Objetivo
Exponer `POST /supply-orders` y persistir la orden.

## Tareas
- OpenAPI para `POST /supply-orders` (payload con `flightNumber` e `items`).
- `SupplyOrderController` + `SupplyOrderService` + `OrderRepository`.
- Validaciones (obligatorios, tipos).
- Migración SQL (`supply_orders`, `supply_order_items`).
- Pruebas (unitarias y de integración).
- Ejemplos en Postman / curl.
