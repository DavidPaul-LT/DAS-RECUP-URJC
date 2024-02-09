# Selección-Estilo-Arquitectura

* Status: accepted
* Deciders: Cristian, Ángel
* Date: 2024-02-09

Technical Story: RF1

## Context and Problem Statement

Hay que establecer un estilo arquitectónico para el sistema de la compañía. Dado que se quiere transformar la arquitectura monolítica de la compañía, el objetivo de esta decisión es elegir entre los modelos arquitectónicos existentes cuál es la mejor opción.

## Decision Drivers

* Necesidad de cambiar a arquitectura que soporte microservicios
* Necesidad de la existencia de una capa de acceso a datos que guarde datos de la compañía, así como de sus usuarios
* Necesidad de la existencia de una capa de lógica de negocio que sirva para interconectar los distintos módulos y componentes que conforman el servidor

## Considered Options

* 0001-1-Arquitectura-Cliente-Servidor-tres-capas
* 0001-2-Arquitectura-Cliente-Servidor-dos-capas

## Decision Outcome

Chosen option: "0001-1-Arquitectura-Cliente-Servidor-tres-capas", because ofrece más ventajas en comparación con la otra aproximación arquitectónica

### Positive Consequences

* Los fallos en las bases de datos no afectan el funcionamiento del servidor

## Pros and Cons of the Options

### 0001-1-Arquitectura-Cliente-Servidor-tres-capas

El sistema se repartirá en microservicios y empleará la arquitectura Cliente - Servidor, bajo la cual, un componente intermediador (segunda capa, lógica de negocio) se encargará de procesar las peticiones de los componentes cliente (primera capa). La arquitectura contará con una tercera capa que gestiona el acceso a las bases de datos.

* Good, because Separar la capa de lógica de negocio de las bases de datos facilita una independencia que permite una gestión más sencilla y específica de las diferentes secciones de la aplicación.

### 0001-2-Arquitectura-Cliente-Servidor-dos-capas

Las capas de lógica de negocio y las bases de datos se unificarían en una sola capa

* Good, because Conserva gran parte de las ventajas expuestas anteriormente de arquitecturas C/S mientras mantiene las bases de datos accesibles más fácilmente.
* Good, because A diferencia del C/S de 3 capas, tiene una arquitectura más unificada y compacta.
* Bad, because Una caída de la capa de lógica de negocio, ya sea por parte de las bases de datos o por algún módulo interno, puede suponer varios problemas.
