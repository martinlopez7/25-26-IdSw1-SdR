| Relación entre Estados | Tipo | Justificación contextualizada |
|------------------------|------|-------------------------------|
| **[*] → NoCreado** | Inicialización | El sistema todavía no tiene datos del examen.
| **NoCreado → Creado** | Transición | El sistema genera las preguntas desde la batería del profesor, crea variantes únicas por alumno y asigna los hashcodes para cada hoja de respuestas. |
| **Creado → Asignado** | Transición | El examen se “asigna” formalmente a los alumnos de la asignatura: se generan los PDFs personalizados con los datos del alumno, el hashcode, y la hoja de respuestas única. |
| **Asignado → Corregido** | Transición | El sistema detecta el hash, identifica cuál modelo debe usar y emplea IA de visión para leer las respuestas marcadas. Luego compara automáticamente con el modelo correcto (sin calificar) y genera un PDF corregido visualmente. |
| **Corregido → [*]** | Finalización | Cuando el sistema genera el documento corregido (o varios), almacena los resultados y termina el ciclo. El docente puede revisar, exportar o calificar manualmente según la normativa.|
