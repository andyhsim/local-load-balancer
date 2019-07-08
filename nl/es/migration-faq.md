---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud, faq, support

subcollection: local-load-balancer

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}
{:faq: data-hd-content-type='faq'}

# Preguntas frecuentes (FAQ) para la migración de IBM Cloud Load Balancer
{: #migration-faq}

Las siguientes preguntas frecuentes se aplican al proceso de migración de IBM Local Load Balancer.

## ¿Cuál es la fecha de anuncio y la fecha efectiva de fin de comercialización (EOM) de Local Load Balancer?
{: faq}

La fecha de anuncio de EOM es el 1 de marzo de 2019 y la fecha efectiva es el 1 de junio de 2019. No se podrán producir nuevas ventas después de esta fecha.

## ¿Habrá soporte disponible después del EOM?
{: faq}

Sí, los clientes existentes de Local Load Balancer dispondrán de soporte.

## ¿Cómo puedo empezar a trabajar con IBM Cloud Load Balancer?
{: faq}

Recomendamos empezar por leer la [documentación de IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started).

## ¿Habrá un método de migración para pasar del servicio Local Load Balancer a IBM Cloud Load Balancer?
{: faq}

No habrá ningún método de migración automatizado. No obstante, puede solicitar que se desactive su servicio Local Load Balancer y pedir el servicio Cloud Load Balancer en la consola de IBM Cloud.

## ¿Qué diferencia hay entre Local Load Balancer y Cloud Load Balancer?
{: faq}

Local Load Balancer es un servicio de equilibrio de carga local basado en hardware, mientras que IBM Cloud Load Balancer es un servicio nativo en la nube que ofrece una solución de equilibrio de carga rentable y escalable automáticamente con soporte tanto para redes públicas como privadas.

## ¿Cloud Load Balancer utiliza la misma terminología que Local Load Balancer?
{: faq}

En algunos casos no. En la tabla siguiente se comparan los términos clave de Local Load Balancer con los términos correspondientes en Cloud Load Balancer cuando son diferentes.

| Término en Local Load Balancer  | Término en Cloud Load Balancer |
| ------------- | ------------- |
| Grupos de servicios | Protocolos |
| Servicio | Instancias de servidor |
| VIP | FQDN |

## ¿Seguiré teniendo una sola dirección IP fija para mi equilibrador de carga cuando migre a Cloud Load Balancer?
{: faq}

Las IP para IBM Cloud Load Balancer no son fijas. Cloud Load Balancer asigna instancias de equilibrador de carga desde una agrupación, lo que requiere en todo momento un nombre de dominio completo (FQDN). En consecuencia, la dirección IP individual de un Cloud Load Balancer puede cambiar.

## ¿IBM Cloud Load Balancer está disponible para soluciones de VSI Públicas/Privadas y nativas?
{: faq}

Sí, Cloud Load Balancer está disponible para VSI públicas y privadas, así como nativas.

## ¿IBM Cloud Load Balancer es compatible con GDPR?
{: faq}

Sí, la oferta de Cloud Load Balancer es compatible con GDPR.

## Tras empezar la migración, ¿cuánto tiempo de inactividad o interrupción de tráfico puedo esperar con mi sistema?

No experimentará ningún tiempo de inactividad ni interrupción de tráfico como resultado de la migración del equilibrador de carga. El único tiempo de inactividad o interrupción de tráfico que puede encontrar es en el momento de actualizar la configuración de Local Load Balancer al nuevo FQDN de IBM Cloud Load Balancer.

## En sus instrucciones se indica que se debe hacer el pedido de IBM Cloud Load Balancer antes de cancelar Local Load Balancer. ¿Habrá algún impacto en mi sistema o mi carga de trabajo mientras configure los dos dispositivos?

No, Cloud Load Balancer y Local Load Balancer son dos ofertas separadas que funcionan independientemente.

## Solía utilizar la opción "conexiones por segundo" con Local Load Balancer. ¿Tengo que configurarla también en Cloud Load Balancer?

No. IBM Cloud Load Balancer ajusta automáticamente su capacidad de carga. Puede obtener más información sobre esto en el tema [escalado horizontal de Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling).

## ¿Qué protocolos puedo elegir al utilizar Cloud Load Balancer?

Puede elegir los protocolos HTTP, HTTPS y TCP. También ofrecemos soporte para Capa 7. Consulte [Visión general de las características](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features) para obtener más información.

## Necesito un tipo de cifrado en particular. ¿Cloud Load Balancer lo admite?

IBM Cloud Load Balancer admite TLS versión 1.2 con descarga SSL. Puede encontrar más información sobre los cifrados soportados en [Suites de cifrado SSL de Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)
