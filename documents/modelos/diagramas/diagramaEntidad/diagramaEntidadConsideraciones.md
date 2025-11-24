| Relación | Tipo y Cardinalidad | Justificación |
|-----------|---------------------|----------------|
| **Profesor – Asignatura** | Agregación (1 o-- many) | El profesor es la entidad central que tiene asignadas las asignaturas (rombo blanco en Profesor), gestionando su impartición. |
| **Asignatura – Grado** | Composición (many *-- 1) | La asignatura es una parte constituyente fundamental del Grado; el grado se compone de estas materias. |
| **Asignatura – Alumno** | Composición (1 *-- many) | La asignatura contiene formalmente a los alumnos matriculados en ella (rombo negro en Asignatura). |
| **Asignatura – Examen** | Composición (1 *-- many) | La asignatura es dueña de los exámenes; si se elimina la asignatura, sus exámenes asociados dejan de tener contexto. |
| **Asignatura – BateríaDePreguntas** | Composición (1 *-- 1) | La asignatura posee una batería de preguntas centralizada que le pertenece exclusivamente. |
| **Grado – Alumno** | Composición (1 *-- many) | El grado estructura y compone al alumnado que cursa los estudios completos. |
| **Alumno – Examen** | Agregación (1 o-- many) | El alumno realiza ("agrega") exámenes a su historial académico, pero el examen es definido por la asignatura. |
| **Examen – Pregunta** | Agregación (1 o-- many) | Un examen selecciona y agrupa una serie de preguntas (rombo blanco), las cuales provienen de la batería. |
| **BateríaDePreguntas – Pregunta** | Composición (1 *-- many) | La batería es el contenedor real de las preguntas; su existencia depende de estar en este repositorio. |
| **Pregunta – Respuesta** | Composición (1 *-- many) | Nivel de detalle más bajo: una pregunta está compuesta inseparablemente por sus opciones de respuesta. |