---
title: Audiences basées sur un événement
description: Utilisez des audiences basées sur un événement dans Marketo Optimizer pour déclencher une entrée de parcours de personne en temps quasi réel en fonction des activités Marketo Engage.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Audiences basées sur un événement

Dans [!DNL Adobe Marketo Optimizer], les _audiences basées sur un événement_ vous permettent d’ajouter des membres de l’audience à un parcours [personne](../marketing/person-journeys.md) en direct en temps quasi réel lorsqu’une activité de [!DNL Marketo Engage] se produit. Vous configurez les audiences basées sur un événement sur le nœud Audience de la zone de travail de parcours :

* Sélectionnez une ou plusieurs activités [!DNL Marketo Engage] (standard ou personnalisées) comme événements de qualification.
* Vous pouvez éventuellement ajouter des filtres de profil de personne (par exemple, secteur, région ou étape du cycle de vie) pour limiter les personnes pouvant entrer.
* Vous pouvez éventuellement définir des contraintes d’attribut d’activité (comme un formulaire, une URL ou un programme spécifique) pour limiter les occurrences de chaque activité à qualifier.

Lorsqu’une activité de qualification est connectée [!DNL Marketo Engage] pour un prospect et répliquée dans [!DNL Adobe Marketo Optimizer], le système évalue l’enregistrement de personne correspondant par rapport à vos filtres et contraintes configurés. Si les conditions sont remplies, la personne accède immédiatement au parcours par le biais du nœud Audience .

_Pour définir une audience basée sur un événement pour un parcours de personne :_

1. Sélectionnez le nœud [_Audience de la personne_](../marketing/person-audience-node.md).

1. Dans les propriétés de nœud sur la droite, choisissez **[!UICONTROL Audience de l’événement]** comme type d’entrée.

   ![Nœud de parcours d’audience de personne défini sur une audience basée sur un événement](./assets/event-based-audience-node.png){width="400"}

1. Cliquez sur **[!UICONTROL Ajouter des critères d’événement]**.

1. Dans la boîte de dialogue _[!UICONTROL Modifier les critères d’événement]_, ajoutez une ou plusieurs activités [!DNL Marketo Engage] comme événements admissibles, par exemple :

   * _Assiste au webinaire_
   * _L’e-mail est diffusé_
   * _Clics dans l’e-mail_

   >[!NOTE]
   >
   >Vous pouvez également sélectionner des activités personnalisées définies dans l’instance de [!DNL Marketo Engage] associée.

   Définissez l’opérateur et les valeurs correspondants pour chaque activité.

   ![Déclencheurs d’activité pour une audience basée sur un événement](./assets/event-based-audience-triggers.png){width="700" zoomable="yes"}

   Une personne est éligible au parcours lorsque l’une de ces activités configurées est consignée pour ce prospect.

1. (Facultatif) Pour utiliser une combinaison d’événement et de filtre pour la qualification de l’audience, ajoutez des filtres au niveau de la personne.

   * Sélectionnez l’onglet **[!UICONTROL Filtres]**.
   * Faites glisser chaque filtre et définissez les critères correspondants.

   ![Filtres de personne pour une audience basée sur un événement](./assets/event-based-audience-filters.png){width="700" zoomable="yes"}

   Si vous ajoutez des filtres, la personne doit satisfaire au moins une condition d’activité configurée et les filtres configurés.

1. Cliquez sur **[!UICONTROL Enregistrer]**