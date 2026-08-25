---
title: Optimisation de l’heure d’envoi des e-mails
description: Configurez l’optimisation de l’heure d’envoi dans les parcours de personne Marketo Optimizer. Définissez les fenêtres d’envoi, ajoutez des nœuds d’attente et affichez les rapports STO dans Coworker.
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Optimisation de l’heure d’envoi des e-mails

Utilisez la fonctionnalité d’optimisation de l’heure d’envoi (STO) pour personnaliser le délai de diffusion des e-mails pour les parcours de personne](./person-journeys.md) en prédisant le moment où chaque profil est le plus susceptible d’interagir. [Au lieu d’une heure d’envoi fixe, STO utilise des signaux d’engagement historiques des e-mails pour planifier la diffusion à l’heure optimale pour chaque destinataire, améliorant ainsi l’engagement global.

STO analyse l&#39;engagement historique de chaque profil à l&#39;aide d&#39;un grand modèle linguistique. Il prédit et classe les heures d’envoi potentielles, puis planifie la diffusion au moment le plus élevé de la fenêtre d’optimisation.

Les informations sur les performances, telles que l’utilisation, l’effet élévateur d’engagement et les comparaisons STO/non-STO, sont disponibles dans le langage naturel dans Coworker.

>[!BEGINSHADEBOX]

De nombreuses **_améliorations futures_** sont prévues pour la STO :

* Configuration globale de la STO dans la zone _[!UICONTROL Admin]_
* Activation de la STO de parcours niveau
* Partage de test/contrôle configurable

>[!ENDSHADEBOX]

## Configuration {#configuration}

Vous pouvez configurer l’optimisation de l’heure d’envoi lorsque vous [ajoutez un nœud _[!UICONTROL Prendre une action]_](./action-nodes.md) à un parcours de personne et choisissez l’action **[!UICONTROL Envoyer un e-mail]**.

1. Sélectionnez le nœud d’action de parcours _Envoyer un e-mail_.

1. Dans les propriétés de nœud sur la droite, activez l’option **[!UICONTROL Optimisation de l’heure d’envoi]**.

   ![Nœud de parcours Envoyer un e-mail - Options d’optimisation de l’heure d’envoi](./assets/email-node-send-time-optimization.png){width="450" zoomable="no"}

1. Pour spécifier la fenêtre et la distribution de test, définissez les options STO :

   * **[!UICONTROL Envoyer dans les prochains]** - Cette valeur détermine la fenêtre d’optimisation (en jours), qui correspond à la période pendant laquelle les e-mails peuvent être diffusés. Par exemple, pour un webinaire ayant lieu dans cinq jours, vous pouvez définir une fenêtre de quatre ou cinq jours. STO sélectionne l’heure d’envoi la mieux prévue pour chaque profil dans cette fenêtre.

   * **Distribution STO/Fixe** - La distribution STO crée automatiquement une _répartition de test et de contrôle_ pour diviser les profils éligibles entre les heures d&#39;envoi optimisées et fixes. La division permet une comparaison directe des performances. (De futures améliorations sont prévues pour autoriser les pourcentages de partage personnalisés.)

   >[!NOTE]
   >
   >Les profils ayant un historique d’engagement solide sont divisés de manière égale en groupes de contrôle et de test afin de mesurer l’impact de la STO. Afin de garantir des résultats statistiquement fiables, la répartition entre STO et non-STO est limitée entre 30 % et 70 %. Cela permet d’éviter que des cohortes plus petites biaisent les résultats et d’assurer des comparaisons significatives.

1. Directement après le nœud _[!UICONTROL Envoyer un e-mail]_, [ajoutez un nœud _Attente_](./wait-nodes.md).

   Un nœud d’attente doit immédiatement suivre une action e-mail compatible avec STO. L’ajout de ce nœud permet de s’assurer que les profils restent dans le parcours jusqu’à ce que la fenêtre d’optimisation complète soit effacée et que tous les envois STO soient terminés. Si vous omettez ce nœud, le système signale la configuration comme non valide.

1. Une fois le parcours de la personne terminé, passez à [publication](./person-journeys.md#publish).

## Rapports {#reporting}

Les données de performances STO sont disponibles via le [collègue](../agents/chat-interface.md) en utilisant la compétence `send-time-report`. Vous pouvez afficher un rapport au niveau du parcours qui résume tous les nœuds d’e-mail ou analyser en profondeur un rapport au niveau du nœud pour une action d’e-mail spécifique.

Le rapport affiche chaque nœud d’e-mail dans le parcours et indique si la fonction STO est activée pour celui-ci. Il présente également une comparaison tabulaire entre les e-mails avec et sans activation de la fonctionnalité STO afin que vous puissiez évaluer l’effet élévateur de l’engagement.

### Générer le rapport STO {#generate-sto-report}

Il existe trois manières de générer un rapport STO à l’aide du collègue :

**Utilisez la commande de barre oblique**

1. Dans le panneau Collègue, saisissez `/` pour afficher la liste des compétences disponibles.
1. Sélectionnez **[!UICONTROL send-time-report]** dans la liste, puis cliquez sur la flèche vers le haut pour envoyer la requête.

   ![Requête de compétence de rapport d’heure d’envoi du collègue](./assets/email-sto-reporting-coworker.png){width="700" zoomable="yes"}

   Si un parcours est ouvert dans l’éditeur, Coworker l’utilise automatiquement en tant que contexte. Sinon, Coworker vous invite à spécifier le parcours.

   Un collègue charge le rapport et affiche une carte récapitulative.

1. Cliquez sur **[!UICONTROL Ouvrir le rapport]** pour afficher le rapport complet avec les détails au niveau du nœud.

**Cliquez sur un nœud d’e-mail**

1. Dans la zone de travail de parcours, cliquez sur le nœud **[!UICONTROL Envoyer un e-mail]**.

1. Dans le panneau Collègue, demandez le rapport STO.

   Comme le nœud est sélectionné, Collègue l’utilise comme contexte et renvoie un rapport dont la portée est limitée uniquement à ce nœud.

   Il charge le rapport et affiche une carte de résumé.

1. Cliquez sur **[!UICONTROL Ouvrir le rapport]** pour afficher le rapport complet.

**Requête en langage naturel**

1. Dans le panneau Collègue, saisissez une requête telle que _Donnez-moi le rapport de l&#39;arrêt pour [nom du parcours]_.

   Un collègue interprète la demande, charge la compétence `send-time-report`, génère le rapport et affiche une carte récapitulative.

1. Cliquez sur **[!UICONTROL Ouvrir le rapport]** pour afficher le rapport complet.

### Afficher les données du rapport d’e-mail {#sto-report-data}

Vous pouvez réduire le panneau Collègue pour augmenter la taille du rapport affiché ou le faire défiler pour afficher toute la largeur.

![Rapport d’optimisation de l’heure d’envoi - Résumé des performances des emails](./assets/email-sto-reporting-summary-report.png){width="700" zoomable="yes"}

Dans la colonne _[!UICONTROL Détails]_, cliquez sur **[!UICONTROL Afficher les résultats de la STO]** pour ouvrir une fenêtre contextuelle. La fenêtre fournit des visualisations de données d’e-mail pour _Comparaison des performances_, _Distribution de l’heure d’envoi_ et _Intégrité des données_.

![Rapport d’optimisation de l’heure d’envoi - Données de performances des e-mails](./assets/email-sto-reporting-data.png){width="500" zoomable="yes"}
