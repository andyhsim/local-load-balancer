---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Statusprüfung für einen Service konfigurieren
{: #configuring-health-checks-for-a-service}

Mit Statusprüfungen kann regelmäßig überprüft werden, ob ein Server online ist und Datenverkehr akzeptiert, damit eine {{site.data.keyword.loadbalancer_short}} Datenverkehr an diesen Server weiterleiten kann. Statusprüfungen sind so konzipiert, dass sie je nach Ihrer angepassten Zeitlimitüberschreitung entweder mit einer 'UP'- oder einer 'DOWN'-Antwort reagieren. Das Standardintervall ist 120 Sekunden.

Es gibt verschiedene Möglichkeiten zum Konfigurieren von Statusprüfungen.

- **Standard:** Die Standardkonfiguration ist 'Ping'.
- **HTTP:** Antwort auf Prüfungen über Port 80 an die aufgeführte IP-Adresse mit HTTP-Code 200 (okay).
- **HTTP-CUSTOM:** Fast wie reguläres HTTP, außer dass Sie den Verbindungstyp zuweisen, die Position der Statusprüfung sowie die erwartete Antwort angeben. Dies ist eine erweiterte Option.
- **Ping:** Ein einfacher Pingtest über ICMP.
- **TCP:** Ähnlich wie ein Pingtest, aber explizit über TCP. Diese Option sollte verwendet werden, wenn ICMP-Verbindungen geblockt sind.

Sie können Statusprüfungen für einen bestimmten Service konfigurieren, wenn Sie [den Service zu einer Servicegruppe hinzufügen](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) oder indem Sie [den Service bearbeiten](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service), nachdem er erstellt wurde.

Sobald die Konfiguration gespeichert wurde, werden die Änderungen sofort wirksam. Sie können nun über das Statussymbol in der Servicegruppe den Status Ihrer Statusprüfungen überprüfen.
