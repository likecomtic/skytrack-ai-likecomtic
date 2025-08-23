# 4+1 — Vista de Casos de Uso (Escenarios) · SkyTrack AI
**Fecha:** 2025-08-23

**Objetivo:** validar el diseño con situaciones reales y medibles.

## 1) Orden on-time
**Dado** un vuelo con STD 15:00Z  
**Cuando** los eventos `delivered` y `verified` existen **antes de T-45m**  
**Entonces** la orden se considera **on-time**.

**Métrica:** % de órdenes con `verified` antes de T-45m.

## 2) Faltante detectado y conciliado
**Dado** una entrega parcial con notas  
**Cuando** se exporta conciliación (CSV out)  
**Entonces** el faltante queda visible para ajuste.

**Métrica:** tasa de faltantes por tipo de ítem.

## 3) Conectividad irregular
**Dado** registros con intermitencia  
**Cuando** se reintenta el POST de eventos  
**Entonces** la idempotencia evita duplicados.

**Métrica:** % de 409 frente a 2xx (esperado bajo).
