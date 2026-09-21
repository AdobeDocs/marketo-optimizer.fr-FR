---
title: Rapport sur l’engagement des e-mails
description: Découvrez le rapport sur l’engagement des e-mails dans Adobe Marketo Optimizer, qui affiche la délivrabilité des e-mails et les mesures d’engagement par e-mail et par parcours.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 6e919a66af259ea1f5facf7f5c3e811d76101e85
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 1%
---

# Rapport Engagement des e-mails

<!-- SPHR-32511: Filter by Program, Filter by Audience, and the program data point for the email performance table are not documented here pending delivery. -->

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
| [!UICONTROL  % diffusés] | Pourcentage d’e-mails envoyés ayant été diffusés. |
| [!UICONTROL Hard bounce] | Nombre d’e-mails dont la diffusion a définitivement échoué. |
| [!UICONTROL Soft Bounce] | Nombre d’e-mails dont la diffusion a temporairement échoué. |
| [!UICONTROL Ouvert] | Nombre de fois où les destinataires ont ouvert l’e-mail. |
| [!UICONTROL  % ouvert] | Pourcentage d’e-mails diffusés ouverts. |
| [!UICONTROL sur lequel l’utilisateur a cliqué] | Nombre de fois où les destinataires ont cliqué sur un lien dans l’e-mail. |
| [!UICONTROL  % ont cliqué] | Pourcentage d’e-mails diffusés ayant reçu un clic. |
| [!UICONTROL Cliquer pour ouvrir le rapport] | Pourcentage d’e-mails ouverts ayant reçu un clic. |
| [!UICONTROL Désabonné] | Nombre de destinataires qui se sont désabonnés de l’e-mail. |
| [!UICONTROL  % de désabonnements] | Pourcentage d’e-mails diffusés ayant entraîné un désabonnement. |

## Filtres {#filters}

Utilisez des filtres pour limiter le rapport à un parcours ou à une personne spécifique. Sélectionnez **[!UICONTROL Réinitialiser tout]** pour effacer chaque filtre et revenir à la vue par défaut.

* **[!UICONTROL Nom du Parcours (Événement)]** - Filtrez par le parcours qui a envoyé l’e-mail. La valeur par défaut est [!UICONTROL  Aucun filtre ].
* **[!UICONTROL Persona (événement)]** - Filtrez par le persona associé à l’e-mail. La valeur par défaut est [!UICONTROL  Aucun filtre ].