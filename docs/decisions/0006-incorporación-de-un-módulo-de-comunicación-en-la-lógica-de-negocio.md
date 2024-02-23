# Incorporación de un método de comunicación en la lógica de negocio

* Status: superseded
* Deciders: Cristian
* Date: 2024-02-23

Technical Story: RF2

## Context and Problem Statement

La arquitectura eventualmente se compondrá de numerosos módulos y/o componentes que necesitan comunicarse entre ellos para intercambiar información. ¿Cómo podrían esos módulos y/o componentes contenidos en la lógica de negocio comunicarse entre sí?

## Decision Drivers

* La lógica de negocio cuenta con varios clases: pedidos, reparto, y estadísticas
* La arquitectura debe contar con los elementos necesarios como para ejecutar los microservicios
* La clase de estadísticas recopila información de pedidos y del reparto. No existe otro tipo de comunicación entre las clases.

## Considered Options

* 0006-1-Crear un módulo que centralice la comunicación entre otros elementos de la lógica de negocio
* 0006-2 Conectar las clases entre sí de forma directa

## Decision Outcome

Chosen option: "0006-2 Conectar las clases entre sí de forma directa", because comes out best.

### Positive Consequences

* La asociación es simple y no requiere de módulos extra.

### Negative Consequences

* Solo permite conexiones de formas básicas. Para operaciones más complejas se requerirá diseñar un módulo apto para esas comunicaciones.

## Pros and Cons of the Options

### 0006-1-Crear un módulo que centralice la comunicación entre otros elementos de la lógica de negocio

Se creará un componente específico para desempeñar la intermediación de mensajes/comunicaciones entre componentes y/o módulos de la lógica de negocio

* Good, because Se consigue un desacoplamiento de la necesidad de comunicación entre los componentes, pasa ahora a ser responsabilidad del nuevo módulo
* Good, because Se dota de una mayor flexibilidad a la comunicación, dado que se permite al resto de elementos de la arquitectura funcionar de manera independiente y responder a estos mensajes en el momento adecuado
* Bad, because Mayor exposición a un riesgo de cuello de botella

### 0006-2 Conectar las clases entre sí de forma directa

En lugar de emplear un módulo centralizado, se opta por asignar la responsabilidad de poder comunicarse con otros elementos a cada módulo o componente integrado en la lógica de negocio

* Good, because Se permite un mayor nivel de detalle.
* Bad, because La complejidad del sistema aumentaría a medida que cada módulo se tenga que preocupar de conocer los detalles de la comunicación de los otros elementos de la arquitectura
