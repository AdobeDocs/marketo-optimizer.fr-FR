---
title: Architecture des données
description: Découvrez comment Marketo Optimizer et Marketo Engage partagent des données, notamment le sens et la latence de la synchronisation des entités, le flux de données d’activité et l’isolation de données basée sur le sandbox.
role: User, Admin
autotag-review: '2026-10-01T18:40:38.362Z'
TQID: 'https://experienceleague.adobe.com/oelEtys81g6TzM8bi-qy1nuWw6scOBry7tbZkMkZ6u0'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
    internal-label: Setup
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
    internal-label: Audiences
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: d4203578-d294-5145-b397-f26f4488a904
    internal-label: Channels
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
source-git-commit: 518a807aeed2471772b4f0a4d6d8d525cd3e22fd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 1%
---

# Architecture des données

[!DNL Adobe Marketo Optimizer] s’intègre à [!DNL Adobe Marketo Engage] pour offrir une vue complète des prospects B2B. Une synchronisation fiable et bidirectionnelle permet aux deux produits de rester alignés et de partager la même vision des personnes, des entreprises, des objets personnalisés et des activités. [!DNL Marketo Engage] reste la source faisant autorité pour les données de personne. Chaque instance [!DNL Marketo Optimizer] est associée à une instance [!DNL Marketo Engage].

## Base des données {#data-foundation}

[!DNL Marketo Optimizer] et [!DNL Marketo Engage] partagent une base de données commune qui les maintient synchronisées tout en alimentant les analyses en aval.

![Diagramme d’architecture de Marketo Optimizer et Marketo Engage qui montre comment les services, les runtimes et les banques de données des deux produits se connectent à Microsoft Azure et AWS](./assets/marketo-optimizer-architecture.svg)

À un niveau élevé :

* **[!DNL Marketo Engage]** est la source définitive des données de lead et d’objet personnalisé, ce qui garantit l’intégrité des données au point de capture.
* Un **calque du courtier de données** coordonne la manière dont les données se déplacent entre les deux produits. Il regroupe les données partagées et répliquées dans une base de données opérationnelle prête à l’emploi. L’ensemble de l’échange s’exécute dans un seul cluster Aurora MySQL.
* **[!DNL Marketo Optimizer]** est la source faisant autorité pour les activités de parcours qu’il exécute.

## Synchronisation des entités {#entity-sync}

Chaque type d’entité se synchronise dans la direction et à la vitesse qui protègent le mieux l’intégrité des données.

| entité [!DNL Marketo Engage] | Direction de synchronisation | Latence |
| --- | --- | --- |
| Lead | Bidirectionnel | Moins d’une seconde |
| Société | Bidirectionnel | Moins d’une seconde |
| Objet personnalisé | Unidirectionnel | Moins de 5 secondes |
| Activité | Unidirectionnel | Moins de 5 secondes |
| Appartenance au programme | Non synchronisé | Non applicable |
| Ressources | Non synchronisé | Non applicable |

La synchronisation fonctionne de deux manières :

* **Leads, sociétés et objets standard :** [!DNL Marketo Engage] possède la table de la personne et la partage par le biais des vues de base de données en lecture et écriture. Les mises à jour d’un produit apparaissent immédiatement dans l’autre et aucune copie en double n’est créée.
* **Objets personnalisés :** les données sont répliquées à partir des [!DNL Marketo Engage] en quelques secondes. Les mises à jour des schémas dans [!DNL Marketo Engage] sont immédiatement disponibles pour les parcours actifs.

[!DNL Marketo Engage] et [!DNL Marketo Optimizer] ne synchronisent pas l’appartenance à un programme ni les ressources. Cette exclusion préserve la vitesse et l’intégrité du système.

>[!NOTE]
>
>Les données synchronisées avec [!DNL Marketo Optimizer] et avec l’entrepôt de données finissent par être cohérentes. Le minutage dépend du mécanisme sous-jacent de capture de données de modification, par lots ou par flux.

Cette conception en temps quasi réel vous donne les données actuelles dans les parcours et les rapports. Vous pouvez effectuer un suivi rapide des prospects hautement prioritaires. Vous pouvez également utiliser des données contextuelles B2B, telles que l’utilisation et l’intention du produit, dans les décisions de parcours à mesure qu’elles changent.

## Flux de données d’activité {#activity-flow}

Les activités suivent un chemin distinct des autres entités. Chaque activité passe par cinq étapes :

1. **Capture de Principal :** [!DNL Marketo Engage] écrit l’activité dans sa base de données partagée et l’indexe dans Apache SOLR pour une recherche rapide dans [!DNL Marketo Engage].
1. **Prise de conscience de l’ensemble des produits :** [!DNL Marketo Engage] publie l’activité dans le pipeline d’activité, donc [!DNL Marketo Optimizer] la reçoit immédiatement.
1. **Transformation analytique :** l’exécution du parcours traite l’activité et l’écrit dans Snowflake, qui transforme les données opérationnelles en données prêtes pour l’analyse. Toutes les étapes s’exécutent jusqu’à présent dans Amazon Web Services (AWS).
1. **Destination en aval :** [!DNL Marketo Optimizer] réplique l’activité dans des jeux de données [!DNL Adobe Experience Platform].
1. **Rapports :** les jeux de données alimentent les rapports [!DNL Adobe Customer Journey Analytics] incorporés. [!DNL Customer Journey Analytics] peut être hébergé sur Microsoft Azure ou AWS. Vous pouvez également interroger les jeux de données avec [!DNL Query Service]. Voir [Jeux de données &#x200B;](./reports/aep-datasets.md).

Les parcours et les audiences d’événement peuvent utiliser à la fois des activités [!DNL Marketo Optimizer] et un sous-ensemble d’activités [!DNL Marketo Engage]. Vous utilisez les deux visionneuses de la même manière. [!DNL Marketo Optimizer] activités ne sont pas renvoyées à [!DNL Marketo Engage].

Utilisez des activités telles que les remplissages de formulaires, les visites web et l’engagement par e-mail pour déclencher, filtrer et créer des branches dans les parcours de personne :

* [Déclencheurs d’événement pour le nœud Écouter pour un événement](./marketing/listen-for-event-nodes.md#event-triggers)
* [Filtres d’événement pour le nœud Écouter un événement](./marketing/listen-for-event-nodes.md#event-filters)
* [Filtres de personnes correspondant pour les nœuds de chemins de division](./marketing/split-merge-paths-nodes.md#matched-person-filters)
* [Audiences basées sur un événement](./audiences/event-based-audiences.md)

## Isolation des données et sandbox {#data-isolation}

[!DNL Marketo Engage], [!DNL Marketo Optimizer] et [!DNL Experience Platform] partagent des données client dans le cadre de cette architecture. Adobe isole logiquement vos données des autres clients à l’aide de sandbox [!DNL Experience Platform]. Les données transitent par des canaux sécurisés et chiffrés. Adobe le stocke dans Adobe Managed Services avec un chiffrement standard et des contrôles d’accès.

Chaque instance de [!DNL Marketo Optimizer] dispose d’une carte de produit dédiée dans le [!DNL Adobe Admin Console] et d’un sandbox dédié. Adobe approvisionne les deux automatiquement, de sorte que vous ne créiez pas de sandbox. Le nom du sandbox utilise le `mktoaep<prefix>` de motif , où le préfixe correspond à votre préfixe [!DNL Marketo Engage]. Si vous utilisez [!DNL Marketo Optimizer] avec plusieurs instances [!DNL Marketo Engage], chaque instance possède sa propre carte de produit et son propre sandbox.

[!DNL Marketo Optimizer] est disponible uniquement dans ce sandbox, même si votre organisation en possède d’autres.

L’approvisionnement n’affecte pas l’accès au sandbox. Les rôles ont généralement accès au sandbox `prod` par défaut, mais [!DNL Marketo Optimizer] ne l’utilise pas. Affectez explicitement le sandbox dédié à chaque rôle de [!DNL Experience Platform] ou les utilisateurs ne peuvent pas travailler dans [!DNL Marketo Optimizer]. Utilisez des groupes d’utilisateurs pour ajouter et supprimer des utilisateurs sans répéter la configuration des rôles. Pour la procédure complète, voir [Accès et autorisations des utilisateurs](./start/user-management.md).

[!DNL Marketo Optimizer] utilise également les services [!DNL Experience Platform] en arrière-plan. Il s’agit notamment du registre des schémas, des destinations pour l’exportation de médias payants, du contrôle d’accès et des [!DNL Customer Journey Analytics]. Vous ne configurez pas de schémas ni d’espaces de noms. [!DNL Marketo Optimizer] ne nécessite pas de [!DNL Real-Time Customer Data Platform], de profil client en temps réel ni de segmentation.

>[!WARNING]
>
>Ne supprimez pas le sandbox [!DNL Marketo Optimizer] dédié. La suppression est permanente et ne peut pas être annulée. Reprovisionnement des [!DNL Marketo Optimizer] pour la récupération.
