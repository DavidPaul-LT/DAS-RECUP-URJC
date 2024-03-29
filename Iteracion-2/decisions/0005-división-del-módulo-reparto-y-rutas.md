# División del módulo reparto y rutas

* Status: accepted
* Deciders: Cristian
* Date: 2024-02-14

Technical Story: RF2

## Context and Problem Statement

Al módulo de reparto y rutas se le exige gestionar el reparto de las flotas de transporte a los clientes y las rutas de los camiones. Sumado a todo esto, se le añaden responsabilidades extra como la de reportar las posibles incidencias que se den en los repartos y la de notificar a los clientes el estado del reparto de su pedido. ¿Es necesario desacoplar las funcionalidades de este módulo en varios módulos que soporten funcionalidades concretas?

## Decision Drivers

* El módulo de reparto y rutas es crítico

## Considered Options

* 0005-1-Dividir el módulo en dos módulos
* 0005-2 Mantener la funcionalidad actual del módulo de Reparto y rutas

## Decision Outcome

Chosen option: "0005-1-Dividir el módulo en dos módulos", because comes out best.

### Positive Consequences

* Al estar divididos, es más fácil realizar un seguimiento de la actividad de cada módulo.
* El sistema se vuelve más simple con el módulo separado.

### Negative Consequences

* Puede suponer una carga mayor para el servidor.
* Es probable que requiera compatibilidad para los módulos que sostengan una comunicación con cualquiera de los módulos de esta partición.

## Pros and Cons of the Options

### 0005-1-Dividir el módulo en dos módulos

Se dividirá el módulo de Reparto y Rutas en dos módulo, uno de Repartos y otro de Rutas. El primero de ellos se encargará de la gestión de las flotas así como de la comunicación de incedentes. Por otro lado, el módulo de Rutas, se encargará de la selección del algoritmo de optimización de rutas que siguen los camiones que se encuentren repartiendo.

* Good, because Se separa la responsabilidad única que se tenía hasta el momento
* Good, because Se promueve la encapsulación, dando lugar a una mayor claridad y simplicidad en el diseño de la arquitectura
* Bad, because Es posible que la división del componente traiga consigo una complejidad adicional en el diseño y desarrollo del sistema

### 0005-2 Mantener la funcionalidad actual del módulo de Reparto y rutas

Las responsabilidades del módulo actual no son lo suficientemente grandes como para requerir que el módulo existente se tenga que dividir en varios módulos

* Bad, because La concentración de carga de trabajo en un solo módulo convierte a este en un punto vulnerable frente a fallas del sistema
