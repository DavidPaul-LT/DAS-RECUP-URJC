# Especificación De La Clase Reparto

* Status: accepted
* Deciders: Ángel, Cristian
* Date: 2024-03-02

Technical Story: RF2.3

## Context and Problem Statement

El módulo interno que facilita los repartos debe ser reforzado añadiendo una lista de atributos. ¿Cómo podemos reflejar en el diagrama estas propiedades?

## Decision Drivers

* Operará con los repartos de las flotas de transporte a los usuarios.
* Las incidencias relacionadas a los repartos se deberán de reportar.

## Considered Options

* 0018-1 Agregar a la clase Reparto de la capa de lógica de negocio de la arquitectura estos atributos

## Decision Outcome

Chosen option: "0018-1 Agregar a la clase Reparto de la capa de lógica de negocio de la arquitectura estos atributos", because comes out best.

## Pros and Cons of the Options

### 0018-1 Agregar a la clase Reparto de la capa de lógica de negocio de la arquitectura estos atributos

La clase de Reparto tendrá los atributos "incidencia", "info_reparto", "ruta_escogida", "transportes", y los métodos "cambiarEstadoReparto", "enviarNotificacionReparto", "mostrarRutaActual" y "seleccionarTransporte"
