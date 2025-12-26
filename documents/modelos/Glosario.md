
<div align="center">

[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/README.md)   [![](https://img.shields.io/badge/-ACTORES%20Y%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md)  [![](https://img.shields.io/badge/-DIAGRAMAS%20DE%20CONTEXTO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/diagramasDeContexto/README.md)  [![](https://img.shields.io/badge/-PRIORIZADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/priorizarCasosDeUso/CasosDeUsoPriorizados.md)<br> [![](https://img.shields.io/badge/-DETALLADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/detalladoCasosDeUso/README.md) [![](https://img.shields.io/badge/-PROTOTIPADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/prototipadoCasosDeUso/README.md) [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/README.md) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/README.md)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)

</div>

# Glosario

| Término | Definición |
|---|---|
| **Grado** | Programa universitario que agrupa alumnos y asignaturas. |
| **Asignatura** | Materia concreta dentro de un grado. Cada asignatura tiene unos alumnos matriculados. |
| **Curso académico** | Periodo temporal (ej. 2024-2025) definido en la asignatura para organizar la matriculación de alumnos. |
| **Profesor** | Docente encargado de llevar una asignatura. |
| **Alumno** | Persona que cursa una o varias asignaturas y realiza el exámenes tipo test. |
| **Batería de preguntas** | Conjunto de preguntas de un asignatura concreta preparadas por un docente para generar exámenes tipo test. |
| **Tema** | Parte o unidad dentro de una asignatura que agrupa varias preguntas relacionadas. Sirve para organizar la batería de preguntas del profesor. |
| **Pregunta** | Elemento básico del exámen tipo test creado por el profesor. Cada pregunta tiene una asignatura, un tema, enunciado, dificultad y las posibles respuestas. |
| **Respuesta** | Opción individual que forma parte de una pregunta. Indica una posible solución al enunciado y define si es la opción correcta o incorrecta. |
| **Exámen** | Documento de evaluación de la asignatura tipo test que un docente genera introduciendo varios parámetros a partir de una batería de preguntas previamente preparada. |
| **Clave de corrección** | Clave alfanumérica que está en cada exámen asignado que guarda: datos del alumno para que no haya manipulaciones fraudulentas durante la realización del exámen y el orden concreto de soluciones del exámen. Esta clave se utilizará por el propio sistema para la futura corrección por inteligencia artificial mediante detección de imágenes. |
| **Evaluación** | Actividad mediante la cual el profesor califica al alumno (Exámen parcial 1-3, Exámen Final o Exámen Extraordinario). |
| **Exámenes generados** | Conjunto de exámenes con un orden de preguntas concreto. Todavía sin claves alfanuméricas que asigne cada exámen a cada alumno. |
| **Exámenes asignados** | Conjunto de exámenes generados con claves alfanuméricas incorporadas. |
| **Pregunta habilitada** | Una pregunta habilitada se tendrá en cuenta por el sistema para la generación de exámenes. |
| **Pregunta inhabilitada** | Una pregunta inhabilitada no se tendrá en cuenta por el sistema para la generación de exámenes. |