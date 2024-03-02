# Diseño de Incidencias

* Status: accepted
* Deciders: Ángel, Cristian
* Date: 2024-03-02

Technical Story: RF2.3.2

## Context and Problem Statement

Dentro de los pedidos, existen incidencias reportables para comunicar el estado del reparto. Para diseñarlo dentro del servidor, hay que seleccionar la forma de definirlo. ¿Cuál sería la más correcta?

## Decision Drivers

* Las incidencias se dividen en 3 tipos: "Camión averiado", "Demora en la entrega", "Entrega no realizada".
* Las incidencias se relacionan con la clase "Reparto".

## Considered Options

* 0017-1 Crear un enumerado "Incidencias"
* 0017-2 Crear una clase "Incidencias"
* 0017-3 Añadir atributo "Incidencias" a la clase "Reparto"

## Decision Outcome

Chosen option: "0017-1 Crear un enumerado "Incidencias"", because comes out best.

## Pros and Cons of the Options

### 0017-1 Crear un enumerado "Incidencias"

Un enumerado permite la recolección de diferentes estados para un mismo atributo con el fin de definir, uno a la vez, en qué estado se encuentra cierto objeto.

* Good, because Al solo permitir que un reparto tome un único estado a la vez, no habrá superposiciones, lo cual supone menos fallos.
* Good, because El diseño es más simple que el de una clase. Se puede optar por su uso de forma más sencilla por cualquier otra clase.

### 0017-2 Crear una clase "Incidencias"

La clase propia de "Incidencia" tendría su propio atributo que define el estado de un reparto.

* Good, because Se puede operar a través de métodos para hacer de la clase algo más versátil.
* Bad, because El diseño de la clase es pesado y si la adición de las incidencias es simple no tendría sentido incluir una clase.

### 0017-3 Añadir atributo "Incidencias" a la clase "Reparto"

El atributo de "incidencia" definiría el estado de un reparto en un momento concreto. Este estaría directamente implementado en la clase reparto como un "string".

* Good, because El diseño es sencillo y se encuentra dentro de la clase de "Reparto", lo cual causa que la clase de "Reparto" no requiera de accesos a elementos externos.
* Bad, because No es tan flexible a los cambios.
