---
title: Créer et promouvoir des webinaires
description: Utilisez l’interface de chat de Marketo Optimizer pour planifier un webinaire, ajouter des co-hôtes et des présentateurs, créer des parcours de promotion et de soutien, et vérifier les rapports, le tout en langage naturel.
keywords: null
role: User
source-git-commit: bc9b09fe125aad1909864db4fa7fc7605bf86597
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---


# Créer et promouvoir des webinaires

L’interface [chat](./chat-interface.md) permet de créer un webinaire en passant par la promotion, la diffusion, la culture post-webinaire et le compte rendu des performances, et ce entièrement via le volet de conversation. Tout ce que l’interface de chat crée utilise la même ressource, les mêmes parcours et les mêmes jetons de webinaire que ceux décrits dans la section [ Présentation des webinaires interactifs ](../marketing/webinars-overview.md), afin que vous puissiez passer du chat à la conception de l’interface à tout moment.

## Points d’entrée

Dans le message d’accueil « Bienvenue dans la gestion marketing », sélectionnez la puce de catégorie **[!UICONTROL Webinaire]** pour afficher les invites suggérées, notamment :

* *« Planifier et diffuser un webinaire »*
* *« Montrez-moi tous mes webinaires à venir »*
* *« Donnez les détails du webinaire [nom du webinaire]«*

![Lancez le workflow de création du webinaire via l’interface de conversation](./assets/webinar-create-start.png){width="700" zoomable="yes"}

Lorsque vous ouvrez le volet de conversation depuis un programme, il étend automatiquement la portée des invites à ce programme.

## Ajouter un webinaire planifié {#add-webinar}

Décrivez le webinaire que vous souhaitez inclure dans un seul message, par exemple :

*« Créez un webinaire interactif intitulé « Cybersécurité 101 : protéger vos données contre les menaces modernes » le 12 octobre 2026 à 16 h 00 Amérique/Los_Angeles pour [programme]. »*

1. Le volet de conversation affiche une liste de contrôle **Plan de tâches** et y travaille : résolvez le programme, définissez le nom, l’heure de début, l’heure de fin, le fuseau horaire et la capacité, puis confirmez.

   ![Spécifiez le nom, la date et l’heure du webinaire dans l’interface de conversation](./assets/webinar-create-name-time.png){width="500" zoomable="yes"}

1. Le volet de conversation répertorie les webinaires **licences** disponibles (par exemple, un module complémentaire de grande capacité avec sa valeur de capacité) et vous demande lequel utiliser. Répondez avec la capacité souhaitée, par exemple *« Utilisez la capacité du webinaire à 1 000*. »

   ![Définissez la licence du webinaire en fonction de la capacité](./assets/webinar-create-license-capacity.png){width="500" zoomable="yes"}

1. Le volet de conversation renvoie le programme, le nom, l’heure de début, le fuseau horaire, la durée et la capacité, et vous demande de **confirmer** avant de créer le webinaire.

1. Après avoir créé le webinaire, l’interface de conversation affiche une **carte du webinaire** avec l’heure de début et de fin, la durée, l’hôte, la capacité, le fournisseur (Adobe Connect), une URL de configuration, une URL de lancement, un lien vers le tableau de bord de l’engagement et des métadonnées de création.

1. L’interface de chat propose ensuite les **meilleures actions suivantes** : _Concevoir votre webinaire_, _Ajouter un co-hôte_, _Ajouter un présentateur_, _Configurer des parcours promotionnels_ et _Configurer un parcours de formation post-webinaire_.

   ![L’interface de chat affiche les meilleures étapes suivantes pour la création du webinaire](./assets/webinar-create-next-steps.png){width="500" zoomable="yes"}

### Ajouter des co-hôtes et des présentateurs {#co-hosts-presenters}

Sélectionnez **[!UICONTROL Ajouter un co-hôte]** ou **[!UICONTROL Ajouter un présentateur]** parmi les meilleures actions suivantes, ou demandez directement, par exemple *« Ajouter un co-hôte [prénom] [nom] [e-mail].«* L’interface de conversation ouvre la même boîte de dialogue d’ajout que celle utilisée dans le concepteur : saisissez un nom et un e-mail, car tout le monde est actuellement ajouté de la même manière plutôt que sélectionné à partir d’un sélecteur de liste. Une confirmation s’affiche une fois la personne ajoutée.

![Ajoutez un co-hôte de webinaire dans l’interface de chat](./assets/webinar-create-add-co-host.png){width="500" zoomable="yes"}

### Concevoir le webinaire

Sélectionnez **[!UICONTROL Concevoir votre webinaire]** pour ouvrir la page de configuration du webinaire, où vous configurez le contenu, la disposition et les paramètres d’enregistrement dans l’aire de conception de [!DNL Adobe Connect] intégrée. Effectuez toutes les modifications de conception dans cette interface ; l&#39;interface de chat vous y connecte plutôt que de concevoir la salle dans le chat. Voir [Conception du webinaire](../marketing/create-webinar.md#create-and-design-a-webinar).

![Ouvrez la conception du webinaire Adobe Connect dans l’interface de conversation](./assets/webinar-create-open-design.png){width="500" zoomable="yes"}

## Création d’un parcours de promotion

1. Demandez à l&#39;interface de chat de configurer un parcours promotionnel.

   Il vous demande de choisir un modèle et de nommer le parcours, par exemple *« parcours d’invitation/d’enregistrement*.

1. L’interface de conversation crée le parcours et lie les e-mails à ses nœuds, créant un flux d’invitations et de rappels avec les mises à jour du statut des membres du webinaire.

1. L’interface de conversation répertorie ce qui reste à configurer dans la zone de travail du parcours.

1. Cliquez sur **[!UICONTROL Modifier les nœuds de parcours]** et répondez aux demandes de renseignements sur ce dont vous avez besoin pour terminer le parcours.

   Vous pouvez charger un document de campagne pour fournir des détails, ou continuer la conversation pour identifier ce qui est nécessaire.

   Vous pouvez également travailler directement dans la zone de travail du parcours pour traiter chaque nœud :

   * Sélectionnez le premier nœud de parcours et définissez l’audience du parcours. [En savoir plus](../marketing/person-audience-node.md)
   * Sélectionnez le nœud invitation _Envoyer un e-mail_ et cliquez sur **[!UICONTROL Modifier l’e-mail]**. [En savoir plus](../marketing/email-channel.md)
   * Sélectionnez le nœud Écouter pour un événement et cliquez sur **[!UICONTROL Modifier l’événement]**. Définissez le filtre d’événement pour le formulaire d’enregistrement sur l’événement _Remplit le formulaire_. [En savoir plus](../marketing/listen-for-event-nodes.md#event-filters)
   * Vérifiez les champs **[!UICONTROL Modifier le statut du membre du webinaire]** sur chaque nœud de changement de statut. [En savoir plus](../marketing/action-nodes.md#actions-and-constraints)

1. Terminez la configuration des autres nœuds et adresse

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Publier maintenant]** pour activer le parcours et commencer la promotion.

## Création d’un parcours post-webinaire

1. Demandez un parcours post-webinaire à l’interface de chat.

   Il vous invite à saisir un modèle et un nom.

1. L’interface de conversation crée un nœud **Chemin de partage** avec les chemins et actions définis :

   * Une branche **_Terminé_** (par exemple, un nœud de réponse et de ressources _Envoyer un e-mail_)
   * Une branche **_no-show_** (par exemple, une branche « a manqué ? regardez à nouveau » _nœud Envoyer un e-mail_)

   Et chacune est suivie d’un nœud _Attente_ et d’un nœud _Envoyer un e-mail_ de relance.

   La condition de division est définie pour identifier l’état du webinaire à l’aide de _A assisté au webinaire_.

1. Cliquez sur **[!UICONTROL Modifier les nœuds de parcours]** et répondez aux demandes de renseignements sur ce dont vous avez besoin pour terminer le parcours.

   Vous pouvez charger un document de campagne pour fournir des détails, ou continuer la conversation pour identifier ce qui est nécessaire.

   Vous pouvez également travailler directement dans la zone de travail du parcours pour traiter chaque nœud.

1. Terminez la configuration des autres nœuds et adresse

1. Une fois l’opération terminée, cliquez sur **[!UICONTROL Publier maintenant]** pour activer le parcours et commencer le suivi.

## Vérifier les rapports

Dans l’interface de chat, vous pouvez poser des questions de création de rapports telles que *« Afficher tous mes webinaires à venir »* ou *« Donner les détails du webinaire [nom] »*. Il fait apparaître le lien du tableau de bord de l’engagement avec les meilleures actions suivantes, telles que **Conception**, **Ajouter un co-hôte** ou **Publier à la date du webinaire**.

Pour des analyses plus approfondies (assiduité, performances d’enquête et de sondage, données par membre), l’interface de chat renvoie vers les onglets **Analytics** et **Membres** du webinaire, ainsi que vers le cumul entre programmes dans **gestion du webinaire**. <!-- See [Webinar reporting](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/prime/marketing-management/webinars/webinar-reporting). -->
