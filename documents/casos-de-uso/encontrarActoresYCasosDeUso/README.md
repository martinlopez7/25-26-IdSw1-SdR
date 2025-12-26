[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/README.md)   [![](https://img.shields.io/badge/-ACTORES%20Y%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md)  [![](https://img.shields.io/badge/-DIAGRAMAS%20DE%20CONTEXTO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/diagramasDeContexto/README.md)  [![](https://img.shields.io/badge/-PRIORIZADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/priorizarCasosDeUso/CasosDeUsoPriorizados.md)<br> [![](https://img.shields.io/badge/-DETALLADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/detalladoCasosDeUso/README.md) [![](https://img.shields.io/badge/-PROTOTIPADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/prototipadoCasosDeUso/README.md) [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/README.md) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/README.md)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)

---

## Actores

### Docente: 

Es el actor que más interactúa con el sistema.

El docente tiene la capacidad de generar exámenes personalizados y asignarlos a cada alumno mediante una clave de identificación única.

Para la generación, el sistema utiliza una batería de preguntas de la asigantura seleccionada previamente poblada por el profesor. Además, este sistema corrige los exámenes realizados por los alumnos mediante inteligencia artificial basada en detección de imágenes para leer la clave, lo que permite recuperar el modelo de corrección asociado, y proceder a corregir las respuestas del alumno.

Estos son sus casos de uso:

| ![Casos de Uso Docente](actoresYCasosDeUso-docente-maestro.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-docente-maestro.puml) |

| ![Casos de Uso Docente](actoresYCasosDeUso-docente-extra.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-docente-extra.puml) |

---

### Administrador institucional:

Es el encargado de la universidad de gestionar las cuentas para los Docentes. Son estas las cuentas que usarán los **Docentes** para `iniciarSesion()` y acceder al sistema.

Estos son sus casos de uso:

| ![Casos de Uso Administrador Institucional](actoresYCasosDeUso-administradorInstitucional.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-administradorInstitucional.puml) |

---

### Tiempo:

Se encarga únicamente de cerrar sesión cuando pasa un tiempo de inactividad concreto.

| ![Casos de Uso Tiempo](actoresYCasosDeUso-tiempo.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-tiempo.puml) |

