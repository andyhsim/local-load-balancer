---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione dei controlli dell'integrità per un servizio
{: #configuring-health-checks-for-a-service}

I controlli dell'integrità sono progettati per controllare regolarmente se un server è online e sta accettando traffico perché un {{site.data.keyword.loadbalancer_short}} ci faccia transitare del traffico. I controlli dell'integrità sono progettati per rispondere con una risposta UP o DOWN, a seconda del tuo timeout personalizzato. L'intervallo predefinito è 120 secondi.

CI sono diversi metodi di configurazione dei controlli dell'integrità.

- **Default:** la configurazione predefinita è Ping.
- **HTTP:** i controlli sulla porta 80 all'indirizzo IP elencato rispondono con il codice HTTP 200 (okay).
- **HTTP-CUSTOM:** molto simile a HTTP regolare, tranne per il fatto che assegni il tipo di connessione, l'ubicazione del tuo controllo dell'integrità e la risposta che prevedi. Questa è un'opzione avanzata.
- **Ping:** un semplice test di ping su ICMP.
- **TCP:** molto simile a un test di ping ma esplicitamente su TCP. Questa opzione deve essere utilizzata se hai delle connessioni ICMP bloccate.

Puoi configurare i controlli dell'integrità per uno specifico servizio quando [aggiungi il servizio a un gruppo di servizi](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) oppure [modificando il servizio](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) dopo che è stato creato.

Dopo che la configurazione è stata salvata, le modifiche diventeranno immediatamente effettive. Potrai monitorare lo stato dei tuoi controlli dell'integrità dall'icona di stato nel gruppo di servizi.
