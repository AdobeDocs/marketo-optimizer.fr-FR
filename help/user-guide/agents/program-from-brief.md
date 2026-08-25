---
title: Créer un programme à partir d’un résumé
description: Utilisez la compétence Création de programme dans Marketo Optimizer pour créer des programmes, des jetons, des listes de personnes et des parcours à partir d’un résumé de campagne.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 4%

---

# Créer un programme à partir d’un brief

Dans [!DNL Adobe Marketo Optimizer], [_program_](../marketing/programs.md) est le conteneur de niveau supérieur pour les parcours, les listes de personnes, les jetons et la configuration dans une campagne. À partir de l’[interface de conversation](./chat-interface.md), la compétence de création de programme construit toute la structure de bout en bout à partir de votre résumé (le programme lui-même, les sous-dossiers, les jetons, les listes de personnes et les parcours de personne) dans une seule conversation guidée.

* **Compétences** - `program-creation`
* **Appel** - Chargez un brief et saisissez _Créer un programme à partir de ce brief_ / _Créer un programme à partir d’un brief_, ou décrivez directement la campagne
* **Lit à partir de / écrit dans** - [!DNL Marketo Optimizer] ; lit également la configuration de type programme de votre client

## Chargement bref

Cliquez sur l’icône _Joindre_ dans l’entrée de conversation pour charger le fichier, puis décrivez ce que vous souhaitez. Le texte du brief est extrait et transmis à l’autre collaborateur en tant que contexte (un indicateur « Brief de la campagne téléchargé : nom de fichier (NkB) » s’affiche dans la conversation).

### Types de fichier pris en charge

| Format | Comportement |
|---|---|
| `.txt`, `.md` | Lecture directe dans le navigateur |
| `.pdf`, `.docx`, `.xlsx`, `.json`, `.csv` | Envoyé au service d’extraction de texte principal. |

Un fichier dont le nom contient *brief* est automatiquement balisé en tant que brief de campagne, sinon Coworker le déduit de son contexte.

### Limite de taille

Le texte court est tronqué à environ 30 000 caractères (environ 7,5 000 jetons) avant d’atteindre Coworker. Les mémoires très longs sont coupés à ce stade (indiqué par une note `(truncated to 29KB)`). Mettez les détails essentiels de la campagne au premier plan.

## Contenus résumés recommandés

L’entrée de flux lit le résumé pour les entrées suivantes, à inclure autant que possible :

* Nom du programme et brève description/objectif
* Signal du type de programme (tel que salon professionnel, événement, webinaire, tournée de présentation, conférence ou événement)
* Critères d’audience des listes de personnes
* Conception du parcours : nombre, critères d’entrée, points de contact/durée et date de mise en production.
* Jetons (valeurs réutilisables telles que la date, le lieu et l’objet de l’événement)

Un collègue demande tout ce qui manque avant la création.

## Phases de création

La compétence s’exécute en trois phases : **ADMISSION → APPROBATION → BUILD**. Rien n’est créé tant que vous n’avez pas approuvé.

### Ingestion

Un collègue extrait les éléments suivants du brief et demande tout ce qui manque :

* Nom de programme
* Dossier parent (par défaut, racine de l’espace de travail si non spécifié)
* Description
* Type de programme (déduit d’une brève formulation si possible)
* Jetons à créer (nom, type, valeur)
* Critères d’audience de la liste des personnes
* Parcours : nombre, critères d’entrée, points de contact, date de mise en production

### Approuver

Un collègue présente un résumé de confirmation avant de continuer :

`I'll create {program} in folder {id}, with {N} token(s), {N} dynamic people list(s), and {N} journey(s). Shall I proceed?`

Aucun outil de création n’est appelé tant que vous n’avez pas répondu avec une autorisation claire (par exemple _procéder_, _continuer_, _le créer_, _approuvé_ et _oui_).

### Build

Les étapes de création s’exécutent dans un ordre fixe ; chacune dépend des identifiants générés par l’étape précédente.

| Étape | Description | Outils | Sortie |
|---|---|---|---|
| **1. Dossier** | Résout le dossier parent par nom ou utilise la racine de l’espace de travail ; peut créer un nouveau sous-dossier | `getRootTree`, `browseFolders`, `createFolder` | Nom du dossier + ID |
| **1.5. Type de programme** | Recherche les types de programme client et sélectionne la correspondance pour le brief | `browseProgramTypes` | Saisir le nom + `programTypeId` |
| **2. Programme** | Crée le programme sous le dossier résolu, lié au type choisi | `createProgram` | Nom, ID et type du programme |
| **3. Jetons** | Crée chaque jeton `my.*` sur le programme | `createProgramToken` | Noms de jetons |
| **4. Listes de personnes** | Génère des règles basées sur des attributs à partir de critères d’audience et crée la liste de personnes dynamiques | `generate_ruleset`, `createSmartListWithRules` | Nom de la liste + `smartListId` |
| **5. Parcours** | Crée chaque parcours de personne avec un nœud d’entrée d’audience de personne connecté à la liste Étape 4 | `create_journey` | Noms de parcours, ID |
| **6. Publier** | Publie ou planifie le parcours si une date de mise en production est définie et confirmée | `publish_journey_with_dates` | Parcours en direct/planifié |
| **7. QA** | Aperçu de la validation en option et vérification complète de l’assurance qualité | `qa_program_preview`, `qa_program` | Rapport Succès/Échec/avertissements |

Dépendances **_Step:_**

* L’ID de programme (étape 2) est requis avant que des jetons, des listes ou des parcours puissent être joints.
* Le `smartListId` de l’étape 4 est transmis à `create_journey` à l’étape 5. Son omission laisse le nœud d’entrée d’audience du parcours vide.
* L’invite de parcours commence toujours _Commencez par le nœud d’audience Personne_ pour vous assurer qu’un nœud d’entrée est renseigné.

## Ressources de sortie

### Programme

Conteneur de niveau supérieur. Sa vue détaillée expose les onglets suivants :

| Tabulation | Contenu |
|---|---|
| **Vue d’ensemble** | Nom, description, type de programme, statut, emplacement du dossier, horodatages |
| **Attributs** | Champs personnalisés définis par type (uniquement si le type de programme les active) |
| **Jetons** | Jetons d’`my.*` inclus dans ce programme |
| **Parcours** | Parcours contenus dans le programme |

### Jetons

Valeurs de `my.*` réutilisables incluses dans le programme (par exemple, `my.eventDate`). Chacun possède un type (`text`, `date`, `rich text`, `score` ou `number`) et une valeur. Ils sont résolus dans les e-mails et le contenu dans la portée du programme.

### Liste des personnes

Une liste de personnes dynamique (intelligente) créée à partir de critères d’audience via des règles générées basées sur des attributs, sous le programme.

### Parcours

Un parcours de personne commençant par un nœud d’entrée d’audience de personne lié à la liste de personnes de l’étape 4, suivi des points de contact du résumé (par exemple, _envoyer un e-mail de bienvenue après 1 jour, suivi après 3 jours_). Si une date de mise en production est définie, le parcours peut être publié immédiatement ou planifié.

## Résolution du type de programme

Les programmes sont **liés de manière permanente** à un type de programme défini par le client lors de la création ; ceci ne peut pas être modifié par la suite. Le flux résout le type explicitement via `browseProgramTypes` dans tous les cas.

| Dossier | Comportement |
|---|---|
| **Plusieurs types disponibles** | Fait correspondre un bref libellé à un type (tel que salon/stand/expo = *salon*/*événement* ; webinaire = *webinaire*/*événement* ; culture/goutte = *culture* ; aucun signal clair = *Défaut*). Si aucune correspondance n’est trouvée, le collaborateur répertorie les types et tâches disponibles. |
| **Client par défaut uniquement** | Utilise *Par défaut* et note qu’un administrateur peut ajouter des [types de programme](../admin/program-types.md) personnalisés. |
| **Aucun type configuré** | Arrête : la création échouerait. Invite un administrateur à configurer les types de programme avant de réessayer. |

## Valeurs par défaut

| Paramètre | Par défaut |
|---|---|
| **Dossier** | Racine Workspace (si aucun dossier n’est spécifié) |
| **Type de programme** | *Par défaut* (si aucun signal bref et aucune sélection manuelle) |
| **Attributs** | Persona dérivé, intention dérivée, niveau d’engagement inclus par défaut (droit d’opposition disponible) |
| **Publication** | Non automatique pour les futures dates de mise en production : cette option est signalée comme étape de `ACTIVATE journey by {date}` manuelle ; la publication immédiate uniquement lors du lancement immédiat et confirmée. |
| **Point de contrôle** | Aucune ressource n’est créée avant l’approbation explicite |

## Limites

| Limite | Détail |
|---|---|
| **Limite de longueur courte** | ~30 000 caractères ; les briefs tronqués perdent leur contenu de fin — placez les éléments essentiels en premier |
| **Type de programme non modifiable** | Ne peut pas être modifié après la création ; vérifiez le type correct avant de valider |
| **Champs internes obligatoires** | `parent` et `programTypeId` sont toujours définis ; l’omission de `parent` entraîne un refus d’accès ; l’omission d’un type revient silencieusement à *Par défaut* |
| **Le Parcours nécessite une liste de personnes** | La `smartListId` de l’étape 4 est obligatoire pour l’étape 5 ; le flux l’applique |
| **Appartenance à une liste asynchrone** | Les listes statiques (à partir de critères) s’affichent pendant plusieurs minutes, et non instantanément |
| **Gestion des erreurs** | Les échecs d’outil sont signalés avec l’erreur exacte ; un collègue vous invite à confirmer l’entrée et à réessayer |
| **Collisions de noms** | Non résolu automatiquement : un nom différent sera demandé |
| **Périmètre** | Marketo Optimizer uniquement ; les utilisateurs [!DNL Marketo Engage] doivent utiliser des compétences distinctes de création/planification de programme |


## Vérification de la qualité

Une fois la création terminée, Coworker propose :

> « Souhaitez-vous que j’exécute une vérification de l’assurance qualité pour valider tout avant le lancement ? »

Confirmez pour exécuter `qa_program_preview`, puis `qa_program`. Le processus renvoie un rapport des contrôles réussis, échoués et des avertissements éventuels, ainsi que les étapes suivantes recommandées.
