# Especificación Del Módulo Estadísticas

* Status: accepted
* Deciders: Ángel, Cristian
* Date: 2024-03-02

Technical Story: RF2.4

## Context and Problem Statement

El módulo interno que facilita las estadísticas debe ser diseñado. ¿Cómo podemos reflejar en el diagrama esta característica?

## Decision Drivers

* El módulo de estadísticas cuenta con información valiosa referida a los pedidos y la situación a tiempo real de los camiones, aparte de la información del usuario, tiempo estimado de entrega, e información del camión de reparto.

## Considered Options

* 0020-1 Crear una clase "Estadistica" conectada a un componente externo
* 0020-2 Crear una clase "Estadística" que gestione los datos personalmente

## Decision Outcome

Chosen option: "0020-1 Crear una clase "Estadistica" conectada a un componente externo", because comes out best.

## Pros and Cons of the Options

### 0020-1 Crear una clase "Estadistica" conectada a un componente externo

Se diseñará una clase de nombre "Estadística" con los atributos "info_usuario", "tiempo_entrega", "info_camion", y los métodos "mostrarInfo" y "crearInforme". Adicionalmente, los datos son obtenidos a partir de un componente de cálculo de estadísticas externo.

### 0020-2 Crear una clase "Estadística" que gestione los datos personalmente

Se diseñará una clase de nombre "Estadística" con los atributos "info_usuario", "tiempo_entrega", "info_camion", y los métodos "mostrarInfo" y "crearInforme". Las estadísticas se gestionan de manera privada dentro de la clase.
