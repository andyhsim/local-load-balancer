---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Limitaciones conocidas

Debido a la naturaleza de un equilibrador de carga proxy, el IP de origen de la solicitud del cliente proviene de la IP del equilibrador de carga. Esto afectará los programas estadísticos de registro y a otras aplicaciones que buscan en la IP de origen para obtener información del cliente. IBM Cloud proporciona una solución para reescribir correctamente las entradas de registro para Apache (Todas las plataformas) e IIS (Windows).

Para acceder a las instrucciones y a los plugins adicionales necesarios, primero debe estar conectado a [VPN de IBM Cloud](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}. Una vez conectado, visite la [Página de descargas](http://downloads.softlayer.local/loadbalancer/){: new_window} para encontrar los plugins y las instrucciones para {{site.data.keyword.loadbalancer_short}}.
