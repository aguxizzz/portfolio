# Plan del portfolio (notas personales)

Objetivo: tener un proyecto fuerte por cada tipo de búsqueda laboral, para poner primero en el CV
el que corresponde según la oferta. Hoy tengo mucho React + Python + SQL; faltan Java, C#, cloud,
data engineering, DevOps y sistemas.

## Reglas para cada proyecto
1. Algo usable de verdad, no un CRUD de ejemplo.
2. README en inglés: qué problema resuelve, diagrama, quick start, decisiones técnicas.
3. Tests contra infraestructura real (Testcontainers / LocalStack), CI en GitHub Actions.
4. Docker / `docker compose up` y listo. Deploy en vivo cuando sea posible.
5. Un "problema difícil" explicable en una entrevista en 2 minutos.

## Proyectos
| # | Para ofertas de | Proyecto | Problema difícil |
|---|---|---|---|
| 1 | Java / Spring | **Conveyor**: cola de jobs distribuida sobre Postgres | SKIP LOCKED, leases, fencing, at-least-once |
| 2 | C# / .NET | **Flagship**: feature flags self-hosted + SDK NuGet | rollouts determinísticos, push en vivo con SignalR, caché del SDK |
| 3 | AWS / Cloud | **Hookbin**: recibir/inspeccionar/reenviar webhooks | serverless + IaC (CDK), DLQ, costo ~0 |
| 4 | Data Engineering | **Precios AR**: índice de precios propio desde supermercados | pipelines incrementales, calidad de datos |
| 5 | Go / Rust | KV store con Raft o reverse proxy | consenso / redes |
| 6 | DevOps | Desplegar 1 y 2 en K8s con observabilidad | Helm, GitOps, OTel |
| 7 | AI | RAG con evals | medir calidad, no solo "un chat" |

## Cómo usarlo en el CV
- Postulación Java → Conveyor primero, después el resto.
- Postulación .NET → Flagship primero.
- Cloud/DevOps → Hookbin + Platform.
- Una línea por proyecto con el resultado concreto (ej: "4 workers × 300 jobs, exactly-once en tests").
