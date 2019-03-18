---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Suppression d'un service
{: #deleting-a-service}

Après avoir ajouté un service à un groupe de services d'un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}), vous pouvez le supprimer à tout moment. Lorsque vous retirez un service d'un groupe de services, l'équilibreur de charge {{site.data.keyword.loadbalancer_short}} ne peut plus l'utiliser sauf s'il est à nouveau ajouté à un groupe de services. 

Vous pouvez également désactiver un service, ce qui permet de conserver le service associé au groupe de services tout en le rendant indisponible pour l'équilibrage. Pour conserver le service associé au groupe de services du {{site.data.keyword.loadbalancer_short}}, [modifiez le service](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-editing-a-service) et décochez la case **Activé(e)**. 

Suivez les étapes ci-dessous pour supprimer le service du {{site.data.keyword.loadbalancer_short}}.

1. Dans la page [Détails de l'équilibreur de charge local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), recherchez le service que vous souhaitez supprimer et développer la flèche sur le côté gauche.
2. Cliquez sur le signe 'x' rouge à la fin de la ligne du service.
3. Cliquez sur **Enregistrer la configuration** au bas de la page pour mettre à jour les paramètres.

Une fois le service supprimé, la configuration est sauvegardée et les modifications prennent effet immédiatement. Si le service associé est le seul service associé à un groupe de services, le groupe ne peut pas effectuer les activités d'équilibrage de charge tant qu'un nouveau service n'est pas ajouté.
