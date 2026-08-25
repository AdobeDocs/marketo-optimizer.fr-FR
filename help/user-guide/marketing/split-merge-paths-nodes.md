---
title: Nœuds de chemins de division et de fusion
description: Découvrez comment utiliser les nœuds de chemins d’accès fractionnés et fusionnés dans des parcours de personne pour segmenter les personnes en chemins d’accès distincts en fonction de conditions définies, puis les réunir en un point commun en aval.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# Nœuds de chemins de division et de fusion

Utilisez les nœuds de chemins d’accès fractionnés et fusionnés dans des parcours de personne pour segmenter les personnes en chemins d’accès distincts en fonction des conditions que vous définissez, puis rassemblez ces chemins d’accès afin que le parcours puisse continuer. Les chemins fractionnés vous permettent d’adapter les actions et les événements à des segments d’audience spécifiques, tandis que les chemins fusionnés réunissent ces segments à un point commun en aval.

## Nœuds de chemins de partage

Utilisez des nœuds fractionnés pour segmenter les personnes en fonction des conditions que vous définissez. Créez des chemins d’accès pour la liste d’audiences en fonction de conditions, définissez chaque chemin d’accès avec des nœuds d’action et d’événement pour le segment, puis combinez les chemins d’accès et poursuivez le parcours.

Un nœud Chemins partagés définit un ou plusieurs chemins segmentés en fonction des filtres de personnes.

<!-- A split based on a people filter is automatically closed with a merge paths node so that all people can move forward to the next step. Split by people paths can include only people actions. These paths cannot be split again and automatically join back. _not currently true_ -->

_**Fonctionnement d’un nœud de partage de chemin par personnes**_

* L’évaluation de chaque chemin s’effectue de haut en bas. Si une personne correspond pour le premier et le deuxième chemin, elle continue uniquement le premier chemin.
* Le nœud prend en charge la définition d’un chemin _Autres personnes_, où vous pouvez ajouter des actions ou des événements pour les personnes qui ne correspondent pas à l’un des segments/chemins définis.

### Filtres correspondants

Pour chaque chemin d’accès que vous définissez pour le nœud, utilisez les types de filtre suivants pour faire correspondre les personnes selon une ou plusieurs conditions :

* Historique des activités - Vous pouvez définir un chemin d’accès en fonction de l’activité de la personne liée aux éléments suivants :

  * Messages e-mail
  * Modification de la valeur des données

* Attributs de personne - Définissez une condition en fonction des attributs d’une personne, tels que le pays, la fonction, l’identité dérivée ou l’appartenance à une liste.

### Ajouter un nœud de chemins de division

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Fractionner les chemins]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours ](./assets/person-journey-canvas-add-node.png){width="200"}

1. Pour définir une condition applicable à _[!UICONTROL Chemin 1]_, cliquez sur **[!UICONTROL Appliquer la condition]**.

1. Dans l’éditeur de conditions, ajoutez un ou plusieurs filtres pour définir le chemin de division.

   * Faites glisser et déposez l’un des filtres de personnes à partir du volet de navigation de gauche et terminez la définition de la correspondance.

   * Ajustez vos conditions en appliquant la logique **[!UICONTROL Filtre]** en haut. Vous pouvez choisir de correspondre à toutes les conditions ou à une seule condition.

     <!-- ![Split path node - conditions person filter logic](./assets/node-split-conditions-people.png){width="700" zoomable="yes"} -->

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

   Chaque chemin doit comporter une combinaison d’actions et d’événements.

1. Cliquez sur l’icône plus ( **+** ) à la fin de l’un de ces chemins et choisissez **[!UICONTROL Fusionner les chemins]** dans les options affichées.

1. Dans les propriétés de nœud à droite, sélectionnez les chemins d’accès à fusionner.

   <!-- ![Journey node - merge paths](./assets/node-merge-select-paths.png){width="600" zoomable="yes"} -->

   À ce stade, les chemins d’accès sont fusionnés afin que les personnes des chemins d’accès sélectionnés se combinent pour former un chemin d’accès unique qui peut continuer à progresser dans le parcours.

1. Si nécessaire, vous pouvez annuler la fusion des chemins en revenant aux propriétés du nœud de chemins de fusion et en décochant la case correspondant aux chemins que vous souhaitez supprimer.