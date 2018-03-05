---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-02"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Foire aux questions
La présente section apporte des réponses aux questions les plus fréquemment posées au sujet de l'équilibreur de charge local.

## Quels sont les produits d'équilibrage de charge offerts par IBM ?
Pour obtenir un comparatif des offres d'équilibrage de charge dans IBM Cloud, consultez cette [rubrique ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://dev-console.bluemix.net/docs/infrastructure/loadbalancer-service/explore-load-balancers.html#explore-load-balancers){: new_window}.

## Quelle différence y a-t-il entre un équilibreur de charge partagé et un équilibreur de charge dédié ?

Il existe deux types d'équilibreurs de charge : un équilibreur partagé et un équilibreur dédié. Avec un équilibreur de charge partagé, plusieurs clients partagent le même périphérique physique et sont limités à un certain nombre de connexions en fonction de leur commande. Les équilibreurs de charge dédiés sont utilisés par un seul client et leur nombre de connexions est limité uniquement par les spécifications du périphérique.

## Qu'est-ce qu'un service ?
Les services sont configurés au sein d'un groupe de services et représentent les serveurs réels auxquels l'équilibreur de charge envoient le trafic. Ils se composent d'une adresse IP de destination, d'un port de destination, d'un diagnostic d'intégrité et d'une pondération.

## Qu'est-ce qu'un groupe de services ?
Un groupe de services représente le moyen par lequel vous configurez le mode de connexion des clients à votre environnement via l'équilibreur de charge. Un groupe de services se compose d'un protocole, d'une méthode d'équilibrage des charges, d'un port virtuel (port auquel se connectent les clients), d'une allocation de connexion (en pourcentage) et des services associés au groupe.

## Pourquoi des erreurs de passerelle 502 se produisent-elles lorsque j'utilise le déchargement SSL ?

Ces erreurs se produisent généralement lorsque le port sortant de l'équilibreur de charge est défini sur le port 443. Si l'équilibrage de charge autorise le trafic sortant, vers votre serveur, vous devez choisir le port non-SSL de votre serveur. Il s'agit généralement du port 80 pour HTTP.

## Puis-je avoir plusieurs certificats SSL sur un seul équilibreur de charge ?

Cela est possible dans certaines configurations. Toutefois, la règle générale veut qu'un seul certificat SSL existe par adresse IP virtuelle (VIP). Un équilibreur de charge local prend en charge une seule VIP, mais cette valeur peut être augmentée en utilisant nos équilibreurs de charge dédiés et d'entreprise.

## Qu'est-ce qu'un port virtuel ?

Dans un équilibreur de charge IBM Cloud, un port représente simplement le port que vous souhaitez utiliser pour exécuter le service. Par exemple, le port 80 pour HTTP.

## Quelle est la méthode d'équilibrage de charge utilisée pour les équilibreurs de type local et dédié ?

Nos équilibreurs de charge sont basés sur un proxy.

## Quels services peuvent bénéficier de l'équilibrage de charge ?

Les services les plus courants sont les ports, tels que HTTP (80), HTTPS (443), FTP (21), DNS (53), POP3 (110) et SMTP (25). Toutefois, n'importe quel service peut bénéficier de l'équilibrage de charge.

## Puis-je ajouter la fonction de déchargement SSL à un équilibreur de charge existant ?

Cette fonctionnalité n'est pas prise en charge actuellement. Vous devez commander un autre équilibreur de charge compatible avec le déchargement SSL.

## Combien de temps faut-il pour installer un équilibreur de charge ?

Les équilibreurs de charge sont installés et prêts à être configurés dans les 5 minutes après votre achat.

## Comment puis-je rétromigrer mon équilibreur de charge local ?

Cette option est disponible uniquement en procédant à l'ouverture d'un ticket.

## Quelles sont les méthodes d'équilibrage proposées par l'équilibreur de charge ?

IBM Cloud offre plusieurs méthodes d'équilibrage, y compris des méthodes uniques et hybrides. Reportez-vous à la rubrique [Méthodes d'équilibrage des charges](load_balancing_methods.html) pour en savoir plus sur chacune des méthodes actuellement offertes.

## Est-il possible d'équilibrer la charge du trafic chiffré SSL avec l'adhérence de session ?

Ceci est possible, mais uniquement avec une méthode d'équilibrage persistante. Les autres méthodes ne sont pas prises en charge, car le trafic est chiffré.

