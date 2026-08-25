---
title: Création et conception d’un webinaire
description: Ajoutez une ressource de webinaire à un programme, concevez-la dans [!DNL Adobe Connect] ajoutez des co-hôtes et des présentateurs, exécutez une session de test et modifiez un webinaire en direct dans [!DNL Marketo Optimizer].
keywords: null
role: User
feature: Channels
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---


# Création et conception d’un webinaire

Ajoutez un webinaire à un programme, concevez son enregistrement et l’expérience de sa salle, puis recrutez du personnel avec des co-animateurs et des présentateurs au sein de [!DNL Marketo Optimizer]. Avant de commencer, consultez la section [Présentation des webinaires interactifs](webinars-overview.md) pour connaître les concepts sous-jacents aux états, jetons et rôles des webinaires, et confirmez que vous disposez du rôle **Créer et gérer des webinaires**.

## Ajouter un webinaire à un programme

1. Recherchez le programme dans l’arborescence _[!UICONTROL Programmes]_ ou [créez un programme](./programs.md#create-program).

1. Cliquez sur l’icône _Plus de menu_ ( **...** ) en regard du nom du programme et sélectionnez **[!UICONTROL Créer un webinaire]**.

1. Dans la boîte de dialogue, saisissez les détails du webinaire de base :

   * **Titre** et **Description**.
   * **Planning** - Date et heure de début, fuseau horaire et durée.
   * **Audience maximale** - la capacité de licence du webinaire à utiliser pour cette session.

   ![Boîte de dialogue Planifier le webinaire avec les champs du programme parent, le nom, la durée, le fuseau horaire, l’heure de début et l’audience maximale, ainsi que les boutons Annuler et Créer](assets/webinar-create-schedule-dialog.png){width="500" zoomable="yes"}.

   >[!NOTE]
   >
   >Les options de diffusion unique ou récurrente, et audio/vidéo, ne sont actuellement pas configurables. Chaque webinaire est une seule session vidéo.

1. Ajoutez **Co-hôtes** et **Présentateurs**.

   >[!NOTE]
   >
   >Dans la version actuelle, vous ajoutez tout le monde en tant que contact externe par nom et adresse e-mail, qu’il dispose ou non d’un compte d’authentification unique Adobe éligible au rôle.<!-- See [Permissions](./webinars-overview.md#permissions) for what each role governs. --> Pour les étapes complètes, voir [_Ajouter des co-hôtes et des présentateurs_](#add-co-hosts-and-presenters).

1. (Facultatif) Personnalisez le modèle, l’image de marque et la mise en page de l’espace.

   Ces options sont gérées dans [!DNL Adobe Connect] et peuvent également être affinées ultérieurement à partir de l’aire de conception. Voir [Conception du webinaire](#design-the-webinar).

1. Cliquez sur **[!UICONTROL Enregistrer]**

   L’enregistrement enregistre le webinaire dans le programme et met ses jetons, attributs et activités à la disposition de chaque parcours et ressource de ce programme.

>[!NOTE]
>
>La création de webinaires est équivalente aux _webinaires interactifs_ dans [!DNL Marketo Engage]. Par conséquent, les champs sont familiers si vous avez réalisé cette opération via cette application.

## Concevoir le webinaire {#design-the-webinar}

Pour ouvrir la surface de conception [!DNL Adobe Connect], directement intégrée à [!DNL Marketo Optimizer], où vous configurez la salle, la page d’enregistrement et les mises en page, utilisez _[!UICONTROL Concevoir votre webinaire]_.

1. Sur la page du webinaire, cliquez sur **Concevoir votre webinaire**.

1. Choisissez un **mode de diffusion** :

   &#x200B;- **En direct** - Les présentateurs et présentatrices animent la session en temps réel.
   &#x200B;- **Simulation en direct** - Le contenu préenregistré est lu à l’heure planifiée, avec le chat en direct, les sondages et les questions/réponses.

1. Choisissez une **salle de webinaire**.

   Créez une nouvelle salle ou réutilisez une salle existante.

1. Sélectionnez un **Modèle**, **Langue** et **Thème**, puis prévisualisez la mise en page.

1. Ajoutez et disposez les capsules selon vos besoins.

   Les pods disponibles comprennent les éléments suivants : partage, notes, vidéo, conversation, liste des participants, fichiers, liens web, sondages, questions/réponses et questionnaire.

1. Entrez dans la salle pour examiner l’expérience, puis quittez une fois l’opération terminée.

1. Enregistrez vos modifications.

   Un message de confirmation s’affiche pour indiquer que le webinaire a bien été conçu.

>[!TIP]
>
>Concevez le webinaire avant d’ajouter des co-animateurs et des présentateurs, de sorte que leur accès et leurs contrôles s’appliquent à la salle terminée.

La personnalisation de la chambre, telle que le logo, les couleurs et les arrière-plans virtuels, est gérée directement dans [!DNL Adobe Connect].

## Ajouter des co-hôtes et des présentateurs {#add-co-hosts-and-presenters}

1. Sur la page du webinaire, accédez à la section **Équipe du webinaire**.

1. Cliquez sur **Ajouter un co-hôte** ou **Ajouter un présentateur**.

1. Dans la boîte de dialogue, saisissez le **[!UICONTROL Prénom]**, **[!UICONTROL Nom]** et **[!UICONTROL Adresse e-mail]** de la personne, puis cliquez sur **[!UICONTROL Ajouter]**.

   >[!NOTE]
   >
   >Dans la version actuelle, tout le monde est ajouté de la même manière, par nom et adresse e-mail, qu’il dispose ou non d’un compte SSO Adobe. Voir [Autorisations](webinars-overview.md#permissions) pour savoir ce que les rôles **co-hôte du webinaire** et **présentateur du webinaire** gouvernent une fois qu’une personne est ajoutée.

   Une confirmation s’affiche une fois la personne ajoutée et elle est répertoriée sous **Co-hôtes** ou **Présentateurs** dans la section Équipe de webinaires.

## Tester le webinaire {#test-the-webinar}

Avant de promouvoir le webinaire, exécutez une session de test pour confirmer que la salle, les capsules et l’accès du présentateur à toutes les fonctions sont corrects.

>[!NOTE]
>
>Le mode test n’affecte pas le statut de membre d’un webinaire d’une personne. Vous pouvez exécuter un test autant de fois que nécessaire sans enregistrer ni inviter personne.

## Modification d’un webinaire en direct {#edit-a-live-webinar}

Vous pouvez modifier un webinaire une fois les enregistrements commencés, mais avec précaution :

&#x200B;- La modification du planning peut déclencher des notifications de mise à jour pour les personnes déjà enregistrées. La possibilité de modifier les webinaires planifiés est configurable.
&#x200B;- Les champs référencés par des jetons dans les e-mails en direct nécessitent une confirmation explicite pour la suppression, car cela interrompt le contenu déjà planifié pour l’envoi.
