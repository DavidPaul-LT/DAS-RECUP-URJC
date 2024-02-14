# Selección Acceso Servidor

* Status: proposed
* Deciders: Angel
* Date: 2024-02-14

Technical Story: RF1

## Context and Problem Statement

Para entrar al servidor, se requiere de un acceso que conecte la capa del cliente con la capa de la lógica de negocio. ¿Qué tipo de conexión es la mejor?

## Decision Drivers

* Habrá clientes tanto de ordenador como de móvil.
* La lógica de negocio contiene microservicios.

## Considered Options

* API Gateway Centralizado
* API Gateway Distribuido

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### API Gateway Centralizado

Actuando de manera similar a un proxy inverso, este gestor de llamadas API recupera recursos desde el lado del servidor.

* Good, because Al ser centralizado, todas las peticiones y accesos a microservicios pasan por el mismo Gateway.
* Bad, because Un gran tráfico en el servicio del negocio puede llevar a que este Gateway se caiga, requiriendo especial cuidado.

### API Gateway Distribuido

A diferencia del API Gateway centralizado, este usa de más Gateways para garantizar acceso a recursos de manera segura e independiente.

* Good, because El orden de peticiones es mejor, haciendo de la recuperación de datos de parte del servidor más ordenado.
* Bad, because La cantidad de Gateways que se requiere implementar son muchos, lo que puede ser costoso e ineficiente.
