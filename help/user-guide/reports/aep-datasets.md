---
title: Jeux de données Experience Platform
description: Découvrez les jeux de données que Marketo Optimizer écrit dans Adobe Experience Platform pour alimenter la création de rapports Customer Journey Analytics et les requêtes ad hoc.
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
source-git-commit: 1ebb0036699252c50f33ba6c0f4a56e8e670aacd
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%
---

# Jeux de données Experience Platform

[!DNL Adobe Marketo Optimizer] réplique les données de prospect, de parcours et d’activité dans des jeux de données [!DNL Adobe Experience Platform]. Ces jeux de données alimentent la page [!UICONTROL Rapports] et l’expérience de rapport [!DNL Adobe Customer Journey Analytics] incorporée. Vous pouvez également les interroger directement avec [!DNL Query Service] pour une analyse ad hoc.

Les jeux de données sont gérés par le système. Une connexion dans [!DNL Customer Journey Analytics] les relie à la vue de données utilisée par [!DNL Marketo Optimizer] rapports. Vous n’avez donc pas besoin de créer cette connexion vous-même. Il s’agit de la même connexion que celle obtenue lorsque vous sélectionnez **[!UICONTROL Analyser dans CJA]** dans une section de rapport. Voir [&#x200B; Analyser un rapport dans Customer Journey Analytics](./reports-overview.md#analyze-a-report-in-cja).

## Jeux de données disponibles {#available-datasets}

Les jeux de données suivants sont renseignés pour chaque instance [!DNL Marketo Optimizer].

>[!NOTE]
>
>Chaque nom de jeu de données utilise le préfixe `AJOB2B`, qui indique le nom du système pour les données [!DNL Marketo Optimizer]. Ce comportement est attendu. Vous pouvez utiliser ces noms pour localiser les jeux de données dans votre sandbox [!DNL Experience Platform].

| Jeu de données | Schéma | Description |
| --- | --- | --- |
| `AJOB2B - Person` | Personne | Attributs de lead standard. |
| `AJOB2B - PersonActivity` | Activité de la personne | Événements d’activité associés à une personne. |
| `AJOB2B - PersonActivityType` | Type d’activité de la personne | Types d’activités associés à une personne. |
| `AJOB2B - PersonActivityTypeEngagementMapping` | Mappage de l’engagement du type d’activité de personne | fait correspondre les types d’activité à leur classification d’engagement, à leur événement de canal et à leur direction. |
| `AJOB2B - Journey` | Parcours | Liste des parcours et de leurs métadonnées de cycle de vie. |
| `AJOB2B - JourneyNode` | Nœud de parcours | Liste des nœuds dans un parcours et des métadonnées associées. |
| `AJOB2B - EngagementAsset` | Ressource d’engagement | Recherche unifiée des identifiants et des noms d’affichage des ressources d’engagement pour tous les types de ressources. |

## Jeux de données de requête avec Query Service {#query-service}

Utilisez des [!DNL Query Service] pour exécuter des requêtes SQL ad hoc sur ces jeux de données lorsque vous avez besoin d’une analyse en dehors des rapports [!DNL Customer Journey Analytics]. L’accès aux requêtes nécessite les autorisations de [!DNL Experience Platform] appropriées pour votre sandbox. Pour connaître la syntaxe et la configuration générales des requêtes, voir [Query Service](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home){target="_blank"}.

![Éditeur de Query Service affichant une requête SELECT sur le jeu de données ajob2b_parcours et un tableau des enregistrements de parcours résultants.](./assets/aep-query-service.png){width="800" zoomable="yes"}

>[!NOTE]
>
>Ces jeux de données sont en lecture seule. Pour modifier les données que [!DNL Marketo Optimizer] capture, mettez à jour les données sources dans [!DNL Marketo Optimizer] ou [!DNL Marketo Engage] au lieu de modifier directement un jeu de données.
