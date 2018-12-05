---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Editar un servicio 

Una vez que se haya añadido un servicio a un grupo de servicios de un equilibrador de carga, se puede editar en cualquier momento. Todos los valores básicos de un servicio son elegibles para ediciones, y también se pueden añadir notas adicionales mediante la característica de edición. 

Siga estos pasos para editar un servicio.

1. Desde la página [Detalles de equilibradores de carga local](view-all-load-balancers.html), localice el servicio que desea editar ampliando la flecha a la izquierda.
2. Edite los campos siguientes, según desee:
  - **IP de destino:** La dirección IP del servidor de destino.
  - **Puerto de destino:** El número de puerto a utilizar para direccionar tráfico al servidor de destino.
  - **Comprobación de estado:** El método de comprobación de estado preferido de estas opciones.
      - **Valor predeterminado:** La configuración predeterminada es Ping.
      - **HTTP:** Comprueba desde el puerto 80 en la dirección IP listada y responde con el código HTTP 200 (correcto).
      - **HTTP-CUSTOM:** Muy similar a HTTP normal, excepto que asigna el tipo de conexión, la ubicación de la comprobación de estado y la respuesta que está anticipando. Esta es una opción avanzada.
      - **Ping:** Una prueba de ping sencilla a través de ICMP.
      - **TCP:** Muy similar a una prueba ping, pero explícitamente a través de TCP.  Esta opción debería utilizarse si tiene conexiones ICMP bloqueados.
  - **Ponderación:** La prioridad numérica para el servicio. Las ponderaciones son un sistema de asignación de valores numéricos a los servidores de los que desea recibir más tráfico. Un número mayor representa una prioridad superior mientras el servidor esté en línea según las comprobaciones de estado. Por ejemplo, si _server1_ tiene una ponderación de 80 y _server2_ de 20, por cada 10 conexiones, a _server1_ se le asignará 8 y _server2_ obtendrá 2. Si _server1_ se queda fuera de línea o se elimina de la agrupación, todas las conexiones irán a _server2_.
  - **Notas:** Campo de texto de formato libre.
  - **Habilitado:** Marque o desmarque este recuadro de selección para habilitar o inhabilitar el servicio.
3. Pulse el botón **Guardar configuración** para actualizar el servicio. Pulse **Cancelar** si desea cancelar la acción.

Después de editar un servicio, las ediciones aparecerán en la fila que contiene el servicio en la sección del servicio. Se pueden realizar ediciones adicionales en cualquier momento repitiendo los pasos anteriores.
