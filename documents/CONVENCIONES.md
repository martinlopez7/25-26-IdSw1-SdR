# 📝 Convenciones de Trabajo en GitHub

Para asegurar un flujo de trabajo eficiente, una trazabilidad clara y el cumplimiento de las rúbricas de evaluación, todo el equipo debe adherirse a las siguientes convenciones para nombrar elementos en GitHub (etiquetas, issues, ramas, commits, Pull Requests y archivo `AI-uso.md`).

---

## 1. Etiquetas (Labels)

Las etiquetas (Labels) son cruciales para la categorización y seguimiento de las incidencias (Issues). Utilizaremos las siguientes etiquetas, tal como se han definido:

| Etiqueta              | Descripción                                                                          
| :-------------------- | :------------------------------------------------------------------------ 
| `bug`                 | Indica un error en un artefacto que debe ser corregido.
| `casoDeUso`           | Relacionado con un Caso de Uso (diagrama, ficha, prototipo).
| `documentation`       | Tareas relacionadas con minutas, READMEs, o el archivo `AI-uso.md`.
| `duda`                | Usar cuando un Issue es una pregunta directa para el cliente.
| `modeloDominio`       | Relacionado con el Modelo del Dominio (diagrama, glosario, etc.).
| `tarea-interna`       | Tarea para el equipo que no requiere interacción con el cliente. 
| `validación-cliente`  | Usar cuando un Issue pide al cliente que apruebe un artefacto. 

---

## 2. Incidencias (Issues)

Los Issues son el motor de nuestra trazabilidad y la principal herramienta de interacción con el cliente (Rúbricas 4 y 5).

### 2.1. Título del Issue

Usaremos prefijos en el título para identificar rápidamente el propósito del Issue.

* **Para el Cliente (Duda):**
    * `[Duda] <Pregunta clara y concisa>`
    * *Ejemplo:* `[Duda] ¿Puede un usuario tener múltiples perfiles de pago vinculados?`
    * *Etiquetas:* `duda`

* **Para el Cliente (Validación):**
    * `[Validación] <Artefacto y versión a validar>`
    * *Ejemplo:* `[Validación] v1 del Modelo del Dominio y Glosario`
    * *Etiquetas:* `validación-cliente`, `modeloDominio`

* **Para el Equipo (Tarea Interna):**
    * `[Tarea] <Acción específica a realizar>`
    * *Ejemplo:* `[Tarea] Redactar v1 de la ficha del CU-03: Generar Informe`
    * *Etiquetas:* `tarea-interna`, `casoDeUso`

* **Para Corregir un Error:**
    * `[Bug] <Descripción del error>`
    * *Ejemplo:* `[Bug] El CU-01 no contempla el caso de usuario ya existente.`
    * *Etiquetas:* `bug`, `casoDeUso`

### 2.2. Cuerpo del Issue

* **Si el Issue es para el cliente:**
    * **MENCIONADLO** explícitamente usando su `@usuario-github-del-cliente`.
    * Explicad el contexto y, si se deriva de una reunión, enlazad a la minuta correspondiente (ej: `Ver /minutas/minuta-20240320.md`).
    * *Ejemplo de cuerpo para Issue `[Duda] ¿Puede un usuario...?`:*
        ```markdown
        Hola @usuario-del-cliente,

        En la reunión del 20/03/2024 (ver /minutas/minuta-20240320.md) se mencionó la funcionalidad de gestión de pagos. Nos ha surgido la duda sobre si un usuario podría tener más de un perfil de pago (ej: una tarjeta de crédito y una cuenta de PayPal) o si solo se permite uno a la vez.

        ¡Gracias!
        ```

* **Si es una tarea interna:**
    * Asignad a 1 miembro del equipo (`Assignees`) para indicar quién es el responsable principal.
    * Describid los entregables esperados o los pasos a seguir.
    * *Ejemplo de cuerpo para Issue `[Tarea] Redactar v1 de la ficha del CU-03`:*
        ```markdown
        Basándonos en los requisitos discutidos en la Sesión 1 (#5, Issue de la minuta), se debe redactar la primera versión de la ficha completa para el Caso de Uso "Generar Informe".

        Entregables:
        - /casos-de-uso/CU-03-GenerarInforme.md (incluyendo Actores, Precondiciones, Flujo Principal, Flujos Alternativos, Postcondiciones).
        - Posiblemente un diagrama de actividad básico (.puml) si se considera necesario.
        ```

---

## 3. Ramas (Branches)

Todo el trabajo de desarrollo se realiza en ramas separadas, nunca directamente sobre `main`. Esto asegura la estabilidad del repositorio y facilita la revisión.

### Formato del Nombre de la Rama:

`tipo/issue-<NÚMERO_ISSUE>-<descripcion-corta-en-kebab-case>`

* **`tipo`**:
    * `feat`: Para implementar una nueva funcionalidad o crear un artefacto nuevo (ej: la primera versión de un CU, o del MdD).
    * `fix`: Para corregir un error (`bug`) en un artefacto existente.
    * `docs`: Para añadir o modificar documentación (minutas, README, `AI-uso.md`).
    * `refactor`: Para reestructurar un artefacto sin cambiar su funcionalidad (ej: reorganizar clases en el MdD).
    * `chore`: Para tareas de mantenimiento del repositorio (ej: configurar `gitignore`, mover archivos).

* **`<NÚMERO_ISSUE>`**: El número del Issue de GitHub que esta rama está abordando. **Esto es crucial para la trazabilidad.**

* **`<descripcion-corta-en-kebab-case>`**: Una breve descripción del trabajo en minúsculas y separada por guiones.

### Ejemplos de Nombres de Rama:

* **Si el Issue es `#10: [Tarea] Crear v1 del Modelo del Dominio`:**
    * `feat/issue-10-modelo-dominio-v1`

* **Si el Issue es `#15: [Bug] El CU-01 no contempla el caso de usuario ya existente`:**
    * `fix/issue-15-cu01-usuario-existente`

* **Si el Issue es `#20: [Tarea] Añadir minuta de la Sesión 2`:**
    * `docs/issue-20-minuta-sesion-2`

---

## 4. Commits

Los mensajes de commit son fundamentales para la Rúbrica 4 ("Trazabilidad") y para entender la evolución de nuestro proyecto. Utilizaremos el estándar de **Conventional Commits**.

### Formato del Mensaje de Commit:

`tipo(alcance): <mensaje breve en imperativo> [refs #NÚMERO_ISSUE]`

* **`tipo`**: Indica el propósito del commit. Son los mismos que los tipos de rama:
    * `feat`: Se introduce una nueva funcionalidad o artefacto.
    * `fix`: Se corrige un error (corresponde a un Issue de tipo `bug`).
    * `docs`: Cambios en la documentación.
    * `style`: Cambios de formato (ej: ordenar elementos en un diagrama `.puml`) que no afectan la lógica.
    * `refactor`: Reestructuración del código o artefacto.
    * `chore`: Tareas de mantenimiento (ej: configuración, estructura de carpetas).

* **`(alcance)`**: (Opcional, pero recomendado) Describe la parte del proyecto afectada.
    * `(mdd)`: Modelo del Dominio.
    * `(cu)`: Casos de Uso (general).
    * `(cu-01)`: Un Caso de Uso específico.
    * `(glosario)`: El glosario de términos.
    * `(minuta)`: Minutas de reuniones.
    * `(repo)`: Relacionado con el repositorio (README, `.gitignore`, estructura).
    * `(ia-uso)`: Cambios en el archivo `AI-uso.md`.

* **`<mensaje breve en imperativo>`**: Una descripción concisa de lo que hace el commit, escrita en modo imperativo (ej: "añade", "corrige", "actualiza").

* **`[refs #NÚMERO_ISSUE]`**: **¡Este es el elemento más crítico!** Es la referencia al número del Issue de GitHub que este commit ayuda a resolver. Esto crea la bidireccionalidad de la trazabilidad.

### Ejemplos de Mensajes de Commit:

* **Para el Issue `#10: [Tarea] Crear v1 del Modelo del Dominio`:**
    * `feat(mdd): añade clases Usuario y Reserva iniciales [refs #10]`
    * `feat(glosario): define términos clave del dominio [refs #10]`

* **Para el Issue `#15: [Bug] El CU-01 no contempla...`:**
    * `fix(cu-01): añade flujo alternativo para usuario existente [refs #15]`

* **Para el Issue `#20: [Tarea] Añadir minuta de la Sesión 2`:**
    * `docs(minuta): añade minuta de la reunión del 28/03/2024 [refs #20]`

* **Para actualizar el uso de IA:**
    * `docs(ia-uso): registra uso de IA para refinar descripción de CU-02 [refs #22]`

---

## 5. Pull Requests (PRs)

Los Pull Requests son el mecanismo para que el trabajo de una rama se revise y se integre en `main`. También son fundamentales para la trazabilidad y la evidencia de trabajo en equipo.

### 5.1. Título del Pull Request:

`[TIPO_COMMIT_PRINCIPAL] <Mismo título del Issue principal que resuelve>`

* **`[TIPO_COMMIT_PRINCIPAL]`**: El `tipo` de commit más relevante en la rama (ej: `[Feat]`, `[Fix]`, `[Docs]`).

* *Ejemplo:* Si el PR resuelve el Issue `#10: [Tarea] Crear v1 del Modelo del Dominio`
    * `[Feat] [Tarea] Crear v1 del Modelo del Dominio`

### 5.2. Cuerpo del Pull Request:

* **Referencia al Issue:** Incluid la frase `Closes #NÚMERO_ISSUE` (o `Fixes #NÚMERO_ISSUE`). Esto hará que GitHub cierre automáticamente el Issue cuando el PR se fusione. **¡No olvidéis esto!**
    * *Ejemplo:* `Closes #10`

* **Revisores:** Asignad a **todos los demás miembros del equipo** como "Reviewers". Esto demuestra la colaboración y la revisión por pares, cumpliendo la Rúbrica 4 ("Autoría y distribución").

* **Interacción con el Cliente (Opcional pero recomendable):**
    * Si el PR integra un artefacto clave que ha sido validado por el cliente, podéis mencionar al `@usuario-github-del-cliente` en el PR y pedirle una última "aprobación" simbólica como evidencia final de la Rúbrica 5.

### Ejemplo de Cuerpo de Pull Request:

```markdown
Closes #10

Este Pull Request implementa la primera versión del Modelo del Dominio y su Glosario asociado, según lo especificado en el Issue #10.

Se han creado los siguientes archivos:
- `/modelos/dominio-v1.puml`
- `/modelos/dominio-v1.png`
- `/modelos/glosario.md`

@[usuario-del-cliente] Este artefacto ha sido revisado internamente por el equipo. Agradeceríamos tu visto bueno final.
```

---

## 6. AI-uso.md

El archivo `AI-uso.md` debe seguir este formato.

```markdown
## Declaración de uso de IA

## Herramientas utilizadas
- [Nombre del modelo/herramienta] (ej: ChatGPT 4, Claude 3.5, Copilot)
- Fechas de uso: [Rango de fechas]

## Contexto de uso

### Para modelo del dominio
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: generación inicial, revisión, sugerencias de clases, etc.]
**¿Qué se aceptó y qué se rechazó?** [Explicar críticamente]

### Para casos de uso
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: ayuda con formato, generación de flujos, etc.]
**¿Qué se aceptó y qué se rechazó?** [Explicar críticamente]

### Para documentación
**¿Se usó?** [Sí/No]
**¿Para qué?** [Describir: mejora de redacción, glosario, etc.]

## Enlaces a conversaciones

### Conversación 1: [Título descriptivo]
**URL completa**: https://...
**Fecha**: YYYY-MM-DD
**Qué se obtuvo**: [Breve descripción]
**Qué se hizo con ello**: [Se usó directamente, se modificó, se descartó]
**Archivo(s) afectado(s)**: [Enlaces a commits]

### Conversación 2: [Título descriptivo]
...

## Validación humana

**¿Cómo validamos lo generado?**
[Explicar: contrastamos con cliente, revisamos contra minutas, 
verificamos con conocimientos de clase, etc.]

**¿Qué errores detectamos de la IA?**
[Ejemplos concretos de cosas que la IA sugirió mal y corregimos]

## Reflexión del equipo

**¿La IA ayudó o entorpeció?**
[Opinión honesta del equipo]

**¿Qué aprendimos sobre el uso de IA en requisitado?**
[Reflexión sobre límites y valor de las herramientas]
```