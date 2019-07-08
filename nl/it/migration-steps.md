---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

subcollection: local-load-balancer

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Migrazione di un Local Load Balancer a IBM Cloud Load Balancer

Puoi migrare il tuo Local Load Balancer a un IBM© Cloud Load Balancer attenendoti alla seguente procedura:

## Passo 1: Ordina un Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

Per ordinare un servizio IBM Cloud Load Balancer, seleziona **IBM Cloud Load Balancer** dal [catalogo IBM Cloud ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window}. Fai clic su **Create** ed esegui quindi questa procedura:

1. Definisci i tuoi parametri del servizio di base, come il nome e la descrizione.
2. Seleziona il tuo data center.
3. Seleziona un tipo di programma di bilanciamento del carico **Public**.
4. Seleziona la sottorete a cui vuoi distribuire il tuo programma di bilanciamento del carico.

  Il tuo programma di bilanciamento del carico avrà una delle proprie interfacce di rete in questa sottorete. Assicurati i tuoi server dell'applicazione siano su questa sottorete o raggiungibili da essa. Se necessario, abilita lo spanning delle VLAN.
  {: note}

5. Crea porte e protocolli di applicazione front-end e back-end con la stessa configurazione dei gruppi di servizi che stai attualmente utilizzando nel tuo Local Load Balancer. Per ulteriori informazioni su questa configurazione, fai riferimento a [Configurazione dei parametri di IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters).
6. Per abilitare l'offload SSL, imposta i protocolli front-end su HTTPS e i protocolli di back-end su HTTP. Seleziona quindi lo stesso certificato SSL del tuo Local Load Balancer dalla casella a discesa Certificate. Il certificato che utilizzi con il tuo Local Load Balancer è presente nell'elenco a discesa perché tutti i certificati SSL esistenti sono gestiti tramite l'[IBM Cloud Certificate Store  ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/classic/security/sslcerts){:new_window}.
7. Modifica i tuoi parametri del controllo di integrità se lo desideri, altrimenti utilizza le impostazioni predefinite. Per ulteriori informazioni sui parametri di controllo dell'integrità, fai riferimento a [Parametri di IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks).
8. Fai clic su **Attach Server** per aggiungere eventuali istanze del server che utilizzavi per il tuo servizio Local Load Balancer.
9. Esamina la pagina, conferma l'accordo di servizio e fai quindi clic su **Create**.

Viene visualizzato l'elenco dei programmi di bilanciamento del carico, che mostra tutte le tue istanze del servizio.

Il tuo programma di bilanciamento del carico appena creato potrebbe non essere visualizzato immediatamente in questo elenco. Dopo qualche minuto, il nuovo programma di bilanciamento del carico verrà visualizzato in grigio, a indicare che il suo stato è `Offline`. Dopo qualche altro minuto, il nuovo programma di bilanciamento del carico verrà visualizzato in verde, a indicare che è `Online`. Potresti dover aggiornare la tua schermata per vedere queste modifiche.
{: note}

Facendo clic sul nome del servizio su questa pagina ti sposti alla pagina della panoramica del servizio. Puoi passare alle schede **Protocolli**, **Controlli di integrità** e **Istanze del server** per modificare ulteriormente la tua configurazione. 

## Passo 2: Verifica che il tuo Cloud Load Balancer stia funzionando come previsto
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

Tieni presente, a questo punto, che ora hai due programmi di bilanciamento del carico che funzionano contemporaneamente: il tuo vecchio Local Load Balancer e il nuovo IBM Cloud Load Balancer.
{: important}

Verifica il nuovo IBM Cloud Load Balancer utilizzando il dominio elencato nella pagina di stato precedente, assicurandoti che funzioni nello stesso modo del VIP dal tuo Local Load Balancer.

Aggiorna quindi tutte le ubicazioni che utilizzano il VIP di Local Load Balancer per utilizzare invece il nuovo dominio di Cloud Load Balancer.

Questa configurazione del nuovo Cloud Load Balancer sarà l'unica volta in cui riscontrerai un tempo di inattività o un'interruzione del traffico nel processo di migrazione.
{: note}

## Passo 3: Annulla il tuo vecchio Local Load Balancer
{: #step-3-cancel-your-local-load-balancer}

Dopo che hai sostituito tutti i VIP di Local Load Balancer con il dominio per il tuo nuovo IBM Cloud Load Balancer, e avere verificato che la funzionalità sta funzionando come previsto, puoi annullare in modo sicuro il tuo servizio Local Load Balancer. Per eseguire questa operazione, attieniti alla seguente procedura:

1. Vai alla [pagina di elenco di Local Load Balancer](https://cloud.ibm.com/classic/network/loadbalancing/local).
2. Individua il programma di bilanciamento del carico che puoi eliminare ed espandi la freccia accanto a esso.
3. Fai clic sulla **X** rossa alla fine della riga per annullare il programma di bilanciamento del carico.
