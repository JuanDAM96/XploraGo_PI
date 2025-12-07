# ADR-001 — Arquitectura Monolítica con Spring Boot

Estado: Aprobado
Fecha: 2025-12-07

## Contexto
Necesitamos una API sencilla de desplegar y mantener en Sprint 1, minimizando complejidad de arquitectura distribuida. El equipo es reducido y el foco es entregar funcionalidad core.

## Decisión
Construiremos un único proyecto Spring Boot que expone endpoints REST y accede directamente a MySQL. Esta API monolítica manejará todas las operaciones del sistema en un solo artefacto desplegable.

## Motivo
La arquitectura monolítica es simple de desplegar, entender y mantener para un equipo pequeño. Elimina la complejidad de microservicios, comunicación entre servicios y orquestación distribuida, permitiendo enfocarnos en funcionalidad.

## Implementación 
1. Crear proyecto Spring Boot con dependencias: Web, Validation, JDBC y Flyway.
2. Organizar código en paquetes: `controller/`, `service/`, `dao/`, `model/`, `dto/`.
3. Implementar endpoint `GET /api/v1/health` que devuelva JSON con estado del sistema.

## Alternativas descartadas 
- Microservicios desde inicio (Spring Cloud)
- Arquitectura hexagonal multi-módulo

## Consecuencias
- Entrega rápida; facilita futura migración por separación de capas.
- Un solo artefacto implica acoplamiento; requiere disciplina en arquitectura interna.

## Trazabilidad
- HUs: HU-001 (Crear grupo), HU-004 (Actividades)
- RNFs: RNF-001 (Rendimiento)
- Trello: https://trello.com/c/oDQT0RxE
