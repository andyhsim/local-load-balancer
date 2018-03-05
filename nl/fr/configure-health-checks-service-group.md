---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration des diagnostics d'intégrité pour un service

Les diagnostics d'intégrité sont conçus pour vérifier régulièrement si un serveur est en ligne et accepter le trafic entrant et sortant de l'équilibreur de charge ({{site.data.keyword.loadbalancer_short}}). Les diagnostics d'intégrité sont conçus pour répondre par ACTIF ou INACTIF selon le délai d'attente défini. L'intervalle par défaut est de 120 secondes.

Il existe plusieurs méthodes de configuration des diagnostics d'intégrité.

- **Par défaut :** La configuration par défaut est Ping.
- **HTTP :** La vérification de l'écoute de l'adresse IP sur le port 80 renvoie le code HTTP 200 (OK).
- **HTTP-PERSO :** Similaire au protocole HTTP, si ce n'est que vous affectez le type de connexion, l'emplacement du diagnostic d'intégrité et la réponse que vous anticipez. Il s'agit d'une option avancée.
- **Ping :** Test ping simple sur le protocole ICMP.
- **TCP :** Similaire au test ping, mais sur un réseau explicitement TCP. Cette option doit être utilisée si vos connexions ICMP sont bloquées.

Vous pouvez configurer des diagnostics d'intégrité pour un service particulier lors de l'[ajout d'un service à un groupe de services](add-service-service-group.html) ou lors de la [modification du service](edit-service-load-balancer.html) après sa création.

Une fois la configuration enregistrée, vos modifications prendront immédiatement effet. Vous serez alors en mesure de surveiller l'état des diagnostics d'intégrité à partir de l'icône de statut dans le groupe de services.
