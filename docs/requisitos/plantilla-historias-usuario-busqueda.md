# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Estudiante | Francisco Javier Rodríguez Domínguez |
| Grupo | ISI_7 |
| Fecha | 28/20/2026 |
| Versión | Versión 1.0 |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Una épica expresa una necesidad amplia que se descompone en historias con valor propio.

Como [rol], quiero [capacidad amplia], para [beneficio].

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta. No cuenta como una cuarta historia de la entrega.

## Justificación de la división

[Escribir dos frases que expliquen los resultados útiles que separa la división.]

## US-01

**Título:** Buscar recetas seleccionando los ingredientes

Como usuario registrado, quiero seleccionar los ingredientes
para buscar recetas que los contengan.

**Fuentes:** UR-08; UC-21; FR-086; acta, criterios de búsqueda.

### Criterios de aceptación

- **CA-01.** Dado una selección de ingredientes, cuando busco una receta, entonces aparecerán solamente las que contengan los ingredientes seleccionados.
- **CA-02.** Dado una lista de ingredientes, cuando busco una receta, entonces podré seleccionar esos ingredientes.
- **CA-03.** Dado [situación], cuando [acción], entonces [resultado observable].

## US-02

**Título:** Buscar recetas excluyendo ingredientes

Como usuario registrado, quiero excluir ingredientes, para buscar recetas que no los contengan.

**Fuentes:** UR-08; UC-21; [FR principal]; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado un ingrediente que excluya, cuando busque una receta, entonces no aparecerán recetas que lo contengan.
- **CA-02.** Dado una lista de ingrediente, cuando busco una receta, entonces podré marcarlo para excluirlo.
- **CA-03.** Dado [situación], cuando [acción], entonces [resultado observable].

## US-03

**Título:** Búsqueda por texto

Como usuario registrado, quiero buscar una receta por título o descripción, para encontrar una receta con dicho título o descripción.

**Fuentes:** UR-08; UC-21; [FR principal]; acta, [apartado pertinente].

### Criterios de aceptación

- **CA-01.** Dado un título, cuando busco una receta, entonces aparecerán solamente las recetas con ese mismo título.
- **CA-02.** Dada una descripción, cuando busco una receta, entonces aparecerán solamente las recetas con esa descripción.
- **CA-03.** Dado [situación], cuando [acción], entonces [resultado observable].

## Mejora tras la revisión INVEST

[Indicar la mejora principal y su motivo. Si se mantiene la redacción, justificar una decisión concreta.]

## Dudas pendientes

[Indicar una duda real si queda algún criterio incompleto. Si no hay dudas, escribir «Ninguna».]

## Declaración de uso de IA

No he utilizado IA.
