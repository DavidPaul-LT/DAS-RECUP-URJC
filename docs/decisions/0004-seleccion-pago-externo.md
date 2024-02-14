# Seleccion Pago Externo

* Status: proposed
* Deciders: Ángel
* Date: 2024-02-14

Technical Story: RF2.2.2

## Context and Problem Statement

Se requiere diseñar un método de pagos de forma telemática. ¿Cuál puede ser la mejor decisión?

## Decision Drivers

* El método de pago debe ser online.
* El método de pago debe permitir tantas entidades bancarias como sea posible.

## Considered Options

* Implementar propia pasarela de pago
* Utilizar API de pasarela de pago

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### Implementar propia pasarela de pago

Se realizaría una pasarela de pago propia de la empresa para realizar los pagos de forma telemática.

* Good, because Es un artefacto único y fácilmente entendible y personalizable para la empresa.
* Bad, because Los costos pueden ser altos.
* Bad, because Puede tomar mucho tiempo, atrasando el producto.
* Bad, because Requiere de arduo trabajo para cumplir el fin de permitir tantas entidades bancarias como pueda.

### Utilizar API de pasarela de pago

En vez de crear una pasarela de pago propia, se podría implementar una de terceros que permita realizar los pagos de forma telemática.

* Good, because No hace falta implementarlo.
* Good, because Los costos pueden ser menores.
* Good, because La variedad de permisión de entidades de cuentas bancarias es grande.
* Bad, because No existe control completo de la pasarela.
