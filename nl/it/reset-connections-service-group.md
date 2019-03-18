---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Reimpostazione delle connessioni per un gruppo di servizi
{: #resetting-connections-for-a-service-group}

Quando un gruppo di servizi è attivo in un programma di bilanciamento del carico, potrebbe esistere una connessione per ogni servizio associato a tale gruppo, in base al modo in cui i client utilizzano il servizio. A volte, i client potrebbero essere connessi a uno o più servizi per un lasso di tempo inappropriato. Poiché le connessioni sono considerate una risorsa limitata, potrebbe essere necessario reimpostare manualmente le connessioni per un gruppo di servizi per garantire che altri client abbiano l'opportunità di utilizzare il programma di bilanciamento del carico. Attieniti alla procedura qui di seguito per reimpostare le connessioni per un programma di bilanciamento del carico.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), identifica la riga del gruppo di servizi di cui desideri reimpostare le connessioni e fai clic su **Actions > Reset Connections**.
2. Conferma l'azione facendo clic su **Yes**. Scegli **No** per annullare l'azione.

Dopo la richiesta di reimpostazione di tutte le connessioni attive, il gruppo di servizio interromperà le connessioni attive a ciascun servizio. Dopo che le connessioni saranno state reimpostate, nella parte superiore dello schermo comparirà una casella di testo verde per confermare la corretta esecuzione dell'azione. Quando le connessioni vengono interrotte, i client potranno riconnettersi come necessario. 

Puoi ripetere la procedura sopra indicata per reimpostare le connessioni per il gruppo di servizi in qualsiasi momento.
