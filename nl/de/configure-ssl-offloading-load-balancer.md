---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# SSL-Auslagerung für eine Lastausgleichsfunktion konfigurieren

Im Rahmen einer Lastausgleichsfunktion kann die SSL-Auslagerung bereitgestellt werden, was zu einer beträchtlichen Reduzierung der Auslastung der Systeme führen kann, die die Funktion aktuell ausführen. Um die SSL-Auslagerung nutzen zu können, muss eine {{site.data.keyword.loadbalancer_short}} erworben werden, die diese Funktionalität bietet. Lastausgleichsfunktionen mit SSL-Funktionalität sind mit der Anmerkung "Mit SSL-Auslagerung" im Dialogfeld **Local Load Balancer bestellen** versehen. Nachdem die für die SSL-Auslagerung aktivierte {{site.data.keyword.loadbalancer_short}} bereitgestellt wurde, muss sie konfiguriert werden. Führen Sie die folgenden Schritte aus, um die SSL-Auslagerung für eine {{site.data.keyword.loadbalancer_short}} zu konfigurieren.

1. Klicken Sie auf der Seite mit den [Details zu Local Load Balancer](view-all-load-balancers.html) im Dropdown-Menü für die Lastausgleichsfunktion auf **Aktionen > SSL konfigurieren**.
2. Wählen Sie das gewünschte SSL-Zertifikat aus der Dropdown-Liste **Zertifikat** aus. Beachten Sie dabei Folgendes:
  - Virtuelle IPs (VIPs) von nicht dedizierten {{site.data.keyword.loadbalancer_short}}en sind auf eine Bitgröße des SSL-Zertifikats von 2048 begrenzt.
  - Um diesen Schritt erfolgreich auszuführen, muss mindestens ein SSL-Zertifikat im Kundenportal gespeichert sein. Weitere Informationen finden Sie unter [SSL-Zertifikat importieren](import-ssl-cert.html).
3. Aktivieren Sie das Kontrollkästchen **Aktiviert**.
4. Wählen Sie die Verschlüsselungen aus, die unterstützt werden sollen.
5. Klicken Sie auf die Schaltfläche **Aktualisieren**.

Nach der Aktivierung der SSL-Auslagerung für eine {{site.data.keyword.loadbalancer_short}} ändert sich der Status des SSL von **inaktiviert** in **aktiv**. Die durch Systeme getragene Last, die zuvor durch SSL-Verbindungen verarbeitet wurde, nimmt in der Regel nach der Aktivierung der SSL-Auslagerung ab. Der Status der SSL-Auslagerung kann sich jederzeit ändern. Wechseln Sie zurück zur Registerkarte für die SSL-Auslagerung und wählen Sie das entsprechende Kontrollkästchen ab, um die SSL-Auslagerung für die {{site.data.keyword.loadbalancer_short}} zu inaktivieren.
