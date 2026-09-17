---
title: Rapports
description: Découvrez l’onglet Rapports dans Adobe Marketo Optimizer, y compris ses sections de rapport, les options d’exportation et de planification, et comment modifier la période.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 32017a2577b7f31632080215ba91b9454c51b9ef
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 2%
---

# Rapports

L’onglet [!UICONTROL Rapports] vous donne des informations sur les performances dans les [!DNL Adobe Marketo Optimizer], notamment l’engagement des parcours, les performances des e-mails et l’activité web. Dans le volet de navigation de gauche, sélectionnez **[!UICONTROL Rapports]** pour l’ouvrir.

Chaque rapport est construit sur des [!DNL Adobe Customer Journey Analytics] et incorporé directement dans des [!DNL Marketo Optimizer]. Cliquez sur l’icône _Liste_ ( ![Icône Liste](../assets/do-not-localize/icon-table-of-contents.svg) ) pour utiliser le panneau **[!UICONTROL Table des matières]** situé à gauche afin de passer d’une section à l’autre.

![page Rapports répertoriant les sections Présentation du Parcours Personne, Engagement, Engagement des e-mails et Engagement web](./assets/reports-table-of-contents.png){width="800" zoomable="yes"}

## Sections du rapport {#report-sections}

L’onglet [!UICONTROL Rapports] organise les rapports préconfigurés en quatre sections. Chaque section comporte un ou plusieurs éléments téléchargeables, ainsi que sa propre page de documentation contenant des détails sur ses mesures et visualisations.

| Section | Éléments téléchargeables | Page de rapport |
| --- | --- | --- |
| [!UICONTROL Présentation du Parcours Personne] | Nombre de parcours actifs | [Rapport de présentation du Parcours Personne](./person-journey-overview-report.md) |
| [!UICONTROL Engagement] | Engagement des personnes, engagement des personnes au fil du temps | [Rapport d’engagement](./engagement-report.md) |
| [!UICONTROL Engagement des e-mails] | Engagement des e-mails | [Rapport d’engagement des e-mails](./email-engagement-report.md) |
| [!UICONTROL Engagement web] | Pages les plus vues | [rapport Engagement web](./web-engagement-report.md) |

## Rapports d’enregistrements individuels {#individual-record-reports}

Certains rapports se concentrent sur un seul enregistrement au lieu d’une vue à l’échelle de la section. Ils sont accessibles à partir d’une autre zone de l’application.

* Pour obtenir des performances d’optimisation de l’heure d’envoi des e-mails, ouvrez le rapport depuis l’interface de chat [!UICONTROL Coworker]. Pour connaître les étapes, voir [Optimisation de l’heure d’envoi des e-mails](../marketing/email-send-time-optimization.md#reporting).
* Pour la progression d’une personne dans un parcours unique, ouvrez le rapport depuis ce parcours.

## Exportation d’un rapport {#export-a-report}

Sélectionnez **[!UICONTROL Partager]** en haut de la page du rapport pour exporter ou planifier la diffusion de ses données.

![Menu Partager avec les options Télécharger CSV, Télécharger PDF, Planifier l’exportation et Gérer les plannings](./assets/reports-share-menu.png){width="500"}

* **[!UICONTROL Télécharger CSV]** - Exportez les données du rapport sous forme de valeurs en texte brut.

* **[!UICONTROL Télécharger PDF]** - Exportez tous les tableaux et visualisations visibles dans le rapport en tant que fichier PDF.

* **[!UICONTROL Planifier l’exportation]** - Configurez une exportation récurrente du rapport, diffusé une fois par semaine ou un mois dans un fichier CSV ou PDF.

* **[!UICONTROL Gérer les plannings]** - Examinez et gérez les exportations planifiées existantes. L’option affiche un nombre continu, par exemple `3/10`, de plannings utilisés par rapport à la limite de votre organisation.

>[!NOTE]
>
>Votre organisation peut avoir un maximum de 10 exportations planifiées sur tous les rapports, sur une fréquence hebdomadaire ou mensuelle. Si vous n’êtes pas administrateur, vous ne pouvez gérer que vos propres exportations planifiées. Les administrateurs peuvent afficher et gérer chaque exportation planifiée dans l’organisation.

## Analyse d’un rapport dans [!DNL Customer Journey Analytics] {#analyze-a-report-in-cja}

>[!AVAILABILITY]
>
>Cette fonction est disponible si votre entreprise dispose d’une licence pour [!DNL Adobe Customer Journey Analytics] et que le profil de produit vous est affecté.

Sélectionnez **[!UICONTROL Analyser dans CJA]** dans n’importe quelle section de rapport pour l’ouvrir dans [!DNL Adobe Customer Journey Analytics] Workspace, où vous pouvez créer des visualisations personnalisées en plus de celles disponibles dans le rapport incorporé.

## Modifier la période {#change-the-date-range}

Chaque section de rapport affiche les données d’une période spécifique, dans le coin supérieur droit de la section. Cliquez dans les champs de période pour afficher les outils de sélection de dates et sélectionnez la période. Vous pouvez choisir un autre paramètre prédéfini ou définir une plage personnalisée.

![Sélecteur de période avec un calendrier de deux mois, des champs de date de début et de fin, et des options prédéfinies](./assets/reports-date-range.png){width="600"}
