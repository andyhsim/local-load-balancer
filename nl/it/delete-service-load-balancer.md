---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eliminazione di un servizio
{: #deleting-a-service}

Dopo essere stato aggiunto a un gruppo di servizi per un {{site.data.keyword.loadbalancer_short}}, un servizio può essere eliminato in qualsiasi momento. L'eliminazione di un servizio da un gruppo di servizi impedisce al {{site.data.keyword.loadbalancer_short}} di utilizzarlo a meno che non venga aggiunto nuovamente in modo manuale a un gruppo di servizi. 

In alternativa, un servizio può essere disabilitato, operazione che manterrà il servizio associato al gruppo di servizi rendendolo però non disponibile per gli sforzi di bilanciamento. Per mantenere il servizio associato al gruppo di servizi del {{site.data.keyword.loadbalancer_short}}, [modifica il servizio](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) e deseleziona la casella di spunta **Enabled**. 

Atteniti alla seguente procedura per eliminare il servizio dal {{site.data.keyword.loadbalancer_short}}.

1. Dalla pagina [Local Load Balancer Details](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), individua il servizio che vuoi eliminare ed espandi la freccia sul lato sinistro.
2. Fai clic sulla 'x' rossa alla fine della riga del servizio.
3. Fai clic su **Save Configuration** in fondo alla pagina perché le impostazioni vengano aggiornate.

Dopo l'eliminazione del servizio, la configurazione verrà salvata e le modifiche diventeranno istantaneamente effettive. Se il servizio eliminato è il solo associato a un gruppo di servizi, il gruppo non potrà eseguire alcuna attività di bilanciamento del carico a meno che non venga aggiunto un nuovo servizio.
