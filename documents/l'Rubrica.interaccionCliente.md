# Evidencia de interacción con cliente (2.0 pts)

El trabajo se desarrolla en fork del repositorio de la asignatura (https://github.com/mmasias/25-26-IdSw1-SdR) en la cuenta del coordinador del equipo. Toda la evidencia de interacción debe estar documentada en este repositorio.

**Sesiones obligatorias**: 2 sesiones de requisitado en horas de clase pactadas. Este es el mínimo exigible para alcanzar el umbral de aprobación en este apartado.

**Evidencias válidas en GitHub:**

**Primarias (peso mayor):**

- Issues creados para requisitos, dudas o validaciones con mención al cliente (@usuario-cliente)
- Comentarios del cliente en issues o PRs (con timestamp visible)
- Minutas como archivos .md en carpeta `/minutas/` con enlaces a issues relevantes
- Commits que referencian issues de decisiones del cliente (usando #número-issue)
- GitHub Discussions con participación del cliente
- Reviews del cliente en PRs de documentación

**Secundarias (complementarias):**

- Emails del cliente referenciados desde issues (captura o forward como archivo en `/evidencias/`)
- Fragmentos de grabación vinculados desde minutas (archivo audio + transcripción de decisiones clave)
- Mensajes de chat/Slack/Teams archivados como evidencia complementaria

**Criterios de puntuación:**

|Puntos|Interacción documentada|Evidencia en repo|Validación|Trazabilidad|
|-|-|-|-|-|
|1.8-2.0|≥3 sesiones (2 obligatorias + ≥1 adicional) con minutas completas (todas las secciones presentes y desarrolladas)|≥5 issues con mención al cliente + ≥3 comentarios/respuestas del cliente en issues o PRs|≥1 issue cerrado con aprobación explícita del cliente sobre requisitos específicos|≥80% de decisiones en minutas enlazadas a issues|
|1.4-1.7|2 sesiones obligatorias con minutas completas (todas las secciones presentes y bien desarrolladas)|≥3 issues con mención al cliente + ≥2 respuestas del cliente|Issue con confirmación presente pero parcial (ej: "ok" sin detallar qué aprueba)|60-79% de decisiones enlazadas a issues|
|1.0-1.3|2 sesiones obligatorias, minutas con 1-2 secciones incompletas o poco desarrolladas|≥2 issues creados pero <2 respuestas del cliente, o intentos documentados sin respuesta|Sin validación explícita, o validación muy ambigua|40-59% de decisiones enlazadas|
|0.5-0.9|Solo 1 sesión obligatoria documentada, o 2 sesiones pero minutas muy deficientes (faltan ≥3 secciones)|≤1 issue con el cliente o issues sin menciones explícitas|Sin validación del cliente|<40% de decisiones enlazadas o ausente|
|0-0.4|Minutas de las 2 sesiones obligatorias inexistentes o ficticias|Sin issues relevantes, sin evidencia creíble de interacción|Sin validación|Sin trazabilidad|

**Aclaración sobre el mínimo obligatorio (1.0 pts)**: 

- Para alcanzar el mínimo de 1.0 pts se requiere documentar las 2 sesiones obligatorias de clase, aunque la documentación sea básica o incompleta
- Si solo se documenta 1 sesión o ninguna, no se alcanza el mínimo (puntuación <1.0) y el trabajo queda suspendido independientemente del resto de apartados

**Indicadores de calidad en issues:**

- Título descriptivo (no genérico: "Validar entidades del modelo de X" mejor que "Dudas")
- Descripción del contexto
- Mención explícita al cliente usando @usuario
- Etiqueta apropiada (ej: `validación-cliente`, `requisito`, `duda-dominio`)
- Enlace desde minuta al issue
- Respuesta del cliente con decisión clara

**Penalizaciones específicas:**

- Minutas creadas retroactivamente (fecha de commit del archivo muy posterior a fecha declarada en minuta): -0.3 pts
- Issues sin mención al cliente pero declarados como "validados por cliente": -0.2 pts por issue
- Evidencia fabricada (ej: capturas de pantalla editadas, commits con fecha manipulada): penalización según apartado de profesionalidad + posible 0 en este criterio

**Casos excepcionales contemplados:**

- **Cliente no responde en GitHub**: Si equipo demuestra ≥3 intentos documentados (issues creados, menciones, emails archivados en `/evidencias/`) espaciados al menos 3 días, se valora calidad de la documentación del intento en lugar de respuesta efectiva. Mínimo exigido baja a 0.8 pts en este caso.
- **Cliente prefiere otra plataforma**: Si cliente solicita explícitamente usar email/Teams/etc., la evidencia debe archivarse en `/evidencias/` y referenciarse desde issues. No penaliza usar plataforma alternativa si está documentado el motivo.
- **Cliente ausente en sesión obligatoria**: Si el cliente falta a una sesión obligatoria de clase, el equipo debe documentar la ausencia en la minuta y demostrar intento de reprogramación. Se ajusta criterio según circunstancias.
