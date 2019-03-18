---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar ponderaciones para el equilibrador de carga
{; #configuring-weights-for-the-load-balancer}

Las ponderaciones son un sistema de asignación de valores numéricos a los servidores de los que desea recibir más tráfico. Un número mayor representa una prioridad superior mientras el servidor esté en línea según las comprobaciones de estado.  

Por ejemplo, si _server1_ tiene una ponderación de 80 y _server2_ de 20, por cada 10 conexiones, a _server1_ se le asignará 8 y _server2_ obtendrá 2. Si _server1_ se queda fuera de línea o se elimina de la agrupación, todas las conexiones irán a _server2_.

Puede configurar ponderaciones para un servicio concreto cuando se [añada el servicio a un grupo de servicios](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) o cuando se [edite el servicio](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) después de que se haya creado.

Una vez que se haya guardado la configuración, los cambios entrarán en vigor inmediatamente. Puede supervisar las conexiones del servicio en los detalles para el servicio.
