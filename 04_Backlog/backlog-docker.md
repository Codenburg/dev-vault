
---
tags: #backlog #docker #devops

---
# Backlog — Docker

## Prioridad Inmediata

- [ ] Entender diferencias: `bind mounts` vs `named volumes` — Resultado: documento con 3 ejemplos y decisión de uso.
- [ ] Investigar `docker compose profiles` — Resultado: snippet con 2 profiles (dev, prod) y comando de ejecución.
- [ ] Optimizar Dockerfile para imágenes de Node — Resultado: Dockerfile con multi-stage y análisis de capas.

## Corto Plazo

- [ ] `.dockerignore` efectivo — Resultado: lista de exclusiones y comparación de tamaños de imagen antes/después.
- [ ] Volúmenes en CI vs local — Resultado: estrategia documentada para tests en CI.
- [ ] Estrategia de persistencia para Postgres en contenedores — Resultado: guía paso a paso.

## Mediano Plazo

- [ ] Networking entre contenedores (bridge vs overlay) — Resultado: ejemplo con 2 servicios en red personalizada.
- [ ] Healthchecks y restart policies — Resultado: configuración en `docker-compose.yml` y pruebas.
- [ ] Monitorización básica (logs y métricas) dentro de contenedores — Resultado: playbook de comandos y setup mínimo.

## Investigación / Deep Dive

- [ ] Storage drivers y su impacto en rendimiento — Resultado: resumen técnico y recomendaciones.
- [ ] Seguridad en imágenes (scans, usuarios no-root) — Resultado: checklist de hardening.
- [ ] Estrategias de rollback para despliegues con contenedores — Resultado: flujo operativo documentado.

## Tareas Administrativas

- [ ] Añadir todas las notas creadas al `MOC - DevOps`.
- [ ] Convertir ítems completados en entradas del `Registro Diario` con fecha.
- [ ] Revisar backlog semanalmente y re-priorizar.

---
## Criterios de cierre

Cada ítem se marca completado solo si:
- Contiene explicación breve y ejemplo reproducible.
- Tiene enlace a nota de concepto o práctica relacionada.
- Se registró en el `Registro Diario` la fecha de finalización.
