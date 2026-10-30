# Puente

Puente es una plataforma para coordinar casos activos de rescate animal.

La idea es reducir la fragmentación que aparece durante un rescate: contactos, hogares de tránsito, veterinarias, gastos, documentos y seguimiento suelen quedar repartidos entre mensajes, planillas y redes sociales.

Puente organiza esa coordinación alrededor de una entidad central: **el caso de rescate**.

## El problema

Cuando una persona rescatista toma responsabilidad sobre un animal puede necesitar resolver varias cosas al mismo tiempo:

- conseguir hogar de tránsito;
- coordinar atención veterinaria;
- registrar tratamientos y documentación;
- cubrir gastos o deuda;
- organizar traslados;
- mantener un historial claro del caso.

Puente busca que esas necesidades puedan coordinarse desde un mismo lugar y que el contexto no se pierda cuando cambia la situación del animal o la persona responsable.

## Primer alcance

### Rescatista
Crea un caso cuando ya tomó responsabilidad sobre el animal.

Cada caso tiene un único owner activo. Ese ownership puede transferirse a otra persona y debe conservar historial.

### Hogar de tránsito
Puede incorporarse voluntariamente a la red o mediante invitación de un rescatista.

Puede declarar disponibilidad y preferencias para recibir casos compatibles.

### Veterinaria
Puede participar antes o después de conseguir tránsito.

Las atenciones, tratamientos, documentos y gastos se vinculan al caso.

### Colaboradores
Más adelante, una vista pública podrá mostrar necesidades económicas activas para facilitar colaboración sin convertir la plataforma en una red social.

## Casos, no publicaciones

Puente no nace como portal de reportes callejeros ni como catálogo de animales.

Un caso comienza cuando una persona rescatista ya asumió responsabilidad sobre un animal. Desde ese momento, la plataforma ayuda a movilizar la red necesaria alrededor del caso.

## Principios de producto

- Un caso siempre tiene un responsable identificable.
- El ownership puede transferirse y queda auditado.
- Un animal puede tener varias necesidades simultáneas.
- El historial del caso no se pierde cuando cambia su situación.
- Las decisiones sensibles permanecen en manos de personas.
- La información sensible tiene acceso controlado.
- La experiencia se diseña mobile-first.

## Arquitectura inicial

La primera versión empieza deliberadamente simple:

```text
React / Next.js
      ↓
 OpenAPI contract
      ↓
Java / Spring Boot
      ↓
   PostgreSQL
```

La arquitectura crecerá sólo cuando una necesidad real del producto lo justifique.

## Stack

**Frontend**
- React / Next.js
- TypeScript

**Backend**
- Java
- Spring Boot

**Data**
- PostgreSQL

**Product & architecture**
- Figma / FigJam
- C4
- ADRs
- OpenAPI

## Estado

En desarrollo activo.

El primer objetivo es completar un flujo real de punta a punta:

**crear caso → persistir → visualizar → gestionar necesidades**
