# Selección de patrón de diseño del módulo de comunicación

* Status: proposed
* Date: 2024-02-14

Technical Story: RF2

## Context and Problem Statement

Es necesario escoger el patrón de diseño para el  nuevo componente de intermediación de comunicación contenido en la capa de lógica de negocio. ¿Qué patrón de diseño es el que mejor se adapta a las necesidades del módulo?

## Decision Drivers

* Se ha optado por incorporar un módulo de comunicación en la capa de lógica de negocio

## Considered Options

* 0007-1 Patrón de diseño Mediator
* 0007-2 Patrón de diseño Broker

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0007-1 Patrón de diseño Mediator

El patrón de diseño Mediator se compone de un mediador y los módulos/componentes que se quieren comunicar entre sí. Por un lado, tenemos a un mediador que contiene una interfaz que define las operaciones que emplean los módulos o componenetes que tratan de comunicarse entre sí, así como un elemento que se encarga de implementar la interfaz y proponcionar la lógica necesaria como para manejar las interacciones entre elementos de la capa de lógica de negocio

* Good, because Se evita el acoplamiento directo entre módulos y/o componentes
* Good, because La comunicación indirecta, centralizada en GestorPedidos, cumple con el principio de responsabilidad única haciendo que el componente mediador sea más fácil de mantener.
* Bad, because Un funcionamiento defectuso del módulo podría suponer una pérdida importante de comunicaciones entre componentes

### 0007-2 Patrón de diseño Broker

En el patrón Broker se tiene un componente principal, el broker de comunicaciones, que actua como intermediario entre los módulos/componentes y los servicios que estos proporcionan. El patrón se compondría de una interfaz de servicio común a todos los servicios y una clase Broker que contiene la lógica que permite dirigir las solicitudes de los módulos o componentes a los servicios apropiados

* Good, because Se evita el acoplamiento directo entre módulos y/o componentes
* Bad, because Su implantación supone asumir una complejidad adicional debido a la necesidad de que el componente Broker sea responsable de determinar a qué servicio se dirige una solicitud
