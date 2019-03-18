---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eliminazione di un gruppo di servizi
{: #deleting-a-service-group}

Quando si elimina un gruppo di servizi, verranno eliminati anche tutti i servizi associati al gruppo. Attieniti alla procedura di seguito per eliminare un gruppo di servizi per un {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), identifica la riga del gruppo di servizi che desideri eliminare e fai clic su **Actions > Remove Group**.
2. Fai clic su **Save Configuration**.

Dopo l'eliminazione, un gruppo di servizi verrà rimosso dal {{site.data.keyword.loadbalancer_short}}. Verranno eliminati anche tutti i servizi associati e la porta virtuale associata al gruppo di servizi sarà disponibile, nel caso serva per un altro gruppo di servizi in futuro. Quando viene eseguita l'operazione di eliminazione, la percentuale di allocazione delle connessioni per i gruppi di servizi restanti deve essere modificata manualmente per i gruppi restanti.
