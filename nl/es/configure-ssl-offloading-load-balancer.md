---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar la descarga SSL en un equilibrador de carga
{: #configuring-ssl-offloading-on-a-load-balancer}

Los equilibradores de carga tienen la capacidad de proporcionar la descarga SSL, que puede reducir drásticamente la carga en los sistemas que actualmente realizan la función. Para utilizar la descarga SSL, debe comprarse un {{site.data.keyword.loadbalancer_short}} que ofrezca la prestación. Los equilibradores de carga que ofrecen la funcionalidad SSL se anotan “con descarga SSL” en el diálogo **Pedir equilibrador de carga local**. Una vez que se haya suministrado el {{site.data.keyword.loadbalancer_short}} habilitado para la descarga de SSL, debe configurarse. Siga los pasos siguientes para configurar la descarga SSL en un {{site.data.keyword.loadbalancer_short}}.

1. Desde la página [Detalles de equilibradores de carga local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), pulse en **Acciones > Configurar SSL** en el menú desplegable para el equilibrador de carga.
2. Seleccione el certificado SSL deseado desde el recuadro desplegable **Certificado**. Tenga en cuenta lo siguiente:
  - Los IP virtuales (VIP) de {{site.data.keyword.loadbalancer_short}} no dedicados están limitados a un tamaño de bits de certificado SSL máximo de 2048.
  - Debe almacenarse al menos un certificado SSL en el Portal de clientes para completar correctamente este paso. Consulte [Importar un certificado SSL](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-importing-an-ssl-certificate).
3. Seleccione el recuadro de selección **Habilitado**.
4. Seleccione los cifrados que desee soportar.
5. Pulse el botón **Actualizar**.

Tras activar la descarga de SSL en un {{site.data.keyword.loadbalancer_short}}, el estado del SSL cambiará de **disabled** a **active**. La carga transportada por sistemas que previamente han manejado conexiones SSL disminuirá generalmente después de que se haya activado la descarga SSL. En cualquier momento, el estado de descarga SSL puede modificarse. Vuelva al separador Descargar SSL y desmarque el recuadro de selección para inhabilitar la descarga SSL para el {{site.data.keyword.loadbalancer_short}}.
