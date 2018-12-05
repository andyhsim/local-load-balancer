---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Servicegruppe bearbeiten

Nachdem Sie eine Servicegruppe zu einer {{site.data.keyword.loadbalancer_short}} hinzugefügt haben, können die Grundeinstellungen (einschließlich Lastausgleichsmethode und virtueller Port), Verbindungszuordnungen und Anmerkungen bearbeitet werden. Bearbeitungen an den einzelnen Servicegruppen sind sofort sichtbar und es können jederzeit weitere Bearbeitungen vorgenommen werden. 

Wenn der Gruppentyp für eine Servicegruppe geändert werden muss, muss die Servicegruppe gelöscht und eine neue Servicegruppe hinzugefügt werden, die den gewünschten Gruppentyp widerspiegelt. 

Führen Sie die folgenden Schritte aus, um eine vorhandene Servicegruppe für eine {{site.data.keyword.loadbalancer_short}} zu bearbeiten.

1. Erweitern Sie auf der Seite mit den [Details zu Local Load Balancer](view-all-load-balancers.html) die Details der Servicegruppe, indem Sie links neben der Zeile, die der Servicegruppe entspricht, die Sie bearbeiten möchten, auf das Erweiterungssymbol klicken.
2. Aktualisieren Sie die Einstellungen für die Servicegruppe:
  - **Methode:** Wählen Sie eine [Lastausgleichsmethode](load_balancing_methods.html) aus der Dropdown-Liste aus.
  - **Virtueller Port:** Die Portnummer, die für die Servicegruppe verwendet wird. Weitere Informationen finden Sie im Abschnitt mit den [häufig gestellten Fragen zu Service-Ports](load-balancing-faqs-2.html#what-services-can-be-load-balanced-). 

  	**Hinweis:** Jeder Servicegruppe muss ein eindeutiger Port zugewiesen werden. Ist kein eindeutiger Port zugewiesen, wird oben auf der Seite ein Fehler angezeigt und die Servicegruppe wird erst dann hinzugefügt, wenn ein eindeutiger virtueller Port zugewiesen wurde.
  - **Zuordnung:** Die Zuordnung für die Servicegruppe.
  - **Anmerkungen:** Unformatierter Text, mit dem die Servicegruppe angegeben wird.
3. Klicken Sie auf die Schaltfläche **Konfiguration speichern**, um die Servicegruppe zu aktualisieren. Wenn Sie die Aktion abbrechen möchten, klicken Sie auf **Abbrechen**.

Bearbeitungen an der Servicegruppe werden in der Anzeige mit den Details unter der zugehörigen Servicegruppe angezeigt. Wenn an der Verbindungszuordnung eine Änderung vorgenommen wurde, können zusätzliche Bearbeitungen für andere Servicegruppen erforderlich sein. Wenn die Lastausgleichsmethode geändert wurde, müssen an Services, die der Gruppe zugeordnet sind, möglicherweise zusätzliche Bearbeitungen vorgenommen werden, um der neuen Lastausgleichsmethode gerecht zu werden. Indem Sie die obigen Schritte wiederholen, können Sie jederzeit weitere Bearbeitungen an der Servicegruppe vornehmen.
