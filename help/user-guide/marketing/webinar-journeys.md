---
title: Parcours de promotion et de suivi de webinaires
description: Créez des parcours de promotion, de jour de diffusion et de formation post-webinaire autour d’un webinaire dans Marketo Optimizer et personnalisez le contenu à l’aide de jetons de webinaire.
keywords: null
role: User
feature: Person Journeys
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '823'
ht-degree: 0%

---


# Parcours de promotion et de suivi de webinaires

Après avoir ajouté un webinaire à un programme, créez un ou plusieurs [parcours &#x200B;](./person-journeys.md) dans ce même programme pour inviter des personnes, leur rappeler, animer la session et assurer un suivi par la suite.

>[!NOTE]
>
>Cette page traite de la création manuelle de ces parcours. Pour que Coworker crée les mêmes parcours pour vous à partir d’un modèle, voir [Créer des webinaires avec Coworker](../agents/webinar-creation.md).

## Création d’un parcours de promotion {#build-promotion-journey}

Un parcours de promotion type invite des personnes, suit leur inscription et leur rappelle l’approche du webinaire.

1. [Créez le parcours de personne](./person-journeys.md#create-a-person-journey).

1. [Sélectionnez une audience pour le parcours &#x200B;](./person-audience-node.md).

1. Ajoutez un nœud **[!UICONTROL Envoyer un e-mail]** avec un e-mail d’invitation.

   Utilisez des jetons de webinaire tels que _Titre_ et _Date et heure de début_ dans le contenu, ainsi qu’un lien vers la page d’enregistrement du webinaire.

1. Ajoutez un nœud **[!UICONTROL Prendre une action]**, sélectionnez l’action **[!UICONTROL Modifier le statut du membre du webinaire]**, sélectionnez le webinaire et définissez le statut sur _Invité_.

   Placez-le immédiatement après le nœud **[!UICONTROL Envoyer un e-mail]** de l’invitation.

   >[!NOTE]
   >
   >En règle générale, vous définissez uniquement _Invité_ et _Enregistré_ à partir d’un parcours de promotion. [!DNL Adobe Connect] définit normalement _Sur demande_, _Pas d’affichage_ et _Sur demande_ automatiquement. La même action peut remplacer ces statuts ultérieurs à partir d’un parcours si nécessaire, mais uniquement vers l’avant, correspondant à la progression linéaire décrite dans [_statut du webinaire_](webinars-overview.md#webinar-status).

1. Hébergez le formulaire d’enregistrement sur une [page de destination](../content/landing-pages.md).

1. Ajoutez un nœud **[!UICONTROL Prendre une action]**, sélectionnez l’action **[!UICONTROL Modifier le statut du membre du webinaire]**, sélectionnez le webinaire, puis définissez le statut sur _Enregistré_ (déclenché par l’envoi du formulaire).

   Le déplacement d’une personne vers _Enregistré_ effectue automatiquement deux opérations :

   * [!DNL Adobe Connect] génère l’URL de jointure individuelle de cette personne.
   * Il envoie l’e-mail de confirmation, si vous en avez configuré un, contenant le jeton _URL de jonction_.

1. Créez une cadence de rappel à l’aide des nœuds **[!UICONTROL Wait]** minutés par rapport au jeton du webinaire _Start Datetime_.

   Par exemple, définissez-le sur une semaine avant, un jour avant et une heure avant.

1. Ajoutez un nœud **[!UICONTROL Wait]** minuté dans le jeton du webinaire _End Datetime_ afin que le parcours s’interrompe jusqu’à la fin de la session active.

   Continuez pour [créer un parcours post-webinaire](#build-post-webinar-journey) à partir d’ici.

   >[!NOTE]
   >
   >Les modifications du statut du webinaire ne sont actuellement pas disponibles en tant que déclencheur **[!UICONTROL Écouter un événement]**. Utilisez plutôt un nœud **[!UICONTROL Attente]** minuté, suivi d’un nœud **[!UICONTROL Chemins partagés]** sur le statut du webinaire, comme illustré ci-dessous, plutôt que d’attendre le changement de statut lui-même.

## Personnaliser les e-mails

Les jetons de webinaire s’affichent dans le contenu de l’e-mail : objet, corps, pré-titre et expéditeur. Consultez [&#x200B; Jetons de webinaire &#x200B;](webinars-overview.md#webinar-tokens) pour en savoir plus.

>[!NOTE]
>
>Les jetons de webinaire ne sont actuellement pas disponibles sur la page de destination d’enregistrement ou dans les formulaires. Personnalisez-les à l’aide de jetons de programme standard et réservez une personnalisation spécifique au webinaire (comme l’URL de jonction et l’URL d’enregistrement) pour les e-mails.

>[!IMPORTANT]
>
>Le jeton **_URL de jonction_** n’est résolu que pour les personnes dont le statut du webinaire est _Enregistré_ ou ultérieur. Le jeton **_URL d’enregistrement_** n’est résolu qu’une fois l’enregistrement publié. Les deux sont résolus à l’avance sur une valeur vide plutôt que sur une erreur. Vérifiez donc que le rendu de vos e-mails est acceptable dans les deux cas avant de publier.

## Diffusion du webinaire {#deliver-webinar}

À l’heure prévue, le webinaire se déroulera en [!DNL Adobe Connect] :

* Les présentateurs et les co-animateurs rejoignent le webinaire par le biais de leur lien individuel dans la section **Équipe du webinaire**.
* Les participants rejoignent à l’aide de leur jeton personnel **URL de jointure**.
* [!DNL Adobe Connect] capture l’activité en session (questions, réponses aux sondages, clics sur les liens, téléchargements de ressources et levées de main) et la renvoie à [!DNL Marketo Optimizer] en tant qu’[activités de webinaire](webinars-overview.md#webinar-activities), disponible pour n’importe quel parcours d’écoute.

Si le webinaire est défini sur **Simulation en direct**, le contenu préenregistré est lu automatiquement à l’heure planifiée pendant que les présentateurs et présentatrices participent en direct par le biais d’un chat, de sondages et de questions/réponses.

## Création d’un parcours post-webinaire {#build-post-webinar-journey}

Une fois la session en direct terminée, [!DNL Adobe Connect] définit le statut du webinaire de chaque personne sur _Avec participation_ ou _Pas d’affichage_. Lorsque le nœud **[!UICONTROL Wait]** de parcours est libéré, la branche utilise ce statut avec un nœud **[!UICONTROL Split paths]**.

1. Ajoutez un nœud **[!UICONTROL Chemins d’accès partagés]** avec une condition sur le statut du webinaire, tel que _A assisté au webinaire_.

1. Sur le chemin _Terminé_, envoyez un e-mail de remerciement.

   Par exemple, envoyez une relecture et un suivi des ressources. Utilisez ensuite un nœud **[!UICONTROL Wait]** et un e-mail call-to-action de l’étape suivante.

1. Sur le chemin _Pas de vue_, envoyez un e-mail _nous vous avons manqué_.

   Dans le contenu de l’e-mail, invitez-les à regarder l’enregistrement. Utilisez ensuite un nœud **[!UICONTROL Attente]** et un e-mail de relance résumant les principaux points à retenir.

1. Personnalisez l’un des chemins à l’aide d’autres activités de webinaire.

   Par exemple, vous pouvez créer une branche ou effectuer une personnalisation en fonction de _Répond à un sondage_ avec une réponse spécifique.

1. Utilisez le jeton **_URL d’enregistrement_** dans l’un des chemins une fois qu’il est résolvable, afin que les gens puissent regarder à la demande.

   **_L’engagement à la demande_** (durée de visionnage, clics sur les liens de lecture et téléchargements) est intégré en tant que mêmes activités de webinaire, balisées avec un mode _À la demande_. Contrairement à ces activités, l’affichage à la demande déplace également une personne _qui n’apparaît pas_ vers le statut du webinaire _À la demande_. Par conséquent, une trajectoire de parcours _Pas d’affichage_ peut atteindre ultérieurement les personnes qui regardent l’enregistrement. Partagez-les davantage sur le statut du webinaire ou revérifiez-les après un certain délai, si vous souhaitez un traitement différent pour les personnes qui regardent à la demande.
