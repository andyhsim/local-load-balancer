---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-01-24"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Modification d'un groupe de services

Après avoir ajouté un groupe de services à un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}), vous pouvez modifier ses paramètres de base (y compris la méthode d'équilibrage et le port virtuel), l'allocation de connexions, ainsi que les notes. Les modifications apportées à chaque groupe de services sont visibles immédiatement et vous pouvez effectuer des modifications supplémentaires à tout moment. 

Si le type de groupe d'un groupe de services doit être modifié, le groupe de services doit être supprimé et un nouveau groupe de services ajouté de manière à refléter le type de groupe souhaité. 

Suivez les étapes ci-dessous pour modifier un groupe de services existant d'un {{site.data.keyword.loadbalancer_short}}.

1. Dans la page [Détails de l'équilibreur de charge local](view-all-load-balancers.html), développez les détails du groupe de services en cliquant sur l'icône Développer située en regard de la ligne correspondant au groupe de services à modifier.
2. Mettez à jour les paramètres du groupe de services : 
  - **Méthode :** Sélectionnez une [méthode d'équilibrage](load_balancing_methods.html) dans la liste déroulante.
  - **Port virtuel :** Numéro de port à utiliser pour le groupe de services. Pour plus d'informations, voir la [FAQ sur les ports de service les plus courants](load-balancing-faqs-2.html#what-services-can-be-load-balanced-). 

  	**Remarque :** Chaque groupe de services doit être affecté à un port unique. Dans le cas contraire, un message d'erreur est affiché en haut de la page et le groupe de services peut ne pas être ajouté tant qu'un port virtuel unique n'est pas affecté.

  - **Allocation :** Allocation du groupe de services.
  - **Notes :** Texte libre pour identifier le groupe de services.
3. Cliquez sur le bouton **Enregistrer la configuration** pour mettre à jour le groupe de services. Cliquez sur le bouton **Annuler** pour annuler l'action.

Les modifications apportées au groupe de services seront répercutées sur l'écran des détails sous le groupe associé. Si une modification a été apportée à l'allocation de connexions, des modifications supplémentaires peuvent être nécessaires pour d'autres groupes de services. Si la méthode d'équilibrage a été modifiée, les services associés au groupe peuvent nécessiter des modifications supplémentaires afin de s'aligner sur la nouvelle méthode d'équilibrage. Vous pouvez effectuer ces modifications quand bon vous semble en répétant les étapes ci-dessus.
