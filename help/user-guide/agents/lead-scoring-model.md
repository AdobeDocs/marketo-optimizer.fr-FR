---
title: Créer des modèles de notation personnalisés
description: Créez, prévisualisez et publiez des modèles de notation de prospect personnalisés dans Marketo Optimizer à l’aide des compétences Scoring Studio dans l’interface de conversation des collaborateurs.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 2%

---

# Créer des modèles de notation personnalisés

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_scoring_studio"
>title="Studio de notation"
>abstract="Utilisez les compétences du Studio de notation pour créer, configurer et publier des modèles de notation de prospect personnalisés via l’interface de conversation des collègues."

La compétence [_Studio de notation_ &#x200B;](./skills.md#scoring-signals) de [!DNL Adobe Marketo Optimizer] fournit une solution de notation de prospect native à l’IA qui vous permet de créer, de configurer et de publier des modèles de notation de prospect. Studio associe un workflow piloté par un agent à une interface utilisateur visuelle. Vous pouvez créer des modèles de notation à l’aide d’invites en langage naturel dans l’interface de conversation [Coworker](./chat-interface.md) ou en interagissant directement avec les commandes de l’interface utilisateur.

* **Compétences** - `scoring-studio`
* **Invocation** - Utilisez une barre oblique pour ouvrir Scoring Studio. Par exemple : _« open Scoring Studio.«_
* **Lit à partir de / écrit sur** - [!DNL Marketo Optimizer] service de notation ; lit [!DNL Marketo Engage] champs de prospect et les types d’activité.

Lors du lancement, Coworker récupère automatiquement le contexte approprié (y compris les types d’activité, les champs de prospect, les listes de personnes et les listes de scores existantes) pour fonder ses suggestions sur vos données.

![Scoring Studio lancé dans l’interface de conversation de Coworker](./assets/scoring-studio.png){width="700" zoomable="yes"}

## Création d’un modèle de notation {#create-model}

Lorsque vous ouvrez Scoring Studio, Coworker propose un exemple de modèle de notation pertinent pré-renseigné avec une liste statique et un ensemble d’activités notées. Vous pouvez accepter ce point de départ suggéré ou fournir votre propre invite pour définir un modèle personnalisé.

### Prévisualiser le modèle {#preview-model}

Après avoir fourni une invite, Coworker génère un aperçu du modèle avant d’apporter des modifications. Les surfaces d’aperçu :

* Dimensions de notation utilisées
* Attributs et activités en cours de notation
* Listes statiques ou listes dynamiques appliquées en tant que segments
* Résumé de l’objectif du modèle, du segment cible et des signaux principaux

Vous pouvez vérifier l’aperçu et choisir de créer le modèle en fonction de celui-ci, ou continuer à l’affiner via la conversation avant de finaliser.

### Structure du modèle {#model-structure}

Le modèle créé est organisé en _dimensions_ et _signaux_. Vous pouvez configurer chaque signal à l’aide du panneau des propriétés de l’interface utilisateur :

* **Type de signal** — Basé sur l&#39;activité ou basé sur les attributs
* **Activité ou attribut** — Élément spécifique à noter
* **Paramètres du signal** — Paramètres réglables pour le signal

Vous pouvez créer et configurer des modèles entièrement via Coworker à l’aide du langage naturel ou interagir directement avec les commandes de l’interface utilisateur.

## Publication d’un modèle de notation {#publish-model}

Lorsque votre modèle est finalisé, demandez à votre collègue de le publier. Le processus de publication gère automatiquement les éléments suivants :

| Étape | Ce qui se passe |
|---|---|
| **Compilation des règles** | Toutes les règles de notation sont compilées et validées |
| **Création de la tâche de score** | Une tâche de score planifiée est créée et configurée pour s’exécuter quotidiennement |

Après la publication, vous avez également la possibilité de déclencher une exécution manuelle pour traiter les scores immédiatement.

## Affichage des résultats de la notation {#view-results}

Une fois l’exécution de notation terminée, les notes sont réécrites dans [!DNL Marketo Engage] via le processus d’importation de prospect. Une fois l’importation terminée, les scores mis à jour peuvent être vérifiés directement dans [!DNL Marketo Engage].

Après chaque exécution, vous pouvez afficher un résumé des résultats qui indique :

* Nombre de personnes notées
* Le score individuel change par personne

Un journal d’audit est disponible pour consulter des détails d’exécution supplémentaires.
