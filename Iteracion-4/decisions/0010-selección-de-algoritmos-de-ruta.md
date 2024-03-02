# Gestión de selección de algoritmos de ruta

* Status: accepted
* Deciders: Angel, Cristian
* Date: 2024-02-22

Technical Story: RF2.3.1, RF2.3.1.1

## Context and Problem Statement

Para el cálculo de la mejor ruta referido a los repartos, se deben de utilizar 2 algoritmos de ruta que irán variando según su conveniencia. Sin embargo, para saber cuál hay que elegir, se debe diseñar un patrón apto para la tarea. ¿Cuál podría ser?

## Decision Drivers

* Los algoritmos se elegirán en base a cuál dé el menor tiempo.
* La ruta será descartada si esta tiene una demora sobre los 30 minutos.

## Considered Options

* 0010-1 Patrón Strategy
* 0010-2 Strategy con Template Method
* 0010-3 Strategy con Factory Method

## Decision Outcome

Chosen option: "0010-1 Patrón Strategy", because comes out best.

## Pros and Cons of the Options

### 0010-1 Patrón Strategy

Este patrón contiene un gestor para la selección de algoritmos de ruta que según sus diversos criterios, elige el algoritmo que se considere más conveniente.

* Good, because Permite elegir el algoritmo óptimo dependiendo de la situación.
* Good, because Si se llegasen a implementar más algoritmos, no habría que cambiar nada respecto al componente o al sistema anterior de acuerdo a la selección de algoritmos.
* Bad, because Si uno de los algoritmos es predominante, no hay sentido para añadir el patrón, solo complicaría el sistema.
* Bad, because Se debe conocer bien el motivo de cambio de algoritmo para que el patrón sea efectivo.

### 0010-2 Strategy con Template Method

Junto con el diseño del Strategy, se añade el método de plantilla, que consiste en una superclase que define las "pautas" que deben seguir todas sus subclases, aunque estas últimas pueden sobrescribir los pasos del algoritmo sin tocar la estructura del padre.

* Good, because Al tener una plantilla general, los cambios no son tan grandes, haciendo la información entendible y similar, solo que cambian los datos.
* Bad, because A medida que el sistema de selección de algoritmos crece, el Template Method se ve severamente afectado.

### 0010-3 Strategy con Factory Method

Junto al Strategy, se diseña el Factory Method, que crea la responsabilidad y la estrategia de selección en base a la característica de entrada.

* Good, because El proceso de selección de la estrategia se realiza automáticamente
* Good, because Puedes cambiar las estrategias o agregar nuevas estrategias fácilmente sin afectar el resto
* Bad, because Implementar la lógica de selección automática puede aumentar la complejidad
* Bad, because La automatización puede llevar a errores si la lógica de selección no está bien implementada
