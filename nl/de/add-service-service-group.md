---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Service zu einer Servicegruppe hinzufügen
{: #adding-a-service-to-a-service-group}

Nachdem eine Servicegruppe zu einer {{site.data.keyword.loadbalancer_short}} hinzugefügt wurde, können Services hinzugefügt werden, um den Lastausgleich zu starten. Einer Servicegruppe können mehrere Services hinzugefügt werden, die für eine Priorisierung gewichtet werden können, wie einzelne Geräte die Arbeitslast zu einem bestimmten Zeitpunkt empfangen sollen. Führen Sie die folgenden Schritte aus, um einen neuen Service zu einer Servicegruppe für eine {{site.data.keyword.loadbalancer_short}} hinzuzufügen.

1. Klicken Sie auf der Seite mit den [Details zu Local Load Balancer](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details) in dem Dropdown-Menü der Zeile, die der Servicegruppe entspricht, zu der ein Service hinzugefügt werden soll, auf **Aktionen > Service hinzufügen**. Alternativ können Sie die Gruppendetails erweitern, indem Sie links neben der Zeile auf das Erweiterungssymbol und anschließend auf die Schaltfläche **Service hinzufügen** klicken. Unten im Abschnitt mit den Servicegruppendetails wird ein Abschnitt für den neuen Service hinzugefügt.
2. Geben Sie die Serviceparameter ein:
  - **Ziel-IP:** Die IP-Adresse des Zielservers.
  - **Zielport:** Die Portnummer zum Weiterleiten des Datenverkehrs an den Zielserver.
  - **Statusprüfung:** Die bevorzugte Methode für die Statusprüfung aus diesen Optionen.

     - **Standard:** Die Standardkonfiguration ist 'Ping'.
     - **HTTP:** Antwort auf Prüfungen über Port 80 an die aufgeführte IP-Adresse mit HTTP-Code 200 (okay).
     - **HTTP-CUSTOM:** Fast wie reguläres HTTP, außer dass Sie den Verbindungstyp zuweisen, die Position der Statusprüfung sowie die erwartete Antwort angeben. Dies ist eine erweiterte Option.
     - **Ping:** Ein einfacher Pingtest über ICMP.
     - **TCP:** Ähnlich wie ein Pingtest, aber explizit über TCP. Diese Option sollte verwendet werden, wenn ICMP-Verbindungen geblockt sind.
  - **Gewichtung:** Die numerisch ausgedrückte Priorität für den Service. Gewichtungen dienen dazu, numerische Werte den Servern zuzuweisen, die mehr Datenverkehr empfangen sollen. Eine höhere Zahl steht für eine höhere Priorität, solange der Server laut Statusprüfung online ist. Wenn _Server1_ beispielsweise die Gewichtung '80' aufweist und _Server2_ die Gewichtung '20', werden für jede 10 Verbindungen, die durchkommen, _Server1_ 8 und _Server2_ 2 zugeordnet. Wenn _Server1_ offline geht oder aus dem Pool entfernt wird, gehen alle Verbindungen an _Server2_.
  - **Anmerkungen:** Feld für Anmerkungen.
3. Wählen Sie das Kontrollkästchen **Aktiviert** aus, um den Service zu aktivieren.
4. Klicken Sie auf die Schaltfläche **Konfiguration speichern**, um den Service hinzuzufügen. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Abbrechen**.

Nachdem Sie einen Service zu einer Servicegruppe hinzugefügt haben, wird dieser im Raster mit den Services für diese Gruppe angezeigt. Wenn der Service aktiviert ist, unterstützt er basierend auf die Gewichtung, die beim Hinzufügen des Service bereitgestellt wurde, den Lastausgleich. Ist der Service inaktiviert, wird er zwar in der Servicegruppe angezeigt, unterstützt den Lastausgleich aber erst, wenn er aktiviert wird. Statusprüfungen werden für den Service in regelmäßigen Abständen durchgeführt und der Status des Service wird basierend auf dieser Prüfung als aktiv oder inaktiv bewertet. Services können jederzeit bearbeitet oder gelöscht werden und angepasste HTTP-Statusprüfungen können einem vorhandenen Service über das Dropdown-Menü 'Aktionen' hinzugefügt werden.
