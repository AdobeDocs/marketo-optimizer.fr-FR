---
title: Présentation de CX Enterprise Coworker dans Adobe Marketo Optimizer
description: Découvrez comment CX Enterprise Coworker utilise les compétences de Marketo Optimizer pour créer et adapter des programmes, vérifier la préparation à la prise de décision par l’IA et appeler les outils MCP.
autotag-review: '2026-11-24T22:43:00.917Z'
TQID: https://experienceleague.adobe.com/V4Kww-NcdfbFxXqWrs7mPq7UYu8AREqDgyfvlMnlURM
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
  - id: 5229c72e-d79b-574f-a03e-5c4bf48172c3
    internal-label: AI Decisioning
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
    internal-label: Programs
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: 418b81a0a39eca0ca7b537c76da972df7eefd09f
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 2%
---

# [!DNL CX Enterprise Coworker] dans [!DNL Adobe Marketo Optimizer] {#coworker-overview}

La conversation [!DNL CX Enterprise Coworker] est une interface de conversation permettant d&#39;effectuer des tâches dans [!DNL Adobe Marketo Optimizer]. Décrivez un objectif en langage simple et [!DNL Coworker] planifie les tâches, les exécute dans [!DNL Marketo Optimizer], valide les résultats et fournit le travail terminé pour votre approbation.

[!DNL Coworker] utilise des compétences créées pour [!DNL Marketo Optimizer] pour vous guider dans les tâches courantes des opérations marketing : création d’un nouveau programme, adaptation d’un programme [!DNL Marketo Engage] existant et vérification que vos données sont prêtes pour la prise de décision par l’IA.

[!DNL Coworker] respecte les [[!DNL Marketo Optimizer] autorisations](../start/permissions-reference.md) existantes de votre organisation. Vous pouvez uniquement effectuer des actions que vous êtes déjà autorisé à effectuer, et les administrateurs contrôlent le moment où vous disposez d’un accès en écriture. [!DNL Coworker] fait partie de l’écosystème Adobe et ne se limite pas à [!DNL Marketo Optimizer].

Pour plus d’informations, consultez les éléments suivants :

* [Présentation de la conversation [!DNL Adobe CX Enterprise Coworker]](https://experienceleague.adobe.com/en/docs/coworker/content/chat/overview)
* [Interface de conversation dans  [!DNL Marketo Optimizer]](./chat-interface.md)
* [[!DNL Coworker] compétences dans  [!DNL Marketo Optimizer]](./skills.md)

## [!DNL Marketo Optimizer] compétences dans [!DNL CX Enterprise Coworker] {#skills}

Utilisez les compétences spécifiques suivantes pour créer et adapter des programmes ou évaluer la préparation des données.

| Compétence | Qu’est-ce que cela peut vous aider ? | Exemple de requête |
| --- | --- | --- |
| `program-creation-marketo-optimizer` | Créez un programme marketing [!DNL Marketo Optimizer] de bout en bout. [!DNL Coworker] vous guide de votre objectif à un programme créé. | Chargez un brief de campagne, puis demandez : _Créez un programme à l&#39;aide du brief ci-joint._ |
| `adapt-program-marketo-optimizer` | Adapter, migrer ou convertir un programme [!DNL Marketo Engage] existant en programme [!DNL Marketo Optimizer]. | _Adaptez notre programme de formation au webinaire d’entreprise du 3e trimestre de [!DNL Marketo Engage] en [!DNL Marketo Optimizer]._ |
| `ai-decisioning-health-marketo-optimizer` | Indiquez si les données de votre client sont prêtes pour la prise de décision par l’IA, la couverture des histoires, la richesse des caractéristiques et la couverture personnelle. | _Quelles données sont utilisées pour la prise de décision par l’IA ?_ |

### Exemple d’invite de création de programme {#program-creation-prompt}

Chargez un résumé ou décrivez directement le programme. Incluez l&#39;audience, le parcours, le contenu et les paramètres que [!DNL Coworker] doit utiliser.

Le diagramme résume les sections d’invite dans l’exemple ci-dessous. Il indique comment organiser la demande, et non l’ordre dans lequel les personnes se déplacent dans le parcours.

![Huit sections d&#39;invite de création de programme : objectif du programme, audience, parcours avec des invitations basées sur l&#39;intention, contenu d&#39;e-mail, activation de LinkedIn, gestion de l&#39;enregistrement, suivi post-événement et paramètres.](./assets/coworker-program-creation-prompts.svg){width="800" zoomable="yes"}

Développez chaque section pour afficher l’exemple d’invite.

+++Objectif du programme

_Créez un programme marketing B2B nommé Experience Cloud Leadership Forum - Sommet de l’expérience optimisé par l’IA, qui se déroule du 3 août au 3 décembre, à l’aide d’e-mails et de LinkedIn. L&#39;événement aura lieu au Bay Area Innovation Centre à 9 h. Démarrer le parcours immédiatement._

+++

+++Audience

_Ciblez des personnes avec une intention de produit quelconque pour Experience Cloud et un score d’engagement supérieur à 1. Exclure les profils désabonnés et suspendus par le marketing._

+++

+++Parcours

_Utilisez le meilleur chemin suivant pour partager l’audience par intention d’Experience Cloud élevée, Medium et faible. Envoyez des invitations par e-mail personnalisées adaptées à chaque niveau d’intention. Fusionner les chemins et attendre deux jours. Vérifiez les ouvertures d’e-mail, les clics, l’engagement du contenu et les enregistrements. Envoyer un aperçu de l&#39;agenda aux membres engagés ; activer les membres non engagés sur LinkedIn et attendre deux jours. Fusionnez les chemins engagés et envoyez un rappel d’enregistrement final 10 jours avant l’événement. Activer l&#39;optimisation de l&#39;heure d&#39;envoi pour tous les e-mails._

+++

+++Contenu d’e-mail

_Créez trois e-mails : invitation exécutive (6 semaines avant l&#39;événement), aperçu de l&#39;agenda (six semaines avant l&#39;événement) et rappel d&#39;inscription final (10 jours avant l&#39;événement). Incluez les objets pertinents, les pré-titres, les appels à l’action (réserver ma place, afficher l’ordre du jour, terminer l’inscription) et le contenu personnalisé par l’IA à l’aide de l’histoire de personne, de la classification de persona, du secteur, de l’intérêt pour la solution, de l’engagement récent et de l’intention d’Experience Cloud. Insérez une image de lieu dans l&#39;invitation, mais pas de bannière dans l&#39;aperçu de l&#39;agenda._

+++

+++LinkedIn

_Ciblez les membres non engagés avec du contenu sponsorisé favorisant la transformation de l&#39;expérience client et la personnalisation de l&#39;IA._

+++

+++Inscription

_Quittez immédiatement les membres inscrits du parcours d&#39;invitation et envoyez un e-mail de préparation de l&#39;exécutif avec des sujets de discussion générés par l&#39;IA, un ordre du jour personnalisé, les détails du lieu, les sessions recommandées et un lien de calendrier._

+++

+++Post-événement

_Acheminez les participants vers le programme de suivi du leadership d’Experience Cloud avec un résumé, des enregistrements, des ressources et une révision de la qualification des ventes. Envoyez les points forts du sommet, le contenu à la demande et les invitations à des événements futurs._

+++

+++Paramètres

_Définissez my.responseToEmail sur `events@example.com` et my.senderName sur Experience Cloud Events. Utilisez un modèle réutilisable où seuls la ville, le lieu, les sujets principaux et l&#39;orientation du secteur changent._

+++

Pour plus d&#39;informations sur la préparation d&#39;un brief, voir [Créer un programme à partir d&#39;un brief](./program-from-brief.md).

## Exemples de cas d’utilisation {#use-cases}

### Créer un programme après avoir vérifié la préparation des données {#check-readiness-create-program}

Un responsable des opérations marketing souhaite savoir que le client est prêt pour la prise de décision par l’IA avant de créer un nouveau programme basé sur les comptes.

1. Pour passer en revue la couverture de l’histoire, la richesse des caractéristiques et la couverture du profil, exécutez le [contrôle de l’intégrité de la prise de décision par l’IA](./ai-decisioning-health.md). Par exemple, demandez-moi : _Afficher les données Marketo utilisées pour la prise de décision par l’IA._
1. Combler les lacunes identifiées dans le rapport.
1. Chargez un brief de campagne et demandez : _Créez un programme avec le brief ci-joint._
1. Examinez et approuvez le programme lorsque [!DNL Coworker] présente le résultat.

Le résultat est un rapport de préparation qui identifie les lacunes, suivi d&#39;un programme basé sur des données qui peuvent soutenir la prise de décision par l&#39;IA.

### Déplacer un programme [!DNL Marketo Engage] existant dans [!DNL Marketo Optimizer] {#adapt-program}

Une équipe de génération de la demande souhaite qu&#39;un programme éprouvé s&#39;exécute dans [!DNL Marketo Optimizer] sans le recréer manuellement.

1. Nommez le programme [!DNL Marketo Engage] à adapter. Par exemple : _Adaptez le programme de formation au webinaire d’entreprise du 3e trimestre de [!DNL Marketo Engage] en [!DNL Marketo Optimizer]._
1. [!DNL Coworker] mappe le programme à [!DNL Marketo Optimizer] éléments et signale tout ce qui n’est pas converti.
1. Examinez le résultat et approuvez-le.

Le résultat est un programme converti pour votre examen, ainsi qu’une liste d’éléments nécessitant une décision manuelle.

## [!DNL Marketo Optimizer] outils MCP {#mcp-tools}

Les compétences [!DNL Coworker] appellent les 37 outils suivants sur le serveur MCP (Model Context Protocol) [!DNL Marketo Optimizer]. Chaque nom d’outil porte le préfixe `marketo-optimizer__`.

Cette référence couvre les outils documentés par des compétences enregistrées, y compris les compétences de support utilisées pendant un workflow. Il n’indique pas le statut de déploiement ni la fréquence d’utilisation. Les noms de compétence figurant dans ce tableau suivent la référence de l’outil et peuvent différer des noms de compétence spécifiques au produit répertoriés ci-dessus.

| Outil | Compétences | But |
| --- | --- | --- |
| `marketo-optimizer__get_workspace_root_tree` | `program-creation-marketo-optimizer` | Recherchez la zone d’espace de travail ou le sous-dossier nommé pour un nouveau programme. |
| `marketo-optimizer__create_program` | `program-creation-marketo-optimizer` | Créez un programme dans la zone ou le dossier confirmé. |
| `marketo-optimizer__list_programs` | `program-creation-marketo-optimizer`, `landing-page-authoring` | Parcourez les programmes ou trouvez où déposer une landing page. |
| `marketo-optimizer__get_program` | `program-creation-marketo-optimizer` | Lire un programme par ID. |
| `marketo-optimizer__update_program` | `program-creation-marketo-optimizer` | Mettez à jour les métadonnées du programme, telles que son nom. |
| `marketo-optimizer__create_program_token` | `program-creation-marketo-optimizer` | Créer ou corriger un jeton de programme approuvé. |
| `marketo-optimizer__list_program_tokens` | `program-creation-marketo-optimizer` | Lire les jetons résolus d’un programme. |
| `marketo-optimizer__create_dynamic_people_list_with_rules` | `program-creation-marketo-optimizer` | Créez une liste de personnes liées au programme et générez des règles d’audience à partir d’une description. |
| `marketo-optimizer__list_people_journeys` | `adapt-program`; référence partagée du module externe de canal | Recherchez une collision de nom de parcours de destination, recherchez un parcours existant après un résultat imprécis ou parcourez les parcours pour trouver du travail sur les canaux. |
| `marketo-optimizer__create_person_journey` | `program-creation-marketo-optimizer`, `adapt-program`, `channel-content-authoring` | Créez un parcours lié à un programme, lancez un parcours adapté ou créez un parcours manquant pour un canal e-mail. |
| `marketo-optimizer__get_person_journey` | `program-creation-marketo-optimizer`, `adapt-program` ; référence partagée du module externe de canal | Lisez un parcours ou sa zone de travail, vérifiez les modifications intermédiaires ou recherchez un parcours pour le travail sur les canaux. |
| `marketo-optimizer__update_person_journey` | `adapt-program` | Ajoutez une étape de création approuvée à la fois au parcours de destination. |
| `marketo-optimizer__run_person_journey_simulation` | `program-creation-marketo-optimizer` | Valider un flux de parcours sans publication. |
| `marketo-optimizer__run_program_qa` | `program-creation-marketo-optimizer` | Exécutez une vérification de préparation en lecture seule sur le programme et ses parcours. |
| `marketo-optimizer__create_channel` | `channel-content-authoring` ; `program-creation-marketo-optimizer` et `image-to-html` via la remise | Créer et lier un canal. Pour les e-mails, le premier appel répertorie les modèles ; le second utilise le modèle sélectionné pour créer et lier l’e-mail. |
| `marketo-optimizer__get_channel` | `channel-content-authoring` | Lire un canal, y compris éventuellement son objet d’e-mail et HTML. |
| `marketo-optimizer__list_channels` | `channel-content-authoring` | Parcourez les canaux par type, éventuellement filtrés par nom. |
| `marketo-optimizer__update_channel_content` | `channel-content-authoring` ; `image-to-html` jusqu’à la remise | Mettre à jour l’objet d’un e-mail dans HTML, y compris en appliquant une HTML convertie. |
| `marketo-optimizer__image_to_html` | `image-to-html` | Démarrez une conversion asynchrone de conception d’e-mail et récupérez l’HTML modifiable. |
| `marketo-optimizer__list_asset_library_images` | `landing-page-authoring` | Recherchez des images de remplacement pour les emplacements de page de destination. |
| `marketo-optimizer__add_asset_to_program_or_folder` | `landing-page-authoring` | Enregistrez une nouvelle page de destination dans le programme ou dossier Optimizer sélectionné. |
| `marketo-optimizer__get_person_story` | `personalization-engine-health` | Lire l’histoire de personnalisation d’une personne à l’aide d’un identifiant numérique. |
| `marketo-optimizer__get_persona_story` | `personalization-engine-health` | Lisez l’histoire pour obtenir un nom de personnage exact. |
| `marketo-optimizer__run_arbitration` | `personalization-engine-health` | Attribuez un nouveau score et sélectionnez à nouveau les parcours pour les personnes qualifiées après confirmation explicite. |
| `marketo-optimizer__get_arbitration_summary` | `personalization-engine-health` | Consultez les statistiques récapitulatives pour la dernière exécution d’arbitrage. |
| `marketo-optimizer__get_arbitration_decisions` | `personalization-engine-health` | Lire les décisions par personne de la dernière exécution d&#39;arbitrage. |
| `marketo-optimizer__get_ai_decisioning_health_summary` | `ai-decisioning-health` | Récupérez le rapport global de préparation des clients. |
| `marketo-optimizer__get_persona_distribution` | `ai-decisioning-health` | Indiquez le nombre et les pourcentages de personnages. |
| `marketo-optimizer__get_people_without_personas` | `ai-decisioning-health` | Indiquez le nombre et le pourcentage de personnes sans persona. |
| `marketo-optimizer__get_person_story_attribute_coverage` | `ai-decisioning-health` | Mesurez la couverture caractéristique-catégorie et identifiez les champs renseignés. |
| `marketo-optimizer__get_person_story_data_completeness` | `ai-decisioning-health` | Rapport sur la richesse, l’exhaustivité et la variation des histoires par persona. |
| `marketo-optimizer__get_person_story_coverage` | `ai-decisioning-health` | Couverture des articles de rapport, tendances et génération en attente. |
| `marketo-optimizer__get_personalization_story_pipeline_status` | `ai-decisioning-health` | Lire le statut du pipeline, l’historique d’exécution et la durée signalée. |
| `marketo-optimizer__get_person_story_refresh_backlog` | `ai-decisioning-health` | Compter les histoires en attente d&#39;actualisation car les données sources ont changé. |
| `marketo-optimizer__get_person_intent_signal_coverage` | `ai-decisioning-health` | Mesurez l’intention du produit, l’intention du mot-clé et la couverture de l’activité. |
| `marketo-optimizer__get_person_story_activity_coverage` | `ai-decisioning-health` | Générez un rapport sur les champs d’engagement capturés et les tendances agrégées des activités. |
| `marketo-optimizer__get_person_audience_membership_distribution` | `ai-decisioning-health` | Indiquez la moyenne et la distribution des adhésions à l’audience par personne. |
