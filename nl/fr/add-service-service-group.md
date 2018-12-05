---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ajout d'un service à un groupe de services

Après avoir ajouté un groupe de services à un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}), vous pouvez ajouter des services pour commencer le processus d'équilibrage. Vous pouvez ajouter plusieurs services à un groupe de services et appliquer une pondération permettant de hiérarchiser les services quant à la manière dont les périphériques reçoivent la charge de travail. Suivez les étapes ci-dessous pour ajouter un nouveau service à un groupe de services pour un {{site.data.keyword.loadbalancer_short}}.

1. Dans la page [Détails de l'équilibreur de charge local](view-all-load-balancers.html), cliquez sur **Actions > Ajouter service** dans le menu déroulant sur la ligne correspondant au groupe de services où ajouter le service. Vous pouvez également développer les détails du groupe en cliquant sur l'icône Développer en regard de la ligne, puis cliquer sur le bouton **Ajouter service**. Une nouvelle section Service est ajoutée en bas de la section des détails relatifs au groupe de services.
2. Entrez les paramètres du service :
  - **IP de destination :** Adresse IP du serveur de destination.
  - **Port de destination :** Numéro de port à utiliser pour acheminer le trafic vers le serveur de destination.
  - **Diagnostic d'intégrité : **Méthode de diagnostic d'intégrité préférée parmi les options ci-dessous.

     - **Par défaut :** La configuration par défaut est Ping.
     - **HTTP :** La vérification de l'écoute de l'adresse IP sur le port 80 renvoie le code HTTP 200 (OK).
     - **HTTP-PERSO :** Similaire au protocole HTTP, si ce n'est que vous affectez le type de connexion, l'emplacement du diagnostic d'intégrité et la réponse que vous anticipez. Il s'agit d'une option avancée.
     - **Ping :** Test ping simple sur le protocole ICMP.
     - **TCP :** Similaire au test ping, mais sur un réseau explicitement TCP. Cette option doit être utilisée si vos connexions ICMP sont bloquées.
  - **Pondération :** Priorité numérique accordée au service. Le système de pondération permet d'attribuer une valeur numérique aux serveurs devant recevoir le plus gros trafic. Une valeur élevée indique une priorité élevée à condition que le serveur soit en ligne conformément aux diagnostics d'intégrité. Par exemple, si le _server1_ a une pondération de 80 et le _server2_ une pondération de 20, sur 10 connexions reçues, le _server1_ reçoit 8 connexions et le _server2_ 2. Si le _server1_ est déconnecté ou retiré du pool, toutes les connexions sont reçues à partir du _server2_.
  - **Notes :** Zone réservée à la saisie de notes.
3. Cochez la case **Activé** pour activer le service.
4. Cliquez sur le bouton **Enregistrer la configuration** pour ajouter le service. Cliquez sur **Annuler** pour annuler l'action.

Lorsqu'un service est ajouté à un groupe de services, il apparaît dans la grille Services du groupe. S'il est activé, il commence à participer à l'équilibrage de charge en fonction de la pondération sélectionnée au moment de l'ajout du service. S'il est désactivé, il apparaît dans le groupe de services, mais ne participe pas à l'équilibrage tant qu'il n'est pas activé. Les diagnostics d'intégrité sont effectués sur le service à intervalles réguliers et l'état du service apparaît comme actif ou inactif, en fonction des résultats du diagnostic d'intégrité. Les services peuvent être modifiés ou supprimés à tout moment et des diagnostics d'intégrité HTTP Custom peuvent être ajoutés à n'importe quel service existant via le menu déroulant Actions.
