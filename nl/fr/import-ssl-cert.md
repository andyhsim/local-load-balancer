---
copyright:
  years: 1994, 2017, 2018
lastupdated: "2018-11-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Importation d'un certificat SSL
{: #importing-an-ssl-certificate}

Après avoir émis un certificat SSL pour un site Web, vous pouvez l'importer dans le portail client. Lorsque vous importez des certificats SSL dans le portail client, les certificats peuvent être appliqués aux produits et aux services qui en ont besoin, tels que le déchargement SSL de l'équilibreur de charge. Par défaut, les certificats SSL émis par IBM© Cloud ne sont pas importés dans la liste, car ils sont censés être utilisés uniquement par le destinataire. Par conséquent, tous les certificats SSL à utiliser avec un produit ou un service IBM doivent être importés manuellement par un utilisateur autorisé sur le compte.

Exécutez la procédure ci-après pour importer un certificat SSL dans le portail client.

1. Depuis votre navigateur, ouvrez le [portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} et connectez-vous à votre compte.
2. Dans la zone de navigation du portail client, sélectionnez **Sécurité > SSL > Certificats**.
3. Cliquez sur le lien **Importer le certificat SSL** à droite de la page **Certificats SSL**.
2. Entrez les détails relatifs au certificat SSL. 

	**Remarque :** Les détails saisis dans la boîte de dialogue d'importation d'un certificat SSL doivent être saisis tels que fournis par l'autorité de certification, y compris l'espacement et les retours à la ligne. Si ce n'est pas le cas, une erreur se produit. Renseignez les zones comme suit :
  - **Certificat :** Détails du certificat, fournis par l'autorité de certification. Il s'agit généralement d'un bloc de texte alphanumérique.
  - **Clé privée :** Détails de la clé privée, fournis par l'autorité de certification. Il s'agit généralement d'un bloc de texte alphanumérique.
  - **Certificat intermédiaire :** Détails du certificat intermédiaire, fournis par l'autorité de certification. Les certificats intermédiaires ne sont pas obligatoires. Toutefois, si des informations sont disponibles pour le certificat SSL, celles-ci doivent être saisies.
  - **Demande de signature de certificat :** Détails de la demande de signature de certificat, fournis par l'autorité de certification. Ces détails ne sont pas obligatoires. Toutefois, ils doivent être saisis lorsqu'ils sont fournis dans le cadre du certificat. Ne modifiez jamais la demande de signature de certificat. Une clé publique peut être incluse avec la demande. Elle ne doit pas être remplacée par la clé privée.
  - **Notes :** Toutes notes relatives au certificat SSL qui pourraient s'avérer utiles à d'autres utilisateurs.
4. Cliquez sur **Importer** pour importer le certificat SSL. Cliquez sur **Annuler** pour annuler l'action.

Une fois le certificat SSL importé dans le portail client, il reste visible dans l'écran Certificats SSL jusqu'à ce qu'il soit supprimé manuellement. Pour tous les produits ou services nécessitant des détails sur le certificat SSL, le nouveau certificat SSL apparaît dans la liste des certificats susceptibles d'être utilisés lors de l'interaction avec la fonctionnalité SSL pour le produit ou le service concerné. Vous pouvez mettre à jour le certificat ou télécharger en toute sécurité ses détails, à tout moment.
