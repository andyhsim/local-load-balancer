---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiunta di un servizio a un gruppo di servizi
{: #adding-a-service-to-a-service-group}

Dopo che un gruppo di servizio è stato aggiunto a un {{site.data.keyword.loadbalancer_short}}, è possibile aggiungere i servizi per avviare il processo di bilanciamento. È possibile aggiungere più servizi a un gruppo di servizi ed è possibile indicarne il peso per consentire un'indicazione della priorità relativa alla modalità di ricezione del carico di lavoro di ciascun dispositivo in un dato momento. Attieniti alla procedura di seguito per aggiungere un nuovo servizio a un gruppo di servizi per un {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), fai clic su **Actions > Add Service** nel menu a discesa sulla riga corrispondente al gruppo di servizi dove desideri aggiungere un servizio. In alternativa, espandi i dettagli del gruppo facendo clic sull'icona di espansione sul lato sinistro della riga e fai clic sul pulsante **Add Service**. Una nuova sezione Service verrà aggiunta in fondo alla sezione dei dettagli del gruppo di servizi.
2. Immetti i parametri del servizio:
  - **Destination IP:** l'indirizzo IP del server di destinazione.
  - **Dest. Port:** il numero porta da utilizzare per instradare il traffico al server di destinazione.
  - **Health Check:** il metodo di controllo dell'integrità preferito da queste opzioni.

     - **Default:** la configurazione predefinita è Ping.
     - **HTTP:** i controlli sulla porta 80 all'indirizzo IP elencato rispondono con il codice HTTP 200 (okay).
     - **HTTP-CUSTOM:** molto simile a HTTP regolare, tranne per il fatto che assegni il tipo di connessione, l'ubicazione del tuo controllo dell'integrità e la risposta che prevedi. Questa è un'opzione avanzata.
     - **Ping:** un semplice test di ping su ICMP.
     - **TCP:** molto simile a un test di ping ma esplicitamente su TCP. Questa opzione deve essere utilizzata se hai delle connessioni ICMP bloccate.
  - **Weight:** la priorità numerica per il servizio. I pesi sono un sistema di assegnazione di valori numerici ai server che desideri ricevano più traffico. Un numero più elevato rappresenta una priorità più elevata a condizione che il server sia online in base ai controlli dell'integrità. Ad esempio, se _server1_ ha un peso di 80 e _server2_ ha un peso di 20, per ogni 10 connessioni che arrivano, a _server1_ ne verranno allocate 8 e a _server2_ ne verranno allocate 2. Se _server1_ va offline o viene rimosso dal pool, tutte le connessioni andranno a _server2_.
  - **Notes:** campo per le note.
3. Seleziona la casella di spunta **Enabled** per abilitare il servizio.
4. Fai clic sul pulsante **Save Configuration** per aggiungere il servizio. Fai clic su **Cancel** per annullare l'azione.

Dopo essere stato aggiunto a un gruppo di servizi, il servizio comparirà nella griglia dei servizi per il gruppo. Se è stato abilitato, comincerà a supportare gli sforzi di bilanciamento del carico in base al peso fornitogli quando è stato aggiunto. Se è disabilitato, sarà comunque presente nel gruppo di servizi ma non contribuirà al bilanciamento se non viene prima attivato. I controlli dell'integrità verranno eseguiti sul servizio periodicamente e il suo stato verrà riflesso come attivo o inattivo, sulla base del risultato del controllo stesso. I servizi possono essere modificati o eliminati in qualsiasi momento e i controlli dell'integrità personalizzati HTTP possono essere aggiunti a qualsiasi servizio esistente mediante il menu a discesa Actions.
