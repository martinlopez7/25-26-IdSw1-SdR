[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)  [![](https://img.shields.io/badge/-CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/)<br> [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md)

---

## Actores

### Docente: 

Es el actor que más interactúa con el sistema.

El docente tiene la capacidad de generar evaluaciones personalizadas y asignarlas a cada estudiante mediante una clave de identificación única.

La personalización de estos exámenes incluye la definición de:

- Cantidad de preguntas.

- Número de variantes del examen.

- Selección específica de tema o temas.

- Proporción de dificultad.

Para la generación, el sistema utiliza una batería de preguntas previamente cargada por el profesor. Adicionalmente, este sistema está equipado para corregir los exámenes realizados por los alumnos. Emplea Inteligencia Artificial basada en detección de imágenes para leer la clave, lo que permite recuperar el modelo de corrección asociado, y proceder a validar las respuestas del estudiante.

Estos son sus casos de uso:

| ![Casos de Uso Docente](actoresYCasosDeUso-docente.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-docente.puml) |

---

### Administrador institucional:

Es el "representante" de la universidad, su función es gestionar las cuentas para los **Docentes**. Son esas las cuentas que usarán los **Docentes** para `iniciarSesion()` y acceder al sistema.

Estos son sus casos de uso:

| ![Casos de Uso Administrador Institucional](actoresYCasosDeUso-administradorInstitucional.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-administradorInstitucional.puml) |

---

### Tiempo:

Se encarga únicamente de cerrar sesión cuando hay un tiempo de inactividad determinado.

| ![Casos de Uso Tiempo](actoresYCasosDeUso-tiempo.svg) |
| :--- |
| [Código UML](actoresYCasosDeUso-tiempo.puml) |

