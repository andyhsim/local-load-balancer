---
copyright:
  years: 1994,2017,2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ajout d'un groupe de services à un équilibreur de charge

Après avoir ajouté un équilibreur de charge ({{site.data.keyword.loadbalancer_short}}), vous pouvez à tout moment lui ajouter un nouveau groupe de services. Les groupes de services sont disponibles sous divers types de groupes et proposent une large palette de méthodes d'équilibrage uniques ou hybrides. Lorsque vous ajoutez un nouveau groupe de services, il importe de veiller à ce que la somme des groupes de type Allocation de connexions soit égale à 100 %. Suivez les étapes ci-dessous pour ajouter un nouveau groupe de services à un {{site.data.keyword.loadbalancer_short}}.

1. Dans la page [Détails de l'équilibreur de charge local](view-all-load-balancers.html), cliquez sur le bouton **Ajouter groupe**. Vous pouvez également cliquer sur **Actions > Ajouter groupe**. Une nouvelle section Groupe de services est ajoutée en bas de la page.
2. Sélectionnez le type de groupe de votre choix dans la liste déroulante **Groupe**, ainsi que la méthode d'équilibrage souhaitée dans la liste déroulante **Méthode**. Consultez la rubrique [Méthodes d'équilibrage de charge](load_balancing_methods.html) pour en savoir plus sur chacune des méthodes.
3. Entrez le numéro de port à associer au groupe de services dans la zone **Port virtuel**. Pour plus d'informations, voir la [FAQ sur les ports de service les plus courants](load-balancing-faqs-2.html#what-services-can-be-load-balanced-). 

	**Remarque :** Chaque groupe de services doit être affecté à un port unique. Dans le cas contraire, un message d'erreur est affiché en haut de la page et le groupe de services peut ne pas être ajouté tant qu'un portail virtuel unique n'est pas affecté.
4. Indiquez son affectation dans la zone **Allocation**.
5. Ajoutez des commentaires dans la zone de texte **Notes**, si besoin.
6. Cliquez sur le bouton **Enregistrer la configuration** pour ajouter le nouveau groupe de services. Cliquez sur **Annuler** pour annuler l'action.

Une fois le groupe de services ajouté, vous pouvez le supprimer ou le modifier à tout moment. Vous pouvez réinitialiser les connexions au groupe de services et ajouter de nouveaux services au groupe. Pour qu'un groupe de services commence l'équilibrage de charge en fonction de ses paramètres d'allocation de connexions, un ou plusieurs services doivent être [ajoutés](add-service-service-group.html) au groupe de services.

## Etapes suivantes

[Ajout d'un service au groupe de services](add-service-service-group.html).
