---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Méthodes d'équilibrage de charge
{: #load-balancing-methods}

| Méthode|Description|
|:---|:---|
|Adresse IP de Hachage|<ul><li>Mappe les demandes client aux serveurs réels en hachant les IP source de la demande.</li><li>Les relations client/serveur sont maintenues sur les ports.</li></ul>|
|Insérer Cookie|<ul><li>Insère un cookie de suivi dans la demande.<span style="mso-spacerun:yes">&nbsp; </span>Les données de session contenues dans le cookie sont utilisées avec la demande suivante pour renvoyer le trafic au même serveur réel.</li><li>La persistance est codée en dur à chaque session.</li><li>Le cookie expire à la fermeture du navigateur du client.</li><li>Nécessite que le client accepte les cookies.</li></ul>|
|Connexions minimum|<ul><li>Le serveur réel ayant le plus petit nombre de connexions actives est prioritaire.</li><li>L'algorithme requiert un écart de 10 connexions, ce qui peut biaiser les résultats pour les clients</li></ul>|
|IP permanente|<ul><li>Lie l'IP source du demandeur au serveur réel qui traite la demande par un hachage des 4 octets de l'adresse IP de demande.</li><li>La persistance dure 60 minutes</li></ul>|
|Round Robin|<ul><li>Chaque nouvelle demande est attribuée au serveur suivant de la série.</li><li>Les accès sont répartis de manière équilibrée sur de grands échantillons, bien que de petits échantillons puissent afficher une quantité disproportionnée.</li></ul>|
|Temps de réponse minimum|<ul><li>Le serveur avec le temps de réponse le plus court reçoit la demande.</li><li>A mesure que le temps de charge et de réponse augmente, les serveurs plus lents commencent à renseigner moins de demandes.</li></ul>|
|Round Robin avec IP permanente|<ul><li>Chaque nouvelle demande est attribuée au serveur suivant de la série.</li><li>L'adresse IP du demandeur est liée au serveur réel, ce qui a pour conséquence d'affecter les demandes suivantes de l'IP au même serveur réel.</li></ul>|
|Round Robin avec Insérer Cookie|<ul><li>Chaque nouvelle demande est attribuée au serveur suivant de la série.</li><li>L'équilibreur de charge insère un cookie dans la demande et utilise les informations de session du cookie pour acheminer le trafic vers le même serveur réel pour les demandes suivantes.</li></ul>|
|Connexions minimum avec IP permanente|<ul><li>Chaque nouvelle demande est attribuée au serveur réel possédant le plus petit nombre de connexions actives.</li><li>L'adresse IP du demandeur est liée au serveur réel, ce qui a pour conséquence d'affecter les demandes suivantes de l'IP au même serveur réel.</li></ul>|
|Connexions minimum avec Insérer Cookie|<ul><li>Chaque nouvelle demande est attribuée au serveur réel possédant le plus petit nombre de connexions actives.</li><li>L'équilibreur de charge insère un cookie dans la demande et utilise les informations de session du cookie pour acheminer le trafic vers le même serveur réel pour les demandes suivantes.</li></ul>|
|Temps de réponse minimum avec IP permanente|<ul><li>Chaque nouvelle demande est attribuée au serveur réel ayant le temps de réponse le plus court.</li><li>L'adresse IP du demandeur est liée au serveur réel, ce qui a pour conséquence d'affecter les demandes suivantes de l'IP au même serveur réel.</li></ul>|
|Temps de réponse minimum avec Insérer Cookie|<ul><li>Chaque nouvelle demande est attribuée au serveur réel ayant le temps de réponse le plus court.</li><li>L'équilibreur de charge insère un cookie dans la demande et utilise les informations de session du cookie pour acheminer le trafic vers le même serveur réel pour les demandes suivantes.</li></ul>|
