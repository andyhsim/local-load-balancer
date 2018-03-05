---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Suprimir un servicio 

Una vez que se haya añadido un servicio a un grupo de servicios para un {{site.data.keyword.loadbalancer_short}}, podrá suprimirse en cualquier momento. La supresión de un servicio de un grupo de servicios impide que el servicio lo utilice {{site.data.keyword.loadbalancer_short}}, a menos que se vuelva a añadir manualmente a un grupo de servicios. 

Como alternativa, un servicio puede ser inhabilitado, lo que mantendrá al servicio asociado con el grupo de servicios, lo que a su vez lo convierte en no disponible para los esfuerzos de equilibrio. Para mantener al servicio asociado con el grupo de servicios de {{site.data.keyword.loadbalancer_short}}, [edite el servicio](edit-service-load-balancer.html) y desmarque el recuadro de selección **Habilitado**. 

Siga estos pasos para suprimir el servicio del {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](view-all-load-balancers.html), localice el servicio que desea suprimir y amplíe la flecha en el lado izquierdo.
2. Pulse la 'x' roja al final de la fila del servicio.
3. Pulse **Guardar configuración** en la parte inferior de la página para que se actualicen los valores.

Después de suprimir el servicio, se guardará la configuración y los cambios entrarán en vigor instantáneamente. Si el servicio suprimido es el único asociado con un grupo de servicios, el grupo no podrá realizar ninguna actividad de equilibrio de carga hasta que se añada un nuevo servicio.
