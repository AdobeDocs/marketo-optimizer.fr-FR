---
title: Compétences du collègue
description: 'Examinez les compétences du collaborateur d’entreprise CX dans Marketo Optimizer : workflows empaquetés pour les programmes, les parcours, les audiences, la notation, le contenu et l’optimisation de l’heure d’envoi.'
TQID: 'https://experienceleague.adobe.com/nNFB9UEghfqVvnBrNtTDnpnLUKKKMAU2nY1Pqt0KkUQ'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 3cf5f37e-e87e-5179-812b-53ce05d7eebbid: 46e599c6-e20f-5f67-9824-93415016f66bid: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4id: d4203578-d294-5145-b397-f26f4488a904
topic_v2: id: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 7%

---

# Compétences des collègues

Une _compétence_ est un workflow empaqueté que Coworker sait exécuter : les éléments de base à la fois du menu `/` et des requêtes en langage naturel. Chaque compétence regroupe des instructions détaillées et les outils spécifiques nécessaires pour une tâche (par exemple, « publier un parcours », « comparer deux listes de personnes », « créer un modèle de notation »).

>[!NOTE]
>
>Chaque compétence est classée en fonction du fait qu’elle mute l’état [!DNL Marketo Optimizer] ou [!DNL Marketo Engage] (**Écriture**), qu’elle ne génère/analyse que (**Lecture**) ou qu’elle possède des fonctions de requête et de mutation égales (**Lecture+Écriture**).

## Programmes et planification {#programs-planning}

| Compétence | Ce qu&#39;il fait | Accès | Surface de produit | Impact / flux de données |
|---|---|---|---|---|
| `falco-program-creation` | Création de programmes [!DNL Marketo Optimizer] de bout en bout : programme, sous-dossiers, jetons, listes, parcours. <p>Voir _[Créer un programme à partir d’un brief](./program-from-brief.md)_. | Écriture | [!DNL Marketo Optimizer] | Lit + écrit [!DNL Marketo Optimizer]. |
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
| `journey-observability` | Déboguer/surveiller la progression : chemins, synchronisation, divisions, décrochages, séjour. <p>Voir _[Déboguer et surveiller la progression du parcours](./journey-observability.md)_. | Lecture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Optimizer] + [!DNL Marketo Engage] (vérification de la liste statique). |

## Audiences et personnes {#audiences-people}

| Compétence | Ce qu&#39;il fait | Accès | Produit | Serveur principal (flux de données) |
|---|---|---|---|---|
| `audience-creation` | Adapter une liste dynamique de [!DNL Marketo Engage], créer une liste de personnes ou ajouter/mettre à jour des règles. <p>Voir _[Création d’audiences pour les programmes](./audience-creation.md)_. | Écriture | [!DNL Marketo Optimizer] | Lit [!DNL Marketo Engage] + lit/écrit [!DNL Marketo Optimizer]. |
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
| `scoring-studio` | Répertorier/obtenir des modèles de notation et les créer/publier. <p>Voir _[Création de modèles de notation personnalisés](./lead-scoring-model.md)_. | Lecture+Écriture | [!DNL Marketo Optimizer] | Lit + écrit des [!DNL Marketo Optimizer] (service de notation) ; lit [!DNL Marketo Engage] champs de prospect/types d’activité. |
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
