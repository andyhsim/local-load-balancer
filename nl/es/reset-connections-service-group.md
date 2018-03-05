---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Restablecer conexiones para un grupo de servicios

Cuando un grupo de servicios está activo en un equilibrador de carga, puede existir una conexión para cada servicio asociado con ese grupo basándose en cómo utilizan los clientes el servicio. A veces, los clientes pueden estar conectados a uno o varios servicios durante una cantidad inapropiada de tiempo. Puesto que las conexiones se consideran un recurso limitado, puede ser necesario restablecer manualmente las conexiones para un grupo de servicios para asegurarse de que otros clientes tengan la oportunidad de utilizar el equilibrador de carga. Siga los pasos siguientes para restablecer las conexiones para un equilibrador de carga.

1. Desde la página [Detalles de equilibradores de carga local](view-all-load-balancers.html), identifique la fila del grupo de servicios en la que desearía restablecer las conexiones y pulse **Acciones > Restablecer conexiones**.
2. Confirme la acción pulsando **Sí**. Seleccione **No** para cancelar la acción.

Después de solicitar que todas las conexiones activas se restablezcan, el grupo de servicios descartará las conexiones activas para cada servicio. Un recuadro de texto verde aparecerá en la parte superior de la pantalla después de que las conexiones se hayan restablecido para confirmar el éxito de la acción. Cuando se descarten las conexiones, los clientes podrán volver a conectarse como sea necesario. 

Puede repetir los pasos anteriores para restablecer las conexiones para el grupo de servicios en cualquier momento.
