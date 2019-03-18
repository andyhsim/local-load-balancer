---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Limitazioni note per il programma di bilanciamento del carico locale
{: #known-limitations-with-local-load-balancer}

A causa della natura di un programma di bilanciamento del carico proxy, l'IP origine della richiesta client proviene dall'IP del programma di bilanciamento del carico. Ciò influenzerà i programmi statistici dei log e altre applicazioni che guardano all'IP di origine per ottenere informazioni sul client. IBM© Cloud fornisce una soluzione per riscrivere correttamente le voci di log per Apache (tutte le piattaforme) e IIS (Windows). 

Per accedere alle istruzioni e ai plugin aggiuntivi necessari, devi prima essere connesso alla VPN di IBM Cloud. Dopo aver stabilito la connessione, visita la [pagina dei download ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](http://downloads.softlayer.local/loadbalancer/){: new_window} per trovare i plugin e le istruzioni per il tuo {{site.data.keyword.loadbalancer_short}}.

**NOTA:** devi aver eseguito l'accesso alla VPN di IBM Cloud per accedere al link di download.
