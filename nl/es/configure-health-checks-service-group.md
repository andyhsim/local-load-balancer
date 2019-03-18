---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurar comprobaciones de estado para un servicio
{: #configuring-health-checks-for-a-service}

Las comprobaciones de estado están diseñadas para comprobar regularmente si un servidor está en línea y acepta tráfico para que un {{site.data.keyword.loadbalancer_short}} pase tráfico por él. Las comprobaciones de estado están diseñadas para responder con una respuesta UP o DOWN dependiendo del tiempo de espera personalizado. El intervalo predeterminado es de 120 segundos.

Existen varios métodos para configurar las comprobaciones de estado.

- **Valor predeterminado:** La configuración predeterminada es Ping.
- **HTTP:** Comprueba si el puerto 80 en la dirección IP listada responde con el código HTTP 200 (correcto).
- **HTTP-CUSTOM:** Muy similar a HTTP normal, excepto que asigna el tipo de conexión, la ubicación de la comprobación de estado y la respuesta que está anticipando. Esta es una opción avanzada.
- **Ping:** Una prueba de ping sencilla a través de ICMP.
- **TCP:** Muy similar a una prueba ping, pero explícitamente a través de TCP. Esta opción debería utilizarse si tiene conexiones ICMP bloqueados.

Puede configurar comprobaciones de estado para un servicio concreto cuando se [añada el servicio a un grupo de servicios](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) o cuando se [edite el servicio](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) después de que se haya creado.

Una vez que se haya guardado la configuración, los cambios entrarán en vigor inmediatamente. Podrá supervisar el estado de sus comprobaciones de estado desde el icono de estado del grupo de servicios.
