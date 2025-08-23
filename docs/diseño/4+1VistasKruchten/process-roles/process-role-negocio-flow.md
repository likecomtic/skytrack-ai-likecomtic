# Vista de Procesos por Rol · SkyTrack AI — Negocio / Producto
**Fecha:** 2025-08-23
**Rol:** Negocio / Producto
**Objetivo:** Ver el **flujo de valor** de "Crear SupplyOrder" en pasos entendibles para stakeholders.

## Flujo (alto nivel)
```mermaid
flowchart TD
  A[Recibir POST /supply-orders] --> B{Validar payload}
  B -- "valido" -->   C[Crear SupplyOrder e items]
  B -- "invalido" --> E((400 Bad Request))
  C --> D[Responder 201 \(id\)]
```
## Puntos de revisión
- Reglas de validación alineadas con negocio.
- Definición de éxito: 201 + id generado.
- Tratamiento de error funcional (400).
