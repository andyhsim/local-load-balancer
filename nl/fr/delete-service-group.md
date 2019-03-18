---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Suppression d'un groupe de services
{: #deleting-a-service-group}

Lorsque vous supprimez un groupe de services, tous les services associés au groupe sont également supprimés. Suivez les étapes ci-dessous pour retirer un groupe de services d'un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}).

1. Dans la page [Détails de l'équilibreur de charge local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), identifiez la ligne du groupe de services à supprimer et cliquez sur **Actions > Supprimer le groupe**.
2. Cliquez sur **Enregistrer la configuration**.

Lorsqu'un groupe de services est supprimé, il est retiré du {{site.data.keyword.loadbalancer_short}}. Tous les services associés sont également supprimés et le port virtuel associé au groupe de services est mis à disposition, au cas où un autre groupe de services serait nécessaire à l'avenir. Lors de la suppression, le pourcentage d'allocation de connexions des groupes de services restants doit être changé manuellement pour tous les groupes restants.
