---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration du déchargement SSL sur un équilibreur de charge

Les équilibreurs de charge peuvent offrir une fonctionnalité de déchargement SSL, qui permet de réduire considérablement la charge sur les systèmes exécutant cette fonction. Pour pouvoir utiliser le déchargement SSL, vous devez acquérir un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}) qui offre cette fonctionnalité. Les équilibreurs de charge compatibles avec cette fonction comportent la mention “avec déchargement SSL” dans la boîte de dialogue **Commander Équilibreur de Charge Local (LLB)**. Lorsque vous disposez d'un {{site.data.keyword.loadbalancer_short}} avec la fonctionnalité de déchargement SSL, vous devez le configurer. Suivez les étapes ci-dessous pour configurer le déchargement SSL sur un {{site.data.keyword.loadbalancer_short}}.

1. Dans la page [Détails de l'équilibreur de charge local](view-all-load-balancers.html), cliquez sur **Actions > Configurer SSL** dans le menu déroulant de l'équilibreur de charge.
2. Sélectionnez le certificat SSL souhaité dans la liste déroulante **Certificat**. Tenez compte des points suivants :
  - Les VIP d'{{site.data.keyword.loadbalancer_short}} non dédiés sont limités à une taille de bit de certificat SSL maximale de 2048.
  - Au moins un certificat SSL doit être stocké sur le portail client pour mener à bien cette étape. Voir [Importation d'un certificat SSL](import-ssl-cert.html).
3. Cochez la case **Activé(e)**.
4. Sélectionnez les chiffrements que vous souhaitez prendre en charge.
5. Cliquez sur le bouton **Mettre à jour**.

Après avoir activé le déchargement SSL sur un {{site.data.keyword.loadbalancer_short}}, SSL passe de l'état **désactivé** à **actif**. En général, la charge supportée par les systèmes qui géraient précédemment les connexions SSL diminue lorsque le déchargement SSL est activé. L'état de déchargement SSL peut être modifié à tout moment. Revenez à l'onglet du déchargement SSL et décochez la case afin de désactiver cette fonctionnalité pour l'équilibreur de charge {{site.data.keyword.loadbalancer_short}}.
