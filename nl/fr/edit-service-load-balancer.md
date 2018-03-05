---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Modification d'un service 

Après avoir ajouté un service au groupe de services de l'équilibreur de charge, vous pouvez le modifier à tout moment. Vous pouvez modifier tous les paramètres de base d'un service et vous pouvez également ajouter des notes supplémentaires à l'aide de la fonction d'édition. 

Suivez les étapes ci-dessous pour modifier un service.

1. Dans la page [Détails de l'équilibreur de charge local](view-all-load-balancers.html), recherchez le service que vous souhaitez modifier en développant la flèche sur la gauche.
2. Modifiez les zones suivantes, selon vos besoins :
  - **IP de destination :** Adresse IP du serveur de destination.
  - **Port de destination :** Numéro de port utilisé pour acheminer le trafic au serveur de destination.
  - **Diagnostic d'intégrité :** Méthode de diagnostic d'intégrité préférée parmi les options ci-dessous.
      - **Par défaut :** La configuration par défaut est Ping.
      - **HTTP :** La vérification de l'écoute de l'adresse IP sur le port 80 renvoie le code HTTP 200 (OK).
      - **HTTP-PERSO :** Similaire au protocole HTTP, si ce n'est que vous affectez le type de connexion, l'emplacement de votre diagnostic d'intégrité et la réponse que vous anticipez. Il s'agit d'une option avancée.
      - **Ping :** Test ping simple sur le protocole ICMP.
      - **TCP :** Similaire au test ping, mais sur un réseau explicitement TCP. Cette option doit être utilisée si vos connexions ICMP sont bloquées.
  - **Pondération :** Priorité numérique accordée au service. Le système de pondération permet d'attribuer une valeur numérique aux serveurs devant recevoir le plus gros trafic. Une valeur élevée indique une priorité élevée à condition que le serveur soit en ligne conformément aux diagnostics d'intégrité. Par exemple, si le _server1_ a une pondération de 80 et le _server2_ une pondération de 20, sur 10 connexions reçues, le _server1_ reçoit 8 connexions et le _server2_ 2. Si le _server1_ est déconnecté ou retiré du pool, toutes les connexions sont reçues à partir du _server2_.
  - **Notes :**  Zone de texte libre.
  - **Activé(e) :** Cochez ou décochez cette case pour activer ou désactiver le service.
3. Cliquez sur le bouton **Enregistrer la configuration** pour mettre à jour le service. Cliquez sur **Annuler** pour annuler l'action.

Une fois que vous avez modifié un service, les modifications apparaissent dans la ligne qui contient le service dans la ligne correspondante. Vous pouvez effectuer des modifications supplémentaires à tout moment en répétant les étapes ci-dessus.
