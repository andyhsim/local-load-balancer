---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Modifica di un servizio
{: #editing-a-service}

Dopo essere stato aggiunto a un gruppo di servizi di un programma di bilanciamento del carico, un servizio può essere modificato in qualsiasi momento. Tutte le impostazioni di base di un servizio possono essere modificate ed è anche possibile aggiungere delle note utilizzando la funzione di modifica. 

Attieniti alla procedura di seguito per modificare un servizio.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), individua il servizio che desideri modificare espandendo la freccia sulla sinistra.
2. Modifica i seguenti campi, come desiderato:
  - **Destination IP:** l'indirizzo IP del server di destinazione.
  - **Dest Port:** il numero porta da utilizzare per instradare il traffico al server di destinazione.
  - **Health Check:** il metodo di controllo dell'integrità preferito da queste opzioni.
      - **Default:** la configurazione predefinita è Ping.
      - **HTTP:** i controlli dalla porta 80 all'indirizzo IP elencato rispondono con il codice HTTP 200 (okay).
      - **HTTP-CUSTOM:** molto simile a HTTP regolare, tranne per il fatto che assegni il tipo di connessione, l'ubicazione del tuo controllo dell'integrità e la risposta che prevedi. Questa è un'opzione avanzata.
      - **Ping:** un semplice test di ping su ICMP.
      - **TCP:** molto simile a un test di ping ma esplicitamente su TCP.  Questa opzione deve essere utilizzata se hai delle connessioni ICMP bloccate.
  - **Weight:** la priorità numerica per il servizio. I pesi sono un sistema di assegnazione di valori numerici ai server che desideri ricevano più traffico. Un numero più elevato rappresenta una priorità più elevata a condizione che il server sia online in base ai controlli dell'integrità. Ad esempio, se _server1_ ha un peso di 80 e _server2_ ha un peso di 20, per ogni 10 connessioni che arrivano, a _server1_ ne verranno allocate 8 e a _server2_ ne verranno allocate 2. Se _server1_ va offline o viene rimosso dal pool, tutte le connessioni andranno a _server2_.
  - **Notes:** campo di testo in formato libero.
  - **Enabled:** seleziona o deseleziona questa casella di spunta per abilitare o disabilitare il servizio.
3. Fai clic sul pulsante **Save Configuration** per aggiornare il servizio. Fai clic su **Cancel** per annullare l'azione.

Dopo che a un servizio sono state apportate delle modifiche, queste ultime compariranno in una riga che contiene il servizio nella sezione Service. È possibile apportare delle modifiche aggiuntive in qualsiasi momento ripetendo la procedura sopra indicata.
