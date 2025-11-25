| Transición de Estado | Tipo | Justificación Funcional |
| :--- | :--- | :--- |
| **No Creado → En Construcción** | Transición | El profesor inicia el proceso de creación de una nueva pregunta. |
| **En Construcción → Habilitada** | Transición | El profesor confirma que la pregunta está completa y correcta. A partir de este momento, el sistema puede seleccionarla para generar exámenes únicos basados en criterios de dificultad y tema. |
| **Habilitada → Inhabilitada** | Transición | El profesor retira la pregunta del uso para futuros usos (por ejemplo, cambio de temario o detección de error tras un examen). No se borra del sistema, pero el generador ya no la elegirá para futuros tests. |
| **Inhabilitada → Habilitada** | Transición | El profesor corrige una errata en una pregunta antigua o decide volver a usarla. La entidad vuelve a estar disponible para la utilización para futuras preguntas. |
| **Habilitada → En Construcción** | Transición | El profesor necesita modificar una pregunta habilitada (corregir errores, actualizar contenido). La pregunta vuelve a estado de edición para realizar los cambios necesarios. |
| **Inhabilitada → En Construcción** | Transición | El profesor necesita modificar una pregunta inhabilitada antes de poder re-habilitarla o realizar cambios en su contenido. |