---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar ponderaciones para el equilibrador de carga

Las ponderaciones son un sistema de asignación de valores numéricos a los servidores de los que desea recibir más tráfico. Un número mayor representa una prioridad superior mientras el servidor esté en línea según las comprobaciones de estado.  

Por ejemplo, si _server1_ tiene una ponderación de 80 y _server2_ de 20, por cada 10 conexiones, a _server1_ se le asignará 8 y _server2_ obtendrá 2. Si _server1_ se queda fuera de línea o se elimina de la agrupación, todas las conexiones irán a _server2_.

Puede configurar ponderaciones para un servicio concreto cuando se [añada el servicio a un grupo de servicios](add-service-service-group.html) o cuando se [edite el servicio](edit-service-load-balancer.html) después de que se haya creado.

Una vez que se haya guardado la configuración, los cambios entrarán en vigor inmediatamente. Puede supervisar las conexiones del servicio en los detalles para el servicio.
