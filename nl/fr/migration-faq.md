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

# Migration d'IBM Cloud Load Balancer - Foire aux questions
{: #migration-faq}

Ci-après les questions les plus fréquemment posées s'appliquant au processus de migration de l'équilibreur de charge local IBM. 

## Quelles sont les dates d'annonce et d'effet concernant la fin de marketing (EOM) de l'équilibreur de charge local ?
{: faq}

La date d'annonce est le 1er mars 2019 et la date d'effet le 1er juin 2019. Aucune nouvelle vente ne peut avoir lieu passé cette date.

## Le support sera-t-il disponible après la date EOM ?
{: faq}

Oui, support sera disponible pour les client existants de l'équilibrage de charge local.

## Comment m'initier à IBM Cloud Load Balancer ?
{: faq}

Nous recommandons de commencer par la lecture de la [documentation IBM Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-getting-started).

## Existe-t-il un chemin de migration depuis le service de l'équilibreur de charge local vers IBM Cloud Load Balancer ?
{: faq}

Aucun chemin de migration automatisé n'existe. Vous pouvez néanmoins demander que votre service d'équilibreur de charge local soit désactivé et commander le service Cloud Load Balancer depuis la console IBM Cloud.

## Quelle est la différence entre les équilibreurs de charge local et cloud ?
{: faq}

L'équilibreur de charge local st un service d'équilibrage de charge local matériel, tandis qu'IBM Cloud Load Balancer est un service natif cloud qui offre une solution d'équilibrage de charge avec mise à l'échelle automatique et abordable, avec support pour les réseaux publics et privés.

## Est-ce que Cloud Load Balancer utilise la même terminologie que l'équilibreur de charge local ?
{: faq}

Pas toujours. Le tableau suivant répertorie les termes clés de l'équilibreur de charge local avec les termes correspondants et différents de Cloud Load Balancer.

| Terme de l'équilibreur de charge local | Terme Cloud Load Balancer |
| ------------- | ------------- |
| Groupes de service | Protocoles |
| Service | Instances de serveur |
| VIP | FQDN/nom de domaine complet |

## Est-ce que je disposerai toujours d'une adresse IP fixe unique pour mon équilibreur de charge lorsque je migrerai vers Cloud Load Balancer ?
{: faq}

Les adresses IP pour IBM Cloud Load Balancer ne sont pas fixes. Cloud Load Balancer affecte des instances d'équilibreur de charge à partir d'un pool, ce qui nécessite en permanence un nom de domaine complet (FQDN). De ce fait, l'adresse IP individuelle d'un équilibreur de charge Cloud Load Balancer peut changer.

## IBM Cloud Load Balancer est-il disponible pour les solutions bare metal et de VSI public/privé ?
{: faq}

Oui, Cloud Load Balancer est disponibles pour les VSI publics et privés, ainsi que pour les serveurs bare metal.

## IBM Cloud Load Balancer est-il conforme au règlement général sur la protection des données (RGPD) ?
{: faq}

Oui, l'offre Cloud Load Balancer est conforme au RGPD.

## Une fois la migration débutée, combien de temps d'indisponibilité ou d'interruption du trafic sur mon système dois-je prévoir ?

Vous n'aurez pas de temps d'indisponibilité ni d'interruption du trafic suite à la migration de l'équilibreur de charge. La seule durée d'indisponibilité ou interruption du trafic que vous pourriez rencontrer concerne le passage de votre configuration de l'équilibreur de charge local au nouveau nom de domaine complet IBM Cloud Load Balancer.

## Selon vos instructions, il faut commander IBM Cloud Load Balancer avant d'annuler l'équilibreur de charge local. Y aura-t-il un impact sur mon système ou ma charge de travail durant la configuration des deux dispositifs ?

Non, Cloud Load Balancer et l'équilibreur de charge local constituent deux offres distinctes qui fonctionnent indépendamment. 

## J'avais l'habitude de choisir une option "connexions par seconde" avec mon équilibreur de charge local. Est-ce que je devrai également configurer cette option avec Cloud Load Balancer ?

Non. IBM Cloud Load Balancer ajuste automatiquement sa capacité de charge. Pour plus d'informations, consultez la rubrique [Mise à l'échelle horizontale de Cloud Load Balancer](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-performing-ibm-cloud-load-balancer-basics#horizontal-scaling).

## Parmi quels protocoles puis-je choisir pour utiliser Cloud Load Balancer ?

Vous disposez des protocoles HTTP, HTTPS et TCP. Nous proposons également un support de Layer 7. Voir [Présentation des fonctionnalités](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-about-ibm-cloud-load-balancer#overview-of-features) pour plus d'informations.

## J'ai besoin d'un type de chiffrement particulier. Est-ce que Cloud Load Balancer prend en charge ce besoin ?

IBM Cloud Load Balancer prend en charge TLS version 1.2 avec déchargement SSL. Vous trouverez des informations supplémentaires sur les chiffrements SSL pris en charge dans [Cloud Load Balancer - Suites de chiffrement SSL](/docs/infrastructure/loadbalancer-service?topic=loadbalancer-service-ssl-offload-with-ibm-cloud-load-balancer#ssl-cipher-suites). 
