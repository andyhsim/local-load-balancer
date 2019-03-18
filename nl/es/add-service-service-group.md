---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Añadir un servicio a un grupo de servicios
{: #adding-a-service-to-a-service-group}

Después de que se haya añadido un grupo de servicios a un {{site.data.keyword.loadbalancer_short}}, se pueden añadir servicios para empezar el proceso de equilibrio. Pueden añadirse varios servicios a un grupo de servicios y pueden ser ponderados para permitir la priorización sobre cómo cada dispositivo debe recibir la carga de trabajo en cualquier momento. Siga los pasos siguientes para añadir un nuevo servicio a un grupo de servicio para un {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), pulse **Acciones > Añadir servicio** en el menú desplegable en la fila correspondiente al grupo de servicios donde desea añadir un servicio. Como alternativa, expanda los detalles del grupo pulsando sobre el icono de expandir en el lado izquierdo de la fila y pulse el botón **Añadir servicio**. Se añadirá una nueva sección de servicio al final de la sección de detalles de grupo de servicio.
2. Especifique los parámetros de servicio:
  - **IP de destino:** La dirección IP del servidor de destino.
  - **Puerto de destino:** El número de puerto a utilizar para direccionar tráfico al servidor de destino.
  - **Comprobación de estado:** El método de comprobación de estado preferido de estas opciones.

     - **Valor predeterminado:** La configuración predeterminada es Ping.
     - **HTTP:** Comprueba si el puerto 80 en la dirección IP listada responde con el código HTTP 200 (correcto).
     - **HTTP-CUSTOM:** Muy similar a HTTP normal, excepto que asigna el tipo de conexión, la ubicación de la comprobación de estado y la respuesta que está anticipando. Esta es una opción avanzada.
     - **Ping:** Una prueba de ping sencilla a través de ICMP.
     - **TCP:** Muy similar a una prueba ping, pero explícitamente a través de TCP. Esta opción debería utilizarse si tiene conexiones ICMP bloqueados.
  - **Ponderación:** La prioridad numérica para el servicio. Las ponderaciones son un sistema de asignación de valores numéricos a los servidores de los que desea recibir más tráfico. Un número mayor representa una prioridad superior mientras el servidor esté en línea según las comprobaciones de estado. Por ejemplo, si _server1_ tiene una ponderación de 80 y _server2_ de 20, por cada 10 conexiones, a _server1_ se le asignará 8 y _server2_ obtendrá 2. Si _server1_ se queda fuera de línea o se elimina de la agrupación, todas las conexiones irán a _server2_.
  - **Notas:** Campo para notas.
3. Seleccione el recuadro de selección **Habilitado** para habilitar el servicio.
4. Pulse el botón **Guardar configuración** para añadir el servicio. Pulse **Cancelar** si desea cancelar la acción.

Después de añadir un servicio a un grupo de servicio, aparecerá en la cuadrícula Servicios para el grupo. Si se ha habilitado, comenzará a ayudar en los esfuerzos del equilibrio de carga basados en la ponderación proporcionada cuando se añadió el servicio. Si está inhabilitada, seguirá apareciendo en el grupo de servicios, pero no ayudará en el equilibrio hasta que se haya activado. Las comprobaciones de estado se realizarán en el servicio en intervalos y su estado se reflejará como up o down, basándose en el resultado de la comprobación de estado. Los servicios pueden editarse o suprimirse en cualquier momento y las comprobaciones de estado personalizadas de HTTP pueden añadirse a cualquier servicio existente mediante el menú desplegable Acciones.
