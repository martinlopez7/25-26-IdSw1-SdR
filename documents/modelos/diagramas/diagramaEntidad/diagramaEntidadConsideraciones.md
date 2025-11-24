| Relación | Tipo y Cardinalidad | Justificación |
| :--- | :--- | :--- |
| **Profesor – Asignatura** | Agregación (1 o-- many) | Un solo profesor puede ser responsable de impartir **varias** asignaturas, mientras que cada asignatura tiene asignado un único profesor titular. |
| **Grado – Asignatura** | Composición (1 *-- many) | Un Grado está formado por **muchas** asignaturas a lo largo de los cursos, pero cada asignatura pertenece exclusivamente a un único Grado. |
| **Asignatura – Alumno** | Asociación (many -- many) | En una asignatura se matriculan **muchos** alumnos y, a su vez, un mismo alumno se matricula en **muchas** asignaturas diferentes. |
| **Asignatura – Examen** | Composición (1 *-- many) | Una asignatura tiene planificados **varios** exámenes (parciales, finales, recuperaciones), pero cada examen corresponde a una única asignatura. |
| **Asignatura – BateríaDePreguntas** | Composición (1 *-- 1) | Cada asignatura tiene asociada **una** única batería de preguntas, y esa batería pertenece solo a esa asignatura. |
| **Grado – Alumno** | Composición (1 *-- many) | Un Grado tiene inscritos a **muchos** alumnos, pero un alumno cursa (en este contexto) un único Grado principal. |
| **Alumno – Examen** | Agregación (1 o-- 1) | Un alumno realiza **una** única instancia/entrega de un examen específico, y esa entrega pertenece a ese único alumno. |
| **Examen – Pregunta** | Agregación (many o-- many) | Un examen consta de **muchas** preguntas, y una misma pregunta puede ser reutilizada y aparecer en **muchos** exámenes distintos. |
| **BateríaDePreguntas – Pregunta** | Composición (1 *-- many) | La batería almacena **muchas** preguntas distintas, pero cada pregunta específica reside en una única batería. |
| **Pregunta – Respuesta** | Composición (1 *-- many) | Una sola pregunta tiene asociadas **varias** opciones de respuesta posibles, que pertenecen únicamente a esa pregunta. |