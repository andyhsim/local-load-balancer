---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-01-23"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eine Servicegruppe zu einer Lastausgleichsfunktion hinzufügen

Nach dem Hinzufügen einer {{site.data.keyword.loadbalancer_short}} kann der {{site.data.keyword.loadbalancer_short}} jederzeit eine neue Servicegruppe hinzugefügt werden. Servicegruppen stehen als verschiedene Typen bereit und bieten ein umfangreiches Angebot an einzelnen und hybriden Lastausgleichsmethoden. Beim Hinzufügen einer neuen Servicegruppe ist es wichtig, dass die Summe aller Verbindungszuordnungen der Gruppe 100 % entspricht. Führen Sie die folgenden Schritte aus, um einer {{site.data.keyword.loadbalancer_short}} eine neue Servicegruppe hinzuzufügen.

1. Klicken Sie auf der Seite mit den [Details für die lokale Lastausgleichsfunktion](view-all-load-balancers.html) auf die Schaltfläche **Gruppe hinzufügen**. Alternativ können Sie **Aktionen > Gruppe hinzufügen** auswählen. Unten auf der Seite wird ein Abschnitt für die neue Servicegruppe hinzugefügt.
2. Wählen Sie den gewünschten Gruppentyp aus der Dropdown-Liste **Gruppe** und die Lastausgleichsmethode aus der Dropdown-Liste **Methode** aus. Weitere Informationen zu den einzelnen Lastausgleichsmethoden finden Sie unter [Lastausgleichsmethoden](load_balancing_methods.html).
3. Geben Sie im Feld **Virtueller Port** die Portnummer ein, die für die Servicegruppe verwendet werden soll. Weitere Informationen finden Sie im Abschnitt mit den [häufig gestellten Fragen zu Service-Ports](load-balancing-faqs-2.html#what-services-can-be-load-balanced-). 

	**Hinweis:** Jeder Servicegruppe muss ein eindeutiger Port zugewiesen werden. Ist kein eindeutiger Port zugewiesen, wird oben auf der Seite ein Fehler angezeigt und die Servicegruppe wird erst dann hinzugefügt, wenn ein eindeutiger virtueller Port zugewiesen wurde.
4. Geben Sie im Feld **Zuordnung** eine Zuordnung ein.
5. Geben Sie bei Bedarf Anmerkungen im Feld **Anmerkungen** ein.
6. Klicken Sie auf die Schaltfläche **Konfiguration speichern**, um die neue Servicegruppe hinzuzufügen. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Abbrechen**.

Nachdem eine Servicegruppe hinzugefügt wurde, kann diese jederzeit gelöscht oder bearbeitet werden. Verbindungen zur Servicegruppe können zurückgesetzt und der Gruppe neue Services hinzugefügt werden. Damit eine Servicegruppe die Last basierend auf ihren zugewiesenen Verbindungszuordnungen verteilen kann, muss mindestens ein Service zur Servicegruppe [hinzugefügt](add-service-service-group.html) werden.

## Nächste Schritte

[Fügen Sie der Servicegruppe einen Service hinzu](add-service-service-group.html).
