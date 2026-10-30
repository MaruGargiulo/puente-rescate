# Domain · Puente

Este documento captura decisiones de dominio tempranas. No representa todavía el modelo de datos ni la implementación.

## Entidades y conceptos iniciales

### Animal
Representa al animal como entidad persistente.

No es equivalente a un caso: el animal puede atravesar distintos momentos y necesidades a lo largo del tiempo.

### RescueCase
Proceso activo coordinado alrededor de un animal.

Un caso comienza cuando una persona rescatista ya tomó responsabilidad efectiva sobre el animal.

### Owner
Cada caso tiene un único owner activo.

El owner puede transferirse, pero toda transferencia debe quedar auditada.

### OwnershipHistory
Registro de cambios de responsabilidad:
- owner anterior;
- nuevo owner;
- fecha;
- actor que inicia/acepta;
- motivo opcional.

### Need
Una necesidad activa del caso.

Ejemplos iniciales:
- foster;
- veterinary care;
- transport;
- funding.

Un caso puede tener varias necesidades simultáneas.

### FosterProfile
Perfil de una persona/hogar disponible para tránsito.

Puede ingresar:
- voluntariamente;
- mediante invitación de un rescatista.

Más adelante podrá incluir:
- disponibilidad;
- ubicación;
- especies;
- tamaño;
- convivencia con otros animales;
- fechas;
- experiencia.

### VetProvider
Veterinaria o profesional que participa en un caso.

Su participación puede ocurrir antes o después de conseguir tránsito.

### VeterinaryCare
Agrupa visitas, tratamientos, medicación, documentos y gastos asociados al caso.

### FinancialNeed
Necesidad económica vinculada al caso.

La primera versión no procesa pagos. Registra:
- costo;
- monto cubierto;
- monto pendiente;
- comprobantes/referencias.

## Decisiones tomadas

- Sólo un rescatista puede iniciar un caso.
- El caso nace cuando ya existe responsabilidad efectiva sobre el animal.
- Un caso tiene un único owner activo.
- El ownership puede transferirse.
- Toda transferencia conserva historial.
- El estado del caso no debe intentar representar todas las necesidades.
- Tránsito, tratamiento y deuda pueden coexistir.
- La plataforma es mobile-first.
- La V0 no incluye animales perdidos/reportes callejeros.
- La V0 no incluye adopción.

## Preguntas abiertas

- ¿Qué distingue exactamente el lifecycle del caso de las necesidades activas?
- ¿Qué acciones requieren exclusivamente al owner?
- ¿Qué rol tienen colaboradores sin ownership?
- ¿Cómo se vincula una veterinaria con un caso?
- ¿Cómo se valida información económica antes de hacerla pública?
- ¿Qué datos de un tránsito deben ser privados?
- ¿Cuándo se considera un caso cerrado?
- ¿El animal puede participar en más de un caso a lo largo de su vida?
