---
title: Nœuds de chemins de division et de fusion
description: Découvrez comment utiliser les nœuds de chemins d’accès fractionnés et fusionnés dans des parcours de personne pour segmenter les personnes en chemins d’accès distincts en fonction de conditions définies, puis les réunir en un point commun en aval.
TQID: 'https://experienceleague.adobe.com/XMN7lgb77bFlJkNXrmPf9ZSCV-GgIuybtr-O3AsqT2U'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
source-git-commit: bc370a501d3f8ff80ad846576b62504aca77f530
workflow-type: tm+mt
source-wordcount: '1083'
ht-degree: 2%
---
# Nœuds de chemins de division et de fusion

Utilisez les nœuds de chemins d’accès fractionnés et fusionnés dans les parcours de personne pour segmenter les personnes en chemins d’accès distincts en fonction des conditions que vous définissez, puis fusionnez ces chemins d’accès afin que le parcours puisse continuer. Les chemins fractionnés vous permettent d’adapter les actions et les événements à des segments d’audience spécifiques, tandis que les chemins fusionnés combinent ces segments à un point commun.

## Nœuds de chemins de partage

Utilisez des nœuds fractionnés pour segmenter les personnes en fonction des conditions que vous définissez. Créez des chemins d’accès pour la liste d’audiences en fonction de conditions, définissez chaque chemin d’accès avec des nœuds d’action et d’événement pour le segment, puis combinez les chemins d’accès et poursuivez le parcours.

Un nœud Chemins partagés définit un ou plusieurs chemins segmentés en fonction des filtres de personnes.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->

_&#x200B;**Fonctionnement d’un nœud de chemin de division**&#x200B;_

* L’évaluation de chaque chemin s’effectue de haut en bas. Si une personne correspond au premier et au second chemin, elle continue uniquement le long du premier chemin.
* Le nœud prend en charge la définition d’un chemin _Autres personnes_, où vous pouvez ajouter des actions ou des événements pour les personnes qui ne correspondent pas à l’un des segments/chemins définis.

### Filtres de personnes appariées

Pour chaque chemin d’accès que vous définissez pour le nœud, utilisez les types de filtres suivants afin de faire correspondre les personnes selon une ou plusieurs conditions.

| Filtres | Description |
| ------- | ----------- |
| Historique des activités | Activités basées sur des conditions évaluées à l’aide d’un ou de plusieurs éléments sélectionnés |
| Brand Concierge | Activités pour les prospects qui interagissent avec [!DNL Brand Concierge]. |
| Attributs de la société | Attributs du profil de la société/du compte, notamment : <li>[!UICONTROL Chiffre d’affaires annuel] <li>[!UICONTROL Nom de la société] <li>[!UICONTROL Pays de facturation] <li>[!UICONTROL Industrie] <li>[!UICONTROL Nombre d’employés] <li>[!UICONTROL Code SIC] <li>[!UICONTROL État] |
| Données d’intention | Attributs basés sur les données d’intention associées au profil de personne. |
| Opportunités | Statut et attributs basés sur les opportunités associées au profil de personne, notamment : <li>[!UICONTROL A une opportunité] <li>[!UICONTROL Nombre d’opportunités] <li>[!UICONTROL Montant total de l’opportunité] <li>[!UICONTROL A été ajouté à l’opportunité] <li>[!UICONTROL A été supprimé de l’opportunité] |
| Attributs de la personne | Attributs du profil de personne B2B, notamment : <li>[!UICONTROL Ville] <li>[!UICONTROL Pays] <li>[!UICONTROL Date de naissance] <li>[!UICONTROL Adresse électronique] <li>[!UICONTROL E-mail non valide] <li>[!UICONTROL Email suspendu] <li>[!UICONTROL Prénom &#x200B;] <li>[!UICONTROL Région d’État déduite] <li>[!UICONTROL Fonction] <li>[!UICONTROL Nom] <li>[!UICONTROL Numéro de téléphone mobile] <li>[!UICONTROL Score d’engagement de personne] <li>[!UICONTROL Numéro de téléphone] <li>[!UICONTROL Code postal &#x200B;] <li>[!UICONTROL État] <li>[!UICONTROL Désabonné] <li>[!UICONTROL Motif de désabonnement] |
| Applications de vente | Activités de lead liées aux [!DNL Sales Qualifier] ou aux [!DNL Marketo Sales Insights]. |
| Filtres spéciaux | Attributs de filtrage qui ne relèvent pas des catégories prédéfinies, offrant ainsi une flexibilité pour les critères de filtre personnalisés ou divers. |

>[!BEGINSHADEBOX]

**Activités [!DNL Marketo Optimizer] prises en charge pour les filtres de condition**

Pour les conditions de chemin d’accès, [!DNL Marketo Optimizer] prend en charge les activités de l’instance [!DNL Marketo Engage] connectée en tant que source de données.

>[!NOTE]
>
>Il ne peut y avoir qu’une seule instance [!DNL Marketo Engage] comme source de données et elle est préconfigurée au moment de la mise en service de votre instance [!DNL Marketo Optimizer].

Vous pouvez créer des conditions autour des activités [!DNL Marketo Engage] suivantes :

* **[!UICONTROL Formulaire Marketo Engage rempli]** - Correspond aux prospects qui ont rempli un formulaire [!DNL Marketo Engage] spécifique à tout moment dans leur journal d’activité non obsolète.
* **[!UICONTROL Page web Marketo Engage visitée]** - Correspond aux prospects qui ont consulté une URL spécifique sur votre site web ou [!DNL Marketo Engage] pages de destination. Il fonctionne directement à l’aide du code de suivi Munchkin installé sur votre site.
* **[!UICONTROL Lien ayant cliqué sur une page web Marketo Engage]** - Correspond aux prospects qui ont cliqué sur un lien ou une ressource spécifique sur une page suivie.
* **[!UICONTROL E-mail Marketo Engage envoyé]** - Correspond aux prospects auxquels [!DNL Marketo Engage] avez tenté d’envoyer un e-mail spécifique, en tenant compte des actions de déploiement avant les hard bounces ou les acceptations de serveur.
* **[!UICONTROL E-mail Marketo Engage diffusé]** - Correspond à un prospect dont le serveur de messagerie (MX) a renvoyé une réponse de succès (message 250 OK) au serveur d’envoi [!DNL Marketo Engage].
* **[!UICONTROL E-mail Marketo Engage retourné]** - Correspond aux leads qui ont subi un hard bounce (échec de diffusion permanent) lors d’un envoi d’e-mail spécifique ou au cours d’une période donnée.
* **[!UICONTROL Marketo Engage email bounce soft]** - Correspond aux leads dont les e-mails ont subi un échec de diffusion temporaire (comme une boîte de réception pleine ou un serveur hors ligne) plutôt qu&#39;un hard bounce permanent.
* **[!UICONTROL Désabonnement des e-mails Marketo Engage]** - Correspond aux prospects qui se sont désabonnés des e-mails marketing non opérationnels. Dans ce cas, [!DNL Marketo Engage] met automatiquement à jour la valeur du champ `Unsubscribed` du prospect sur `true`, en les supprimant des futurs envois d’e-mail standard.
* **[!UICONTROL E-mail Marketo Engage ouvert]** - Correspond aux prospects qui ont ouvert un e-mail [!DNL Marketo Engage] suivi.
* **[!UICONTROL Lien cliqué dans l’e-mail Marketo Engage]** - Correspond aux prospects qui ont cliqué sur un lien (ou un lien spécifique) dans un e-mail [!DNL Marketo Engage].

>[!ENDSHADEBOX]

### Ajouter un nœud de chemins de division

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours &#x200B;](./assets/person-journey-canvas-add-node.png){width="200"}

1. Pour définir une condition applicable à _[!UICONTROL Chemin 1]_, cliquez sur **[!UICONTROL Appliquer la condition]**.

1. Pour définir le chemin de division, ajoutez un ou plusieurs filtres dans l’éditeur de conditions.

   * Faites glisser et déposez l’un des filtres de personnes à partir du volet de navigation de gauche et terminez la définition de la correspondance.

   * Cliquez sur **[!UICONTROL Ajouter une contrainte]** pour chaque contrainte que vous souhaitez utiliser pour affiner la correspondance du filtre.

     ![Nœud de chemin partagé - Filtre de personne correspondant pour la condition de chemin](./assets/journey-node-split-conditions-people.png){width="700" zoomable="yes"}

   * Affinez vos conditions en appliquant la logique **[!UICONTROL Filtre]** en haut. Vous pouvez choisir de correspondre à toutes les conditions ou à une seule condition.

   * Cliquez sur **[!UICONTROL Terminé]**.

1. Pour ajouter d’autres chemins d’accès, cliquez sur **[!UICONTROL Ajouter un chemin d’accès]** et répétez les étapes précédentes pour ajouter des conditions applicables au chemin d’accès.

   Vous pouvez également libeller chaque chemin d’accès en fonction de ces conditions ou utiliser les libellés par défaut.

1. Si nécessaire, réorganisez les chemins en fonction de la priorité que vous souhaitez pour la division.

   Le filtrage des chemins d’accès est évalué dans l’ordre décroissant. Chaque personne suit le premier chemin correspondant.

   Cliquez sur les flèches vers le haut et vers le bas en haut à droite de chaque carte de chemin pour la déplacer vers le haut ou le bas dans la liste des chemins.

   <!-- ![Split path node - reorder paths](./assets/node-split-reorder-paths-people.png){width="500" zoomable="yes"} -->

1. Activez l’option **[!UICONTROL Autres personnes]** pour ajouter un chemin par défaut pour les personnes qui ne correspondent pas aux chemins définis.

   Lorsque cette option n’est pas activée, les personnes qui ne correspondent pas à un segment/chemin défini passent au-delà de la division et passent à l’étape suivante du parcours.

Lorsque des conditions sont définies pour chaque chemin, vous pouvez ajouter des nœuds d’action ou d’événement à appliquer aux personnes situées sur un chemin.

## Nœuds de chemins de fusion

1. Accédez à la zone de travail de parcours et localisez le nœud de chemins de division avec plusieurs chemins d’accès.

   Chaque chemin doit comporter une combinaison de nœuds d’action et d’événement.

1. Cliquez sur l’icône plus ( **+** ) à la fin de l’un de ces chemins et choisissez **[!UICONTROL Fusionner les chemins]** dans les options affichées.

1. Dans les propriétés de nœud à droite, sélectionnez les chemins d’accès à fusionner.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   À ce stade, les chemins d’accès sont fusionnés afin que les personnes des chemins d’accès sélectionnés se combinent pour former un chemin d’accès unique qui peut continuer à progresser dans le parcours.

1. Si nécessaire, vous pouvez annuler la fusion des chemins en revenant aux propriétés du nœud de chemins de fusion et en décochant la case correspondant aux chemins que vous souhaitez supprimer.