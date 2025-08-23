# Guía de estilo (idioma)

**Fecha:** 2025-08-23

## Propósito
Alinear el idioma del proyecto para que documentación y clases sean **claras para hispanohablantes** y el **código sea estándar** para ingeniería.

## Regla principal
- **Documentación, clases, PRD, backlog, tickets, ADRs:** **Español**.
- **Código (nombres de clases/métodos/variables, endpoints, claves JSON, nombres de carpetas):** **Inglés**.

## Convenciones rápidas
- Entidad en docs: “**Orden de Suministro**” → código: `SupplyOrder`  
- Entidad en docs: “**Evento de Trazabilidad**” → código: `TrackingEvent`
- Campos comunes (código): `id`, `createdAt`, `status`, `flightNumber`
- Endpoints REST (inglés, kebab-case): `/supply-orders`, `/tracking-events`

## Estados & prioridades
- Estados en backlog: `To Do` → `In Progress` → `In Review` → `Done`
- Prioridad: `P0` (bloqueante), `P1` (alto), `P2` (medio), `P3` (bajo)

## Commits (ejemplo)
```
feat(order): create supply order endpoint (POST /supply-orders)
docs(prd): add acceptance criteria for on-time scenario
```

## Trazabilidad
Cada ticket debe referenciar: PRD ⟷ C4 ⟷ tests ⟷ commit/PR.
