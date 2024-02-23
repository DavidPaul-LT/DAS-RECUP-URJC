# Especificación de la clase Cliente

* Status: accepted
* Deciders: Ángel y Cristian
* Date: 2024-02-22

Technical Story: RF2.1

## Context and Problem Statement

El módulo interno que faclita el acceso a los datos de los clientes debe ser reforzado añadiendo una lista de atributos. ¿Cómo podemos reflejar en el diagrama estas propiedades?

## Decision Drivers

* Este módulo de clientes consiste en un identificador de cliente, nombre, apellidos, email y teléfono móvil.

## Considered Options

* 0013-1 Agregar a la clase Cliente de la capa de lógica de negocio de la arquitectura estos atributos

## Decision Outcome

Chosen option: "0013-1 Agregar a la clase Cliente de la capa de lógica de negocio los atributos", because Satisface los requerimientos del usuario

### Positive Consequences

* Satisface los requerimientos del usuario

## Pros and Cons of the Options

### 0013-1 Agregar a la clase Cliente de la capa de lógica de negocio de la arquitectura estos atributos

Dentro de la capa de lógica de negocios se añadirá una clase Cliente que se empleará para devolver los datos de los bases de datos concernientes a los clientes. Esta clase se diseñará conteniendo los atributos de identificador de cliente, nombre, apellidos, email y teléfono móvil.

* Good, because Satisface los requerimientos del usuario
