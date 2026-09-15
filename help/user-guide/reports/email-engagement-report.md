---
title: Rapport sur l’engagement des e-mails
description: Découvrez le rapport sur l’engagement des e-mails dans Adobe Marketo Optimizer, qui affiche la délivrabilité des e-mails et les mesures d’engagement par e-mail et par parcours.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 8c47a9c69c32ba0a37ba2efadb6ad4c1b796c21d
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%
---

# Rapport Engagement des e-mails

<!-- SPHR-39569: content drafted, but hide: true and hide-from-toc stay until eng confirms this shipped to production. Filter by Program, Filter by Audience, and the program data point from SPHR-32511 are not documented here pending delivery-state confirmation. -->

Utilisez le rapport [!UICONTROL Engagement des e-mails] pour examiner la délivrabilité des e-mails et les performances de l’engagement sur l’ensemble de votre instance, ventilées par e-mail et par parcours.

_Pour afficher le rapport :_

1. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Rapports]**.
1. Cliquez sur l’icône _Liste_ ( ![Icône Liste](../assets/do-not-localize/icon-table-of-contents.svg) ) et sélectionnez **[!UICONTROL Engagement des e-mails]** dans le panneau _[!UICONTROL Table des matières]_.

![Rapport sur l’engagement des e-mails avec les filtres Nom du Parcours et Persona, une période des 30 derniers jours et un tableau des mesures d’activité des e-mails.](./assets/reports-email-engagement.png){width="700" zoomable="yes"}

Vous pouvez [modifier la période](./reports-overview.md#change-the-date-range) à l’aide du même sélecteur de période disponible dans d’autres sections du rapport.

Sélectionnez **[!UICONTROL Partager]** en haut du rapport pour télécharger ou planifier l’exportation de toutes les données du rapport. Voir [_Exporter un rapport_](./reports-overview.md#export-a-report) dans la présentation des rapports.

## Tableau des rapports {#report-table}

Le rapport [!UICONTROL Engagement des e-mails] affiche une ligne pour chaque e-mail, avec les dimensions de ligne suivantes.

* **[!UICONTROL Nom de l’e-mail]** - Nom de l’e-mail.
* **[!UICONTROL Nom du Parcours]** - Nom du parcours qui a envoyé l’e-mail.

Les colonnes Mesures sont regroupées sous **[!UICONTROL Activités de messagerie]**.

| Colonne | Description |
| --- | --- |
| [!UICONTROL Envoyé] | Nombre d&#39;emails envoyés. |
| [!UICONTROL Délivrés] | Nombre d’e-mails diffusés. |
| [!UICONTROL &#x200B; % diffusés] | Pourcentage d’e-mails envoyés ayant été diffusés. |
| [!UICONTROL Hard bounce] | Nombre d’e-mails dont la diffusion a définitivement échoué. |
| [!UICONTROL Soft Bounce] | Nombre d’e-mails dont la diffusion a temporairement échoué. |
| [!UICONTROL Ouvert] | Nombre de fois où les destinataires ont ouvert l’e-mail. |
| [!UICONTROL &#x200B; % ouvert] | Pourcentage d’e-mails diffusés ouverts. |
| [!UICONTROL sur lequel l’utilisateur a cliqué] | Nombre de fois où les destinataires ont cliqué sur un lien dans l’e-mail. |
| [!UICONTROL &#x200B; % ont cliqué] | Pourcentage d’e-mails diffusés ayant reçu un clic. |
| [!UICONTROL Cliquer pour ouvrir le rapport] | Pourcentage d’e-mails ouverts ayant reçu un clic. |
| [!UICONTROL Désabonné] | Nombre de destinataires qui se sont désabonnés de l’e-mail. |
| [!UICONTROL &#x200B; % de désabonnements] | Pourcentage d’e-mails diffusés ayant entraîné un désabonnement. |

<!--

## Filters {#filters}

Use filters to narrow the report to a specific journey, persona, or date range. Select **[!UICONTROL Reset all]** to clear every filter and return to the default view.

* **[!UICONTROL Journey Name (Event)]** - Filter by the journey that sent the email. Default is [!UICONTROL No filter].
* **[!UICONTROL Persona (Event)]** - Filter by the persona associated with the email. Default is [!UICONTROL No filter].
* **[!UICONTROL Date range]** - Filter by a specific date span, shown as explicit start and end dates. Default is [!UICONTROL Last 30 days].
-->