# skytrack-ai-likecomtic
SkyTrack AI — Trazabilidad inteligente desde tierra hasta el aire. Seguimiento y auditoría de suministros y servicios a aeronaves, vinculados a un número de vuelo, desde la solicitud hasta la entrega a bordo.

# SkyTrack AI
**Trazabilidad inteligente desde tierra hasta el aire**  

SkyTrack AI es un proyecto didáctico para construir, paso a paso, un sistema que rastrea **suministros y servicios** asociados a una **aeronave** (p. ej., catering, agua, limpieza), enlazados a un **número de vuelo**. No es un “flight tracker”; es **trazabilidad operativa** con evidencia.

## Estructura del repositorio
- `docs/analysis/` — **Análisis**: primeros pasos, PRD, prompts y artefactos de descubrimiento.
- `docs/design/` — **Diseño**:  
  - **C4**: **N1 (Contexto)**, **N2 (Contenedores)**, **N3 (Componentes)**.  
  - **4+1**: **Vista Lógica**, **Vista de Desarrollo**, **Vista de Procesos**, **Vista Física**, **Vista de Casos de Uso (Escenarios)**.  
  - **ADRs** (decisiones arquitectónicas).
- `docs/backlog/` — **Backlog y tickets** (se agregará en la masterclass de desarrollo).
- `assets/` — Materiales para el curso (imágenes, word, etc.).
- `src/` — Código fuente (se creará durante la masterclass de desarrollo).
- `csv/` — Carpeta/volumen para `in/` y `out/` (import/export CSV en el MVP).

## Orden recomendado de lectura
1. `docs/analysis/primeros-pasos.md`
2. `docs/analysis/prd.md`
3. `docs/design/c4-n1-n2.md` y `docs/design/c4-n3.md`
4. `docs/design/4plus1/*`
5. `docs/design/adrs/*`

## Convenciones
- Diagramas como código con **Mermaid** (GitHub los renderiza).
- Timestamps en **UTC**. Idempotencia de eventos (`orderId + type + at`).

## Licencia
MIT — ver `LICENSE`.

---
**Fecha:** 2025-08-22
