---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Limitaciones conocidas con el equilibrador de carga local
{: #known-limitations-with-local-load-balancer}

Debido a la naturaleza de un equilibrador de carga proxy, el IP de origen de la solicitud del cliente proviene de la IP del equilibrador de carga. Esto afectará los programas estadísticos de registro y a otras aplicaciones que buscan en la IP de origen para obtener información del cliente. IBM© Cloud proporciona una solución para reescribir correctamente las entradas de registro para Apache (Todas las plataformas) e IIS (Windows).

Para acceder a las instrucciones y a los plugins adicionales necesarios, primero debe estar conectado a VPN de IBM Cloud. Una vez conectado, visite la [Página de descargas ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](http://downloads.softlayer.local/loadbalancer/){: new_window} para encontrar los plugins y las instrucciones para {{site.data.keyword.loadbalancer_short}}.

**NOTA:** Debe iniciar la sesión en la VPN de IBM Cloud para acceder al enlace de descarga.
