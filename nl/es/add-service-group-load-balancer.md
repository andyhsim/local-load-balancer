---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Añadir un grupo de servicios a un equilibrador de carga
{: #adding-a-service-group-to-a-load-balancer}

Después de que se haya añadido un {{site.data.keyword.loadbalancer_short}}, se puede añadir un nuevo grupo de servicios al {{site.data.keyword.loadbalancer_short}} en cualquier momento. Los grupos de servicios están disponibles en una variedad de tipos de grupos y ofrecen una amplia gama de métodos de equilibrio únicos o híbridos. Al añadir un nuevo grupo de servicios, es importante asegurarse de que la suma de todas las asignaciones de conexión de los grupos es igual al 100 %. Siga los pasos siguientes para añadir un nuevo grupo de servicios a un {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), pulse el botón **Añadir grupo**. Como alternativa, puede pulsar **Acciones > Añadir grupo**. Se añadirá una nueva sección Grupo de servicio a la parte inferior de la página.
2. Seleccione el tipo de grupo deseado de la lista desplegable **Grupo** y seleccione el método de equilibrio deseado desde la lista desplegable **Método**. Consulte los [Métodos de equilibrio de carga](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods) para obtener más información sobre cada método de equilibrio de carga.
3. Especifique el número de puerto que se utilizará para el grupo de servicios en el campo **Puerto virtual**. Consulte las [Preguntas frecuentes de los puertos de servicio comunes](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-) para obtener más información.

	**Nota:** Cada grupo de servicios debe estar asignado a un puerto exclusivo. Si un puerto exclusivo no está asignado, aparecerá un error en la parte superior de la página y el grupo de servicio puede no añadirse hasta que se asigne un portal virtual exclusivo.
4. Especifique una asignación en el campo **Asignación**.
5. Especifique notas en el recuadro de texto de **Notes**, si lo desea.
6. Pulse el botón **Guardar configuración** para añadir el nuevo Grupo de servicios. Pulse **Cancelar** si desea cancelar la acción.

Después de añadir un grupo de servicios, se puede suprimir o editar en cualquier momento. Las conexiones pueden restablecerse en el grupo de servicios y se pueden añadir nuevos servicios al grupo. Para que un grupo de servicios empiece a equilibrar la carga basándose en sus asignaciones de conexión asignadas, debe [añadirse](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) uno o varios servicios al grupo de servicios.

## Qué sucede a continuación
{: #what-happens-next-a}

[Añadir un servicio al grupo de servicios](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group).
