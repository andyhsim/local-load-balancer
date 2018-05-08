---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-02"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Domande frequenti (FAQ)
Questo argomento contiene le risposte alle domande frequenti sul programma di bilanciamento del carico locale.

## Quali prodotti di bilanciamento del carico offre IBM?
Per un confronto dettagliato delle offerte di bilanciamento del carico in IBM Cloud, fai riferimento a questo [argomento ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## Qual è la differenza tra un programma di bilanciamento del carico condiviso e uno dedicato?

Ci sono due tipi di programmi di bilanciamento del carico: condivisi e dedicati. Con un programma di bilanciamento del carico condiviso, diversi clienti condividono lo stesso dispositivo fisico e sono limitati a uno specifico numero di connessioni, a seconda di cosa sia stato ordinato. I programmi di bilanciamento del carico dedicati sono utilizzati solo da un singolo cliente e le relative connessioni sono limitate solo dalle specifiche del dispositivo.

## Cos'è un servizio?
I servizi sono configurati all'interno di un gruppo di servizi e rappresentano i server reali a cui il programma di bilanciamento del carico bilancerà il traffico. Consistono in un IP di destinazione, una porta di destinazione, il controllo dell'integrità e il peso.

## Cos'è un gruppo di servizi?
Un gruppo di servizi è lo strumento con cui configuri il modo in cui i client stabiliscono una connessione al loro ambiente tramite il programma di bilanciamento del carico. Un gruppo di servizi consiste in un protocollo, un metodo di bilanciamento del carico, una porta virtuale (che è la porta a cui si connetteranno i client), un'allocazione delle connessioni (percentuale) e i servizi associati al gruppo.

## Perché sto ricevendo degli errori 502 relativi al gateway quando utilizzo l'offload SSL?

Ciò è di norma causato dalla porta in uscita del programma di bilanciamento del carico che è impostata sulla porta 443. Se il bilanciamento del carico è abilitato, il traffico in uscita al tuo server dovrà essere impostato alla porta non SSL del tuo server. È di norma la porta 80 per HTTP.

## Posso avere più certificati SSL su un singolo programma di bilanciamento del carico?

Ciò è possibile in specifiche configurazioni. La regola generale è un certificato SSL per VIP (Virtual IP). Un programma di bilanciamento del carico locale supporta un singolo VIP ma ciò può essere aumentato sui nostri programmi di bilanciamento del carico dedicati e aziendali.

## Cos'è una porta virtuale?

Una porta virtuale in un programma di bilanciamento del carico IBM Cloud è semplicemente la porta su cui desideri eseguire il servizio. Un esempio è la porta 80 per HTTP.

## Quale metodo di bilanciamento del carico viene utilizzato per i programmi di bilanciamento del carico locali e dedicati?

I nostri programmi di bilanciamento del carico sono basati sul proxy.

## Per quali servizi è possibile bilanciare il carico?

I più comuni sono le porte come HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3 (110) e SMTP (25). È tuttavia possibile bilanciare il carico di qualsiasi servizio.

## Posso aggiungere l'offload SSL a un programma di bilanciamento del carico esistente?

Ciò non è attualmente supportato. Occorrerà effettuare un nuovo ordine per un programma di bilanciamento del carico con l'offload SSL.

## Quanto tempo ci vuole per installare un programma di bilanciamento del carico?

I programmi di bilanciamento del carico dovrebbero essere installati e disponibili per la tua configurazione cinque minuti circa dopo l'acquisto.

## Come posso eseguire il downgrade del mio programma di bilanciamento del carico locale?

Questa opzione è disponibile solo aprendo un ticket.

## Quali metodi di bilanciamento del carico sono disponibili con un programma di bilanciamento del carico?

IBM Cloud offre più metodi di bilanciamento, inclusi sia metodi singoli che ibridi. Fai riferimento a [Metodi di bilanciamento del carico](load_balancing_methods.html) per ulteriori informazioni su ciascun metodo di bilanciamento del carico da noi attualmente offerto.

## È possibile bilanciare il carico del traffico con crittografia SSL con la persistenza di sessione?

Ciò è possibile ma solo con un metodo di bilanciamento persistente. Gli altri metodi non sono supportati poiché il traffico è crittografato.

