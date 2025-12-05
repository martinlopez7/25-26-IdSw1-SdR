[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/README.md)   [![](https://img.shields.io/badge/-ACTORES%20Y%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md)  [![](https://img.shields.io/badge/-DIAGRAMAS%20DE%20CONTEXTO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/diagramasDeContexto/README.md)  [![](https://img.shields.io/badge/-PRIORIZADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/priorizarCasosDeUso/CasosDeUsoPriorizados.md)<br> [![](https://img.shields.io/badge/-DETALLADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/detalladoCasosDeUso/README.md) [![](https://img.shields.io/badge/-PROTOTIPADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/prototipadoCasosDeUso/README.md) [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/README.md) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/README.md)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)

---

## ACTA DE DECISIONES Y ACCIONES

**Objetivo de la Reunión:** Revisión y refinamiento del modelo de dominio, diagrama de estados de la entidad "Examen" y casos de uso del sistema.

---

### Decisiones sobre el Modelo de Dominio

* **Batería de Preguntas:** La batería de preguntas se asocia directamente a la `Asignatura`, no al `Profesor`.
* **Atributo "Tema":** El atributo `tema` se elimina de la entidad `Asignatura` y se mantiene únicamente en la entidad `Pregunta`.
* **Atributos de Pregunta:** Se confirman los atributos para `Pregunta`: `enunciado`, `asignatura`, `tema` y `dificultad` (restringida a "fácil" y "difícil").

### Decisiones sobre el Diagrama de Estados (Entidad Examen)

* **Definiciones Clave:**
    * **Creación:** Genera el examen y su clave alfanumérica (hashcode), que representa la *solución* del examen.
    * **Asignación:** Vincula un examen (con su clave/solución) a un alumno específico.
    * **Impresión:** El examen impreso incluirá los datos del alumno (nombre, DNI) para evitar la necesidad de OCR sobre escritura manual.
* **Estados Finales Acordados:**
    1.  `No Creado`
    2.  `Creado` (Estado por defecto tras la generación; implica "no asignado").
    3.  `Asignado` (Vinculado a un alumno concreto).
    4.  `Corregido` (Procesada la hoja de respuestas).

### Decisiones sobre Casos de Uso

* **Separación de Casos de Uso:** `Generar Examen` y `Asignar Examen` serán casos de uso separados.
* **Interfaz de Generación:** La interfaz de `Generar Examen` podrá ofrecer la opción de asignar los exámenes generados inmediatamente (funcionalidad "dos en uno").
* **Asignación en Lote:** Debe existir una opción separada para `Asignar batería de exámenes a alumnos` (asignación desde el conjunto de exámenes ya creados).
* **Inicio de Sesión:** El caso de uso `Iniciar Sesión` se considera estándar e implícito.
* **Nuevo Requisito a Evaluar:** Se evaluará la implementación de un cierre de sesión automático por inactividad para la gestión de licencias de concurrencia.

---