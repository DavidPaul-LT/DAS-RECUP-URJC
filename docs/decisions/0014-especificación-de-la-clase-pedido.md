# Especificación de la clase Pedido

* Status: superseded
* Deciders: Ángel y Cristian
* Date: 2024-02-22

Technical Story: RF2.2

## Context and Problem Statement

El módulo interno que permite realizar pedidos, debe contar con la característica de poder realizar un pedido hasta 3 veces. ¿Cómo podemos reflejar en el diagrama estas propiedades?

## Decision Drivers

* Este módulo permite a los clientes realizar pedidos de los productos de la empresa
* Se debe poder realizar un pedido hasta 3 veces

## Considered Options

* 0014-1 Agregar a la clase Pedido contenida en la capa de lógica de negocio las características

## Decision Outcome

Chosen option: "0014-1 Agregar a la clase Pedido contenida en la capa de lógica de negocio las características", because Satisface los requerimientos del usuario

### Positive Consequences

* Satisface los requerimientos del usuario

## Pros and Cons of the Options

### 0014-1 Agregar a la clase Pedido contenida en la capa de lógica de negocio las características

La clase obtiene los atributos "lim_pedidos", "info_cliente", "info_pedido", "coste_total", "coste_individual_productos" y "direccion_envio". También tendrá los métodos "calcularCostePedido", "mostrarPedido", "realizarPago", "cancelarPedido".

* Good, because Satisface los requerimientos del usuario
