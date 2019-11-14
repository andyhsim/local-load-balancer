---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2019-11-12"

keywords: confiure, configuring, health checks, service 
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}

# Configuring Health Checks for a Service
{: #configuring-health-checks-for-a-service}

Health Checks are designed to regularly check if a server is online and accepting traffic for a {{site.data.keyword.loadbalancer_short}} to pass traffic through. Health Checks are designed to respond with either an UP or DOWN reply depending upon your custom timeout. The default interval is 120 seconds.
{: shortdesc}

There are several methods of configuring health checks.

- **Default:** The default configuration is Ping.
- **HTTP:** Checks over port 80 to the IP address listed responds with HTTP code 200 (okay).
- **HTTP-CUSTOM:** Much like regular HTTP, except you assign the type of connection, the location of your health check, and the response that you are anticipating. This is an advanced option.
- **Ping:** A simple ping test over ICMP.
- **TCP:** Much like a ping test but explicitly over TCP. This option should be used if you have ICMP connections blocked.

You can configure Health Checks for a particular service when you [add the Service to a Service Group](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) or by [editing the Service](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) after it has been created.

Once your configuration has been saved, the changes will take effect immediately. You will be able to monitor the status of your health checks from the status icon in the service group.
