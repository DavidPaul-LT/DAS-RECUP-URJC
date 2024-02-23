# Selección proveedor de servicios de pasarela de pago

* Status: accepted
* Deciders: Cristian, Ángel
* Date: 2024-02-22

Technical Story: RF2.2.2.1

## Context and Problem Statement

El módulo de Pedidos es el responsable de que los clientes puedan realizar sus pedidos, empleando para ello pasarelas de pago externas al sistema de la compañía. ¿Cuál es la pasarela de pago idónea para procesar los pagos de los clientes?

## Decision Drivers

* Este módulo debe contar una funcionalidad que permita el pago online a los clientes.

## Considered Options

* 0009-1-Emplear Paypal
* 0009-2-Emplear Stripe
* 0009-3-Emplear Amazon Pay

## Decision Outcome

Chosen option: "0009-2-Emplear Stripe", because comes out best.

### Positive Consequences

* Beneficia a la compañía

## Pros and Cons of the Options

### 0009-1-Emplear Paypal

Unido al módulo de Pedidos, en la capa de lógica de negocio, se encontraría ubicado un componente llamado Paypal. Este componente recoge el uso de software ajeno como la API del servicio así como una API Gateway, entre otros componentes que nos son externos.

* Good, because Se consigue desligar las responsabilidades entre las funciones relacionadas con el procesamiento de pagos y el resto del sistema
* Bad, because Una dependencia elevada del componente podría implicar un alto nivel de acoplamiento

### 0009-2-Emplear Stripe

Unido al módulo de Pedidos, en la capa de lógica de negocio, se encontraría ubicado un componente llamado Stripe. Este componente recoge el uso de software ajeno como la API del servicio así como una API Gateway, entre otros componentes que nos son externos.

* Good, because Se consigue desligar las responsabilidades entre las funciones relacionadas con el procesamiento de pagos y el resto del sistema
* Bad, because Una dependencia elevada del componente podría implicar un alto nivel de acoplamiento

### 0009-3-Emplear Amazon Pay

Unido al módulo de Pedidos, en la capa de lógica de negocio, se encontraría ubicado un componente llamado AmazonPay. Este componente recoge el uso de software ajeno como la API del servicio así como una API Gateway, entre otros componentes que nos son externos.

* Good, because Se consigue desligar las responsabilidades entre las funciones relacionadas con el procesamiento de pagos y el resto del sistema
* Bad, because Una dependencia elevada del componente podría implicar un alto nivel de acoplamiento
