# Selección Tipo Base de Datos

* Status: accepted
* Deciders: Angel
* Date: 2024-02-14

Technical Story: RF1

## Context and Problem Statement

En la arquitectura, se tiene planteada la existencia de 2 bases de datos a las que el sistema podrá acceder para guardar u obtener datos. ¿Qué tipo de base de datos debería de tener la arquitectura?

## Decision Drivers

* En el acceso a los datos, habrá dos bases de datos. Una gestiona los datos de los usuarios, la otra gestiona los pedidos.

## Considered Options

* Base de datos SQL
* Base de datos NoSQL

## Decision Outcome

Chosen option: "Base de datos SQL", because comes out best.

### Positive Consequences

* Los datos estarán ordenados y será más fácil encontrarlos.

### Negative Consequences

* Los tiempos de recuperación de datos se verán aumentados, haciendo de esta acción algo más lento.

## Pros and Cons of the Options

### Base de datos SQL

Siendo una base de datos relacional y ordenada de SQL (Structured Query Language), esto permitirá acceder a los datos de forma sencilla.

* Good, because Los datos se ordenan de forma específica.
* Good, because La recuperación de datos es más eficaz y rápida.
* Bad, because El control otorgado a la base de datos no es completo.
* Bad, because Puede ser complicado de implementar debido a su complejidad.

### Base de datos NoSQL

Este tipo de base de datos no utilizan el Structured Query Language, haciendo de ellas bases de datos no relacionales.

* Good, because La implementación es menos costosa en términos de tiempo.
* Bad, because Los datos se encuentran desordenados, haciendo de la recuperación de ellos algo más complicado y tardado.
* Bad, because Son incompatibles con bases SQL, que son estandarizadas y más frecuentes.
