---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Servicegruppe löschen

Beim Löschen einer Servicegruppe werden alle dieser Gruppe zugeordneten Services gelöscht. Führen Sie die folgenden Schritte aus, um eine Servicegruppe für eine {{site.data.keyword.loadbalancer_short}} zu löschen.

1. Geben Sie auf der Seite mit den [Details zu Local Load Balancer](view-all-load-balancers.html) die Zeile der Servicegruppe an, die gelöscht werden soll, und klicken Sie auf **Aktionen > Gruppe entfernen**.
2. Klicken Sie auf **Konfiguration speichern**.

Nach dem Löschen einer Servicegruppe wird diese aus der {{site.data.keyword.loadbalancer_short}} entfernt. Alle zugehörigen Services werden auch gelöscht und der virtuelle Port, der der Servicegruppe zugeordnet ist, ist für den Fall verfügbar, dass er zukünftig für eine andere Servicegruppe benötigt wird. Beim Löschen muss der Prozentsatz der Verbindungszuordnung für die verbleibenden Servicegruppen manuell geändert werden.
