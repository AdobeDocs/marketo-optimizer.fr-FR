---
title: Compétences du collègue
description: Examinez les compétences de vos collègues dans Marketo Optimizer pour les parcours, les audiences, les programmes, le contenu, les analyses et la prise de décision par l’IA. Découvrez ce que chaque compétence peut vous apporter.
autotag-review: '2026-09-22T14:02:17.516Z'
TQID: 'https://experienceleague.adobe.com/nNFB9UEghfqVvnBrNtTDnpnLUKKKMAU2nY1Pqt0KkUQ'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: 5334f0f5d9d958ea47b055b067a7308950352e9c
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 4%
---

# Compétences des collègues

Une _compétence_ est un workflow empaqueté que Coworker peut exécuter. Les compétences sont les composants qui sous-tendent le menu `/` et les requêtes en langage naturel. Chaque compétence regroupe des instructions détaillées et les outils spécifiques nécessaires à une tâche, comme la publication d’un parcours, la comparaison de deux listes de personnes ou la création d’un modèle de notation.

La classification de chaque compétence reflète le type d’action qu’elle effectue :

* _Rechercher_ les compétences recherchent ou répertorient les enregistrements existants.
* _Analyser_ examiner les compétences, comparer ou générer des rapports sur les données sans les modifier.
* Les compétences _Affichage_ affichent un rapport ou une mesure en lecture seule.
* Les compétences _Modifier_ modifient les paramètres ou le contenu d’un objet existant.
* _Créer_ les compétences permettent de créer un objet.

## Parcours {#journeys}

Ces compétences permettent de créer, publier, déboguer et gérer des parcours de personne.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Observabilité du Parcours** | Déboguer et surveiller les mouvements des personnes dans un parcours, y compris les chemins, le timing, les divisions, les décrochages et le temps d’arrêt. Voir _[Déboguer et surveiller la progression du parcours](./journey-observability.md)_. | Analyser |
| **Contrôle de trafic de Parcours** | Simuler la manière dont les profils se répartissent sur tous les parcours actifs. | Analyser |
| **Publication Parcours** | Publiez, lancez ou planifiez un parcours, y compris le mode de démarrage, les dates et la confirmation. | Modifier |
| **Arrêt du Parcours** | Abandonnez un parcours en cours d’exécution pour l’arrêter immédiatement ou fermez-le pour le réduire de manière élégante. | Modifier |
| **Parcours Modifier les dates** | Modifiez la date de début ou de fin sur un brouillon, un parcours planifié ou un Live Copy sans le republier. | Modifier |
| **Parcours de rentrée** | Configurez les paramètres de rentrée d’un parcours, notamment si la rentrée est autorisée, le délai de refroidissement et le nombre maximal d’entrées. | Modifier |
| **Création de Parcours** | Créez et modifiez des parcours de personne à l’aide de requêtes en langage naturel. | Créer |
| **Webinaire en Parcours** | Configurez un parcours promotionnel avant un webinaire et un parcours de suivi après. | Créer |

## Listes d’audiences et de personnes {#audience-people-lists}

Ces compétences permettent de créer et de gérer des listes de personnes et des définitions d’audience.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Parcourir les membres de la liste dynamique** | Parcourez et filtrez les membres d’une liste de personnes dynamique ou statique. | Rechercher |
| **Comparaison de listes de personnes** | Comparer deux listes de personnes et afficher les membres qui se chevauchent | Analyser |
| **Supprimer de la liste statique** | Supprimez les membres qui correspondent aux critères de langage naturel d’une liste statique. | Modifier |
| **Création d’une audience** | Adapter une liste dynamique [!DNL Marketo Engage], créer une liste de personnes ou ajouter ou mettre à jour ses règles. Voir _[Création d’audiences pour les programmes](./audience-creation.md)_. | Créer |

## Programmes, dossiers et canaux {#programs-folders-channels}

Ces compétences gèrent la structure du programme, les jetons et la configuration des canaux.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Créer un programme** | Créez des programmes à partir d’un résumé de campagne. Voir _[Créer un programme à partir d’un brief](./program-from-brief.md)_. | Analyser |
| **Adapter le programme** | Générer des récits de migration à partir de programmes [!DNL Marketo Engage] pour l&#39;adaptation [!DNL Marketo Optimizer]. | Analyser |
| **Jetons de ressources** | Créez et gérez des valeurs `{{my.token}}` dans des programmes, des dossiers et des parcours. | Modifier |
| **Canaux FCS** | Créer, publier, arrêter et cloner des canaux dans le service Canaux , y compris les schémas XDM et la configuration. | Modifier |
| **Création de dossier** | Créez des dossiers d’organisation dans l’arborescence de ressources. | Créer |
| **Campagne intégrée WhatsApp** | Créez et publiez une campagne intégrée [!DNL WhatsApp] sur un nœud de parcours. | Créer |
| **Création de programme marketing** | Créez un programme complet, comprenant des sous-dossiers, des jetons, des listes de personnes et des parcours. | Créer |
| **Création de programmes et de lots de Parcours** | Créez plusieurs paires de programmes et de parcours dans une seule demande par lots. | Créer |

## E-mail et pages de destination {#email-landing-pages}

Ces compétences permettent de créer et de gérer des e-mails, des formulaires et des pages de destination.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Liste des Forms** | Répertoriez les formulaires et affichez leurs détails et champs. | Rechercher |
| **Liste des pages de destination** | Répertorier les pages de destination, afficher leurs détails et gérer leur statut de brouillon ou publié. | Rechercher |
| **Audit des e-mails** | Effectuez l’audit d’un e-mail par rapport à son groupe cible, y compris l’inférence personnelle et un bref examen section par section. | Analyser |
| **Création d’e-mails** | Créez ou mettez à jour un nœud d’e-mail de parcours, y compris en effectuant la composition à partir d’un brief ou d’un PDF, en le liant à un nœud et en écrivant du contenu. | Modifier |
| **Création de formulaires** | Créez ou mettez à jour un formulaire de capture de prospect autonome, publiez-le et éventuellement incorporez-le dans une page de destination. | Créer |
| **Création de pages de destination** | Créez ou mettez à jour une page de destination à partir d’un brief, y compris la planification du contenu, la sélection des modèles, le remplissage des emplacements et l’ajout d’un formulaire, puis publiez-la. Joignez également une page de destination publiée en tant que lien call-to-action sur un e-mail. | Créer |
| **Vérification du rendu des emails** | Rechercher les problèmes de rendu de [!DNL Microsoft Outlook] dans un email et y remédier automatiquement. | Modifier |

## Personnalisation du contenu {#content-personalization}

Cette compétence parcourt les modèles et personnalise le contenu des e-mails pour différents profils.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| Personalization de contenu **** | Parcourez et prévisualisez des modèles, puis modifiez le contenu ou générez des variantes. Voir _[Personnaliser le contenu d’un e-mail par persona](./personalize-content.md)_. | Créer |

## Analyses et optimisation {#analytics-optimization}

Ces compétences génèrent des rapports sur les performances et configurent l’optimisation de l’heure d’envoi et les modèles de notation.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Surface Analytics** | Générez des rapports d’analyse à partir de requêtes en langage naturel, couvrant les tendances d’activité, les performances des e-mails, les données de prospect et de compte, l’appartenance à des segments et à des listes, ainsi que les mesures de parcours. Les données du rapport sont actualisées toutes les deux heures. Voir _[Générer des rapports d’analyse](./surface-analytics.md)_. | Analyser |
| **Envoyer le rapport d’heure** | Affichez le rapport de performances de l’optimisation de l’heure d’envoi (STO) au niveau du parcours ou pour un nœud d’e-mail individuel. | Analyser |
| **Simulation STO d’e-mail** | Prévisualisez l’heure d’envoi prévue, la qualité de l’audience et la carte thermique d’engagement pour un nœud d’e-mail avant d’activer STO. | Analyser |
| **Optimisation de l’heure d’envoi** | Activer ou désactiver STO sur un nœud d’e-mail de parcours. | Modifier |
| **Configuration de l’engagement** | Affichez et modifiez les poids d’activité pour le modèle de score d’engagement de la personne. | Modifier |
| **Scoring Studio** | Répertorier et afficher les modèles de notation, puis en créer et en publier de nouveaux. Voir _[Création de modèles de notation personnalisés](./lead-scoring-model.md)_. | Créer |

## Prise de décision et intention de l’IA {#ai-decisioning-intent}

Ces compétences évaluent le niveau de préparation des données pour la prise de décision par l’IA et configurent le score d’intention.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **AI Decisioning Health** | Indiquez si les données d’une organisation sont prêtes pour la prise de décision par l’IA, y compris la disponibilité des prospects, la distribution des rôles, la richesse des histoires et l’intention. | Analyser |
| **Intention d’analyse** | Interroger et valider le classement des intentions au niveau du prospect, les tendances, ainsi que la taxonomie des produits et des mots-clés. | Analyser |
| **Configuration de l’intention** | Affichez et modifiez les poids d’activité pour le modèle de score d’intention de la personne. | Modifier |

## Gestion des connaissances et des compétences {#knowledge-skill-management}

Ces compétences répondent aux questions des produits et vous permettent d’acquérir de nouvelles compétences personnalisées.

| Compétence | Ce qu&#39;il fait | Type |
| --- | --- | --- |
| **Connaissance du produit** | Répondez aux questions pratiques et conceptuelles à l’aide de [!DNL Marketo Optimizer] documentation publiée sur Experience League. | Rechercher |
| **Création de compétences** | Créer, tester et affiner de nouvelles compétences personnalisées. | Créer |
