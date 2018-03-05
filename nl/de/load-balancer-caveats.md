---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Bekannte Einschränkungen

Aufgrund der Eigenschaften einer Proxy-basierten Lastausgleichsfunktion kommt die Quellen-IP der Clientanforderung von der IP der Lastausgleichsfunktion. Dies hat Auswirkungen auf statistische Protokollierungsprogramme und andere Anwendungen, die die Quellen-IP beim Abrufen von Clientinformationen berücksichtigen. IBM Cloud stellt eine Lösung bereit, mit der Protokolleinträge ordnungsgemäß für Apache (alle Plattformen) und IIS (Windows) neu geschrieben werden.

Um auf diese Anweisungen und die erforderlichen zusätzlichen Plug-ins zugreifen zu können, müssen Sie zunächst eine Verbindung mit der [IBM Cloud-VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window} herstellen. Sobald Sie verbunden sind, rufen Sie die [Downloadseite](http://downloads.softlayer.local/loadbalancer/){: new_window} auf, um nach den Plug-ins und den Anweisungen für die {{site.data.keyword.loadbalancer_short}} zu suchen.
