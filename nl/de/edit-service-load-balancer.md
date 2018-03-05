---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Service bearbeiten 

Nachdem ein Service zu einer Servicegruppe der Lastausgleichsfunktion hinzugefügt wurde, kann er jederzeit bearbeitet werden. Alle Grundeinstellungen eines Service dürfen bearbeitet werden. Zudem können mit der Bearbeitungsfunktion zusätzliche Anmerkungen hinzugefügt werden. 

Führen Sie die folgenden Schritte aus, um einen Service zu bearbeiten.

1. Suchen Sie auf der Seite mit den [Details für die lokale Lastausgleichsfunktion](view-all-load-balancers.html) nach dem Service, den Sie bearbeiten möchten, indem Sie links auf den Pfeil klicken.
2. Bearbeiten Sie die folgenden Felder wie gewünscht:
  - **Ziel-IP:** Die IP-Adresse des Zielservers.
  - **Zielport:** Die Portnummer zum Weiterleiten des Datenverkehrs an den Zielserver.
  - **Statusprüfung:** Die bevorzugte Methode für die Statusprüfung aus diesen Optionen.
      - **Standard:** Die Standardkonfiguration ist 'Ping'.
      - **HTTP:** Antwort auf Prüfungen über Port 80 an die aufgeführte IP-Adresse mit HTTP-Code 200 (okay).
      - **HTTP-CUSTOM:** Fast wie reguläres HTTP, außer dass Sie den Verbindungstyp zuweisen, die Position der Statusprüfung sowie die erwartete Antwort angeben. Dies ist eine erweiterte Option.
      - **Ping:** Ein einfacher Pingtest über ICMP.
      - **TCP:** Ähnlich wie ein Pingtest, aber explizit über TCP. Diese Option sollte verwendet werden, wenn ICMP-Verbindungen geblockt sind.
  - **Gewichtung:** Die numerisch ausgedrückte Priorität für den Service. Gewichtungen dienen dazu, numerische Werte den Servern zuzuweisen, die mehr Datenverkehr empfangen sollen. Eine höhere Zahl steht für eine höhere Priorität, solange der Server laut Statusprüfung online ist. Wenn _Server1_ beispielsweise die Gewichtung '80' aufweist und _Server2_ die Gewichtung '20', werden für jede 10 Verbindungen, die durchkommen, _Server1_ 8 und _Server2_ 2 zugeordnet. Wenn _Server1_ offline geht oder aus dem Pool entfernt wird, gehen alle Verbindungen an _Server2_.
  - **Anmerkungen:** Feld für unformatierten Text.
  - **Aktiviert:** Wählen Sie dieses Kontrollkästchen aus oder ab, um den Service zu aktivieren oder zu inaktivieren.
3. Klicken Sie auf die Schaltfläche **Konfiguration speichern**, um den Service zu aktualisieren. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Abbrechen**.

Nach dem Bearbeiten eines Service werden die entsprechenden Bearbeitungen im Abschnitt 'Service' in der Zeile mit dem Service angezeigt. Indem Sie die obigen Schritte wiederholen, können Sie jederzeit weitere Bearbeitungen vornehmen.
