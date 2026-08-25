---
title: Nœud de Parcours d’audience de personne
description: Configurez le nœud audience de personne dans Journey Optimizer B2B pour spécifier les profils qui rejoignent un parcours à l’aide de listes de personnes dynamiques ou d’audiences basées sur un événement.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Nœud d’audience de personne

Le nœud _audience personne_ spécifie les profils de personnes qui rejoignent le parcours. Lorsque vous [créez un parcours de personne](./person-journeys.md), le parcours commence toujours par un nœud d’audience de personne qui définit son entrée. Le nœud d’audience de personne peut avoir l’un des deux types d’entrée d’audience suivants : une liste de personnes dynamique ou un déclencheur d’événement.

Si la liste de personnes dynamique dont vous avez besoin pour le parcours de personnes n’existe pas déjà, [créez la liste de personnes](../audiences/people-lists.md#create-a-people-list) puis configurez le nœud Audience de la personne .

_Pour configurer l&#39;audience de parcours :_

1. Cliquez sur le nœud **[!UICONTROL Audience de la personne]**.

   Cette action affiche les propriétés du nœud sur la droite.

   ![Nœud de parcours d’audience de personne](./assets/person-audience-node-properties.png){width="600" zoomable="yes"}

1. Utilisez l’une des options de configuration d’audience suivantes pour l’audience de personne :

   * **[!UICONTROL Liste dynamique]** - Utilisez une liste de personnes dynamique, basée sur des règles. Les règles de liste sont évaluées au moment de l’exécution du parcours pour qualifier les membres du parcours. Les personnes qui seront ultérieurement disqualifiées pour la liste dynamique ne seront pas supprimées du parcours. Voir _[Listes dynamiques](../audiences/people-lists.md#dynamic-lists)_.

   * **[!UICONTROL Audience de l’événement]** - Utilisez une audience d’événement pour définir l’audience du parcours en fonction des événements admissibles. Définissez des membres d’audience à l’aide du filtrage de profil de personne et déclenchez une entrée de parcours selon des critères d’événement. Voir _[Audiences basées sur un événement](../audiences/event-based-audiences.md)_.