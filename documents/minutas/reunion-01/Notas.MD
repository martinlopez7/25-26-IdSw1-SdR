[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/README.md)   [![](https://img.shields.io/badge/-ACTORES%20Y%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md)  [![](https://img.shields.io/badge/-DIAGRAMAS%20DE%20CONTEXTO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/diagramasDeContexto/README.md)  [![](https://img.shields.io/badge/-PRIORIZADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/priorizarCasosDeUso/CasosDeUsoPriorizados.md)<br> [![](https://img.shields.io/badge/-DETALLADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/detalladoCasosDeUso/README.md) [![](https://img.shields.io/badge/-PROTOTIPADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/prototipadoCasosDeUso/README.md) [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/README.md) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/README.md)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)

**NOTAS DE LA REUNIÓN:**

**Problema:**

El proceso de realización y corrección de los exámenes tipo test dirigidos a una gran cantidad de alumnos se debe adaptar a la modernidad, es decir, al uso de inteligencia artificial para evitar fraudes y para ahorrar tiempo al docente.

**Solución:** 

Sistema en el que el docente pueda generar un examen (tipo test) con un número de preguntas concreto, dificultad concreta (en proporciones) y único para cada alumno a partir de una batería de preguntas que el profesor ha preparado previamente. La realización de este test será de forma tradicional (a papel). El alumno durante el transcurso del examen completa su hoja de respuestas (que tendrá en la parte inferior un código hash concreto que irá asociado a la resolución de ese mismo tipo de examen). Para la corrección de este examen el docente pone las hojas de respuesta en un escáner que lee este código hash para saber en base a qué modelo de solución corregir y lo corrige utilizando inteligencia artificial.

**Aspectos a tener en cuenta:**

- Este sistema trabaja con datos sensibles: preguntas de examen, soluciones de exámenes, datos de los alumnos (nombre, DNI, grado). El cliente en un principio pensó en tener esta aplicación en la nube, sin embargo, si quiere comercializar esta solución, tendría que gestionar todo el volumen de datos, por lo que si se produce una brecha de seguridad en la aplicación, él sería el responsable (porque es el promotor de la aplicación). Por esto mismo el cliente ha considerado que lo mejor es que la aplicación sea local (de escritorio) y multiplataforma (primera versión en Windows y macOS ya que es lo que el profesorado de la universidad utiliza cómodamente, posteriormente en Linux).

**Forma de comercialización:** 

Cada universidad puede comprar un determinado número de licencias (cuantos profesores pueden estar utilizando la app de forma simultánea)

**Aplicación dividida en dos partes:**

- App en local para el usuario final

- Gestor de licencias (comprueba si un usuario está dado de alta en esa universidad y si la universidad en ese momento tiene una licencia disponible)

**Actores en cada parte:**

- App en local para el usuario final:
  - Administrador institucional
  - Usuario final (docente)

- Gestor de licencias:
  - Administrador general
  - Técnico

Podría darse el caso de que el administrador institucional sea también un profesor de esta institución (usuario final). En este caso, tiene privilegios compartidos.

**Casos de uso de cada actor:**

 <u>Administrador institucional</u>

Módulo usuarios de docentes:

- Dar de alta a un profesor, leer a un profesor, actualizar a un profesor y eliminar a un profesor (CRUD): puede dar de alta a todos los profesores que desee ya que las licencias NO están ligadas al usuario si no a la concurrencia de uso de la app.

Módulo gestión licencias

- Adquirir licencia, leer licencia, actualizar licencia y eliminar licencia (CRUD)

<u>Usuario final</u>

Módulo de asignación (triangulación para combinación única)

- Crear grado, leer grado, actualizar grado, eliminar grado (CRUD)

- Crear asignatura, leer asignatura, actualizar asignatura, eliminar asignatura (CRUD)

- Crear alumno, leer alumno, actualizar alumno, eliminar alumno (CRUD)

- Asignar alumno a un grado, desasignar alumno de un grado

- Asignar grado a una asignatura, desasignar grado de una asignatura

- Asignar alumno a una asignatura (especificando curso académico), desasignar alumno de una asignatura

- Importar listado de alumnos

Módulo gestión de preguntas (batería de preguntas)

- Crear pregunta, ver pregunta, actualizar pregunta, eliminar pregunta (CRUD): enunciado, cuatro opciones de respuesta, opción correcta, asignatura, tema y dificultad (fácil, medio, difícil)

- Importar preguntas desde un fichero con formato específico

- Exportar preguntas a un fichero encriptado con formato específico

Módulo configuración general:

- Exportar configuración global en un archivo

- Importar configuración global en un archivo

Módulo examen

- Generar examen: indicar asignatura, curso, semestre, número de examen (P1, P2, P3, EF, EE), número de preguntas, proporción de dificultad de preguntas, tema/temas, cantidad de tipos de examen (desde 1 hasta la cantidad de alumnos matriculados en la asignatura). Esto genera un pdf con tantas hojas como alumnos tenga el en esa asignatura, de tal forma que cada examen y hoja de respuestas es único para cada alumno (un examen no puede tener preguntas duplicadas). Estas hojas vienen ya con los datos del alumno y con una clave alfanumérica (hashcode) que representa el modelo de corrección al que se tendrá que ceñir el escáner. Todo esto queda almacenado para que no haya cambios durante la realización del examen.

Módulo corrección

- Corregir exámenes: El docente proporciona al sistema un pdf con las hojas de respuestas. El sistema utiliza inteligencia artificial (reconocimiento de imagen) para detectar la posición de las respuestas marcadas por el alumno. Luego, mediante un sistema basado en reglas tradicional, comprueba si estas respuestas estaban bien o mal en función de la clave alfanumérica (que guarda la referencia al modelo de corrección) de la parte inferior de la hoja, que el sistema ha leído previamente. Finalmente, almacena los resultados y genera un pdf o varios (descarga individual o fichero único con todo) prácticamente igual en el que sobrescribe cada hoja de respuestas con un tick o una cruz al lado de la respuesta en función si está bien o mal. 

**EL SISTEMA NO CALIFICA, SOLO CORRIGE, ES EL PROFESOR EL QUE PONE LA NOTA (Ley Europea).** 

**PREGUNTAS PARA JORGE:**

1. En la anterior reunión nos dijiste que un profesor puede generar un examen y seleccionar que solo quiere un único tipo de examen, es decir, que todos los exámenes tendrán el mismo contenido de preguntas pero en distinto orden. De tal forma que todas las hojas de respuesta tendrán la misma clave que referencia al mismo modelo de corrección. ¿Cómo corregirá las respuestas el sistema si las respuestas de todas las hojas del pdf están en distinto orden pero todas se corrigen con el mismo modelo?

**Respuesta:** Los exámenes, aunque contengan las mismas preguntas, son distintos porque cambia el orden de las mismas y cada ordenación de preguntas lleva una clave de calificación diferente. Eso implica que el hash de cada alumno siempre será distinto.
