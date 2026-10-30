# Product & Engineering Roadmap

Puente se construye por evolución de producto, no por tecnologías aisladas.

Cada card debe responder:
1. qué problema del producto resolvemos;
2. qué debemos modelar antes de implementar;
3. qué conocimiento técnico aparece por necesidad;
4. qué evidencia deja la decisión.

## 00 · Domain discovery
- Modelar dominio inicial.
- Separar lifecycle del caso de necesidades simultáneas.
- Diseñar flujo mobile-first del rescatista.

## 01 · First vertical slice
Primer flujo real:

**crear caso → persistir → recuperar → visualizar**

Arquitectura inicial:
- React / Next.js;
- OpenAPI;
- Spring Boot;
- PostgreSQL.

## 02 · Ownership
- owner único;
- transferencia;
- aceptación;
- audit trail;
- reglas e invariantes.

## 03 · Foster network
- perfil de tránsito;
- invitación;
- disponibilidad;
- pedido de tránsito;
- matching inicial por reglas simples.

## 04 · Veterinary care
- veterinarias;
- visitas;
- tratamiento;
- documentos;
- gastos;
- necesidad económica.

## 05 · Public collaboration
- necesidades públicas verificadas;
- deuda/monto cubierto/monto pendiente;
- colaboración externa;
- pagos reales sólo cuando el modelo esté maduro.

## 06 · Identity & permissions
- authentication;
- authorization;
- privacy;
- ownership;
- roles/permisos.

## 07 · Async coordination
Cuando aparezca la necesidad:
- notifications;
- events;
- queues;
- workers;
- retries;
- idempotency.

Kafka se estudia después de operar una cola real.

## 08 · Files & infrastructure
- object storage;
- S3;
- Docker;
- AWS;
- CI/CD;
- secrets;
- backups.

## 09 · Observability
- logs;
- metrics;
- traces;
- health;
- correlation IDs;
- OpenTelemetry.

## 10 · AI
Sólo con producto funcional:
- mensaje informal → borrador de caso estructurado;
- resúmenes;
- detección de información faltante;
- asistencia de matching;
- tools / MCP;
- evals.

Las decisiones sensibles siguen siendo humanas.

## Aprendizaje

Los recursos se incorporan dentro de las issues cuando aparece un problema real.

La señal de avance no es terminar un curso. Es poder:
- modelar;
- implementar;
- romper;
- observar;
- explicar la decisión.
