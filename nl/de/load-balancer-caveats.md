---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Bekannte Einschränkungen bei Local Load Balancer
{: #known-limitations-with-local-load-balancer}

Aufgrund der Eigenschaften einer Proxy-basierten Lastausgleichsfunktion kommt die Quellen-IP der Clientanforderung von der IP der Lastausgleichsfunktion. Dies hat Auswirkungen auf statistische Protokollierungsprogramme und andere Anwendungen, die die Quellen-IP beim Abrufen von Clientinformationen berücksichtigen. IBM© Cloud stellt eine Lösung bereit, mit der Protokolleinträge ordnungsgemäß für Apache (alle Plattformen) und IIS (Windows) neu geschrieben werden.

Sie müssen zuerst eine Verbindung zum VPN von IBM Cloud herstellen, damit Sie Zugriff auf die Anweisungen und die erforderlichen zusätzlichen Plug-ins erhalten. Nach dem Herstellen der Verbindung rufen Sie die [Downloadseite ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://downloads.softlayer.local/loadbalancer/){: new_window} auf. Dort finden Sie die Plug-ins und Anweisungen für Ihre Instanz von {{site.data.keyword.loadbalancer_short}}. 

**Hinweis:** Für den Zugriff auf den Download-Link müssen Sie beim IBM Cloud-VPN angemeldet sein.
