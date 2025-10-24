# Organización del repositorio (1.0 pts)

Se valora la capacidad de organizar el trabajo de forma que sea navegable y auditable. No se prescribe una estructura única, pero debe seguir principios de claridad y trazabilidad similares a los ejemplos vistos en clase.

**Principios obligatorios:**

- **Navegabilidad**: Cualquier evaluador debe poder localizar artefactos sin búsqueda exhaustiva
- **Separación lógica**: Diferentes tipos de artefactos en ubicaciones diferenciadas
- **README descriptivo**: Documento raíz que explica la estructura elegida
- **Nomenclatura consistente**: Convención de nombres clara y mantenida

Una estructura es válida **siempre que el README raíz explique claramente dónde está cada cosa**.

**Criterios de puntuación:**

|Puntos|README raíz|Estructura lógica|Nomenclatura|Accesibilidad|
|-|-|-|-|-|
|0.9-1.0|**README completo** con: índice navegable (enlaces a carpetas clave), explicación de estructura elegida, convenciones de nomenclatura usadas, guía rápida de "dónde está qué". **Actualizado**: Refleja estructura real del repo|**Separación clara**: Diferentes tipos de artefactos en ubicaciones diferenciadas y lógicas. **READMEs locales**: Carpetas principales tienen README explicando su contenido. **Coherencia**: Estructura mantenida consistentemente (no mezcla criterios)|**Convención declarada**: Documento explicita convención (ej: "CU-XX-nombre", "minuta-YYYYMMDD"). **Aplicada consistentemente**: ≥90% archivos siguen la convención. **Significativa**: Nombres descriptivos, no genéricos|**Localización inmediata**: Artefactos clave (MdD final, CdU priorizados, minutas) localizables en <30 segundos. **Sin archivos huérfanos**: ≤2 archivos fuera de estructura. **Exportaciones presentes**: Diagramas .puml tienen .svg/.png|
|0.7-0.8|**README presente** con elementos básicos: índice, algo de explicación. **Mayormente actualizado**|**Separación**: Presente con alguna inconsistencia menor. **Algunos READMEs locales**. **Coherencia**: Mayormente mantenida|**Convención**: Implícita o parcialmente declarada. **Aplicada**: 70-89% archivos consistentes. **Mayormente significativa**|**Localización**: Artefactos principales localizables con algo de exploración. **Archivos fuera**: ≤5. **Exportaciones**: Mayoría presente|
|0.5-0.6|**README básico**: Lista carpetas sin mucha explicación. **Desactualizado parcialmente**|**Separación**: Básica, algunas mezclas. **Sin READMEs locales**. **Coherencia**: Parcial|**Convención**: No declarada pero algo consistente. **Aplicada**: 50-69% consistentes. **Nombres aceptables**|**Localización**: Requiere búsqueda. **Archivos fuera**: ≤10. **Exportaciones**: Parciales|
|0.1-0.4|**README mínimo** o sin explicación útil. **Desactualizado**|**Estructura**: Confusa o caótica. **Sin coherencia**|**Sin convención** aparente. **Nombres genéricos**: "documento1", "final", "nuevo"|**Difícil navegación**: Imposible localizar sin búsqueda exhaustiva. **Desorden**: >10 archivos mal ubicados|
|0|Sin README o inútil|Sin estructura discernible|Nomenclatura caótica|Repositorio innavegable|

**Antipatrones penalizados:**

|Antipatrón|Descripción|Penalización|
|-|-|-|
|Archivos en raíz|>5 archivos sueltos en raíz del repo (excepto README, .gitignore)|-0.2 pts|
|Duplicación sin control|Múltiples versiones sin convención clara ("final", "final2", "finalFINAL")|-0.3 pts|
|Archivos temporales|Presencia de archivos temporales, backups automáticos (.DS_Store, ~, .tmp)|-0.1 pts|
|README genérico|README copiado sin adaptar al proyecto específico|-0.2 pts|
|Exportaciones ausentes|Diagramas .puml sin exportación visual (.svg/.png)|-0.2 pts|

**Libertad dentro de principios:**

El equipo puede elegir:

- Nombres de carpetas (en español, inglés, o combinación razonable)
- Profundidad de la jerarquía (más o menos subcarpetas)
- Convención específica de nomenclatura (mientras sea consistente)
- Ubicación de artefactos complementarios

Lo que NO puede faltar:

- README raíz explicativo
- Separación lógica de tipos de artefactos
- Forma de localizar versiones de MdD y CdU
- Minutas accesibles cronológicamente

**Relación con otros apartados:**

- La estructura debe facilitar la trazabilidad (apartado 4)
- Los artefactos deben ser localizables para evaluación técnica (apartados 1, 2, 3)
- La organización refleja profesionalidad del equipo

**Buenas prácticas valoradas:**

- (+0.1) `.gitignore` apropiado para el proyecto
- (+0.1) Badges en README (estado, última actualización)
- (+0.1) Estructura que facilita navegación por versiones (tags git, releases)