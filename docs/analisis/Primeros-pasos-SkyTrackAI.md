# Primeros pasos — SkyTrack AI (Análisis)
**Fecha:** 2025-08-22 · **Rol:** Pre‑work / Punto de partida antes del PRD

Este documento te ayuda a arrancar con buen pie: qué preguntar, qué decidir y qué dejar listo antes de escribir el PRD.

## Objetivo del documento
*Arrancamos situando el propósito del documento.*
- Aterrizar el contexto y las preguntas clave al negocio.
- Decidir temprano lo esencial (buy vs build) y riesgos.
- Dejar salidas claras para redactar el PRD sin dudas.

**Resumen del punto**
- Saber qué preguntar, qué decidir y qué entregar antes del PRD.

## 1) Contexto y dolor a resolver
*Con el objetivo claro, enfoquémonos en el problema a resolver.*
- Plan vs entrega a bordo no siempre coincide.
- Registros dispersos en hojas o Excel.
- Falta evidencia oportuna para evitar demoras.

**Resumen del punto**
- Necesitamos trazabilidad visible y a tiempo.
- El problema es de información, no solo de operación.

## 2) Conversaciones con negocio (guía práctica)
*Ahora, cómo conversar con negocio para alinear expectativas y datos.*
- ¿Qué suministros/servicios son más frecuentes y cuáles fallan más?
- ¿Qué significa “a tiempo” (T‑45m, T‑30m)?
- ¿Quiénes participan y qué evidencias necesitan?
- ¿Cómo se hace hoy? ¿Dónde se pierde información?
- ¿Qué reporte mínimo necesitan al final del día?

**Resumen del punto**
- Preguntas simples que destraban requisitos reales.
- Con ellas alimentamos el PRD.

## 3) Journey operativo (resumen)
*Con las respuestas en mano, mapeamos el recorrido del suministro.*
- Solicitud (SupplyOrder).
- Preparación en almacén (picking/control).
- Despacho al gate/avión (in transit).
- Entrega y verificación a bordo (delivered/verified).
- Conciliación (reportes/auditoría).

**Resumen del punto**
- Cada hito debe reflejarse en al menos un evento.
- El journey guía los escenarios y pruebas.

## 4) Decisiones tempranas (buy vs build)
*Antes de escribir el PRD, decide cómo avanzar estratégicamente.*
- Comprar si te cubre ≥80% y se integra rápido (CSV/Excel).
- Construir si el flujo es muy particular (gate, T‑45m).
- Mixto: comprar lo genérico y construir el core.

**Resumen del punto**
- No reinventar la rueda innecesariamente.
- Lo importante es asegurar el ‘core’ del dominio.

## 5) Salidas que deben quedar listas
*Documentemos lo que debe quedar listo para no frenar el PRD.*
- Requisitos priorizados del MVP.
- Journey acordado y eventos mínimos.
- Riesgos y supuestos iniciales.
- Criterio de decisión documentado (ADRs).

**Resumen del punto**
- Con estas salidas, el PRD se escribe en una sentada.

## 6) Checklist antes del PRD
*Para cerrar, verifiquemos que no falte nada.*
- Problema y objetivos validados con negocio.
- Usuarios y restricciones operativas claras.
- Entradas/Salidas de datos definidas (CSV/Excel).
- Aprobación para pasar a PRD.

**Conclusiones**
- Este pre‑work ordena la conversación con negocio y acelera el PRD.
- El journey y los eventos son la columna vertebral de la trazabilidad.
- Decidir bien (buy/build/mixto) ahorra tiempo y foco durante el curso.
