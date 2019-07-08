---

copyright:
  years: 2017, 2018
lastupdated: "2019-04-22"

keywords: migrate, update, load balancer, local, cloud

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

# Migration d'un équilibreur de charge local vers IBM Cloud Load Balancer

Vous pouvez migrer votre équilibreur de charge local vers un service IBM© Cloud Load Balancer en exécutant la procédure suivante.

## Etape 1 : Commander Cloud Load Balancer
{: #step-1-order-a-cloud-load-balancer}

Pour commander un service IBM Cloud Load Balancer, sélectionnez **IBM Cloud Load Balancer** dans le [catalogue IBM Cloud ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")]( https://cloud.ibm.com/catalog/infrastructure/load-balancer-group){:new_window}. Cliquez sur **Créer**, puis procédez comme suit :

1. Définissez les paramètres de service de base, tels que le nom et la description.
2. Sélectionnez votre centre de données.
3. Sélectionnez un type d'équilibreur de charge **Public**.
4. Sélectionnez le sous-réseau où vous souhaitez déployer votre équilibreur de charge. 

  L'une des interfaces réseau de votre instance de service Load Balancer se trouvera sur ce sous-réseau. Assurez-vous que vos serveurs d'applications sont installés sur ce sous-réseau et sont accessibles à partir de celui-ci. Si nécessaire, activez la superposition (spanning) VLAN.
  {: note}

5. Créez des ports et protocoles d'application de front end et de back end avec la même configuration que les groupes de services que vous utilisez actuellement dans votre équilibreur de charge local. Pour plus d'informations sur cette configuration, voir [Configuration des paramètres de l'équilibreur de charge IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configuring-ibm-cloud-load-balancer-parameters).
6. Pour activer le déchargement SSL, définissez les protocoles de front end sur HTTPS, et ceux de back end sur HTTP. Sélectionnez ensuite dans la zone de liste déroulante Certificat le même certificat SSL que pour votre équilibreur de charge local. Le certificat que vous utilisez avec votre équilibreur de charge local figure dans la liste déroulante car tous les certificats SSL existants sont gérés via le [catalogue de certificats IBM Cloud ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/classic/security/sslcerts){:new_window}.
7. Ajustez les paramètres de diagnostic d'intégrité si besoin, ou utilisez les paramètres par défaut. Pour plus d'informations sur les paramètres de diagnostic d'intégrité, voir [Configuration des paramètres de l'équilibreur de charge IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-configuring-ibm-cloud-load-balancer-parameters#configure-health-checks).
8. Cliquez sur **Connecter un serveur** pour ajouter les instances de serveur utilisées pour votre service d'équilibreur de charge local. 
9. Vérifiez la page, confirmez le contrat de service, puis cliquez sur **Créer**.

La liste des équilibreurs de charge s'affiche, avec toutes vos instances de service.

L'équilibreur de charge que vous venez de créer peut ne pas s'afficher immédiatement dans la liste. Après quelques minutes, il apparaît en grisé, ce qui correspond au statut hors ligne (`Offline`). Patientez encore quelques minutes et il s'affiche en vert, indiquant qu'il est en ligne (`Online`). Vous devrez peut-être actualiser votre écran pour voir ces changements.
{: note}

Lorsque vous cliquez sur le nom du service sur cette page, la page de présentation du service s'ouvre. Vous pouvez accéder aux onglets **Protocoles**, **Diagnostics d'intégrité** et **Instances de serveur ** pour éditer davantage votre configuration.

## Etape 2 : Vérifier que votre équilibreur de charge Cloud Load Balancer fonctionne comme prévu
{: #step-2-verify-your-cloud-load-balancer-is-working-as-expected}

Vous devez être conscient qu'à ce stade, vous disposez de deux équilibreurs de charge travaillant en même temps : votre ancien équilibreur de charge local et le nouvel équilibreur de charge IBM Cloud Load Balancer.
{: important}

Testez le nouvel équilibreur de charge IBM Cloud Load Balancer à l'aide du domaine indiqué à la page de statut ci-dessus, afin de vous assurez qu'il fonctionne de la même façon que le VIP de votre équilibreur de charge local.

Mettez ensuite à jour les emplacements utilisant le VIP de l'équilibreur de charge local pour qu'ils utilisent à la place le nouveau domaine Cloud Load Balancer.

Cette configuration du nouvel équilibreur de charge Cloud Load Balancer constitue le seule moment où vous pourriez connaître un temps d'indisponibilité ou une interruption du trafic lors du processus de migration.
{: note}

## Etape 3 : Annuler votre ancien équilibreur de charge local
{: #step-3-cancel-your-local-load-balancer}

Une fois que vous avez remplacé tous les VIP de l'équilibreur de charge local par le domaine de votre nouvel équilibreur de charge IBM Cloud Load Balancer, et que vous avez vérifié que son bon fonctionnement, vous pouvez alors annuler votre service d'équilibreur de charge local. Pour cela, procédez comme suit :

1. Accédez à la [page de liste d'équilibreurs de charge locaux](https://cloud.ibm.com/classic/network/loadbalancing/local).
2. Localisez l'équilibreur de charge à supprimer et développez la flèche en regard. 
3. Cliquez sur le **X** rouge à la fin de la liste pour annuler l'équilibreur de charge. 
