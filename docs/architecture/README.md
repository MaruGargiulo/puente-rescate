# Architecture

La arquitectura inicial de Puente debe mantenerse deliberadamente simple.

Primer objetivo:

```text
Mobile/Web
   ↓
Next.js / React
   ↓
OpenAPI
   ↓
Spring Boot
   ↓
PostgreSQL
```

## Visual documentation

Usamos distintas representaciones para preguntas distintas:

- C4 Context: dónde vive Puente respecto del mundo exterior.
- C4 Container: frontend, backend y data store.
- Sequence diagram: cómo fluye un caso de uso en el tiempo.
- ERD/DBML: relaciones persistentes.
- Statechart: lifecycle y transiciones válidas.

No crear Component diagrams hasta que el código tenga boundaries reales que valga la pena comunicar.
