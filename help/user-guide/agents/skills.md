---
title: Compétences du collègue
description: 'Examinez les compétences de vos collègues dans Marketo Optimizer : workflows empaquetés pour les programmes, les parcours, les audiences, la notation, le contenu et l’optimisation de l’heure d’envoi.'
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 7%

---

# Compétences des collègues

Une _compétence_ est un workflow empaqueté que l’agent sait exécuter, c’est-à-dire les éléments qui sous-tendent le menu `/` et les requêtes en langage naturel. Chaque compétence regroupe des instructions détaillées et les outils spécifiques nécessaires pour une tâche (par exemple, « publier un parcours », « comparer deux listes de personnes », « créer un modèle de notation »).

>[!NOTE]
>
>Chaque compétence est classée en fonction du fait qu’elle mute l’état [!DNL Marketo Optimizer] ou [!DNL Marketo Engage] (**Écriture**), qu’elle ne génère/analyse que (**Lecture**) ou qu’elle possède des fonctions de requête et de mutation égales (**Lecture+Écriture**).

## Programmes et planification {#programs-planning}

| Compétence | Ce qu&#39;il fait | Accès | Surface de produit | Impact / flux de données |
|---|---|---|---|---|
| `falco-program-creation` | Création de programmes [!DNL Marketo Optimizer] de bout en bout : programme, sous-dossiers, jetons, listes, parcours. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer]. Voir _[Créer un programme à partir d’un brief](./program-from-brief.md)_. |
| `adapt-program` | Générer des récits de migration à partir de programmes [!DNL Marketo Engage] pour l&#39;adaptation [!DNL Marketo Optimizer]. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Engage], écrit [!DNL Marketo Optimizer] |
| `folder-creation` | Créez des dossiers d’organisation dans l’arborescence de ressources. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `program-creation` *(Créer des programmes)* | Créez des programmes Marketo à partir d’un résumé de campagne. | Écriture | [!DNL Marketo Engage] | Lit + écrit [!DNL Marketo Engage] |
| `program-planning` *(Planifier Des Campagnes)* | Transformer des résumés en documents de configuration/d’implémentation. | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |
| `program-qa` *(Valider les programmes)* | Valider/auditer les programmes (règles uniquement, plan de test ou résumé). | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |

## Parcours {#journeys}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `journey-creation` | Créez et modifiez des parcours de personne en langage naturel. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `journey-edit-dates` | Modifier la date de début/fin d’un parcours sans le publier | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `journey-publish` | Publier/lancer/planifier des parcours de personnes. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `journey-stop` | Interrompre, fermer, arrêter, arrêter ou tuer des parcours. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `journey-reentry` | Configurer la rentrée : autoriser/interdire, réinitialiser, max. les entrées. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `journey-trafficcontrol` | Exécutez une simulation du contrôle du trafic montrant le routage des profils. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] (simulation) |
| `journey-observability` | Déboguer/surveiller la progression : chemins, synchronisation, divisions, décrochages, séjour. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] + [!DNL Marketo Engage] (vérification de la liste statique). |

## Audiences et personnes {#audiences-people}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `audience-creation` | Adapter une liste dynamique de [!DNL Marketo Engage], créer une liste de personnes ou ajouter/mettre à jour des règles. | Écriture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Engage] + lit/écrit [!DNL Marketo Optimizer].  Voir _[Création d’audiences pour les programmes](./audience-creation.md)_. |
| `people-list-comparison` | Comparer deux listes de personnes et afficher les membres qui se chevauchent | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] |
| `import-leads` | Inspectez la qualité des données CSV et validez les importations dans [!DNL Marketo Engage]. | Lecture+Écriture | Les deux | Lit + écrit [!DNL Marketo Engage] |
| `lead-investigation` *(Enquêter sur les leads)* | Examiner l’activité, la notation, la qualification et le cycle de vie d’un prospect. | Lecture | [!DNL Marketo Engage] | Lit [!DNL Marketo Engage] |

## Contenu et canaux {#content-channels}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `content-personalization` | Parcourir/prévisualiser des modèles et modifier du contenu/générer des variantes. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer]. Voir _[Personnaliser le contenu d’un e-mail par persona](./personalize-content.md)_. |
| `asset-tokens` | CRUD de jeton complet sur les programmes/dossiers/parcours. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `fcs-channels` | Recherches de canal et CRUD + publication/arrêt/suppression. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |

## Notation et signaux {#scoring-signals}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `scoring-studio` | Répertorier/obtenir des modèles de notation et les créer/publier. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit des [!DNL Marketo Optimizer] (service de notation) ; lit [!DNL Marketo Engage] champs de prospect/types d’activité. Voir _[Création de modèles de notation personnalisés](./lead-scoring-model.md)_. |
| `engagementconfiguration` | Afficher la configuration de l&#39;engagement et modifier/mettre à jour les poids. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `intentconfiguration` | Afficher la configuration d&#39;intention et définir/mettre à jour les poids. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `intent-query` | Interroger et expliquer les scores d’intention par personne/segment/liste. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] |

## Optimisation de l’heure d’envoi {#sto}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `send-time-optimization` | Vérifiez le statut STO et activez/désactivez-le sur un nœud d’e-mail. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer] |
| `send-time-report` | Récupérez/affichez le rapport des performances de la STO. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] |

## Connaissances {#knowledge}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `product-knowledge` | Répondez aux questions pratiques/conceptuelles de la documentation [!DNL Marketo Optimizer] sur Experience League. | Lecture | Les deux | Lit les documents externes — aucune donnée de produit |

## Cross-back-end {#cross-backend}

Ces compétences s’étendent sur plusieurs serveurs principaux :

- **`adapt-program`** — `gather_program_assets` lit [!DNL Marketo Engage] (`get_program`, `get_smart_campaign`, `list_emails`), puis écrit via `falcomcp_create_journey` — serveur principal classique.
- **`audience-creation`** — lit [!DNL Marketo Engage] listes dynamiques (`get_smart_list` / `get_smart_campaign`), puis écrit [!DNL Marketo Optimizer] listes de personnes.
- **`journey-observability`** — [!DNL Marketo Optimizer] lit plus un `check_lead_in_marketo_static_list` [!DNL Marketo Engage] lire.
- **`scoring-studio`** : lit [!DNL Marketo Engage] champs de prospect/types d&#39;activité ainsi que [!DNL Marketo Optimizer] service de notation.

Tous les outils `falco-mcp_*` et parcours/jeton/notation/STO/FCS accèdent aux services [!DNL Marketo Optimizer] ; les outils CSV/programme/prospect [!DNL Marketo Engage].

