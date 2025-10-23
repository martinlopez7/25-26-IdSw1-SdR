# Modelo del dominio (2.5 pts)

El modelo del dominio representa la realidad operativa del cliente en lenguaje conceptual, sin contaminación de decisiones de implementación. Se documenta en carpeta `/modelos/` del repositorio.

**Artefactos requeridos:**

- Diagrama UML de clases conceptuales (archivo `.puml` y exportación `.svg`/`.png`)
- Glosario de términos
- Escenarios de ejemplo con objetos concretos (mínimo 2)
- Diagramas dinámicos (estados/actividad/secuencia) para procesos clave

**Criterios de puntuación:**

|Puntos|Cobertura y corrección conceptual|Artefactos y completitud|Validación|
|-|-|-|-|
|2.3-2.5|**Cobertura**: ≥90% de entidades mencionadas por cliente están modeladas. **Corrección conceptual**: 0 clases técnicas de implementación, 0 errores graves de cardinalidad, relaciones semánticamente ricas (usa composición, agregación, asociación según naturaleza real). **Vocabulario**: 100% términos en lenguaje del cliente|**Glosario**: Completo, define todas las clases y asociaciones ambiguas. **Escenarios**: ≥2 escenarios con objetos concretos bien desarrollados. **Diagramas dinámicos**: ≥1 diagrama que captura flujo temporal de procesos clave. **Atributos**: Todas las clases con ≥3 atributos relevantes o justificación explícita de por qué no|**Validación explícita**: ≥1 issue/minuta donde cliente valida modelo conceptual. **Iteraciones**: Evidencia de ≥3 versiones del modelo con changelog documentando evolución|
|1.9-2.2|**Cobertura**: 70-89% de entidades. **Corrección**: ≤2 clases técnicas que deberían ser conceptuales, ≤3 errores menores de cardinalidad. **Relaciones**: Mayoría usa tipos apropiados (no todo son asociaciones simples). **Vocabulario**: ≥80% términos del cliente|**Glosario**: Presente, define ≥80% de términos. **Escenarios**: 2 escenarios básicos. **Diagramas dinámicos**: ≥1 diagrama presente pero incompleto. **Atributos**: ≥80% de clases con atributos adecuados|**Validación**: Evidencia de revisión por cliente aunque no explícita. **Iteraciones**: ≥2 versiones documentadas|
|1.2-1.8|**Cobertura**: 50-69% de entidades. **Corrección**: 3-5 clases técnicas mezcladas, errores conceptuales no críticos (ej: agregación donde debería ser composición). **Relaciones**: Mezcla entre relaciones apropiadas y uso excesivo de asociaciones simples. **Vocabulario**: 60-79% términos del cliente|**Glosario**: Básico, define 50-79% de términos. **Escenarios**: 1 escenario o 2 muy superficiales. **Diagramas dinámicos**: Ausentes o muy básicos. **Atributos**: 60-79% de clases con atributos|**Validación**: Sin evidencia clara de revisión por cliente. **Iteraciones**: ≥1 versión documentada|
|0.5-1.1|**Cobertura**: 30-49% de entidades. **Corrección**: ≥6 clases técnicas (Controller, Service, Manager, DAO), confusión evidente entre dominio y diseño técnico. **Relaciones**: Predominio de asociaciones simples tipo "mapa mental". **Vocabulario**: <60% términos del cliente, lenguaje técnico inapropiado|**Glosario**: Incompleto (<50% términos) o ausente. **Escenarios**: Ausentes o irrelevantes. **Diagramas dinámicos**: Ausentes. **Atributos**: <60% de clases con atributos|**Validación**: Sin validación. **Iteraciones**: Sin evidencia de evolución|
|0-0.4|Modelo irrelevante, cobertura <30%, o ausencia de modelo|Artefactos ausentes o no verificables|Sin validación ni iteraciones|

**Errores críticos que fuerzan puntuación ≤1.1:**

|Error|Descripción|Ejemplo|
|-|-|-|
|Contaminación técnica|Incluir clases de implementación en lugar de conceptos del dominio|`VentaController`, `PacienteDAO`, `ServicioReservas` en lugar de `Venta`, `Paciente`, `Reserva`|
|Cardinalidades injustificadas|>50% de asociaciones sin cardinalidad o con cardinalidades arbitrarias|Relaciones 1-1 donde la realidad es 1-* sin justificación documentada|
|Ausencia de glosario|Glosario con <50% de términos definidos o directamente ausente|Clases en diagrama sin definición en glosario|
|Solo asociaciones simples|>80% de relaciones son asociaciones simples (estilo "mapa mental")|No usa composición para relaciones parte-todo, ni agregación para contención débil|

**Definición de "validación explícita":**

- Issue en GitHub donde cliente comenta/aprueba el modelo conceptual con referencia específica a clases/relaciones
- Minuta donde se documenta revisión del modelo con decisiones tomadas
- Comentarios del cliente en PR de versión del modelo

**Casos excepcionales:**

- **Cliente con dominio técnico**: Si el dominio del cliente es inherentemente técnico (ej: gestión de infraestructura IT), clases como "Servidor" o "BaseDatos" son conceptuales, no técnicas. La distinción está en si representa realidad del cliente o arquitectura de la solución.
- **Dominios simples**: Si el dominio tiene genuinamente <10 entidades relevantes, la cobertura se evalúa sobre el 100% de ese conjunto reducido, no sobre un número absoluto.
