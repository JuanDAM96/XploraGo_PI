# RNF-002 — Disponibilidad
Estado: Aprobado
Versión: v1.0.0
Fecha: 2025-12-07
Autores: Juan Antonio Lucas Márquez

## Descripción
El servicio debe estar operativo y accesible durante la demo E1.

## Métrica
Disponibilidad percibida durante la ventana de demo (uptime %).

## Umbral
≥ 99% en el periodo de evaluación (no más de ~9 minutos de caída en 15 horas de demo acumulada).

## Método(s) de verificación
- Ping/healthcheck cada 1 min durante la ventana de demo; registro en log.
- Verificación manual de login y chat al inicio y mitad de la sesión.

## Trazabilidad
- HU: HU-002, HU-007
- Release: E1-v1.1

## Historial de cambios
- v1.0.0 (2025-12-07): Definición inicial para E1.
