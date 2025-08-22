# PRD — SkyTrack AI
**Documento de Alcance y Requisitos (versión para estudiantes)**  
**Fecha:** 2025-08-22 · **Autor:** likecomtic  
*Tagline: Trazabilidad inteligente desde tierra hasta el aire.*

Este PRD explica, con lenguaje simple, qué vamos a construir y por qué. Úsalo como referencia durante el curso; cuando digamos “ver PRD”, nos referimos a este documento.

## 1) ¿Qué es SkyTrack AI?
*Venimos de entender el contexto general del curso; ahora aterrizamos qué es exactamente SkyTrack AI.*
- Sistema para seguir y auditar suministros/servicios a aeronaves (catering, combustible, repuestos, limpieza).
- Todo se vincula a un número de vuelo (flightNumber).
- La trazabilidad cubre desde la solicitud hasta la entrega verificada a bordo.

**Resumen del punto**
- Seguimos suministros/servicios, no “vuelos”.
- El número de vuelo es el hilo conductor.
- Buscamos evidencia de punta a punta.

## 2) Alcance del MVP (lo mínimo valioso)
*Con la definición clara, pasemos a fijar el alcance mínimo valioso que construiremos.*
**Incluye**
- Crear una orden de suministros (SupplyOrder) asociada a flightNumber.
- Registrar eventos de seguimiento (TrackingEvent) para contar el progreso.
- Consultar el estado e historial de una orden por su ID.
- Importar/exportar datos por Excel/CSV para facilitar operación inicial.

**Por ahora NO incluye**
- Integraciones “online” con ERP/almacén (usaremos CSV/Excel).
- Dashboards de BI avanzados (habrá reportes básicos exportables).
- Mensajería compleja (WhatsApp multiusuario, bots).
- Suministro de hardware (escáneres, impresoras).

**Resumen del punto**
- MVP enfocado en órdenes y eventos.
- Operación con archivos al inicio (CSV/Excel).
- Escalaremos integraciones y BI más adelante.

## 3) Personas y casos típicos
*Definido el alcance, identifiquemos quiénes usan el sistema y qué necesitan hacer.*
**¿Quiénes usan el sistema?**
- Operador/proveedor: prepara y entrega, escanea y registra eventos.
- Supervisor/coordinador: monitorea que todo llegue a tiempo.
- Auditor/calidad: valida evidencias y tiempos.

**Ejemplos de uso**
- Crear una orden de catering para el vuelo XX123 con sus ítems.
- Registrar que la orden salió del almacén, llegó a la puerta y se entregó a bordo.
- Consultar el estado e historial de la orden.

**Resumen del punto**
- Tres roles principales: operador, supervisor y auditor.
- Los flujos clave son crear, registrar y consultar.
- La información debe ser oportuna y verificable.

## 4) Funcionalidades (explicadas sin tecnicismos)
*Con los casos claros, concretemos las funcionalidades del MVP.*
- Crear orden: registrar la solicitud con número de vuelo e ítems a entregar.
- Ver orden: consultar una orden por su ID para conocer su estado.
- Registrar evento: anotar un hito (requested, picked, in_transit, delivered, verified).
- Listar eventos: ver el historial cronológico de una orden.

**Resumen del punto**
- Cuatro funciones base para operar el MVP.
- Eventos estandarizados para facilitar la auditoría.
- Todo gira alrededor de la SupplyOrder.

## 5) Cualidades del producto (no funcionales)
*Además de qué hace, definamos cómo debe comportarse el sistema.*
- Seguridad básica: ingreso con token (JWT) y permisos por rol.
- Desempeño razonable en demo: crear una orden debe ser muy rápido.
- Observabilidad: trazas y métricas para entender qué pasó.
- Portabilidad: despliegue fácil en entornos de prueba.

**Resumen del punto**
- Seguridad y desempeño razonable desde el día 1.
- Métricas y logs como parte del MVP.
- Facilidad de despliegue para practicar.

## 6) Conceptos clave (glosario rápido)
*Para evitar malos entendidos, alineemos el vocabulario.*
- SupplyOrder: pedido de suministro/servicio para una aeronave.
- SupplyItem: ítem o servicio dentro de una orden.
- TrackingEvent: evento con hora, actor y opcionalmente ubicación/notas.
- FlightNumber: número del vuelo asociado.

**Resumen del punto**
- Cuatro conceptos sostienen el dominio.
- Usaremos estos nombres en todo el curso.

## 7) ¿Qué pantallas o acciones veremos?
*Con el vocabulario claro, bajemos a acciones visibles para el usuario.*
- Crear orden (formulario sencillo).
- Detalle de la orden (estado actual e historial).
- Registrar evento (acciones por hito).

Si eres técnico, estos flujos se exponen como endpoints (POST/GET). Los detallamos en los Tickets.

**Resumen del punto**
- Tres vistas/acciones para cubrir el MVP.
- Contratos técnicos en los Tickets del backlog.

## 8) Cómo sabremos que vamos bien (métricas)
*Para medir progreso real, definamos indicadores simples.*
- Órdenes entregadas antes de T‑45m.
- Tiempo promedio de entrega por tipo de suministro.
- Órdenes con evidencia completa (eventos + checklist).

**Resumen del punto**
- Enfoque en puntualidad, eficiencia y evidencia.
- Podremos comparar turnos y proveedores.

## 9) Riesgos a tener en cuenta
*Anticipemos las piedras en el camino para preparar mitigaciones.*
- Conectividad limitada en rampa.
- Datos de vuelo incompletos o tardíos.
- Adopción del proceso de registro/escaneo.

**Resumen del punto**
- Tener plan B para conectividad.
- Asegurar calidad de datos de vuelo.
- Acompañar a operación en el cambio.

## 10) Plan por etapas (alto nivel)
*Con todo alineado, veamos el orden en que avanzaremos.*
- Documentación y diseño (PRD, diagramas y decisiones).
- Backlog y Tickets (con criterios DoR/DoD).
- Desarrollo del MVP (endpoints y pantallas base).
- Pruebas mínimas y evidencia.
- Reportes básicos y ajustes.

**Resumen del punto**
- Ruta clara del papel al código.
- Evidencia y calidad desde el principio.

## 11) Dónde está cada cosa (trazabilidad)
*Finalmente, mapeemos dónde vive cada artefacto para no perdernos.*
- Pre‑work de análisis: `/docs/analysis/primeros‑pasos.md`
- Diagramas como código (DaC): `/docs/dac/`
- C4 y 4+1: `/docs/design/`
- ADRs (decisiones): `/docs/design/adrs/`
- Backlog y Tickets: `/docs/backlog/`

**Conclusiones**
- El MVP se centra en SupplyOrder + TrackingEvent con operación simple por CSV/Excel.
- La trazabilidad se apoya en eventos estandarizados y contratos claros.
- Mediremos éxito por puntualidad, eficiencia y evidencia documentada.
- Con estos cimientos, pasamos del diseño al código con menos fricción.
