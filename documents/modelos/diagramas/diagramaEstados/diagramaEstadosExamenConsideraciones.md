| Relación entre Estados | Tipo | Justificación contextualizada |
|------------------------|------|-------------------------------|
| **[*] → NoCreado** | Inicialización | El sistema todavía no tiene datos del examen.
| **NoCreado → Creado** | Transición | El sistema genera los exámenes teniendo en cuenta el nº de preguntas, el nº de examenes, la asignatura, temas, proporcion de dificultad y demás. |
| **Creado → Asignado** | Transición |El examen se asigna formalmente a los estudiantes de la asignatura mediante la vinculación del modelo de corrección correspondiente a cada alumno y guarda un hash único del modelo de corrección asignado a cada estudiante. De este modo, se asegura que no haya cambios en las respuestas o en los criterios de corrección. |
| **Asignado → Corregido** | Transición | El sistema detecta el hash, identifica cuál modelo debe usar y emplea IA de visión para leer las respuestas marcadas. Luego compara automáticamente con el modelo correcto (sin calificar) y genera un PDF corregido visualmente. |
| **Corregido → [*]** | Finalización | Cuando el sistema genera el documento corregido (o varios), almacena los resultados y termina el ciclo. El docente puede revisar, exportar o calificar manualmente según la normativa.|
