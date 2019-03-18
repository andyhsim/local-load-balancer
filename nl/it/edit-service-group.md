---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Modifica di un gruppo di servizi
{: #editing-a-service-group}

Dopo l'aggiunta di un gruppo di servizi a un {{site.data.keyword.loadbalancer_short}}, è possibile modificarne le impostazioni di base (compresi il metodo di bilanciamento e la porta virtuale), l'allocazione delle connessioni e le note. Le modifiche a ogni gruppo di servizi sono immediatamente visibili ed è possibile apportare ulteriori modifiche in qualsiasi momento. 

Se è necessario modificare il tipo di gruppo per un gruppo di servizi, è necessario eliminare il gruppo di servizi e aggiungere un nuovo gruppo di servizi che rifletta il tipo di gruppo desiderato. 

Attieniti alla procedura di seguito per modificare un gruppo di servizi esistenti per un {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), espandi i dettagli del gruppo di servizi facendo clic sull'icona di espansione sul lato sinistro della riga corrispondente al gruppo di servizi che desideri modificare.
2. Aggiorna le impostazioni del gruppo di servizi:
  - **Method:** seleziona un metodo di bilanciamento ([Balancing Method](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-load-balancing-methods)) dall'elenco a discesa.
  - **Virtual Port:** il numero porta che verrà utilizzato per il gruppo di servizi. Per ulteriori informazioni, fai riferimento alle [domande frequenti relative alle porte di servizio comuni](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-faqs-for-local-load-balancer#what-services-can-be-load-balanced-). 

  	**Nota:** a ogni gruppo di servizi deve essere assegnata una porta univoca. Se non viene assegnata una porta univoca, verrà visualizzato un errore nella parte superiore della pagina e il gruppo di servizi non potrà essere aggiunto finché non verrà assegnato un portale virtuale univoco.
  - **Allocation:**  l'allocazione per il gruppo di servizi.
  - **Notes:** testo in formato libero per identificare il gruppo di servizi.
3. Fai clic sul pulsante **Save Configuration** per aggiornare il gruppo di servizi. Fai clic sul pulsante **Cancel** per annullare l'azione.

Le modifiche apportate al gruppo di servizio verranno riflesse nello schermo Details nel gruppo associato. Se è stata apportata una modifica all'allocazione delle connessioni, potrebbero essere necessarie ulteriori modifiche per gli altri gruppi di servizi. Se è stata apportata una modifica al metodo di bilanciamento, i servizi associati al gruppo potrebbero richiedere ulteriori modifiche per un allineamento al nuovo metodo di bilanciamento. Ulteriori modifiche al gruppo di servizi possono essere apportate in qualsiasi momento ripetendo la procedura sopra indicata.
