---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione dei pesi per il programma di bilanciamento del carico
{; #configuring-weights-for-the-load-balancer}

I pesi sono un sistema di assegnazione di valori numerici ai server che desideri ricevano più traffico. Un numero più elevato rappresenta una priorità più elevata a condizione che il server sia online in base ai controlli dell'integrità.  

Ad esempio, se _server1_ ha un peso di 80 e _server2_ ha un peso di 20, per ogni 10 connessioni che arrivano, a _server1_ ne verranno allocate 8 e a _server2_ ne verranno allocate 2. Se _server1_ va offline o viene rimosso dal pool, tutte le connessioni andranno a _server2_.

Puoi configurare i pesi per uno specifico servizio quando [aggiungi il servizio a un gruppo di servizi](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) oppure [modificando il servizio](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) dopo che è stato creato.

Dopo che la configurazione è stata salvata, le modifiche diventeranno immediatamente effettive. Puoi monitorare le connessioni del servizio nei relativi dettagli.
