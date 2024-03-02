# Especificación De La Clase Rutas

* Status: accepted
* Deciders: Ángel, Cristian
* Date: 2024-03-02

Technical Story: RF2.3

## Context and Problem Statement

El módulo interno que facilita las rutas debe ser reforzado añadiendo una lista de atributos. ¿Cómo podemos reflejar en el diagrama estas propiedades?

## Decision Drivers

* La gestión de rutas cuenta con 2 algoritmos de optimización que se aplicarán de acuerdo a unos criterios internos en función a la demora del camión.

## Considered Options

* 0019-1 Agregar a la clase Rutas de la capa de lógica de negocio de la arquitectura estos atributos

## Decision Outcome

Chosen option: "0019-1 Agregar a la clase Rutas de la capa de lógica de negocio de la arquitectura estos atributos", because comes out best.

## Pros and Cons of the Options

### 0019-1 Agregar a la clase Rutas de la capa de lógica de negocio de la arquitectura estos atributos

La clase de Rutas tendrá los atributos "ruta_elegida" e "demora", y el método "seleccionarRuta"
