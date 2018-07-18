---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Service löschen 

Nachdem ein Service zu einer Servicegruppe für eine {{site.data.keyword.loadbalancer_short}} hinzugefügt wurde, kann er jederzeit gelöscht werden. Durch das Löschen eines Service aus einer Servicegruppe wird verhindert, dass der Service von der {{site.data.keyword.loadbalancer_short}} genutzt wird, es sei denn, er wird manuell wieder einer Servicegruppe hinzugefügt. 

Alternativ kann ein Service inaktiviert werden. Dadurch ist der Service zwar der Servicegruppe zugeordnet, kann aber nicht für den Lastausgleich verwendet werden. Damit der Service der Servicegruppe der {{site.data.keyword.loadbalancer_short}} zugeordnet bleibt, [bearbeiten Sie die Service](edit-service-load-balancer.html) und inaktivieren Sie das Kontrollkästchen **Aktiviert**. 

Führen Sie die folgenden Schritte aus, um den Service aus der {{site.data.keyword.loadbalancer_short}} zu löschen.

1. Suchen Sie auf der Seite mit den [Details zu Local Load Balancer](view-all-load-balancers.html) nach dem Service, den Sie löschen möchten, und erweitern Sie den Pfeil auf der linken Seite.
2. Klicken Sie am Ende der Zeile des Service auf das rote 'x'.
3. Um die Einstellungen zu aktualisieren, klicken Sie unten auf der Seite auf **Konfiguration speichern**.

Nachdem der Service gelöscht wurde, wird die Konfiguration gespeichert und die Änderungen werden sofort wirksam. Wenn der gelöschte Service der einzige Service ist, der einer Servicegruppe zugeordnet ist, kann die Gruppe erst wieder Lastausgleichsaktivitäten durchführen, wenn ein neuer Service hinzugefügt wird.
