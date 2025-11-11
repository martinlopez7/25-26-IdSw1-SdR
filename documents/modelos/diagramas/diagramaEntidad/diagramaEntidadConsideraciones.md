| Relación | Tipo y Cardinalidad | Justificación |
|-----------|---------------------|----------------|
| **Examen – Pregunta** | Composición (many *-- many) | Un examen contiene varias preguntas y una pregunta puede formar parte de otros exámenes. |
| **Examen – ModeloCorrección** | Composición (1 *-- 1) | Cada examen tiene un único modelo de corrección y un modelo de corrección solo pertenece a un examen. |
| **Profesor - Examen** | Composición (1 *-- many) | Un profesor puede crear varios examenes pero un examen solo puede ser creado por un profesor. |
| **Profesor – Pregunta** | Agregación (1 o-- many) | Un profesor puede crear varias preguntas y una pregunta solo puede ser creada por un profesor |
| **Asignatura – BateríaDePreguntas** | Composición (1 *-- 1) | Una asignatura tiene una batería de preguntas y una batería de preguntas solo puede pertenecer a una asignatura. |
| **BateríaDePreguntas – Pregunta** | Composición (1 *-- many) | Una batería de preguntas tiene muchas preguntas y una pregunta esta en una sola batería de preguntas. |
| **Asignatura – Examen** | Composición (1 *-- many) | Una asignatura puede tener varios examenes pero un examen solo puede pertenecer a una sola asignatura. |
| **Asignatura – Profesor** | Agregación (many o-- 1) | Una asignatura tiene un solo profesor asignado, pero un profesor puede impartir varias asignaturas. |
| **Asignatura – Alumno** | Composición (many o-- many) | Una asignatura puede ser impartida a muchos alumnos, y un alumno puede cursar varias asignaturas. |
| **Alumno – Examen** | Agregación (1 o-- 1) | Un alumno realiza un exámen, y un examen solo puede ser realizado por un solo alumno. |
| **Grado – Asignatura** | Composición (many o-- many) | Un grado contiene varias asignaturas y una asignatura puede estar contenida en varios grados. |
| **Grado – Alumno** | Composición (1 *-- many) | Un grado puede ser cursado por varios alumnos, pero un alumno solo puede cursar un solo grado. |