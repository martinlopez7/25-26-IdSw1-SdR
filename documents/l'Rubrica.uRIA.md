# Uso responsable de IA - Declaración obligatoria (1.0 pts)

**Contexto operativo**: El uso de modelos de lenguaje (LLMs) es permitido como herramienta de apoyo, pero debe ser declarado y demostrar que hubo trabajo intelectual del equipo. El objetivo es transparencia, no prohibición.

**Artefacto obligatorio: `/AI-uso.md` en raíz del repositorio**

**Estructura mínima requerida:**

```markdown
# Declaración de uso de IA

## Herramientas utilizadas
- [Nombre del modelo/herramienta] (ej: ChatGPT 4, Claude 3.5, Copilot)
- Fechas de uso: [Rango de fechas]

## Contexto de uso

### Para modelo del dominio
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: generación inicial, revisión, sugerencias de clases, etc.]
**¿Qué se aceptó y qué se rechazó?** [Explicar críticamente]

### Para casos de uso
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: ayuda con formato, generación de flujos, etc.]
**¿Qué se aceptó y qué se rechazó?** [Explicar críticamente]

### Para documentación
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: mejora de redacción, glosario, etc.]

## Enlaces a conversaciones

### Conversación 1: [Título descriptivo]
**URL completa**: https://...
**Fecha**: YYYY-MM-DD
**Qué se obtuvo**: [Breve descripción]
**Qué se hizo con ello**: [Se usó directamente, se modificó, se descartó]
**Archivo(s) afectado(s)**: [Enlaces a commits]

### Conversación 2: [Título descriptivo]
...

## Validación humana

**¿Cómo validamos lo generado?**
[Explicar: contrastamos con cliente, revisamos contra minutas, 
verificamos con conocimientos de clase, etc.]

**¿Qué errores detectamos de la IA?**
[Ejemplos concretos de cosas que la IA sugirió mal y corregimos]

## Reflexión del equipo

**¿La IA ayudó o entorpeció?**
[Opinión honesta del equipo]

**¿Qué aprendimos sobre el uso de IA en requisitado?**
[Reflexión sobre límites y valor de las herramientas]
```

**Criterios de puntuación:**

|Puntos|Declaración y honestidad|Uso crítico demostrado|Evidencia de trabajo humano|Reflexión|
|-|-|-|-|-|
|0.9-1.0|**Declaración completa**: Todas las secciones presentes y desarrolladas. **Específica**: Indica exactamente qué herramienta, cuándo, para qué. **Enlaces completos**: ≥3 URLs a conversaciones completas con IA, no extractos. **Archivos afectados**: Enlaces a commits donde se aplicó contenido de IA|**Pensamiento crítico visible**: Explica qué se aceptó y QUÉ SE RECHAZÓ con razones. **Errores detectados**: ≥2 ejemplos concretos de sugerencias de IA que corrigieron. **Validación documentada**: Explica cómo contrastaron con cliente/minutas/conocimiento|**Proceso visible en el repo**: El apartado 4 (trazabilidad) ya demuestra trabajo iterativo mediante commits, issues y evolución de artefactos. **Vocabulario del cliente**: Uso de términos específicos del cliente (no genéricos de IA) en artefactos finales|**Reflexión genuina**: Opinión honesta sobre utilidad de IA en el proceso. **Limitaciones reconocidas**: Identifican claramente qué NO puede hacer la IA en requisitado. **Aprendizaje**: Conclusiones sobre uso apropiado|
|0.7-0.8|**Declaración presente**: Mayoría de secciones completas. **Razonablemente específica**. **Enlaces**: ≥2 URLs completas a conversaciones. **Algunos enlaces** a archivos|**Algo de crítica**: Menciona aceptación/rechazo aunque sin gran detalle. **Algún error detectado**: ≥1 ejemplo. **Validación mencionada**|**Proceso parcialmente visible**: Hay evidencia de iteración en el repo aunque no óptima|**Reflexión básica**: Opinión presente aunque superficial|
|0.5-0.6|**Declaración básica**: Algunas secciones incompletas. **Vaga**: "Usamos ChatGPT para mejorar". **Enlaces**: ≥1 URL o descripciones genéricas sin enlaces. **Pocos enlaces** a commits|**Poca crítica**: Solo dice que usó IA, no evalúa. **Sin errores identificados**. **Validación vaga**|**Proceso poco visible**: Trabajo parece concentrado en pocos commits|**Reflexión mínima**: Una o dos frases genéricas|
|0-0.4|**Declaración muy incompleta** o claramente fabricada después. **Sin especificar herramientas o contexto**. **Sin enlaces** a conversaciones|**Sin pensamiento crítico**: No hay evidencia de evaluación. **Sin validación**|**Sin proceso visible**: Generación aparentemente única sin iteración|**Sin reflexión** o completamente genérica|

**Casos de uso ACEPTABLE de IA:**

|Uso|Ejemplo|Por qué está bien|
|-|-|-|
|Brainstorming inicial|"Dame ideas de clases conceptuales para un sistema de reservas deportivas"|Punto de partida, luego validado con cliente|
|Mejora de redacción|"Revisa la claridad de este flujo de caso de uso: [texto]"|El contenido es del equipo, IA mejora forma|
|Generación de plantillas|"Dame una plantilla markdown para fichas de casos de uso"|Es estructura, no contenido del dominio|
|Validación de sintaxis UML|"¿Esta cardinalidad es correcta para esta relación?"|Verificación técnica, no decisión de dominio|
|Ayuda con formato|"Convierte esta lista en tabla markdown"|Presentación, no contenido|

**Casos de uso INACEPTABLE de IA:**

|Uso|Ejemplo|Por qué está mal|
|-|-|-|
|Generación del modelo completo|"Crea un modelo del dominio para gestión de reservas deportivas"|La IA no conoce el contexto específico del cliente|
|Casos de uso sin validación|"Genera 5 casos de uso para este sistema" sin contrastar con cliente|Requisitos inventados, no reales|
|Copia directa de minutas|Que la IA "resuma" la reunión sin estar presente|Falsificación de evidencia|
|Respuestas del cliente simuladas|Simular interacciones con el cliente mediante IA|Fraude académico|
|Delegación completa|Entregar lo que genera la IA sin revisión crítica|No hay aprendizaje|

**Penalizaciones adicionales (acumulativas con puntuación base):**

|Situación detectada|Penalización|Cómo se detecta|Procedimiento|
|-|-|-|-|
|AI-uso.md ausente completamente|-1.0 pts del total|Revisión directa del repo|Automático|
|Uso no declarado con evidencia|-2.0 pts del total|Texto idéntico a outputs conocidos de IA, o coincidencia >80% entre equipos|Requiere evidencia documentada + dar oportunidad de descargo al equipo|
|Plagio entre equipos|Nota final = 0|Coincidencia >80% en artefactos clave entre equipos diferentes|Informe a coordinación académica|
|Falsificación de evidencia|Nota final = 0|Minutas/emails claramente generados por IA presentados como reales|Informe a coordinación académica|

**Señales de alerta (requieren investigación):**

|Señal|Qué revisar|
|-|-|
|Vocabulario muy genérico|¿Coincide con términos del cliente en minutas?|
|Sin iteración visible en commits|¿Historia de git muestra evolución o generación única?|
|Todos los artefactos el mismo día|¿Distribución temporal del trabajo?|
|Modelo con clases que el cliente nunca mencionó|¿Conceptos validados contra minutas?|

**Demostración de trabajo humano legítimo:**

El uso adecuado del repositorio (apartado 4: trazabilidad y versionado) ya demuestra el proceso de creación iterativo del equipo. La historia de git, los issues con discusiones, y la evolución de artefactos son la evidencia natural de trabajo intelectual genuino.

**Ejemplo de declaración honesta y aceptable:**

```markdown
## Enlaces a conversaciones

### Conversación 1: Modelo inicial de reservas
**URL completa**: https://chat.openai.com/share/abc123...
**Fecha**: 2024-10-15
**Qué se obtuvo**: Modelo genérico de sistema de reservas con clases 
Usuario-Reserva-Recurso-Pago
**Qué se hizo**: Usamos estructura Usuario-Reserva-Recurso como punto 
de partida. Descartamos "Pago" porque el cliente dijo explícitamente 
en minuta 2024-10-19 que no gestiona pagos.
**Archivos afectados**: modelos/dominio-v1.puml (commit abc1234)

## Validación humana
Después de la sesión con @prof-cliente, descartamos el 60% de lo que 
la IA sugirió porque propuso un "sistema de reservas genérico" cuando 
nuestro cliente tiene particularidades específicas: usa "slots" no 
"horarios", gestiona "equipamiento" no "recursos", y tiene concepto 
de "abono" que ninguna IA nos sugirió.

## Reflexión
La IA fue útil para no empezar de cero antes de la primera sesión, 
pero sus sugerencias son demasiado genéricas. Lo más valioso fue 
la sesión con el cliente, no lo que la IA generó.
```

**Relación con calificación global:**

- Una buena declaración puede subir hasta 1 punto en profesionalidad
- La ausencia o falsedad puede bajar hasta 3 puntos del total
- El uso crítico y bien documentado de IA se valora positivamente
- La delegación completa a IA sin trabajo intelectual es causa de suspenso