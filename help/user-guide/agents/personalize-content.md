---
title: Personnaliser le contenu d'un e-mail par persona
description: Utilisez les compétences de Personalization de contenu dans Marketo Optimizer pour transformer un e-mail en variantes basées sur les personas et basées sur les données. Personnaliser ou analyser des e-mails.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---


# Personnaliser le contenu des e-mails par persona

La compétence Personalization de contenu _transforme un e-mail en variantes basées sur les rôles et basées sur les données. Vous n’avez donc pas à créer un e-mail distinct pour chaque audience._ Au lieu d’envoyer un seul message après un événement, cette compétence résout votre audience en [personnage dérivé](../audiences/personas.md) cohortes, surface les informations et génère des variantes personnalisées. Chaque variante est enregistrée en tant que contenu conditionnel dans un seul e-mail. Ainsi, chaque personne reçoit automatiquement la version qui correspond à son persona lorsqu’un parcours l’envoie.

* **Compétences** - `content-personalization`
* **Appel** - Dans l’interface [chat](./chat-interface.md), décrivez une audience cible pour un nouvel e-mail, ou sélectionnez **[!UICONTROL Personnaliser cet e-mail]** ou **[!UICONTROL Analyser cet e-mail]** sur un e-mail existant dans un nœud [Envoyer un e-mail](../marketing/action-nodes.md)
* **Lit à partir de / écrit sur** - [!DNL Marketo Optimizer]

## Principaux concepts {#key-concepts}

| Terme | Définition |
|---|---|
| **cohorte Persona** | Groupe de personnes qui partagent un profil [ dérivé](../audiences/personas.md) tel que _PDG/PDV_ ou _contributeur individuel_. |
| **Segment** | Groupe de personnes défini selon n’importe quel critère, comme une personne, un secteur ou un niveau d’engagement. Une cohorte de personnages est un segment défini spécifiquement par des personnages dérivés partagés. |
| **Groupe cible** | L’audience que vous décrivez en langage naturel. La compétence la résout en cohortes de personas correspondantes. |
| **** | Une conclusion basée sur les données à propos du message, du positionnement ou du ton qui fonctionne le mieux pour une cohorte de personas, tirée de vos propres données. |
| **Variante** | Version personnalisée des sections d’e-mail que vous avez choisi de personnaliser, générée pour une cohorte de personas. |
| **E-mail personnalisé IA** | L’e-mail unique enregistré qui regroupe chaque variante en tant que bloc [contenu conditionnel](../content/conditional-content.md). |
| **Audit des emails** | Analyse d’un e-mail existant par rapport à chacun de vos segments de groupe cible, montrant ce qui résonne et ce qu’il faut améliorer pour chaque profil avant de le personnaliser. |

## Conditions préalables {#prerequisites}

* Accès à [!DNL Marketo Optimizer] avec Coworker activé.
* [Rôles dérivés](../audiences/personas.md) résolus dans vos données. La compétence s’appuie sur ces classifications pour créer des cohortes de personas. La prise en charge des personas personnalisés est prévue pour une version ultérieure.
* Suffisamment de données historiques pour obtenir des informations. Si les informations ne sont pas disponibles pour une cohorte de personas, la compétence vous indique que les données sont insuffisantes et se replie sur les bonnes pratiques générales pour cette personne.
* Un [ modèle d’e-mail ](../content/templates.md) ou un e-mail existant référencé par un nœud d’action [_Envoyer un e-mail_](../marketing/action-nodes.md).
* Un parcours de personne](../marketing/person-journeys.md) qui contient le nœud d’action _Envoyer un e-mail_ utilisé pour diffuser l’e-mail personnalisé.[

## Création et personnalisation d’un e-mail à partir d’un modèle {#create-personalize-from-template}

Ce flux crée un nouvel e-mail et le personnalise dans la même conversation.

1. **Fournissez le contenu.** Chargez un résumé du contenu ou décrivez le contenu de votre choix en langage naturel.

1. **Sélectionnez un [modèle](../content/templates.md)** dans votre bibliothèque de modèles.

1. **Examiner le brouillon.**

   Coworker mappe votre contenu au modèle et génère un e-mail de brouillon. Vous pouvez effectuer des modifications de texte de base en ligne.

   >[!WARNING]
   >
   >Seules les modifications de texte de base sont disponibles en ligne lors de la création. Pour des modifications avancées, enregistrez l’e-mail et ouvrez-le dans l’[espace de conception visuelle](../content/email-authoring.md).

1. **Décrivez le groupe cible** en langage naturel.

1. **Examinez les cohortes de personas résolues**.

   Un collègue examine vos données et renvoie les cohortes de persona qui correspondent à votre description, avec un nombre pour chacune d’elles. Modifiez la description du groupe cible et réessayez si nécessaire.

1. **Confirmez le groupe cible**.

   Ensuite, le collaborateur récupère des informations pour chaque cohorte de personnes résolue.

1. **Sélectionnez les sections à personnaliser** telles que l’objet ou une section de corps, et passez en revue les variantes générées.

   Régénérer une variante si elle ne correspond pas. Le nombre de cohortes de personnages n’est pas fixe. Cela dépend de votre groupe cible et de vos données.

1. **Enregistrez l’e-mail**.

   Toutes les variantes sont stockées dans un seul e-mail personnalisé d’IA, et non dans des e-mails distincts.

<!-- screenshot: Coworker chat panel showing the resolved persona cohorts with counts, and the "Personalized variants" review grid -->

## Analyse d’un email existant {#analyze-existing-email}

Sur un nœud de parcours [_Envoyer un e-mail_](../marketing/action-nodes.md) qui fait référence à un e-mail existant, le panneau **[!UICONTROL Prendre une action]** affiche le nom de l’e-mail avec deux options : **[!UICONTROL Personnaliser cet e-mail]** et **[!UICONTROL Analyser cet e-mail]**.

<!-- screenshot: Send Email node "Take an action" panel showing the email name and the Personalize this email / Analyze this Email options -->

Sélectionnez **[!UICONTROL Analyser cet e-mail]** pour exécuter un audit des e-mails :

1. **Décrivez le groupe cible** pour lequel vous souhaitez effectuer une personnalisation, en termes de son rôle.

   Par exemple, _Personnes ayant des rôles marketing_ ou _Personnes ayant des fonctions de leadership_.

1. **Vérifier l’audit des e-mails.**

   Coworker résout votre description en segments de persona et affiche une vignette **Audit des e-mails** répertoriant chaque segment, puis examine l’e-mail par rapport à chacun d’eux pour mettre en évidence ce qui résonne et ce qui doit être amélioré.

1. Un collègue demande ce qu’il faut faire ensuite, notamment **[!UICONTROL voir l’audit section par section]** et **[!UICONTROL personnaliser cet e-mail]**.

1. Sélectionnez **[!UICONTROL Voir l’audit section par section]** pour ouvrir une vue **_Analyse e-mail_** avec un sélecteur de persona et des recommandations spécifiques pour chaque section.

   Chaque section indique le nombre de modifications recommandées et chaque persona indique le nombre de recommandations (`4 recommendations for SVP/VP`, par exemple). Vous pouvez également appliquer les recommandations directement en saisissant _personnaliser_ dans le chat.

1. Dans l’audit, sélectionnez **[!UICONTROL Personnaliser cet e-mail]** pour appliquer les informations et générer des variantes.

   Voir la section suivante, [_Personnaliser un e-mail existant_](#personalize-existing-email).

<!-- screenshot: Email analysis view with persona selector, per-section "N changes" badges, and "what needs work" recommendations -->

## Personnaliser un email existant {#personalize-existing-email}

Sélectionnez **[!UICONTROL Personnaliser cet e-mail]** sur un nœud d’action _Envoyer un e-mail_ ou continuez à partir d’un [audit des e-mails](#analyze-existing-email) pour personnaliser un e-mail que vous avez déjà créé.

1. **Examinez les cohortes de personas résolues.**

   Un collègue examine vos données et renvoie les cohortes de persona qui correspondent à votre description, avec un nombre pour chacune d’elles. Modifiez la description du groupe cible et réessayez si nécessaire.

   Si vous êtes arrivé à cette étape à partir d’un audit d’e-mail, Coworker continue directement à partir des informations d’audit.

1. **Sélectionnez les sections à personnaliser** dans l’aperçu de l’e-mail, telles que l’objet et les sections de contenu spécifiques, puis confirmez.

1. **Vérifier les variantes générées.**

   En plus des rôles, les variantes peuvent également varier selon le secteur, par exemple un CXO dans le secteur des soins de santé par rapport à un CXO dans le secteur des services financiers. Coworker présente une grille **[!UICONTROL Variantes personnalisées]**, une carte par cohorte de persona, chacune avec un objet, un titre, un corps et une option **[!UICONTROL Aperçu]**.

   Sélectionnez l’icône _Informations_ sur une carte pour afficher l’insight derrière cette variante (le persona sur lequel elle repose et l’insight d’engagement qui l’a façonnée) et régénérez une variante si nécessaire.

   Vous pouvez filtrer la grille par persona.

1. **Enregistrez la visionneuse.**

   Cliquez sur **[!UICONTROL Enregistrer]** et confirmez. Un collègue confirme que l’e-mail est désormais disponible dans la bibliothèque d’IA, puis demande s’il faut appliquer les modifications à l’e-mail d’origine également, ce qui le met à jour.

<!-- screenshot: "Personalized variants" grid showing persona cards with subject, headline, body, Preview, and the info-icon insight tooltip -->

## Sortie enregistrée et utilisation dans un parcours {#saved-output}

Quel que soit le flux à partir duquel vous commencez, la personnalisation génère un seul e-mail personnalisé **AI** stocké dans la bibliothèque d’IA. L’e-mail contient des blocs [contenu conditionnel](../content/conditional-content.md) indexés par persona. Pour modifier des sections, l’ouvrir dans l’[espace de conception visuelle](../content/email-authoring.md) et prévisualiser la résolution de chaque bloc saisi par une personne à l’aide du clavier, utilisez **[!UICONTROL Simuler du contenu]**.

Pour utiliser l’e-mail dans un parcours, ajoutez un nœud [Envoyer un e-mail](../marketing/action-nodes.md) et sélectionnez **[!UICONTROL E-mails personnalisés IA]** au lieu de **[!UICONTROL Créer un e-mail]**, puis sélectionnez l’e-mail enregistré. Appliquez votre configuration et vos règles métier au nœud comme d’habitude.

<!-- screenshot: Send Email node configuration with "AI Personalized Emails" selected and the saved email applied -->

## Comportement au moment de l’exécution {#run-time-behavior}

Vous sélectionnez l’e-mail personnalisé IA unique dans le parcours, et non une variante par audience. Lorsque le parcours s’exécute, l’e-mail est automatiquement résolu sur la variante correspondant au persona de chaque destinataire. Vous ne choisissez pas de variante par destinataire.

## Limites {#limitations}

| Limite | Détail |
|---|---|
| **Personnages personnalisés** | Pas encore pris en charge. La compétence classe uniquement les cohortes de personnages à partir de [personnages dérivés](../audiences/personas.md) prêts à l’emploi. |
| **Données insuffisantes pour obtenir des informations** | Si vos données ne prennent pas en charge une insight pour une cohorte de personas, la compétence l’indique et se réfère aux bonnes pratiques générales pour cette personne. |
| **Modification en ligne lors de la création** | Seules les modifications de texte de base sont disponibles en ligne lorsque vous [créez et personnalisez un email à partir d’un modèle](#create-personalize-from-template). Les modifications avancées nécessitent l’[espace de conception visuelle](../content/email-authoring.md). |
| **Point de départ requis** | La personnalisation d’un e-mail nécessite un modèle ou un e-mail existant référencé par un nœud Envoyer un e-mail . |
