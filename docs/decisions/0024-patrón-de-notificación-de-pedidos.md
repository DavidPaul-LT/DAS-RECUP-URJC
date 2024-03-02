# Patrón de Notificación de Pedidos

* Status: accepted
* Deciders: Ángel, Cristian
* Date: 2024-03-02

## Context and Problem Statement

Se deberá de establecer comunicación para que las notificaciones se manden correctamente en caso de que haya una modificación en el pedido del cliente. ¿Qué se puede hacer?

## Decision Drivers

* Se deberá comunicar al cliente cada vez que se realice un cambio en su pedido.
* Los usuarios que hayan realizado un pedido y se encuentren en espera de su entrega serán notificados del estado del pedido.

## Considered Options

* 0024-1 Patrón Observer
* 0024-2 Patrón Observer con Factory Method

## Decision Outcome

Chosen option: "0024-2 Patrón Observer con Factory Method", because comes out best.

## Pros and Cons of the Options

### 0024-1 Patrón Observer

El patrón permite definir un mecanismo de suscripción para notificar a varios objetos de cualquier evento que le suceda al objeto que están observando.

* Good, because En caso de incluir nuevas formas de notificar, no hay por qué cambiar el funcionamiento del patrón.
* Bad, because Los suscriptores son notificados en orden aleatorio, lo que puede suponer un problema si se tarda demasiado en procesar el envío de una notificación o si hay demasiadas peticiones de notificación por enviar.

### 0024-2 Patrón Observer con Factory Method

Además de implementar el Observer, se agrega el Factory Method, que permite crear instancias de los diferentes tipos de medio de comunicación.

* Good, because La separación de responsabilidades es importante ya que el Observer se puede encargar de enfocarse en la lógica de notificación de cambio de estado del sujeto observado.
* Good, because Esta opción se encuentra preparada para otros tipos de comunicación que se añadan ya que no hay que diseñarlos manualmente, el Factory Method se encarga de ello.
* Bad, because Puede suponer una sobrecarga adicional en términos de memoria al suponer clases extra a diseñar.
