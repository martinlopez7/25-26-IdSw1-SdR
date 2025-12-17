<div align="center">

[![](https://img.shields.io/badge/-INICIO-white?style=flat&logo=Emlakjet&logoColor=black)](/README.md) [![](https://img.shields.io/badge/-MODELO%20DEL%20DOMINIO-white?style=flat&logo=diagramsdotnet&logoColor=black)](/documents/modelos/diagramas/README.md)   [![](https://img.shields.io/badge/-ACTORES%20Y%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md)  [![](https://img.shields.io/badge/-DIAGRAMAS%20DE%20CONTEXTO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/diagramasDeContexto/README.md)  [![](https://img.shields.io/badge/-PRIORIZADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/priorizarCasosDeUso/CasosDeUsoPriorizados.md)<br> [![](https://img.shields.io/badge/-DETALLADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/detalladoCasosDeUso/README.md) [![](https://img.shields.io/badge/-PROTOTIPADO%20DE%20CASOS%20DE%20USO-white?style=flat&logo=showwcase&logoColor=black)](/documents/casos-de-uso/prototipadoCasosDeUso/README.md) [![](https://img.shields.io/badge/-SESIONES%20DE%20REQUISITADO-white?style=flat&logo=LiveChat&logoColor=black)](/documents/minutas/README.md) [![](https://img.shields.io/badge/-RECURSOS%20ADICIONALES-white?style=flat&logo=openstreetmap&logoColor=black)](/documents/evidencias/README.md)  [![](https://img.shields.io/badge/-GLOSARIO-white?style=flat&logo=gitbook&logoColor=black)](/documents/modelos/Glosario.md) [![](https://img.shields.io/badge/-USO%20DE%20IA-white?style=flat&logo=chatbot&logoColor=black)](/documents/AI-uso.md)

</div>

## Declaración de uso de IA

## Herramientas utilizadas
- Nombres de los modelos/herramientas: Gemini 2.5, Gemini 3, ChatGPT, Claude Sonnet, DeepSeek

## Contexto de uso

### Para modelo del dominio
**¿Se usó?** 
**¿Para qué?** 
**¿Qué se aceptó y qué se rechazó?** 

Si, se ha utilizado. En nuesro caso no hemos utilizado la IA para generar el modelo de dominio desde 0. Esto es porque el modelo de dominio consiste en la representación de la realidad en el contexto operativo del interesado (en nuestro caso, un cliente), por lo que una inteligencia artificial es dificil o prácticamente imposible que entienda esta realidad al completo, de tal forma que solo la comprendemos nosotros ya que somos los que hemos tenido trato con el cliente. Para lo que sí que hemos utilizado la inteligencia artificial es para validar nuestros diagramas. Es decir, le enviábamos a la IA una imagen de nuestro diagrama de entidades (por ejemplo) y le pedíamos que nos describiese la realidad a través de ese diagrama, de tal forma que así nosotros podíamos ver si lo que nos decía la IA era acorde a nuestra idea de la realidad del cliente.

### Para casos de uso
**¿Se usó?** 
**¿Para qué?** 
**¿Qué se aceptó y qué se rechazó?** 

Sí, se ha utilizado. La actividad de la disciplina de requisitos en la que más se ha utilizado la IA es el prototipado de los casos de uso. Es decir, adjuntábamos a la IA el detallado de un caso de uso previamente hecho junto con una explicación de la precondición y postcondición y le pedíamos que nos diese propuestas de su prototipado en Salt basándose en la información adjuntada. Y sobre esa base hacíamos correcciones o mejoras.

### Para documentación
**¿Se usó?** 
**¿Para qué?**

Sí, se ha utilizado. Se ha utilizado para dar forma a los archivos en markdown (tablas, divs), revisar faltas ortográficas y para generar las convenciones internas de trabajo que hemos seguido durante todo el desarrollo del proyecto.

## Validación humana

**¿Cómo validamos lo generado?**

Para el modelo de dominio, comparábamos la interpretación que hacía la IA de los diagramas con nuestras ideas y minutas; si la IA interpretaba algo diferente a lo que el cliente nos dijo, sabíamos que el diagrama podría estar mal modelado.

En cuanto a los prototipos de los casos de uso, la validación consistió en probar el código generado para verificar la interfaz y comprobar que cumplía con el detallado. 

**¿Qué errores detectamos de la IA?**

A veces, la IA infería cosas genéricas que no tenian nada que ver con el contexto específico de nuestro cliente.

Al generar prototipos complejos, a veces cometía errores de sintaxis.

En conversaciones largas, la IA solía a olvidar las normas específicas que definian el contexto del cliente mencionadas al principio, proponiendo soluciones genéricas en lugar de personalizadas.

## Reflexión del equipo

**¿La IA ayudó o entorpeció?**

Ayudó. En muchos casos acelera el flujo de trabajo ya que permite centrarnos en que hay que hacer y no tanto en el cómo. Hubiese entorpecido si hubiéramos confiado al 100% en ella, ya que sus propuestas iniciales casi siempre requerían ajuste.

**¿Qué aprendimos sobre el uso de IA en requisitado?**

Aprendimos que la IA funciona muy bien para validar y para dar forma, pero no para hacerlo todo desde cero. La IA no estuvo en las reuniónes con el cliente, por lo que no entiende la realidad del cliente. Lo que hemos aprendido mayoritariamente es que en un proyecto grande la disciplina de requisitos no la puedes delegar completamente a la IA; es simplemente una especie de asistente que necesita supervisión constante para asegurar que lo que se construye es lo que se busca realmente.