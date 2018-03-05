---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Editar un grupo de servicios

Después de añadir un grupo de servicios a un {{site.data.keyword.loadbalancer_short}}, sus valores básicos (como el método de equilibrio y el puerto virtual), Asignación de conexiones y Notas, se pueden editar. Las ediciones para cada grupo de servicios son inmediatamente visibles y se pueden realizar ediciones adicionales en cualquier momento. 

Si el tipo de grupo para un grupo de servicios necesita modificarse, el grupo de servicios deberá suprimirse y deberá añadirse un nuevo grupo de servicios que refleje el tipo de grupo deseado. 

Siga estos pasos para editar un grupo de servicios existente para un {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](view-all-load-balancers.html), expanda los detalles del grupo de servicios pulsando el icono Expandir en el lado izquierdo de la fila correspondiente al grupo de servicios que desea editar.
2. Actualice los valores del grupo de servicios:
  - **Método:** Seleccione un [Método de equilibrio](load_balancing_methods.html) en la lista desplegable.
  - **Puerto virtual:** Número de puerto que se utilizará para el grupo de servicios. Consulte las [Preguntas frecuentes de los puertos de servicio comunes](load-balancing-faqs-2.html#what-services-can-be-load-balanced-) para obtener más información. 

  	**Nota:** Cada grupo de servicios debe estar asignado a un puerto exclusivo. Si un puerto exclusivo no está asignado, aparecerá un error en la parte superior de la página y el grupo de servicio puede no añadirse hasta que se asigne un portal virtual exclusivo.

  - **Asignación:** Asignación para el grupo de servicios.
  - **Notas:** Texto de formato libre para identificar el grupo de servicios.
3. Pulse el botón **Guardar configuración** para actualizar el grupo de servicios. Pulse el botón **Cancelar** para cancelar la acción.

Las ediciones en el grupo de servicios se reflejarán en la pantalla Detalles del grupo asociado. Si se ha realizado un cambio en la Asignación de conexiones, puede que sean necesarias ediciones adicionales para otros grupos de servicios. Si se ha realizado un cambio en el método de equilibrio, los servicios asociados con el grupo pueden requerir ediciones adicionales para alinearse con el nuevo método de equilibrio. Se pueden realizar ediciones adicionales al grupo de servicios en cualquier momento repitiendo los pasos anteriores.
