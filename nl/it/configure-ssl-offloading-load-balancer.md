---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configurazione dell'offload SSL su un programma di bilanciamento del carico
{: #configuring-ssl-offloading-on-a-load-balancer}

I Load Balancers possono fornire l'offload SSL, che può ridurre notevolmente il carico sui sistemi che attualmente stanno eseguendo la funzione. Per utilizzare l'offload SSL, è necessario acquistare un {{site.data.keyword.loadbalancer_short}} che offre la funzionalità. I programmi di bilanciamento del carico che offrono la funzionalità SSL sono indicati come “with SSL offload” nella finestra di dialogo **Order Local Load Balancer**. Dopo che è stato eseguito il provisioning del {{site.data.keyword.loadbalancer_short}} abilitato all'offload SSL, è necessario configurarlo. Attieniti alla procedura di seguito per configurare l'offload SSL su un {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), fai clic su **Actions > Configure SSL** nel menu a discesa per il programma di bilanciamento del carico.
2. Seleziona il certificato SSL desiderato dalla casella a discesa **Certificate**. Nota quanto segue:
  - I VIP (virtual IP) {{site.data.keyword.loadbalancer_short}} non dedicati sono limitati a una dimensione in bit dei certificati SSL massima di 2048.
  - Almeno un certificato SSL deve essere archiviato sul Portale del cliente per completare correttamente questo passo. Fai riferimento a [Importazione di un certificato SSL](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-importing-an-ssl-certificate).
3. Seleziona la casella di spunta **Enabled**.
4. Seleziona le crittografie che desideri supportare.
5. Fai clic sul pulsante **Update**.

Dopo l'attivazione dell'offload SSL su un {{site.data.keyword.loadbalancer_short}}, lo stato dell'SSL cambia da **disabled** a **active**. Il carico trasportato dai sistemi che precedentemente gestivano le connessioni SSL generalmente si ridurrà dopo l'attivazione dell'offload SSL. Lo stato dell'offload SSL può essere modificato in qualsiasi momento. Ritorna alla scheda Offload SSL e deseleziona la casella di spunta per disabilitare l'offload SSL per il {{site.data.keyword.loadbalancer_short}}.
