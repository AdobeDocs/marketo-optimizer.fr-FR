---
title: Listes de personnes
description: Créez et gérez des listes de personnes dans Marketo Optimizer pour le ciblage de parcours, l’appartenance dynamique basée sur des règles et l’activation de destinations de liste statique.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 2%

---

# Listes de personnes

Dans [!DNL Adobe Marketo Optimizer], les listes de personnes sont les conteneurs d’audience au niveau de la personne pour le ciblage et l’entrée de parcours de personnes, avec des listes dynamiques pour la qualification en direct basée sur des règles et des listes statiques pour l’appartenance fixe ou gérée par parcours.

## Accès et navigation dans les listes de personnes {#access-browse}

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion marketing]**.

1. À droite dans la liste de ressources **[!UICONTROL Marketing]**, sélectionnez **[!UICONTROL Listes des personnes]**.

   ![Accéder aux listes de personnes pour gérer vos audiences](./assets/people-lists.png){width="800" zoomable="yes"}

La page comporte deux onglets où vous pouvez afficher et gérer les **[!UICONTROL listes dynamiques]** et **[!UICONTROL listes statiques]**. Cliquez sur l’onglet pour basculer entre les deux types de vue de la liste.

Vous pouvez saisir du texte dans l’outil _Rechercher_ en haut de la liste pour filtrer la liste affichée par nom. Utilisez les outils de liste pour personnaliser la liste affichée :

* Cliquez sur l’icône _Personnaliser le tableau_ ( ![Icône Personnaliser le tableau](../assets/do-not-localize/icon-falco-customize-table.svg) ) pour contrôler les colonnes affichées.
* Cliquez sur l’icône _Réinitialiser les colonnes_ ( ![Icône Réinitialiser la largeur des colonnes](../assets/do-not-localize/icon-falco-reset-columns.svg) ) pour réinitialiser les largeurs de colonne.

À partir de cet espace, vous pouvez également :

* Création de listes dynamiques et statiques
* Accéder aux listes pour vérifier l’appartenance actuelle
* Appliquer des filtres d’abonnement

<!--
## Audience Hub

The AI Audience Hub is a centralized, AI-driven starting point for all audience-related capabilities across [!DNL Adobe Marketo Optimizer]. It is designed to accelerate first-time user success while progressively unlocking advanced intelligence, insights, and control for returning and power users.

The Hub acts as:

* A guided starting point for discovering, creating, and refining person lists, account lists, and buying groups

* A visibility layer for audience health, coverage, overlap, engagement patterns, and AI-driven insights

* A control center for audience governance, optimization, reuse, and readiness for activation across journeys and sales workflows

### High level structure

Prompt-based starting point - Quick Start prompts and freeform input to help users discover, create, or optimize audiences.

1. AI insights feed - Surfaces key audience signals such as overlap, gaps, saturation risk, and optimization opportunities.

1. Adaptive audience library - A personalized view of people lists, account lists, and buying groups that adapts based on usage, relevance, and activation.

1. Optimization and arbitration nudges - Guides users to refine, split, or reuse audiences before activation.

1. Audience visibility and reporting - High-level insight into audience health, engagement patterns, and usage across active journeys.


### Empty and Error States (High-Level)

No audiences / no data - Show Quick Start prompts to help first-time users create or import person lists

Low data or incomplete audience - Explain what's missing (e.g., insufficient contacts, missing persona coverage, or low engagement data) and suggest next steps.

AI insights unavailable - Provide a graceful fallback with a clear explanation, so users understand why insights aren't shown and what actions they can take manually.
-->

## Créer une liste de personnes {#create-people-list}

1. Cliquez sur **[!UICONTROL Créer une liste]** en haut à droite de la page _[!UICONTROL Listes de personnes]_.

1. Dans la boîte de dialogue, sélectionnez un programme comme **[!UICONTROL Parent]** pour la liste.

1. Saisissez un **[!UICONTROL Nom]** (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la liste.

1. Choisissez la liste **[!UICONTROL Type]** :

   * [**[!UICONTROL Statique]**](#static-lists) - L’appartenance est déterminée par les filtres de qualification évalués lors de la création de la liste. L’appartenance à la liste ne se met pas à jour, sauf si vous qualifiez ou disqualifiez manuellement des enregistrements.
   * [**[!UICONTROL Dynamique]**](#dynamic-lists) - L’appartenance est déterminée dynamiquement par des filtres admissibles. L’appartenance à la liste s’actualise automatiquement.

   ![Boîte de dialogue Créer une liste de personnes](./assets/people-list-create-dialog.png){width="450"}

1. Cliquez sur **[!UICONTROL Créer]**.

>[!NOTE]
>
>La suppression et la duplication ne sont actuellement pas prises en charge pour les listes de personnes dans cette version de Beta.

## Listes statiques {#static-lists}

L’appartenance à une liste statique est définie par des filtres simples qui référencent les attributs et les activités des personnes. L&#39;adhésion ne change que si vous remplissez ou disremplissez manuellement les conditions d&#39;adhésion.

>[!NOTE]
>
>Les définitions de filtre de liste statique sont appliquées une seule fois lorsque vous ajoutez ou supprimez des membres de la liste. Le filtre défini n’est pas disponible par la suite. Si vous souhaitez conserver une définition d’audience cohérente à l’aide de filtres, utilisez plutôt une liste dynamique .

<!--
What internet says about Marketo static lists -- which of these is also true in Marketo Optimizer?

* Manual Targeting: Storing fixed cohorts, such as attendees of a specific webinar, people who purchased a certain product, or a list of competitors.
* Third-Party Syncing: Allowing external platforms (like Amplitude or Twilio Segment) to automatically sync and export groups of users directly into Marketo as targeted audiences.
* Status Tracking: Helping marketers organize leads into specific categories or track multi-value interests without needing to create new, permanent database fields.List 
* Segmentation: Acting as a reliable, unchanging recipient or suppression list for email campaigns and engagement programs. Unlike a Smart List—which dynamically adds or removes people based on changing criteria or rules—a static list serves as a reliable snapshot. People remain on the list until explicitly added or removed by you or a backend flow.

So far, activating to a destination is the only thing that they are used for that I have found.
-->

### Ajouter des membres {#static-list-add-members}

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Ajouter des personnes]** en haut à droite.

1. Dans la boîte de dialogue, définissez les règles de qualification de vos prospects en glissant-déposant des filtres depuis la gauche.

   Vous pouvez filtrer les personnes à l’aide de n’importe quelle combinaison des éléments suivants :

   * Historique des activités
   * Attributs de la société
   * Attributs de la personne
   * Filtres spéciaux tels que l’appartenance à un parcours

   Pour chaque filtre que vous ajoutez, cliquez sur **[!UICONTROL Ajouter des contraintes]** afin d’affiner les critères correspondants du filtre.

   ![Ajoutez des filtres avec des contraintes pour ajouter des personnes à la liste statique](./assets/people-list-static-add-people-filters.png){width="700" zoomable="yes"}

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un bref instant, les membres admissibles apparaissent dans la liste.

   ![Membres de la liste statique](./assets/people-list-static-members.png){width="700" zoomable="yes"}

### Supprimer des membres {#static-list-remove-members}

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Supprimer des personnes]** en haut à droite.

1. Dans la boîte de dialogue _[!UICONTROL Supprimer des personnes]_, ajoutez les filtres pour faire correspondre les membres que vous souhaitez disqualifier.

   ![Ajoutez des filtres pour supprimer des personnes de la liste statique](./assets/people-list-static-members-remove-people-filters.png){width="700" zoomable="yes"}

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un bref instant, les membres disqualifiés quittent la liste.

### Activer vers une destination {#static-list-activate}

Lorsque vous activez une liste statique, elle est exploitable dans les systèmes en aval, avec une synchronisation continue au lieu d’exportations manuelles. Cela s’avère utile pour le ciblage, la suppression et l’orchestration des médias achetés en aval.

* La liste statique agit comme un conteneur pour les personnes.
* L’activation envoie/synchronise cet abonnement vers une destination.
* La destination peut ensuite faire quelque chose avec ces personnes, par exemple les cibler sur LinkedIn ou les supprimer d’une audience externe.

Étant donné que le modèle d’activation est conçu pour être persistant, et non pour une exportation ponctuelle :

* Les personnes ajoutées ultérieurement à la liste sont propagées automatiquement.
* Les personnes supprimées ultérieurement sont automatiquement désactivées.
* Les marketeurs évitent les exportations répétées de fichiers CSV et les chargements manuels.
* Les parcours peuvent actualiser l’audience au fil du temps pour une orchestration continue.

>[!PREREQUISITES]
>
>Vous devez disposer d’une ou de plusieurs [destinations configurées](./destinations.md) pour votre sandbox [!DNL Marketo Optimizer] avant de pouvoir activer une liste statique vers une destination.

1. Sélectionnez l’onglet **[!UICONTROL Listes statiques]**.

1. Recherchez la liste statique que vous souhaitez activer vers une destination.

1. Cliquez sur l’icône _Plus de menu_ ( **...** ) en regard de la liste et choisissez **[!UICONTROL Activer vers la destination]**.

   ![Accès au menu Plus pour une liste statique](./assets/people-lists-static-more-menu.png){width="450"}

   Vous pouvez également ouvrir la liste statique et utiliser le menu _[!UICONTROL Plus]_ en haut à droite.

   <!-- which UI is it?  _Activate_ ( ![Customize table icon](../assets/do-not-localize/icon-falco-activate-dest.svg) ) icon next to the static list name. -->

1. Cochez la case correspondant à la connexion de destination configurée.

   ![Destinations configurées disponibles pour activation](./assets/static-list-activate-destination-select.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

1. Confirmez l’activation dans la boîte de dialogue _[!UICONTROL Activer la liste vers la destination]_ en cliquant sur **[!UICONTROL Activer]**.

Une fois l’activation terminée, une confirmation s’affiche (_La destination a été activée._) et que la destination est répertoriée comme **[!UICONTROL Active]** dans l’onglet **[!UICONTROL Destinations]** de la liste. Une liste statique peut être activée vers plusieurs destinations à la fois ; l’appartenance se synchronise avec chacune d’elles.

Pour passer en revue les destinations vers lesquelles une liste statique est activée, ouvrez la liste et sélectionnez l’onglet **[!UICONTROL Destinations]**. Par défaut, aucune destination n’est connectée à une nouvelle liste.

#### Désactiver une destination {#deactivate-destination}

1. Ouvrez la liste statique et sélectionnez l’onglet **[!UICONTROL Destinations]**.

1. Cliquez sur l’icône _moins_ ( **-** ) sur la ligne de la destination à supprimer.

1. Confirmez dans la boîte de dialogue _[!UICONTROL Désactiver la destination]_.

La désactivation supprime la destination de la liste. Les personnes de la liste sont également supprimées de l’audience de destination connectée.

## Listes dynamiques {#dynamic-lists}

L’appartenance à une liste dynamique est définie à l’aide de filtres simples qui référencent les attributs et les activités des personnes. L’appartenance est automatiquement maintenue en qualifiant et en disqualifiant les prospects selon la logique du filtre.

### Définir des règles d’appartenance {#set-membership-rules}

1. Ouvrez la liste dynamique et sélectionnez l’onglet **[!UICONTROL Règles]**.

1. Cliquez sur le bouton **[!UICONTROL Modifier les règles]**.

   ![Règles d’accès pour la création d’une liste de personnes dynamique](./assets/people-list-dynamic-rules-edit.png){width="550" zoomable="yes"}

1. Dans la boîte de dialogue, définissez les règles de qualification de vos prospects en glissant-déposant des filtres depuis la gauche.

   Vous pouvez qualifier des prospects pour la liste à l’aide de n’importe quelle combinaison des éléments suivants :

   * Historique des activités
   * Attributs de la société
   * Attributs de la personne
   * Filtres spéciaux tels que l’appartenance à un parcours

   Pour chaque filtre que vous ajoutez, cliquez sur **[!UICONTROL Ajouter des contraintes]** afin d’affiner les critères correspondants du filtre.

   ![Ajouter des filtres avec des contraintes pour renseigner la liste dynamique](./assets/people-list-dynamic-rules-edit-filters.png){width="700" zoomable="yes"}

1. Pour enregistrer vos modifications, cliquez sur **[!UICONTROL Terminé]**.

1. Sélectionnez l’onglet **[!UICONTROL Membres]**.

   Après un bref instant, les membres admissibles apparaissent dans la liste.

   ![Membres générés pour la liste dynamique](./assets/people-list-dynamic-rules-members.png){width="700" zoomable="yes"}

   Pour ouvrir la page [détails de la personne](./person-details.md) où vous pouvez afficher le résumé et les activités récentes, cliquez sur le nom d’une personne dans la liste.

### Duplication de liste dynamique {#duplicate-dynamic-list}

Pour une liste dynamique, une action en double est similaire à une fonction de clonage. Utilisez cette fonction pour répliquer le filtrage d’appartenance et l’ajouter à un autre programme.

1. Dans l’onglet _[!UICONTROL Listes dynamiques]_, cliquez sur l’icône _Plus_ ( **...** ) en regard de la liste et choisissez **[!UICONTROL Dupliquer]**.

1. Dans la boîte de dialogue, sélectionnez le programme **[!UICONTROL Parent]** pour la liste dupliquée.

1. Saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

   Par défaut, la boîte de dialogue utilise le nom de la liste d’origine suivie de `_copy`. Saisissez un nom unique différent pour la liste, le cas échéant.

   ![&#x200B; Boîte de dialogue Dupliquer la liste &#x200B;](./assets/people-list-duplicate-dialog.png){width="375"}

1. Cliquez sur **[!UICONTROL Dupliquer]**.
