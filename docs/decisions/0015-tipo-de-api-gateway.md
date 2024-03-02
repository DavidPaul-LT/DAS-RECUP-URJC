# Tipo de API Gateway

* Status: accepted
* Deciders: Angel, Cristian
* Date: 2024-02-23

Technical Story: RF1

## Context and Problem Statement

Tras haber diseñado el tipo de conexión al servidor, es momento de decidir sobre el componente de dónde se va a obtener ese acceso (Es decir, qué servicio externo vamos a utilizar). ¿Cuál sería el más conveniente?

## Decision Drivers

* Se debe poder acceder a la lógica de negocio desde la capa cliente.

## Considered Options

* 0015-1 Amazon API Gateway Versión 4
* 0015-2 NGINX API Gateway Versión 1.32.0
* 0015-3 Kong API Gateway Versión 3.6

## Decision Outcome

Chosen option: "0015-1 Amazon API Gateway Versión 4", because comes out best.

## Pros and Cons of the Options

### 0015-1 Amazon API Gateway Versión 4

El componente API Gateway será tomado de forma externa por parte del ofrecido por Amazon Services. Este API Gateway irá entre la capa de cliente y la capa de lógica de negocio, sirviendo así como un puente de establecimiento de conexión.

* Good, because Ofrece ambos tipos de Gateways, tanto HTTP como REST.

### 0015-2 NGINX API Gateway Versión 1.32.0

El componente API Gateway será tomado de forma externa por parte del ofrecido por NGINX. Este API Gateway irá entre la capa de cliente y la capa de lógica de negocio, sirviendo así como un puente de establecimiento de conexión.

* Good, because Este API Gateway ofrece una experiencia sincrónica a base de enrutar todas las solicitudes a sus servicios correspondientes.

### 0015-3 Kong API Gateway Versión 3.6

El componente API Gateway será tomado de forma externa por parte del ofrecido por Kong. Este API Gateway irá entre la capa de cliente y la capa de lógica de negocio, sirviendo así como un puente de establecimiento de conexión.

* Good, because Esta herramienta es compatible con plugins configurables para recopilar datos.
* Bad, because Ofrece únicamente un API REST.
