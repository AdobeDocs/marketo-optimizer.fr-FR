---
title: Écoute d’un nœud d’événement
description: Configurez Écouter pour un nœud d’événement dans Marketo Optimizer. Définissez des déclencheurs d’événement, appliquez des filtres facultatifs et faites avancer les personnes lorsque des activités ou des modifications de données se produisent.
TQID: 'https://experienceleague.adobe.com/6v3i6M-Hhr2RAWrS68WaEVb8VJEzJZbD7vXOJOsjgc8'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
source-git-commit: bc370a501d3f8ff80ad846576b62504aca77f530
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 2%
---
# Écoute d’un nœud d’événement

Pour passer à l’étape suivante du parcours lorsqu’un événement se produit, ajoutez le nœud _Écouter un événement_.

## Déclencheurs d’événement {#event-triggers}

Définissez les critères d’événement qui déclenchent le nœud de parcours et déplacez le membre de l’audience vers l’avant.

| Déclencheurs | Description |
| -------- | ----------- |
| Brand Concierge | Activités pour les prospects qui interagissent avec [!DNL Brand Concierge]. |
| E-mail | Activités d’e-mail pour les prospects, y compris les envois, la diffusion et l’engagement. |
| Événement | Activités de webinaire interactives pour les prospects, y compris l’enregistrement, la participation et les interactions. |
| Opportunités | Activités liées aux enregistrements d’opportunité associés aux prospects ou aux comptes. |
| Applications de vente | Activités de lead liées aux [!DNL Sales Qualifier] ou aux [!DNL Marketo Sales Insights]. |
| Autres | Les activités qui ne relèvent pas des catégories prédéfinies, ce qui offre une certaine flexibilité pour les déclencheurs d’événements personnalisés ou divers. |

>[!BEGINSHADEBOX]

**Activités Marketo Engage prises en charge pour les déclencheurs**

Lors du déclenchement d’événements, [!DNL Marketo Optimizer] prend en charge les activités de l’instance [!DNL Marketo Engage] connectée en tant que source de données.

>[!NOTE]
>
>Il ne peut y avoir qu’une seule instance [!DNL Marketo Engage] comme source de données et elle est préconfigurée au moment de la mise en service de votre instance [!DNL Marketo Optimizer].

Vous pouvez créer des déclencheurs d’événement autour des activités [!DNL Marketo Engage] suivantes :

* **[!UICONTROL Remplit un formulaire Marketo Engage]** - Se déclenche lorsqu’un prospect envoie un formulaire [!DNL Marketo Engage] spécifié.
* **[!UICONTROL Page web Marketo Engage des visites]** - Se déclenche lorsqu’un prospect avec un cookie de suivi Munchkin visite une page web spécifiée.
* **[!UICONTROL Lien des clics sur la page web Marketo Engage]** - Se déclenche lorsqu’un prospect clique sur un lien hypertexte suivi sur une page web sur laquelle est installé le code de suivi Munchkin [!DNL Marketo Engage].
* **[!UICONTROL L’e-mail Marketo Engage est diffusé]** - Se déclenche lorsque le serveur de messagerie (MX) d’un prospect renvoie une réponse de succès (un message 250 OK) au serveur d’envoi [!DNL Marketo Engage].
* **[!UICONTROL Bounces d&#39;e-mails Marketo Engage]** - Se déclenche lorsqu&#39;un serveur de messagerie cible rejette un e-mail [!DNL Marketo Engage] envoyé en tant qu&#39;erreur permanente, comme un utilisateur non valide ou un domaine inconnu.
* **[!UICONTROL Rebonds d&#39;email Marketo Engage soft]** - Se déclenche lorsqu&#39;un serveur de messagerie cible rejette un email [!DNL Marketo Engage] envoyé comme problème temporaire (par exemple serveur occupé ou boîte pleine). [!DNL Marketo Engage] tente automatiquement de relancer les soft bounces jusqu’à trois fois via les serveurs MX avant de signaler les problèmes.
* **[!UICONTROL Désabonnements des e-mails Marketo Engage]** - Se déclenche lorsqu’un prospect se désinscrit des e-mails marketing non opérationnels. Lorsqu’il est déclenché, [!DNL Marketo Engage] met automatiquement à jour la valeur du champ de `Unsubscribed` du prospect vers `true`, en les supprimant des futurs envois d’e-mail standard.
* **[!UICONTROL Ouvre l’e-mail Marketo Engage]** - Se déclenche lorsqu’un prospect ouvre un e-mail [!DNL Marketo Engage] suivi.
* **[!UICONTROL Clics sur le lien dans l’e-mail Marketo Engage]** - Se déclenche lorsqu’un prospect clique sur un lien (ou un lien limité spécifique) contenu dans un e-mail [!DNL Marketo Engage].

>[!ENDSHADEBOX]

## Filtres d’événement {#event-filters}

Vous pouvez inclure un filtrage pour limiter les déclencheurs d’événement correspondants en fonction de divers critères :

| Filtres | Description |
| ------- | ----------- |
| Historique des activités | Activités basées sur des conditions évaluées à l’aide d’un ou de plusieurs éléments sélectionnés |
| Brand Concierge | Activités pour les prospects qui interagissent avec [!DNL Brand Concierge]. |
| Attributs de la société | Attributs du profil de la société/du compte, notamment : <li>[!UICONTROL Chiffre d’affaires annuel] <li>[!UICONTROL Nom de la société] <li>[!UICONTROL Pays de facturation] <li>[!UICONTROL Industrie] <li>[!UICONTROL Nombre d’employés] <li>[!UICONTROL Code SIC] <li>[!UICONTROL État] |
| Données d’intention | Attributs basés sur les données d’intention associées au profil de personne. |
| Opportunités | Statut et attributs basés sur les opportunités associées au profil de personne, notamment : <li>[!UICONTROL A une opportunité] <li>[!UICONTROL Nombre d’opportunités] <li>[!UICONTROL Montant total de l’opportunité] <li>[!UICONTROL A été ajouté à l’opportunité] <li>[!UICONTROL A été supprimé de l’opportunité] |
| Attributs de la personne | Attributs du profil de personne B2B, notamment : <li>[!UICONTROL Ville] <li>[!UICONTROL Pays] <li>[!UICONTROL Date de naissance] <li>[!UICONTROL Adresse électronique] <li>[!UICONTROL E-mail non valide] <li>[!UICONTROL Email suspendu] <li>[!UICONTROL Prénom ] <li>[!UICONTROL Région d’État déduite] <li>[!UICONTROL Fonction] <li>[!UICONTROL Nom] <li>[!UICONTROL Numéro de téléphone mobile] <li>[!UICONTROL Score d’engagement de personne] <li>[!UICONTROL Numéro de téléphone] <li>[!UICONTROL Code postal ] <li>[!UICONTROL État] <li>[!UICONTROL Désabonné] <li>[!UICONTROL Motif de désabonnement] |
| Applications de vente | Activités de lead liées aux [!DNL Sales Qualifier] ou aux [!DNL Marketo Sales Insights]. |
| Filtres spéciaux | Attributs de filtrage qui ne relèvent pas des catégories prédéfinies, offrant ainsi une flexibilité pour les critères de filtre personnalisés ou divers. |

>[!BEGINSHADEBOX]

**Activités Marketo Engage prises en charge pour les filtres**

Lors du filtrage des événements déclenchés, [!DNL Marketo Optimizer] prend en charge les activités de l’instance [!DNL Marketo Engage] connectée en tant que source de données.

>[!NOTE]
>
>Il ne peut y avoir qu’une seule instance [!DNL Marketo Engage] comme source de données et elle est préconfigurée au moment de la mise en service de votre instance [!DNL Marketo Optimizer].

Vous pouvez créer des filtres d’événement autour des activités [!DNL Marketo Engage] suivantes :

* **[!UICONTROL Formulaire Marketo Engage rempli]** - Correspond aux prospects qui ont rempli un formulaire [!DNL Marketo Engage] spécifique à tout moment dans leur journal d’activité non obsolète.
* **[!UICONTROL Page web Marketo Engage visitée]** - Correspond aux prospects qui ont consulté une URL spécifique sur votre site web ou [!DNL Marketo Engage] pages de destination. Il repose directement sur le code de suivi Munchkin installé sur votre site.
* **[!UICONTROL Lien ayant cliqué sur une page web Marketo Engage]** - Correspond aux prospects qui ont cliqué sur un lien ou une ressource spécifique sur une page suivie.
* **[!UICONTROL E-mail Marketo Engage envoyé]** - Correspond aux prospects auxquels [!DNL Marketo Engage] avez tenté d’envoyer un e-mail spécifique, en tenant compte des actions de déploiement avant les hard bounces ou les acceptations de serveur.
* **[!UICONTROL E-mail Marketo Engage diffusé]** - Correspond aux prospects dont le serveur de messagerie (MX) a renvoyé une réponse de succès (message 250 OK) au serveur d’envoi [!DNL Marketo Engage].
* **[!UICONTROL E-mail Marketo Engage non envoyé]** - Correspond aux leads qui ont subi un hard bounce (échec de diffusion permanent) lors d’un envoi d’e-mail spécifique ou au cours d’une période donnée.
* **[!UICONTROL Marketo Engage email bounce soft]** - Correspond aux leads dont les e-mails ont subi un échec de diffusion temporaire (comme une boîte de réception pleine ou un serveur hors ligne) plutôt qu&#39;un hard bounce permanent.
* **[!UICONTROL Désabonnement des e-mails Marketo Engage]** - Correspond aux prospects qui se sont désabonnés des e-mails marketing non opérationnels. Dans ce cas, [!DNL Marketo Engage] met automatiquement à jour la valeur du champ `Unsubscribed` du prospect sur `true`, en les supprimant des futurs envois d’e-mail standard.
* **[!UICONTROL E-mail Marketo Engage ouvert]** - Correspond aux prospects qui ont ouvert un e-mail [!DNL Marketo Engage] suivi.
* **[!UICONTROL Lien cliqué dans l’e-mail Marketo Engage]** - Correspond aux prospects qui ont cliqué sur un lien (ou un lien spécifique) dans un e-mail [!DNL Marketo Engage].

>[!ENDSHADEBOX]

## Ajouter un nœud d’événement {#add-event-node}

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin et choisissez **[!UICONTROL Écouter un événement]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours ](./assets/person-journey-canvas-add-node.png){width="200"}

1. Dans les propriétés de nœud sur la droite, cliquez sur **[!UICONTROL Ajouter des critères d’événement]**.

1. Dans la boîte de dialogue _[!UICONTROL Modifier l’événement]_, ajoutez un événement et définissez les contraintes que vous souhaitez faire correspondre au déclencheur.

   Faites glisser et déposez le déclencheur d’événement dans l’espace du créateur et définissez la définition. Cliquez sur **[!UICONTROL Ajouter une contrainte]** pour chaque contrainte que vous souhaitez utiliser pour affiner la correspondance d’événement.

   ![Modifier l’événement - Déclencheurs d’événement](./assets/edit-event-triggers.png){width="700" zoomable="yes"}

   Vous pouvez ajouter plusieurs événements à faire correspondre. Le premier événement éligible avance le profil de la personne vers l’avant dans le parcours.

1. (Facultatif) Sélectionnez l’onglet **[!UICONTROL Filtres]** et ajoutez des critères de filtrage pour les déclencheurs.

   Faites glisser et déposez le filtre dans l’espace du créateur et définissez la définition. Cliquez sur **[!UICONTROL Ajouter une contrainte]** pour chaque contrainte que vous souhaitez utiliser pour affiner la correspondance du filtre.

   ![Modifier l&#39;événement - Filtrage des événements](./assets/edit-event-filters.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

   À tout moment, vous pouvez cliquer sur **[!UICONTROL Modifier l’événement]** pour modifier les critères d’événement du nœud.

1. Si nécessaire, définissez l’option **[!UICONTROL Temporisation]** pour limiter la période d’écoute de l’événement.

   >[!NOTE]
   >
   >Le parcours se termine après une temporisation, sauf si vous définissez un chemin de temporisation dans lequel vous pouvez ajouter d’autres nœuds.

   Activez l’option **[!UICONTROL Temporisation]** et sélectionnez la durée pendant laquelle le parcours attend qu’un événement se produise avant d’expirer.

   ![Options de délai d’expiration activées pour le nœud Écouter le parcours d’événement ](./assets/person-journey-event-node-timeout.png){width="550" zoomable="yes"}

   Vous pouvez choisir de terminer le chemin ici ou d’effectuer une autre action en définissant un autre chemin. Pour créer un nouveau chemin dans le parcours où vous pouvez ajouter des actions et des événements applicables aux profils lorsque l’événement ne se produit pas, cochez la case **[!UICONTROL Définir le chemin de temporisation]**.
