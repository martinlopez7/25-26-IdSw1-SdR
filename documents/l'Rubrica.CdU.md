## 3. Casos de uso y criterios de aceptación (2.5 pts)

Los casos de uso describen la funcionalidad deseada del sistema desde la perspectiva de los actores. Se documentan en carpeta `/casos-de-uso/` del repositorio, con trazabilidad a evidencias de origen.

**Artefactos requeridos:**

- Diagrama(s) de casos de uso con actores y relaciones  (archivo `.puml` y exportación `.svg`/`.png`)
- Fichas de especificación por caso de uso en formato markdown usando diagramas de estados
- Prototipos de interfaz (sin contaminar requisitos con decisiones de UI)

**Criterios de puntuación:**

| Puntos | Identificación y priorización | Especificación y detalle | Criterios y validación | Trazabilidad |
|--------|------------------------------|-------------------------|----------------------|--------------|
| 2.3-2.5 | **Actores**: Todos los roles identificados con justificación clara. **Casos de uso**: ≥5 casos identificados, nombres descriptivos que empiezan con verbo. **Priorización**: Método declarado (MoSCoW/valor-esfuerzo/Kano) aplicado consistentemente con justificación documentada. **Estructuración**: Relaciones include/extend correctamente aplicadas donde corresponde | **Flujos principales**: ≥3 casos con flujo principal completo, evitando "piensa", "decide" (actor) y "graba en BD", "ventana de" (sistema). **Flujos alternativos**: ≥2 flujos alternativos por caso prioritario, manejando excepciones. **Precondiciones/postcondiciones**: Verificables y completas. **Diagramas de estados**: ≥1 por caso complejo mostrando transiciones | **Criterios**: ≥2 criterios Given/When/Then por caso prioritario, 100% verificables (entrada observable + acción + salida medible). **Prototipos**: Presentes para casos con UI significativa, evitando decisiones prematuras de diseño. **Validación**: ≥1 issue cerrado con aprobación explícita del cliente sobre casos de uso | ≥80% de casos enlazados a evidencia de origen (minuta/issue). Changelog documenta evolución. Matriz de trazabilidad presente |
| 1.9-2.2 | **Actores**: Roles principales identificados. **Casos de uso**: ≥4 casos, nombres mayormente descriptivos. **Priorización**: Método aplicado con justificación básica. **Estructuración**: Include/extend usados pero con algunas relaciones cuestionables | **Flujos principales**: ≥2 casos completos, algunos detalles de implementación presentes pero no dominantes. **Flujos alternativos**: ≥1 flujo alternativo por caso prioritario. **Precondiciones/postcondiciones**: Mayormente verificables. **Diagramas**: Presentes pero básicos | **Criterios**: ≥2 criterios por caso, ≥80% verificables. **Prototipos**: Presentes con algún detalle prematuro de UI. **Validación**: Evidencia de revisión por cliente | 60-79% de casos enlazados. Changelog básico |
| 1.2-1.8 | **Actores**: Actores básicos identificados. **Casos de uso**: ≥3 casos, algunos nombres genéricos. **Priorización**: Presente pero inconsistente o sin justificación clara. **Estructuración**: Relaciones include/extend limitadas o mal aplicadas | **Flujos principales**: ≥2 casos identificados, varios detalles prematuros ("botón", "ventana", "se graba"). **Flujos alternativos**: Algunos presentes pero incompletos. **Precondiciones/postcondiciones**: Básicas. **Diagramas**: Ausentes o muy básicos | **Criterios**: ≥1 criterio por caso, 50-79% verificables. **Prototipos**: Ausentes o mezclados con especificación. **Validación**: Validación muy básica | 40-59% enlazados. Changelog mínimo |
| 0.5-1.1 | **Actores**: Confusos o incompletos. **Casos de uso**: <3 casos o mal identificados. **Priorización**: Ausente o arbitraria. **Estructuración**: Sin relaciones o mal estructurados | **Flujos**: Incompletos, lenguaje técnico dominante ("el sistema ejecuta query", "se muestra popup"). **Flujos alternativos**: Ausentes. **Condiciones**: No verificables. **Diagramas**: Ausentes | **Criterios**: <50% verificables o ausentes. **Prototipos**: Ausentes o completamente prematuros. **Validación**: Sin validación | <40% enlazado o sin trazabilidad |
| 0-0.4 | Casos de uso ausentes, irrelevantes, o sin especificación mínima | Sin detalle o contaminación técnica extrema | Sin criterios verificables | Sin trazabilidad |

**Casos excepcionales:**

- **Cliente cambia requisitos drásticamente**: Si cambio ocurre >50% del periodo, documentar en issue. No penaliza si está documentado con evidencia del cliente.
- **Casos de uso muy simples**: Si genuinamente no requieren flujos alternativos (ej: "Consultar catálogo"), documentar justificación en la ficha. No penaliza si está justificado.

**Relación con modelo del dominio:**

- Los casos de uso deben referenciar conceptos definidos en el glosario del modelo del dominio
- Actores deben tener correspondencia con roles identificados en el MdD
- Se valorará positivamente la consistencia terminológica entre ambos artefactos