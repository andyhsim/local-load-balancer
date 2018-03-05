---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration des pondérations pour l'équilibreur de charge

Le système des pondérations permet d'attribuer une valeur numérique aux serveurs auxquels vous souhaitez affecter le plus gros trafic. Une valeur élevée indique une priorité élevée à condition que le serveur soit en ligne conformément aux diagnostics d'intégrité.   

Par exemple, si le _server1_ a une pondération de 80 et le _server2_ une pondération de 20, sur 10 connexions reçues, le _server1_ reçoit 8 connexions et le _server2_ 2. Si le _server1_ est déconnecté ou retiré du pool, toutes les connexions sont reçues à partir du _server2_.

Vous pouvez configurer les pondérations pour un service particulier lors de l'[ajout d'un service à un groupe de services](add-service-service-group.html) ou lors de la [modification du service](edit-service-load-balancer.html) après sa création.

Une fois la configuration enregistrée, vos modifications prendront immédiatement effet. Vous pouvez surveiller les connexions du service à partir de la page des détails de ce service.
