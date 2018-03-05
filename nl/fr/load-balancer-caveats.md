---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-07"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Limitations connues

Compte tenu de la nature d'un équilibreur de charge proxy, l'IP source de la demande client provient de l'IP de l'équilibreur de charge. Ceci aura des effets sur les programmes statistiques de journaux et autres applications utilisant l'IP source pour obtenir les informations sur le client. IBM Cloud fournit une solution permettant de réécrire correctement les entrées de journaux pour Apache (toutes plateformes) et IIS (Windows).

Pour accéder aux instructions et plug-in supplémentaires, vous devez d'abord vous connecter au réseau privé virtuel [IBM Cloud VPN](https://console.bluemix.net/docs/infrastructure/iaas-vpn/getting-started.html){: new_window}. Une fois connecté, accédez à la page des [téléchargements](http://downloads.softlayer.local/loadbalancer/){: new_window} et recherchez les plug-in et instructions relatifs à votre {{site.data.keyword.loadbalancer_short}}.
