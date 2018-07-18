---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-02"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Häufig gestellte Fragen
Dieser Abschnitt enthält Antworten auf häufig gestellte Fragen zu Local Load Balancer.

## Welche Produkte für den Lastausgleich bietet IBM?
Einen detaillierten Vergleich der Angebote für den Lastausgleich in IBM Cloud finden Sie im Thema [ ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## Was ist der Unterschied zwischen einer gemeinsam genutzten und einer dedizierten Lastausgleichsfunktion?

Es gibt zwei Typen von Lastausgleichsfunktionen: gemeinsam genutzt und dediziert. Bei einer gemeinsam genutzten Lastausgleichsfunktion nutzen verschiedene Kunden das gleiche physische Gerät und sind je nachdem, was bestellt wurde, an eine bestimmte Anzahl an Verbindungen gebunden. Dedizierte Lastausgleichsfunktionen werden in der Regel ausschließlich von einem Kunden verwendet und die Verbindungen unterliegen nur den entsprechenden Spezifikationen des Geräts.

## Was ist ein Service?
Services werden in einer Servicegruppe konfiguriert und stellen die realen Server dar, auf die die Lastausgleichsfunktion Netzverkehr verteilt. Sie setzen sich aus einer Ziel-IP, einem Zielport, Statusprüfungen und einer Gewichtung zusammen.

## Was ist eine Servicegruppe?
Mit einer Servicegruppe konfigurieren Sie die Art und Weise, wie Clients mit der Lastausgleichsfunktion eine Verbindung zu Ihrer Umgebung herstellen. Eine Servicegruppe setzt sich aus einem Protokoll, einer Lastausgleichsmethode, einem virtuellen Port (dem Port, zu dem Clients eine Verbindung herstellen), einer Verbindungszuordnung (Prozentsatz) und den der Gruppe zugeordneten Services zusammen.

## Warum erhalte ich bei der Verwendung der SSL-Auslagerung Gateway-Fehler des Typs 502?

Diese Art von Fehlern treten normalerweise dann auf, wenn der abgehende Port der Lastausgleichsfunktion auf Port 443 festgelegt ist.  Wenn der Lastausgleich aktiviert ist, muss abgehender Datenverkehr an den Server an den Nicht-SSL-Port des Servers geleitet werden.  Dies ist in der Regel Port 80 für HTTP.

## Kann ich mehrere SSL-Zertifikate für eine einzelne Lastausgleichsfunktion haben?

Dies ist in bestimmten Konfigurationen möglich.  Als allgemeine Regel gilt ein SSL-Zertifikat pro virtuelle IP (VIP). Eine lokale Lastausgleichsfunktion unterstützt nur eine einzelne virtuelle IP, dies kann jedoch mit unseren dedizierten und unternehmensorientierten Lastausgleichsfunktionen erweitert werden.

## Was ist ein virtueller Port?

Ein virtueller Port bei einer Lastausgleichsfunktion in IBM Cloud ist ganz einfach der Port, an dem der Service ausgeführt werden soll. Ein Beispiel wäre Port 80 für HTTP.

## Welche Lastausgleichsmethode wird für lokale und dedizierte Lastausgleichsfunktionen verwendet?

Unsere Lastausgleichsfunktionen basieren auf Proxys.

## Für welche Services kann ein Lastausgleich durchgeführt werden?

Zu den am häufigsten verwendeten zählen Ports wie HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3 (110) und SMTP (25). Es kann jedoch für jeden Service ein Lastausgleich durchgeführt werden.

## Kann die SSL-Auslagerung einer vorhandenen Lastausgleichsfunktion hinzugefügt werden?

Dies wird momentan nicht unterstützt. Es muss eine neue Bestellung für eine Lastausgleichsfunktion mit SSL-Auslagerung aufgegeben werden.

## Wie lange dauert die Installation einer Lastausgleichsfunktion?

Lastausgleichsfunktionen sollten etwa fünf Minuten nach dem Erwerb installiert und konfiguriert werden können.

## Wie kann ich für meine lokale Lastausgleichsfunktion einen Downgrade durchführen?

Diese Option ist nur durch das Öffnen eines Tickets verfügbar.

## Welche Lastausgleichsmethoden stehen im Rahmen einer Lastausgleichsfunktion zur Verfügung?

IBM Cloud bietet verschiedene Lastausgleichsmethoden, darunter Einzel- und Hybridmethoden.  Weitere Informationen zu den aktuell angebotenen Lastausgleichsmethoden finden Sie unter [Lastausgleichsmethoden](load_balancing_methods.html).

## Ist es möglich, für mit SSL verschlüsselten Datenverkehr einen Lastausgleich mit Sitzungsattraktivität durchzuführen?

Dies ist möglich, allerdings nur mit einer persistenten Lastausgleichsmethode. Andere Methoden werden nicht unterstützt, da der Datenverkehr verschlüsselt ist.

