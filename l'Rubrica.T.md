# Trazabilidad y versionado (1.0 pts)

La trazabilidad emerge naturalmente del trabajo bien hecho en GitHub: commits descriptivos, issues que documentan decisiones con el cliente, y referencias cruzadas entre artefactos. No se requieren documentos adicionales de trazabilidad.

**Dónde se evidencia la trazabilidad:**

- En los **commits**: mensajes descriptivos que explican qué cambió y por qué
- En las **issues** y **discussions**: conversaciones con el cliente que quedan documentadas
- En los **artefactos**: cada caso de uso referencia su origen y validación
- En la **historia de git**: evolución visible del trabajo

**Criterios de puntuación:**

|Puntos|Commits|Issues y comunicación con cliente|Trazabilidad integrada|Autoría y distribución|
|-|-|-|-|-|
|0.9-1.0|**Descriptivos**: ≥80% commits con mensaje >10 palabras explicando el cambio. **Formato consistente**: Siguen convención (ej: "feat(mdd): añade clase Reserva", "fix(cu-03): corrige flujo alternativo"). **Atomicidad**: Commits enfocados en un cambio específico, no mezclan temas. **Referencias**: Mencionan issues relacionados (#23, #45). **Frecuencia**: Commits distribuidos temporalmente (no todo el último día)|**Issues relevantes**: ≥5 issues creados mencionando explícitamente al cliente (@usuario-cliente). **Categorización**: Labels usados consistentemente (validación-cliente, requisito, duda-dominio). **Bidireccionalidad**: Issues enlazan a commits que los resuelven Y commits referencian issues. **Cierre documentado**: Issues cerrados con explicación de la decisión tomada. **Discussions**: ≥2 threads sobre decisiones importantes de modelado|**En casos de uso**: ≥80% de CdU tienen sección trazabilidad con origen (minuta/issue) y validación del cliente. **En modelo**: README de `/modelos/` explica evolución del modelo. **Versionado**: Archivos con versiones claras (dominio-v1, v2, v3...). **Consistencia**: Referencias cruzadas entre MdD y CdU funcionan (conceptos citados existen en glosario)|**Firmas git**: 100% commits con autor identificable (git config correcto). **Distribución equitativa**: Todos los miembros tienen commits significativos (no todo concentrado en 1-2 personas). **Visible en GitHub**: Insights > Contributors muestra participación balanceada. **Sin commits retroactivos**: Fechas de commit coherentes con fechas de minutas|
|0.7-0.8|**Descriptivos**: 60-79% commits descriptivos. **Formato**: Mayormente consistente con algunos genéricos. **Atomicidad**: Algunos commits mezclan cambios pero no domina. **Referencias**: Parciales|**Issues**: ≥3 issues con cliente mencionado. **Labels**: Uso básico. **Bidireccionalidad**: Parcial. **Cierre**: Algunos bien documentados. **Discussions**: ≥1 thread|**En CdU**: 60-79% con trazabilidad. **En modelo**: Evolución básicamente explicada. **Versionado**: Presente con alguna inconsistencia. **Consistencia**: Mayoría de referencias funcionan|**Firmas**: Mayoría correctas. **Distribución**: Desigual pero todos participan. **Visible**: Desequilibrio moderado|
|0.5-0.6|**Descriptivos**: 40-59%. **Formato**: Inconsistente. **Atomicidad**: Commits grandes frecuentes. **Referencias**: Pocas|**Issues**: ≥2 issues relevantes. **Labels**: Uso mínimo. **Bidireccionalidad**: Limitada. **Cierre**: Básico. **Discussions**: Escasas|**En CdU**: 40-59% con trazabilidad. **En modelo**: Explicación mínima. **Versionado**: Confuso. **Consistencia**: Referencias rotas o incompletas|**Firmas**: Mayoría identificables. **Distribución**: Muy concentrada. **Visible**: Desequilibrio notable|
|0.1-0.4|**Commits genéricos**: "update", "fix", "cambios". **Sin formato**. **Commits enormes**. **Sin referencias**|**Issues**: <2 o sin cliente mencionado. **Sin labels**. **Sin bidireccionalidad**. **Cierre sin explicación**|**Trazabilidad**: <40% o ausente. **Sin explicación** de evolución. **Versionado**: Caótico|**Autoría**: Confusa o concentrada en 1 persona. **Sin distribución** real|
|0|Sin commits descriptivos|Sin issues con cliente|Sin trazabilidad|Sin autoría clara o trabajo individual|

**Ejemplos de commits:**

|Bueno|Malo|
|-|-|
|`feat(mdd): añade clase Reserva con relación a Usuario`|`update`|
|`fix(cu-03): corrige flujo alternativo según feedback #45`|`cambios`|
|`docs(glosario): define 'disponibilidad' según cliente`|`fix`|
|`refactor(mdd): cambia asociación a composición refs #23`|`varios cambios`|

**Ejemplos de issues bien hechos:**

```markdown
Título: Validar cardinalidad Profesor-Curso

@prof-cliente en la minuta del 19/10 mencionó que algunos cursos 
son co-impartidos por varios profesores. 

¿Debemos modelar esto como:
- 1 Profesor → 1..* Cursos (un profesor da varios cursos)
- 1..* Profesores → 1 Curso (varios profesores dan un curso)

O ambas cosas son posibles?

Ver línea 23 de modelos/dominio-v2.puml

Labels: validación-cliente, duda-dominio
```

**Estructura de trazabilidad en CdU** (repetimos del apartado 3):

```markdown
## Trazabilidad
- Origen: Minuta 2024-10-19 (#15)
- Issue: #23
- Validación: #25 (cliente aprobó 2024-10-22)
```

**Penalizaciones específicas:**

|Situación|Penalización|Justificación|
|-|-|-|
|Commits retroactivos evidentes (fecha muy posterior a minuta que referencian)|-0.3 pts|Indica fabricación de evidencia|
|Issues que declaran validación del cliente sin mención real de @cliente|-0.2 pts|Trazabilidad falsa|
|Commits sin autor identificable (git config mal configurado)|-0.2 pts|Imposibilita auditoría de autoría|
|80%+ del trabajo concentrado en 1-2 personas sin justificación documentada|-0.3 pts|No es trabajo en equipo|
|Commits >200 líneas mezclando cambios no relacionados|-0.2 pts|Dificulta seguimiento de cambios|
|Todos los commits el mismo día/última semana|-0.2 pts|Indica trabajo no iterativo|

**Configuración git obligatoria** (cada miembro):

```bash
git config user.name "Nombre Apellido"
git config user.email "email@alumnos.uneatlantico.es"

# Verificar
git config --list|grep user
```

**Cómo verificar distribución del trabajo:**

En GitHub: `Insights > Contributors` debe mostrar:

- Todos los miembros con commits
- Distribución temporal (no todo concentrado)
- Líneas añadidas/modificadas balanceadas

**Buenas prácticas valoradas positivamente:**

- (+0.1) Uso de milestones para agrupar issues por sesión
- (+0.1) Project board mostrando progreso del trabajo
- (+0.1) Templates de issues personalizados para el proyecto
- (+0.1) Branch strategy clara (ej: feature branches con nombres descriptivos)

**Casos excepcionales:**

- **Miembro del equipo ausente justificadamente**: Si un miembro tiene baja médica documentada >50% del periodo, no penaliza la distribución. Debe documentarse en issue.
- **Commits de merge automáticos**: No cuentan para estadística de mensajes descriptivos.
- **Rebase/squash de commits**: Aceptable si el commit final es descriptivo y mantiene referencias a issues.
