---
copyright:
  years: 1994, 2017
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:note: .note}

# Limitations connues pour l'équilibreur de charge local
{: #known-limitations-with-local-load-balancer}

Compte tenu de la nature d'un équilibreur de charge proxy, l'IP source de la demande client provient de l'IP de l'équilibreur de charge. Ceci aura des effets sur les programmes statistiques de journaux et autres applications utilisant l'IP source pour obtenir les informations sur le client. IBM© Cloud fournit une solution permettant de réécrire correctement les entrées de journaux pour Apache (toutes plateformes) et IIS (Windows).

Pour accéder aux instructions et plug-in supplémentaires, vous devez d'abord vous connecter au réseau privé virtuel (VPN) IBM Cloud. Une fois connecté, accédez à la [page des téléchargements ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](http://downloads.softlayer.local/loadbalancer/){: new_window} et recherchez les plug-in et instructions relatifs à votre {{site.data.keyword.loadbalancer_short}}.

Vous devez être connecté au VPN IBM Cloud pour accéder au lien de téléchargement.
{: note}
