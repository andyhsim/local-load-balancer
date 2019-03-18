---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Lastausgleichsmethoden
{: #load-balancing-methods}

| Methode|Beschreibung|
|:---|:---|
|Konsistente Hash-IP|<ul><li>Ordnet Clientanforderungen zu realen Servern durch das Hashing der Quellen-IPs der Anforderung zu.</li><li>Client/Server-Beziehungen werden über Ports hinweg verwaltet.</li></ul>|
|Cookie-Insert|<ul><li>Fügt einen Tracking-Cookie in eine Anforderung ein.<span style="mso-spacerun:yes">&nbsp; </span>Die im Cookie enthaltenen Sitzungsdaten werden bei nachfolgenden Anforderungen zum Zurücksenden von Datenverkehr an denselben realen Server verwendet.</li><li>Die Persistenz ist für jede Sitzung fest-codiert.</li><li>Das Cookie läuft ab, sobald der Browser des Clients geschlossen wird.</li><li>Setzt voraus, dass der Client Cookies akzeptiert.</li></ul>|
|Least-Connection|<ul><li>Der reale Server mit der niedrigsten Anzahl an aktiven Verbindungen hat Priorität.</li><li>Der Algorithmus erfordert eine Differenz von 10 Verbindungen, was zu einer Verfärbung der Ergebnisse für Kunden führen kann.</li></ul>|
|Persistente IP|<ul><li>Bindet die Quellen-IP des Anforderers an den realen Server, der die Anforderung anhand eines Hashwerts aller vier Oktetten der anfordernden IP-Adresse verarbeitet.</li><li>Bleibt 60 Minuten lang persistent.</li></ul>|
|Round-Robin|<ul><li>Jede neue Anforderung wird dem nächsten realen Server im Umlauf zugewiesen.</li><li>Eine 'ausgeglichene' Verteilung erfolgt bei einer ausreichend großen Anzahl an Clients; wenn es nur wenige Clients sind, findet zwar eine Lastverteilung statt, diese ist aber nicht zwingend 'ausgeglichen'.</li></ul>|
|Kürzeste Antwortzeit|<ul><li>Der Server mit der kürzesten Antwortzeit erhält die Anforderung.</li><li>Bei steigender Arbeitslast und Antwortzeit verarbeiten langsamere Server weniger Anforderungen.</li></ul>|
|Round-Robin mit persistenter IP|<ul><li>Jede neue Anforderung wird dem nächsten realen Server im Umlauf zugewiesen.</li><li>Die IP-Adresse des Anforderers wird an den realen Server gebunden, was dazu führt, dass nachfolgende Anforderungen von dieser IP demselben realen Server zugeordnet werden.</li></ul>|
|Round-Robin mit Cookie-Insert|<ul><li>Jede neue Anforderung wird dem nächsten realen Server im Umlauf zugewiesen.</li><li>Die Lastausgleichsfunktion fügt ein Cookie in die Anforderung ein und verwendet die Sitzungsinformationen aus dem Cookie, um den Datenverkehr bei nachfolgenden Anforderungen an denselben realen Server weiterzuleiten.</li></ul>|
|Least-Connection mit persistenter IP|<ul><li>Jede neue Anforderung wird dem realen Server zugewiesen, der zu diesem Zeitpunkt die wenigsten aktiven Verbindungen aufweist.</li><li>Die IP-Adresse des Anforderers wird an den realen Server gebunden, was dazu führt, dass nachfolgende Anforderungen von dieser IP demselben realen Server zugeordnet werden.</li></ul>|
|Least-Connection mit Cookie-Insert|<ul><li>Jede neue Anforderung wird dem realen Server zugewiesen, der zu diesem Zeitpunkt die wenigsten aktiven Verbindungen aufweist.</li><li>Die Lastausgleichsfunktion fügt ein Cookie in die Anforderung ein und verwendet die Sitzungsinformationen aus dem Cookie, um den Datenverkehr bei nachfolgenden Anforderungen an denselben realen Server weiterzuleiten.</li></ul>|
|Kürzeste Antwortzeit mit persistenter IP|<ul><li>Jede neue Anforderung wird dem realen Server mit der kürzesten Antwortzeit zugewiesen.</li><li>Die IP-Adresse des Anforderers wird an den realen Server gebunden, was dazu führt, dass nachfolgende Anforderungen von dieser IP demselben realen Server zugeordnet werden.</li></ul>|
|Kürzeste Antwortzeit mit Cookie-Insert|<ul><li>Jede neue Anforderung wird dem realen Server mit der kürzesten Antwortzeit zugewiesen.</li><li>Die Lastausgleichsfunktion fügt ein Cookie in die Anforderung ein und verwendet die Sitzungsinformationen aus dem Cookie, um den Datenverkehr bei nachfolgenden Anforderungen an denselben realen Server weiterzuleiten.</li></ul>|
