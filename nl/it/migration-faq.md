---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud, faq, support

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
{:faq: data-hd-content-type='faq'}

# Domande frequenti sulla migrazione di IBM Cloud Load Balancer
{: #migration-faq}

Le seguenti domande frequenti si applicano al processo di migrazione di IBM Local Load Balancer.

## Quali sono la data di annuncio e quella effettiva per la fine della commercializzazione (EOM - End of Marketing - di Local Load Balancer?
{: faq}

La data di annuncio della fine della commercializzazione è il 1° marzo 2019 e la data effettiva è il 1° giugno 2019. Nessuna nuova vendita può avere luogo dopo questa data.

## Sarà disponibile il supporto dopo la fine della commercializzazione?
{: faq}

Sì, il supporto sarà disponibile per i clienti di Local Load Balancer esistenti.

## Come inizio a lavorare con IBM Cloud Load Balancer?
{: faq}

Ti consigliamo di iniziare leggendo la [documentazione di IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started).

## Esisterà un percorso di migrazione dal servizio Local Load Balancer a IBM Cloud Load Balancer?
{: faq}

Non esisterà alcun percorso di migrazione automatizzato. Tuttavia, puoi richiedere che il tuo servizio Local Load Balancer venga disattivato e ordinare il servizio Cloud Load Balancer dalla console IBM Cloud.

## Quale è la differenza tra Local Load Balancer e Cloud Load Balancer?
{: faq}

Local Load Balancer è un servizio di bilanciamento del carico locale basato sull'hardware mentre IBM Cloud Load Balancer è un servizio nativo del cloud che offre una soluzione di bilanciamento del carico conveniente e a ridimensionamento automatico con un supporto sia per le reti pubbliche che per quelle private.

## Cloud Load Balancer usa la stessa terminologia di Local Load Balancer.
{: faq}

In alcuni casi, non lo fa. La seguente tabella mette a confronto i termini chiave in Local Load Balancer con i loro termini corrispondenti e differenti.

| Termine di Local Load Balancer  | Termine di Cloud Load Balancer |
| ------------- | ------------- |
| Gruppi di servizi | Protocolli |
| Servizio | Istanze del server |
| VIP | FQDN |

## Avrò ancora un singolo indirizzo IP fisso per il mio programma di bilanciamento del carico quando eseguo la migrazione a Cloud Load Balancer?
{: faq}

Gli IP per IBM Cloud Load Balancer non sono fissi. Cloud Load Balancer assegna le istanze del programma di bilanciamento del carico da un pool, che richiede sempre un FQDN (fully-qualified domain name). Di conseguenza, il singolo indirizzo IP di un Cloud Load Balancer può variare.

## IBM Cloud Load Balancer è disponibile per le VSI pubbliche/private e le soluzioni Bare metal?
{: faq}

Sì, Cloud Load Balancer è disponibile per le VSI pubbliche e private, così come Bare metal.

## IBM Cloud Load Balancer è conforme al GDPR?
{: faq}

Sì, l'offerta Cloud Load Balancer è conforme al GDPR.

## Dopo che ho iniziato la migrazione, quanto tempo di inattività o di interruzione del traffico posso aspettarmi con il mio sistema?

Non riscontrerai tempi di inattività o interruzioni del traffico a seguito della migrazione del programma di bilanciamento del carico. I soli tempi di inattività o le sole interruzioni del traffico che potresti riscontrare possono verificarsi quando aggiorni la tua configurazione del Local Load Balancer al nuovo FQDN di IBM Cloud Load Balancer.

## Le vostre istruzioni indicano di ordinare IBM Cloud Load Balancer prima che io annulli il Local Load Balancer. Ci saranno ripercussioni sul mio sistema o sul mio carico di lavoro mentre configuro i due dispositivi?

No, Cloud Load Balancer e Local Load Balancer sono due offerte separate che funzionano in modo indipendente.

## Di solito sceglievo un'opzione di "connessioni al secondo" con il Local Load Balancer. Devo configurarla anche con il Cloud Load Balancer?

No. IBM Cloud Load Balancer regola automaticamente la sua capacità di carico. Puoi trovare ulteriori informazioni in merito nell'argomento relativo al [ridimensionamento orizzontale di Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling).

## Quali protocolli posso scegliere quando utilizzo il Cloud Load Balancer?

Puoi scegliere i protocolli HTTP, HTTPS e TCP. Offriamo anche il supporto L7. Per ulteriori informazioni, fai riferimento alla [Panoramica delle funzioni](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features).

## Ho bisogno di un particolare tipo di cifratura. Cloud Load Balancer lo supporta?

IBM Cloud Load Balancer supporta TLS versione 1.2 con offload SSL. Puoi trovare ulteriori informazioni sulle cifrature SSL supportate in [Suite di cifratura SSL di Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites)
