---
title: Architecture De Haut Niveau
description: Découvrez l’architecture des données qui connecte Marketo Optimizer et Marketo Engage, y compris la synchronisation bidirectionnelle, la latence des entités et l’isolation des données du client.
role: User, Admin
TQID: 'https://experienceleague.adobe.com/oelEtys81g6TzM8bi-qy1nuWw6scOBry7tbZkMkZ6u0'
product_v2: id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2: id: 3c1de303-7a7c-59a6-abca-8c534730e19cid: 64b90904-e4f0-5c1b-a871-8c6a40b204a1id: d4203578-d294-5145-b397-f26f4488a904
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d00e9f03-e50b-4162-b143-0c0817c937c2id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 1%

---


# Architecture détaillée

[!DNL Adobe Marketo Optimizer] s’intègre à [!DNL Adobe Marketo Engage] pour offrir une vue à 360 degrés des prospects B2B. Une synchronisation bidirectionnelle fiable conserve la [!DNL Marketo Engage] et la [!DNL Marketo Optimizer], offrant aux deux plateformes une vue unique et partagée des personnes, des entreprises, des objets personnalisés et des activités. Le flux de données hautes performances en temps quasi réel garantit que les enregistrements restent à jour et exploitables, de sorte que les campagnes et les parcours puissent répondre aux prospects dès leur engagement.

## Base des données

[!DNL Marketo Optimizer] et [!DNL Marketo Engage] partagent une base de données commune qui les maintient synchronisées tout en alimentant les analyses en aval.

![Diagramme d’architecture de Marketo Optimizer et Marketo Engage qui montre comment les services, runtimes et entrepôts de données des deux produits se connectent à Microsoft Azure et AWS](./assets/marketo-optimizer-architecture.svg)

À un niveau élevé :

* **[!DNL Marketo Engage]Core** est la source définitive de données d’objet de prospect et personnalisées, assurant l’intégrité des données au point de capture.
* Une **couche du courtier de données** coordonne le déplacement des données entre [!DNL Marketo Engage] et [!DNL Marketo Optimizer], en agrégeant les données partagées et répliquées dans un environnement opérationnel et prêt à l’emploi. Cet échange complet s’exécute dans une instance AWS Aurora partagée unique, formant la base en boucle fermée pour une orchestration B2B à grande échelle.
* Les **activités** suivent un chemin défini : elles sont d’abord écrites dans la base de données [!DNL Marketo Engage] et indexées dans Apache SOLR pour une recherche rapide dans le produit, puis publiées dans le pipeline d’activité afin d’[!DNL Marketo Optimizer] une reconnaissance instantanée. L’exécution du parcours traite cette activité et l’écrit dans Snowflake, transformant ainsi les données opérationnelles en données prêtes pour l’analyse. De là, l’activité est répliquée dans des jeux de données [!DNL Adobe Experience Platform] et [!DNL Adobe Customer Journey Analytics] à alimenter les rapports.
* Différents types d’entités se synchronisent à des vitesses et des directions différentes pour équilibrer la fraîcheur et l’intégrité du système :

| entité [!DNL Marketo Engage] | Direction de synchronisation | Latence |
| --- | --- | --- |
| Lead | Bidirectionnel | &lt; 1 s |
| Société | Bidirectionnel | &lt; 1 s |
| Objet personnalisé | Unidirectionnel | &lt; 5 s |
| Activité | Unidirectionnel | &lt; 5 s |
| Appartenance au programme | Non synchronisé | — |
| Ressources | Non synchronisé | — |

Les leads et les sociétés se mettent à jour instantanément dans les deux directions sans créer de doublons de données. Les objets personnalisés se répliquent en quelques secondes, de sorte que les mises à jour de schéma dans [!DNL Marketo Engage] soient immédiatement exploitables dans un parcours actif. L’appartenance à un programme et Assets sont délibérément exclues de la synchronisation pour préserver la vitesse et l’intégrité du système.

Cette conception de latence quasi nulle signifie que les tableaux de bord d’analyse et les systèmes en aval sont alimentés en temps quasi réel, ce qui permet d’optimiser les campagnes en direct et d’effectuer un suivi rapide des prospects hautement prioritaires.

### Isolation et connexion des données

* Les données clients sont partagées entre [!DNL Marketo Engage], [!DNL Marketo Optimizer] et [!DNL Experience Platform] dans le cadre de la synchronisation des données de produit et de l’architecture d’analyse.
* Les données sont logiquement isolées par client et protégées par les contrôles de sécurité d’Adobe.
* Les données sont transférées sur des canaux sécurisés et chiffrés, puis stockées dans les services gérés par Adobe à l’aide du chiffrement standard et des contrôles d’accès.
* Selon le type de données, les informations peuvent être synchronisées entre [!DNL Marketo Engage] et [!DNL Marketo Optimizer] ou répliquées vers [!DNL Experience Platform] pour prendre en charge les fonctionnalités de reporting et d’analyse, tout en préservant la sécurité et l’isolement des clients.
