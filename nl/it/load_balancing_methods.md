---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Metodi di bilanciamento del carico
{: #load-balancing-methods}

| Metodo|Descrizione|
|:---|:---|
|Consistent Hash IP|<ul><li>Associa le richieste client ai server reali mediante hashing degli IP di origine della richiesta.</li><li>Le relazioni client/server vengono mantenute sulle porte.</li></ul>|
|Insert Cookie|<ul><li>Inserisce un cookie di traccia nella richiesta.<span style="mso-spacerun:yes">&nbsp; </span>I dati sessione contenuti nel cookie vengono utilizzati con la richiesta successiva per inviare nuovamente il traffico allo stesso server reale.</li><li>La persistenza è integrata nel codice del programma (hardcoded) in base a ogni singola sessione.</li><li>Il cookie scade dopo che il browser del client è stato chiuso.</li><li>Per essere effettivo richiede che il client accetti i cookie.</li></ul>|
|Least Connections|<ul><li>Il server reale con il numero minore di connessioni attive ottiene la priorità massima.</li><li>L'algoritmo richiede una differenza di 10 connessioni, che potrebbe falsare i risultati per i clienti</li></ul>|
|Persistent IP|<ul><li>Collega l'IP di origine del richiedente al server reale che elabora la richiesta mediante un hash di tutti e 4 gli ottetti dell'indirizzo IP richiedente.</li><li>Persiste per 60 minuti</li></ul>|
|Round Robin|<ul><li>Ogni nuova richiesta viene assegnata al server reale successivo nella rotazione.</li><li>Una distribuzione bilanciata si verifica su campioni di grandi dimensioni, sebbene dei campioni di piccole dimensioni potrebbero visualizzare un bilanciamento sproporzionato.</li></ul>|
|Shortest Response|<ul><li>Il server con il tempo di risposta più breve riceve la richiesta.</li><li>Man mano che il carico e il tempo di risposta aumentano, i server più lenti iniziano a rispondere a meno richieste.</li></ul>|
|Round Robin with Persistent IP|<ul><li>Ogni nuova richiesta viene assegnata al server reale successivo nella rotazione.</li><li>L&rsquo;indirizzo IP del richiedente viene collegato al server reale e, di conseguenza, le richieste successive dall'IP vengono assegnate allo stesso server reale.</li></ul>|
|Round Robin with Insert Cookie|<ul><li>Ogni nuova richiesta viene assegnata al server reale successivo nella rotazione.</li><li>Il programma di bilanciamento del carico inserisce un cookie nella richiesta e utilizza le informazioni sulla sessione dal cookie per indirizzare il traffico allo stesso server reale per le richieste successive.</li></ul>|
|Least Connections with Persistent IP|<ul><li>Ogni nuova richiesta viene assegnata al server reale con il numero minore di connessioni attive al momento.</li><li>L&rsquo;indirizzo IP del richiedente viene collegato al server reale e, di conseguenza, le richieste successive dall'IP vengono assegnate allo stesso server reale.</li></ul>|
|Least Connections with Insert Cookie|<ul><li>Ogni nuova richiesta viene assegnata al server reale con il numero minore di connessioni attive al momento.</li><li>Il programma di bilanciamento del carico inserisce un cookie nella richiesta e utilizza le informazioni sulla sessione dal cookie per indirizzare il traffico allo stesso server reale per le richieste successive.</li></ul>|
|Shortest Response with Persistent IP|<ul><li>Ogni nuova richiesta viene assegnata al server reale con il tempo di risposta più breve.</li><li>L&rsquo;indirizzo IP del richiedente viene collegato al server reale e, di conseguenza, le richieste successive dall'IP vengono assegnate allo stesso server reale.</li></ul>|
|Shortest Response with Insert Cookie|<ul><li>Ogni nuova richiesta viene assegnata al server reale con il tempo di risposta più breve.</li><li>Il programma di bilanciamento del carico inserisce un cookie nella richiesta e utilizza le informazioni sulla sessione dal cookie per indirizzare il traffico allo stesso server reale per le richieste successive.</li></ul>|
