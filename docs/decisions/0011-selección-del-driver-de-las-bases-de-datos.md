# Selección del driver de las bases de datos

* Status: accepted
* Deciders: Angel, Cristian
* Date: 2024-02-22

Technical Story: RF1

## Context and Problem Statement

Se necesita determinar qué driver se empleará para acceder a las bases de datos de los que se dispone en la arquitectura. ¿Qué Software Gestor de Bases de Datos (SGBD) podemos usar?

## Decision Drivers

* Dado que las dos bases de datos son ambas relacionales, es beneficioso usar el mismo driver para evitar crear una complejidad adicional en la arquitectura

## Considered Options

* 0011-1 MySQL
* 0011-2 PostgreSQL
* 0011-3 SQLite

## Decision Outcome

Chosen option: "0011-1 MySQL", because comes out best.

### Positive Consequences

* Beneficia a la compañía

## Pros and Cons of the Options

### 0011-1 MySQL

En la capa de lógica de negocio, se diseñará un componente MySQLDriver que sirve como driver a las bases de datos relacionales. Este componente permite el establecimiento la conexión entre las bases de datos empleadas y los componentes o módulos que requieran de hacer consultas o manipular las mismas.

* Good, because MySQL proporciona una interfaz para que el acceso y la modificación de los datos almacenados sea más llevadera
* Good, because MySQL sigue los estándares SQL ANSI, lo que facilita la migración de aplicaciones entre diferentes sistemas de gestión de bases de datos relacionales

### 0011-2 PostgreSQL

En la capa de acceso a datos, se añadirá un componente PostgreSQLDriver que sirve como driver a las bases de datos relacionales. Este componente permite el establecimiento la conexión entre las bases de datos empleadas y los componentes o módulos que requieran de hacer consultas o manipular las mismas.

* Good, because Es compatible con los estándares SQL

### 0011-3 SQLite

En la capa de acceso a datos, se añadirá un componente SQLiteDriver que sirve como driver a las bases de datos relacionales. Este componente permite el establecimiento la conexión entre las bases de datos empleadas y los componentes o módulos que requieran de hacer consultas o manipular las mismas.

* Good, because No requiere un servidor de bases de datos separado
