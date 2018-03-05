---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Verbindungen für eine Servicegruppe zurücksetzen

Wenn eine Servicegruppe für eine Lastausgleichsfunktion aktiv ist, kann in Abhängigkeit davon, wie Clients den Service verwenden, für jeden Service, der dieser Gruppe zugeordnet ist, eine Verbindung bestehen. Zuweilen kann es sein, dass Clients unzulässig lange mit einem oder mehreren Services verbunden sind. Da Verbindungen als eine begrenzte Ressource angesehen werden, kann es notwendig sein, die Verbindungen manuell für eine Servicegruppe zurückzusetzen, um sicherzustellen, dass andere Clients die Möglichkeit haben, die Lastausgleichsfunktion zu nutzen. Führen Sie die folgenden Schritte aus, um Verbindungen für eine Lastausgleichsfunktion zurückzusetzen.

1. Geben Sie auf der Seite mit den [Details für die lokale Lastausgleichsfunktion](view-all-load-balancers.html) die Zeile der Servicegruppe an, für die die Verbindungen zurückgesetzt werden sollen, und klicken Sie auf **Aktionen > Verbindungen zurücksetzen**.
2. Bestätigen Sie die Aktion durch Klicken auf **Ja**. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Nein**.

Nachdem angefordert wurde, dass alle aktiven Verbindungen zurückgesetzt werden sollen, löscht die Servicegruppe die aktiven Verbindungen zu den einzelnen Services. Sobald die Verbindungen zurückgesetzt wurden, wird oben in der Anzeige ein grünes Textfeld angezeigt, das den Erfolg der Aktion bestätigt. Wenn Verbindungen gelöscht werden, können Clients bei Bedarf eine erneute Verbindung herstellen. 

Sie können die obigen Schritte jederzeit zum Zurücksetzen der Verbindungen für die Servicegruppe wiederholen.
