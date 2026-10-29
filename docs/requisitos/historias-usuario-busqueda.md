# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Estudiante | Brais Curra González |
| Grupo | ISI_4 |
| Fecha | 29/10/2026 |
| Versión | Versión 1.0 |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.

## Épica de búsqueda

Una épica expresa una necesidad amplia que se descompone en historias con valor propio.

Como usuario registrado, quiero buscar recetas mediante texto, ingredientes incluidos e ingredientes excluidos, para localizar recetas publicadas y validadas que se ajusten a mis criterios.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta. No cuenta como una cuarta historia de la entrega.

## Justificación de la división

La división separa tres formas de expresar una intención de búsqueda: encontrar recetas por una palabra o frase, exigir determinados ingredientes y descartar ingredientes no deseados. Cada historia produce un resultado útil por sí misma y pueden combinarse para refinar una misma consulta, de acuerdo con UC-21.

## US-01

**Título:** Buscar recetas mediante una palabra o frase

Como usuario registrado, quiero buscar recetas mediante una palabra o frase,
para encontrar recetas cuyo título o descripción breve coincida con mi búsqueda.

**Fuentes:** UR-08; UC-21; FR-085; acta v1.1, apartado 2, «Criterios de búsqueda» y «Búsqueda sin resultados».

### Criterios de aceptación

- **CA-01.** Dada una sesión iniciada y la frase «pollo al horno», cuando el usuario ejecuta la búsqueda, entonces el sistema muestra solo recetas publicadas y validadas cuyo título o descripción breve contiene esa frase seguida y en el mismo orden, sin distinguir mayúsculas ni tildes.
- **CA-02.** Dado que ninguna receta coincide con la palabra o frase introducida, cuando el usuario ejecuta la búsqueda, entonces el sistema informa de que no hay resultados, conserva el texto y muestra separadamente una corrección ortográfica o una alternativa relacionada si dispone de ella.
- **CA-03.** Dado que el usuario no ha indicado ningún criterio, cuando solicita la búsqueda, entonces el sistema solicita al menos un criterio, conserva la búsqueda y no la ejecuta.

### Revisión INVEST

- **Independiente:** produce resultados útiles sin exigir ingredientes incluidos o excluidos.
- **Negociable:** concreta la necesidad de buscar texto, pero deja abierta la interacción y presentación detallada que no fija la historia.
- **Valiosa:** permite localizar recetas a partir de una palabra o frase del título o la descripción.
- **Estimable:** delimita el campo consultado, la normalización de mayúsculas y tildes y el tratamiento de frases.
- **Pequeña:** se limita a la búsqueda textual y a su respuesta inmediata, sin incluir detalle, historial ni otros filtros.
- **Comprobable:** los tres criterios permiten distinguir una coincidencia textual correcta, una búsqueda sin resultados y una solicitud sin criterio.

## US-02

**Título:** Buscar recetas por ingredientes incluidos

Como usuario registrado, quiero seleccionar ingredientes que deseo encontrar,
para obtener recetas que contengan todos esos ingredientes.

**Fuentes:** UR-08; UC-21; FR-086; acta v1.1, apartado 2, «Criterios de búsqueda» y «Resultados y detalle».

### Criterios de aceptación

- **CA-01.** Dada una sesión iniciada y los ingredientes «tomate» y «albahaca» seleccionados, cuando el usuario ejecuta la búsqueda, entonces el sistema muestra solo recetas publicadas y validadas que contienen ambos ingredientes.
- **CA-02.** Dada una selección de ingredientes incluidos, cuando el usuario ejecuta la búsqueda, entonces el sistema muestra los resultados publicados y validados ordenados por fecha de publicación, de más recientes a más antiguos.
- **CA-03.** Dada una selección de ingredientes incluidos que no coincide con ninguna receta publicada y validada, cuando el usuario ejecuta la búsqueda, entonces el sistema informa de que no hay resultados y conserva los ingredientes seleccionados para poder modificarlos.

### Revisión INVEST

- **Independiente:** permite obtener recetas usando únicamente ingredientes incluidos.
- **Negociable:** fija que deben cumplirse todos los ingredientes, pero no impone una interacción concreta para seleccionar o retirar elementos.
- **Valiosa:** reduce los resultados a recetas que contienen todos los ingredientes que el usuario necesita encontrar.
- **Estimable:** define la selección de ingredientes, la condición de coincidencia, el estado de las recetas y la respuesta cuando no hay resultados.
- **Pequeña:** cubre la inclusión de ingredientes y su validación, sin incorporar texto, detalle ni filtros fuera del alcance de la acta.
- **Comprobable:** los tres criterios permiten comprobar la inclusión de todos los ingredientes, el orden de los resultados y la respuesta ante una búsqueda sin resultados.

## US-03

**Título:** Buscar recetas excluyendo ingredientes

Como usuario registrado, quiero seleccionar ingredientes que deseo excluir,
para obtener recetas que no contengan ninguno de ellos.

**Fuentes:** UR-08; UC-21; FR-087; acta v1.1, apartado 2, «Criterios de búsqueda» y «Búsqueda sin resultados».

### Criterios de aceptación

- **CA-01.** Dada una sesión iniciada y los ingredientes «cacahuete» y «nueces» seleccionados para excluirlos, cuando el usuario ejecuta la búsqueda, entonces el sistema muestra solo recetas publicadas y validadas que no contienen cacahuete ni nueces.
- **CA-02.** Dado que «cacahuete» está seleccionado como ingrediente excluido, cuando el usuario ejecuta la búsqueda, entonces cada resultado publicado y validado no contiene cacahuete.
- **CA-03.** Dado que el ingrediente «cacahuete» está seleccionado simultáneamente para incluirlo y excluirlo, cuando el usuario solicita ejecutar la búsqueda, entonces el sistema señala el conflicto, no ejecuta la búsqueda y permite corregir la selección.

### Revisión INVEST

- **Independiente:** produce un conjunto útil de recetas sin ingredientes no deseados, aunque se combine con otros criterios.
- **Negociable:** mantiene la regla de exclusión, pero no prescribe cómo se presenta la lista ni las alternativas ofrecidas.
- **Valiosa:** ayuda a evitar recetas con ingredientes que el usuario no desea.
- **Estimable:** delimita la selección de exclusiones, la respuesta ante un conflicto y la conservación de exclusiones en las sugerencias.
- **Pequeña:** se centra en excluir ingredientes y en su interacción directa con la consulta, sin abarcar alergias automáticas, historial ni recomendaciones.
- **Comprobable:** los tres criterios permiten distinguir la exclusión de un ingrediente, la respuesta ante un conflicto y la conservación de exclusiones en las sugerencias.

## Revisión INVEST

| Comprobación | ¿Se ha aplicado? | ¿Cumple? | Justificación |
| --- | --- | --- | --- |
| Independiente | Sí | Sí | US-01 ofrece búsquedas por texto, US-02 ofrece búsquedas por ingredientes incluidos y US-03 ofrece búsquedas por ingredientes excluidos. Cada historia produce resultados útiles sin requerir que se implementen las otras dos, aunque pueden compartir infraestructura. |
| Negociable | Sí | Sí | Las tres historias expresan la necesidad y el beneficio para la persona usuaria, dejan margen para decidir la solución y respetan los acuerdos confirmados del acta v1.1. |
| Valiosa | Sí | Sí | Cada historia aporta un beneficio concreto: localizar por texto, encontrar recetas que contengan todos los ingredientes seleccionados o evitar recetas que contengan cualquiera de los ingredientes excluidos. |
| Estimable | Sí | Sí | El alcance, las fuentes, los criterios de aceptación y los resultados esperados están delimitados para cada historia, sin incluir capacidades ajenas como otros filtros, historial o recomendaciones. |
| Pequeña | Sí | Sí | Cada historia se centra en una única capacidad de búsqueda y sus resultados: texto, inclusión de ingredientes o exclusión de ingredientes. La combinación de criterios se mantiene como comportamiento del caso de uso, no como una historia adicional. |
| Comprobable | Sí | Sí | Cada historia tiene tres criterios con estructura Dado-Cuando-Entonces y datos concretos. Permiten verificar la coincidencia textual, la inclusión de todos los ingredientes, la exclusión de cualquiera de los seleccionados, el conflicto y la respuesta sin resultados. |

## Mejora tras la revisión INVEST

La revisión INVEST ha separado las tres intenciones en historias con valor propio, ha sustituido criterios genéricos por resultados observables y ha limitado el alcance a las concreciones aprobadas en el acta v1.1. La combinación de criterios se mantiene como comportamiento transversal de UC-21, sin convertirla en una cuarta historia.

## Dudas pendientes

Ninguna para el alcance aprobado de L06. Quedan fuera los demás filtros, las recomendaciones, el historial, los favoritos, las acciones sobre la receta y la aplicación automática de alergias o intolerancias del perfil.

## Declaración de uso de IA

No he utilizado IA.
