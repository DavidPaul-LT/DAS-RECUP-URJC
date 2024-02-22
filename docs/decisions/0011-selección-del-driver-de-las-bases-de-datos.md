# Selección del driver de las bases de datos

* Status: proposed
* Date: 2024-02-22

Technical Story: RF1

## Context and Problem Statement

Se necesita determinar qué driver se empleará para acceder a las bases de datos de los que se dispone en la arquitectura. ¿Qué Software Gestor de Bases de Datos (SGBD) podemos usar?

## Decision Drivers

* Dado que las dos bases de datos son ambas relacionales, es beneficioso usar el mismo driver para evitar crear una compljidad adicional en la arquitectura

## Considered Options

* 0011-1 MySQL
* 0011-2 PostgreSQL
* 0011-3 SQLite

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0011-1 MySQL

MySQL es un sistema de gestión de bases de datos relacionales ampliamente utilizado en aplicaciones de software. Su función principal es almacenar, organizar y recuperar datos de manera eficiente.

* Good, because MySQL proporciona una interfaz para que el acceso y la modificación de los datos almacenados sea más llevadera
* Good, because MySQL sigue los estándares SQL ANSI, lo que facilita la migración de aplicaciones entre diferentes sistemas de gestión de bases de datos relacionales
