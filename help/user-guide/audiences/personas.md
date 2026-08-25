---
title: Personnages dérivés
description: Utilisez les personnes dérivées dans Marketo Optimizer pour cibler les listes de personnes et les chemins de parcours. Découvrez les mappages de persona par défaut et le filtre de persona dérivé.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Personnages dérivés

La classification des personas transforme les données client brutes en une compréhension sémantique des acheteurs que l’IA peut utiliser pour générer du contexte et orienter des décisions personnalisées sur chaque canal et parcours. Ce profil unifié permet d’effectuer les opérations suivantes :

* _Embranchement de Parcours_ - Partagez les chemins d’accès des prospects par rôle, personne et profondeur d’engagement
* _Arbitrage de Parcours_ - Détermine à quel parcours de maturation un prospect appartient actuellement, évitant les collisions de messages entre les programmes simultanés
* _Personnalisation du contenu_ - Contenu qui est un récit spécifique à un rôle (« pour un cadre » ou « pour un praticien »)
* _Sales Qualifier context_ - Les représentants du développement commercial (BDR) reçoivent un résumé sur un seul écran indiquant l&#39;identité de la personne, ses intérêts et son stade actuel sur le parcours des acheteurs

## Personnages par défaut {#default-ersonas}

Pour la version Beta de Marketo Optimizer, les rôles par défaut suivants sont définis en fonction de l’attribut de titre de la tâche :

| Persona | Titres de poste |
| ------- | ---------- |
| [!UICONTROL PDG/PDV] | PDG, DPI, directeur des technologies de l’information, directeur financier, vice-président exécutif de la stratégie |
| [!UICONTROL SVP/VP] | Vice-président principal du marketing, vice-président directeur des ventes, vice-président directeur des opérations, vice-président directeur des produits, vice-président directeur informatique |
| [!UICONTROL Cadre supérieur / Responsable] | Responsable marketing principal, responsable informatique, responsable des opérations, responsable des ventes, responsable des ressources humaines |
| [!UICONTROL Contributeur individuel] | Responsable de compte, Ingénieur logiciel, Spécialiste marketing, Représentant du succès client |
| [!UICONTROL Analyste] | Analyste commercial, Analyste des données, Analyste des études de marché, Analyste financier, Analyste des opérations |
| [!UICONTROL Développeur ou développeuse] | Développeur front-end, Développeur back-end, Développeur full-stack, Développeur d’applications mobiles, Ingénieur DevOps |
| [!UICONTROL Professionnels] | Spécialiste RH, Conseiller juridique, Responsable de la conformité, Chef de projet, Spécialiste des achats |
| [!UICONTROL Consultant] | Consultant en gestion, conseiller en TI, consultant en processus d&#39;affaires, consultant en marketing |
| [!UICONTROL Other] (Autre) | Spécialiste de l&#39;industrie, conseiller indépendant, consultant indépendant, expert en la matière |

>[!NOTE]
>
>Dans la prochaine mise à jour de la disponibilité générale, vous pouvez modifier l’un de ces rôles par défaut en fonction des besoins de votre entreprise. Il prend également en charge les définitions de persona personnalisées et le mappage.

## Filtrer par persona dérivé {#derived-persona-filter}

[!DNL Marketo Optimizer] dérive un persona pour chaque enregistrement de personne en évaluant les attributs d’enregistrement par rapport aux personas définis. _Vous pouvez utiliser le résultat déduit (« Persona dérivé_) comme filtre lors de la définition de l’audience pour une liste de personnes ou pour la segmentation dans un parcours de personnes.

Le filtre _[!UICONTROL Persona dérivé]_ s’affiche dans le panneau de filtrage sous la catégorie **[!UICONTROL Attributs de personne]**.

### Listes de personnes {#people-lists}

Lors de la gestion des membres dans une [liste de personnes statique](./people-lists.md#static-lists) ou de la définition de règles pour une [liste de personnes dynamique](./people-lists.md#dynamic-lists), vous pouvez filtrer par _persona dérivé_ pour cibler toutes les personnes dont les attributs correspondent à une personne configurée spécifique.

![Filtrage des personas dérivé pour une liste de personnes](./assets/derived-persona-filter-people-list.png){width="750" zoomable="yes"}

**Liste statique — Ajouter des membres**

1. Ouvrez la liste statique et cliquez sur **[!UICONTROL Ajouter des personnes]** en haut à droite.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour appliquer le filtre et qualifier les personnes correspondantes dans la liste.

**Liste dynamique — Définit les règles d&#39;appartenance**

1. Ouvrez la liste dynamique et sélectionnez l’onglet **[!UICONTROL Règles]**.

1. Cliquez sur **[!UICONTROL Modifier les règles]**.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour enregistrer la règle.

   L’appartenance est automatiquement mise à jour lorsque les enregistrements de la personne sont évalués par rapport à la règle.

### Parcours de personne {#person-journeys}

Lorsque vous configurez la segmentation d’un parcours de personne dans un nœud [_Partage de chemins_ &#x200B;](../marketing/split-merge-paths-nodes.md), vous pouvez utiliser un persona dérivé comme filtre de profil de personne pour contrôler quelles personnes entrent dans le chemin du parcours.

![Filtrage des personas dérivés pour une condition de chemin de partage](./assets/derived-persona-filter-split-path.png){width="750" zoomable="yes"}

1. Cliquez sur le nœud **[!UICONTROL Chemins fractionnés]** dans la zone de travail du parcours.

1. Dans le panneau des propriétés de nœud à droite, cliquez sur **[!UICONTROL Appliquer la condition]** ou **[!UICONTROL Modifier la condition]** pour un chemin d’accès.

1. Dans la boîte de dialogue de filtre, développez **[!UICONTROL Attributs de personne]** et faites glisser **[!UICONTROL Persona dérivé]** sur la zone de travail.

1. Dans la condition de filtre, choisissez **[!UICONTROL is]** et sélectionnez une ou plusieurs personnes dans la liste.

1. Cliquez sur **[!UICONTROL Terminé]** pour enregistrer le filtre du chemin d’accès.

