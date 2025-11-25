| Transición de Estado | Tipo | Justificación Funcional |
| :--- | :--- | :--- |
|  |
| **No Creado → En Construcción** | Transición | La pregunta pasa a un estado de construcción en el cual se espera que el el sistema elija las preguntas de la batería de preguntas. |
| **En Construcción → Habilitada** | Transición | El profesor confirma que la pregunta está completa y correcta. A partir de este momento, el sistema puede seleccionarla para generar exámenes únicos basados en criterios de dificultad y tema. |
| **Habilitada → Inhabilitada** | Transición |  El profesor retira la pregunta del uso para futuros usos (por ejemplo, cambio de temario o detección de error tras un examen). No se borra del sistema para no corromper el historial de exámenes pasados que usaron esta pregunta, pero el generador ya no la elegirá para futuros tests. |
| **Inhabilitada → Habilitada** | Transición |  El docente corrige una errata en una pregunta antigua o decide volver a usarla. La entidad vuelve a estar disponible para la utilización para futuras preguntas. |
| **Habilitada / Inhabilitada → [*]** | Finalización |  Borrado definitivo de la base de datos local. Se ejecuta cuando el profesor determina que la pregunta no es necesaria ni para futuros exámenes. |