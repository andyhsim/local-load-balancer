---
copyright:
  years: 1994, 2017 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Réinitialisation de connexions pour un groupe de services
{: #resetting-connections-for-a-service-group}

Lorsqu'un groupe de services est actif sur un équilibreur de charge, une connexion peut exister pour chaque service associé à ce groupe en fonction du mode choisi par les clients pour utiliser le service. Les clients peuvent parfois être connectés à un ou plusieurs services pendant un laps de temps inapproprié. Les connexions étant considérées comme des ressources limitées, il peut s'avérer nécessaire de réinitialiser manuellement les connexions d'un groupe de services afin de garantir que d'autres clients ont la possibilité d'utiliser l'équilibreur de charge. Suivez les étapes ci-dessous pour réinitialiser les connexions d'un équilibreur de charge.

1. Dans la page [Détails de l'équilibreur de charge local](/docs/infrastructure/local-load-balancer?topic=local-load-balancer-viewing-local-load-balancer-details), recherchez la ligne correspondant au groupe de services pour lequel réinitialiser les connexions et cliquez sur **Actions > Réinitialiser Connexions**.
2. Validez l'action en cliquant sur **Oui**. Cliquez sur **Non** pour annuler l'action.

Après avoir demandé la réinitialisation de toutes les connexions actives, le groupe de services abandonne les connexions actives pour chaque service. Une zone de texte verte s'affiche en haut de l'écran pour confirmer la bonne réinitialisation des connexions. Lorsque les connexions sont abandonnées, les clients peuvent se reconnecter, si nécessaire. 

Vous pouvez répéter les étapes ci-dessus pour réinitialiser les connexions du groupe de services à tout moment.
