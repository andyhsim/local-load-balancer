---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Gewichtungen für die Lastausgleichsfunktion konfigurieren
{; #configuring-weights-for-the-load-balancer}

Gewichtungen dienen dazu, numerische Werte den Servern zuzuweisen, die mehr Datenverkehr empfangen sollen. Eine höhere Zahl steht für eine höhere Priorität, solange der Server laut Statusprüfung online ist.  

Wenn _Server1_ beispielsweise die Gewichtung '80' aufweist und _Server2_ die Gewichtung '20', werden für jede 10 Verbindungen, die durchkommen, _Server1_ 8 und _Server2_ 2 zugeordnet. Wenn _Server1_ offline geht oder aus dem Pool entfernt wird, gehen alle Verbindungen an _Server2_.

Sie können Gewichtungen für einen bestimmten Service konfigurieren, wenn Sie [den Service zu einer Servicegruppe hinzufügen](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) oder indem Sie [den Service bearbeiten](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service), nachdem er erstellt wurde.

Sobald die Konfiguration gespeichert wurde, werden die Änderungen sofort wirksam. Sie können die Verbindungen des Service über die Details für den Service überwachen.
