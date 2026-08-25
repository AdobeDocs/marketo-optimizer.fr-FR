---
title: Écoute d’un nœud d’événement
description: Configurez Écouter pour un nœud d’événement dans Marketo Optimizer. Définissez des déclencheurs d’événement, appliquez des filtres facultatifs et faites avancer les personnes lorsque des activités ou des modifications de données se produisent.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 5%

---

# Écoute d’un nœud d’événement

Ajoutez le nœud _Écouter un événement_ pour faire passer votre audience à l’étape suivante du parcours lorsqu’un événement se produit.

## Déclencheurs d’événement {#event-triggers}

Vous pouvez créer des déclencheurs autour des activités [!DNL Marketo Engage], par exemple :

* Remplit le formulaire : se déclenche lorsqu’une personne envoie un formulaire [!DNL Marketo Engage] sur votre page de destination.
* Page web des visites - Se déclenche lorsqu’un prospect consulte une page web suivie (vous pouvez spécifier des URL exactes ou utiliser des caractères génériques).
* Clics sur le lien : se déclenche lorsqu’un utilisateur clique sur un lien suivi dans un e-mail marketing.
* Modifications de la valeur des données - Se déclenche lorsqu’un champ spécifique (comme le statut, la note ou le secteur du lead) est mis à jour dans l’enregistrement d’une personne.
* Campagne demandée : souvent utilisé pour les intégrations d’API ou de webhook, ce déclencheur lance une campagne lorsqu’un autre programme ou service web l’appelle.
* La note est modifiée - Se déclenche lorsque la note d’un prospect augmente ou diminue au-delà d’un certain seuil.
* Mobile push activé : se déclenche dans les campagnes intelligentes de marketing mobile lorsqu’une notification push fait l’objet d’une interaction sur un appareil.

## Filtres d’événement {#event-filters}

| Filtres | Description |
| ------- | ----------- |
| Historique des activités > E-mail | Activités d&#39;email basées sur des conditions évaluées à l&#39;aide d&#39;un ou plusieurs emails sélectionnés : <li>Lien ayant fait l’objet d’un clic dans l’e-mail <li>E-mail ouvert |
| Historique des activités > Valeur des données modifiée | Pour un attribut de personne sélectionné, une modification de valeur s’est produite. Ces types de modifications sont les suivants : <li>Nouvelle valeur <li>Valeur précédente <li>Motif <li>Source <li>Date d’activité <li> Min. nombre de fois |

## Ajouter un nœud d’événement {#add-event-node}

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours ](./assets/person-journey-canvas-add-node.png){width="200"}

1. Dans les propriétés de nœud sur la droite, cliquez sur **[!UICONTROL Ajouter des critères d’événement]**.

1. Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, ajoutez les événements à déclencher.

   ![Modifier l’événement - Déclencheurs d’événement](./assets/edit-event-triggers.png){width="600" zoomable="yes"}

1. (Facultatif) Sélectionnez l’onglet **[!UICONTROL Filtres]** dans la boîte de dialogue et ajoutez des critères de filtrage pour les déclencheurs.

1. Cliquez sur **[!UICONTROL Modifier l’événement]** et définissez les détails de l’événement.

   ![Modifier l&#39;événement - Filtrage des événements](./assets/edit-event-filters.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

<!--
1. If needed, set the **[!UICONTROL Timeout]** option to limit the time period to listen for the event.

   >[!NOTE]
   >
   >The journey ends after a timeout unless you define a timeout path, where you can add other nodes.

   Enable the **[!UICONTROL Timeout]** option and select the duration for which the journey waits for an event to occur before it times out.

   You can choose to end the path here or take a different course of action by setting another path. To create a new path in the journey where you can add actions and events applicable to accounts when the event does not occur, select the **[!UICONTROL Set timeout path]** check box.

   ![Journey event node - set timeout path](assets/node-event-timeout-set-path.png){width="700" zoomable="yes"}
-->

>[!NOTE]
>
>La fonctionnalité de temporisation d’Écouter pour un nœud d’événement ne fonctionne pas actuellement. Il est prévu de le publier ultérieurement.

