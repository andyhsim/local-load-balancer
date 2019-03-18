---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Aggiunta di un gruppo di servizi a un programma di bilanciamento del carico
{: #adding-a-service-group-to-a-load-balancer}

Dopo che è stato aggiunto un {{site.data.keyword.loadbalancer_short}}, è possibile aggiungere un nuovo gruppo di servizi al {{site.data.keyword.loadbalancer_short}} in qualsiasi momento. I gruppi di servizi sono disponibili in diversi tipi di gruppo e offrono un'ampia gamma di metodi di bilanciamento singoli o ibridi. Quando aggiungi un nuovo gruppo di servizi, è importante che ti assicuri che la somma di tutte le allocazioni delle connessioni dei gruppi sia uguale al 100%. Attieniti alla procedura di seguito per aggiungere un nuovo gruppo di servizi a un {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), fai clic sul pulsante **Add Group**. In alternativa, puoi fare clic su **Actions > Add Group**. Una nuova sezione Service Group verrà aggiunta in fondo alla pagina.
2. Seleziona il tipo di gruppo che desideri dall'elenco a discesa **Group** e seleziona il metodo di bilanciamento che desideri dall'elenco a discesa **Method**. Fai riferimento a [Metodi di bilanciamento del carico](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods#load-balancing-methods) per ulteriori informazioni su ciascun metodo di bilanciamento del carico.
3. Immetti il numero porta che verrà utilizzato per il gruppo di servizi nel campo **Virtual Port**. Per ulteriori informazioni, fai riferimento alle [domande frequenti relative alle porte di servizio comuni](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-). 

	**Nota:** a ogni gruppo di servizi deve essere assegnata una porta univoca. Se non viene assegnata una porta univoca, verrà visualizzato un errore nella parte superiore della pagina e il gruppo di servizi non potrà essere aggiunto finché non verrà assegnato un portale virtuale univoco.
4. Immetti un'allocazione nel campo **Allocation**.
5. Immetti eventuali note nella casella di testo **Notes**, se vuoi.
6. Fai clic sul pulsante **Save Configuration** per aggiungere il nuovo gruppo di servizi. Fai clic su **Cancel** per annullare l'azione.

Dopo che hai aggiunto un gruppo di servizi, può essere eliminato o modificato in qualsiasi momento. Le connessioni possono essere reimpostate al gruppo di servizi e al gruppo possono essere aggiunti dei nuovi servizi. Perché un gruppo di servizi inizi a bilanciare il carico in base alle sue allocazioni di connessione assegnate, al gruppo di servizi devono essere [aggiunti](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group) uno o più servizi.

## Cosa succede poi

[Aggiunta di un servizio al gruppo di servizi](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-adding-a-service-to-a-service-group).
