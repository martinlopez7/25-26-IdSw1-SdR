| Relación | Tipo y Cardinalidad | Justificación |
|-----------|---------------------|----------------|
| **Universidad – Grado** | Composición (1 *-- many) | Una universidad tiene varios grados y cada grado pertenece a una sola universidad. |
| **Universidad – Profesor** | Agregación (many o-- many) | Una universidad tiene varios profesores, pero un profesor puede estar asociado a varias universidades. |
| **Alumno – Grado** | Composición (many *-- 1) | Un alumno solo puede estar matriculado en un grado pero un grado puede tener varios alumnos matriculados. |
| **Grado – Asignatura** | Agregación (many o-- many) | Un grado contiene varias asignaturas y una asignatura puede estar asociada a distintos grados. |
| **Asignatura – Profesor** | Agregación (many o-- 1) | Una asignatura tiene un profesor asignado, y un profesor puede impartir varias asignaturas. |
| **Asignatura – Alumno** | Composición (many o-- many) | Una asignatura puede ser cursada por muchos alumnos, y un alumno puede cursar varias asignaturas. |
| **Asignatura – Examen** | Composición (1 *-- many) | Una asignatura puede tener varios examenes pero un examen solo puede pertenecer a una sola asignatura. |
| **Examen – Pregunta** | Composición (many *-- many) | Un examen contiene varias preguntas, pero una pregunta puede formar parte de otros exámenes. |
| **Asignatura – Tema** | Composición (1 *-- many) | Una asignatura contiene varios temas, y cada tema pertenece a una única asignatura. |
| **Pregunta – Tema** | Composición (many *-- 1) | Una pregunta es de un solo tema pero un tema puede tener varias preguntas. |
| **Alumno – Examen** | Agregación (1 o-- 1) | Un alumno realiza un exámen, y un examen puede ser realizado un solo alumno. |
| **Pregunta – BateríaDePreguntas** | Composición (many *-- 1) | Una pregunta forma parte de una batería de preguntas y en una batería de preguntas hay varias preguntas. |
| **Examen – ModeloCorrección** | Composición (1 *-- 1) | Cada examen tiene un único modelo de corrección y este solo pertenece a ese examen. |
| **Profesor – BateríaDePreguntas** | Composición (1 *-- 1) | Un profesor crea y mantiene una batería de preguntas y una batería de preguntas solo puede ser creada y mantenida por un profesor. |
| **Profesor – Pregunta** | Agregación (1 o-- many) | Un profesor puede crear varias preguntas y una pregunta solo puede ser creada por un profesor |
