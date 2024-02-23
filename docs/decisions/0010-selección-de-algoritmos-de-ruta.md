# Gestión de selección de algoritmos de ruta

* Status: proposed
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
* 0010-2 Patrón Bridge
* 0010-3 Patrón Command

## Decision Outcome

Chosen option: "", because comes out best.
