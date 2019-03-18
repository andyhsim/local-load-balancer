---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Suprimir un grupo de servicios
{: #deleting-a-service-group}

Al suprimir un grupo de servicios, todos los servicios asociados con el grupo también se suprimirán. Siga estos pasos para suprimir un grupo de servicios para un {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), identifique la fila del grupo de servicios que desea suprimir y pulse **Acciones > Eliminar grupo**.
2. Pulse **Guardar configuración**.

Después de suprimir un grupo de servicios, se eliminará del {{site.data.keyword.loadbalancer_short}}. Todos los servicios asociados también se suprimirán y el puerto virtual asociado con el grupo de servicios estará disponible, en caso de que sea necesario para otro grupo de servicios en el futuro. Tras la supresión, el porcentaje de asignación de conexión para los grupos de servicios restantes debe cambiarse manualmente para los grupos restantes.
