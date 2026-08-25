---
title: Architecture De Haut Niveau
description: Découvrez l’architecture des données qui connecte Marketo Optimizer et Marketo Engage, y compris la synchronisation bidirectionnelle, la latence des entités et l’isolation des données du client.
role: User, Admin
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 2%

---


# Architecture détaillée

[!DNL Adobe Marketo Optimizer] s’intègre à [!DNL Adobe Marketo Engage] pour offrir une vue à 360 degrés des prospects B2B. Une synchronisation bidirectionnelle fiable conserve l’alignement de Marketo Engage et de Marketo Optimizer, ce qui donne aux deux plateformes une vue unique et partagée des personnes, des entreprises, des objets personnalisés et des activités. Le flux de données hautes performances en temps quasi réel garantit que les enregistrements restent à jour et exploitables, de sorte que les campagnes et les parcours puissent répondre aux prospects dès leur engagement.

## Base des données

[!DNL Marketo Optimizer] et [!DNL Marketo Engage] partagent une base de données commune qui maintient les deux plateformes synchronisées tout en alimentant les analyses en aval.

![Diagramme d’architecture de Marketo Optimizer et Marketo Engage qui montre comment les services, runtimes et entrepôts de données des deux produits se connectent à Microsoft Azure et AWS](./assets/marketo-optimizer-architecture.svg)

À un niveau élevé :

* **Marketo Engage Core** est la source définitive des données de lead et d&#39;objet personnalisé, assurant l&#39;intégrité des données au point de capture.
* Une **couche du courtier de données** coordonne la manière dont les données se déplacent entre Marketo Engage et Marketo Optimizer, en agrégeant les données partagées et répliquées dans un environnement opérationnel et prêt à l’emploi. Cet échange complet s’exécute dans une instance AWS Aurora partagée unique, formant la base en boucle fermée pour une orchestration B2B à grande échelle.
* Les **activités** suivent un chemin défini : elles sont d’abord écrites dans la base de données Marketo Engage et indexées dans Apache SOLR pour une recherche rapide dans le produit, puis publiées dans le pipeline d’activité afin que Marketo Optimizer ait une visibilité instantanée. L’exécution du Parcours traite cette activité et l’écrit dans Snowflake, transformant ainsi les données opérationnelles en données prêtes pour l’analyse. De là, l’activité est répliquée dans les Jeux de données AEP et CJA afin d’alimenter les rapports.
* Différents types d’entités se synchronisent à des vitesses et des directions différentes pour équilibrer la fraîcheur et l’intégrité du système :

| Entité Marketo Engage | Direction de synchronisation | Latence |
| --- | --- | --- |
| Lead | Bidirectionnel | &lt; 1 s |
| Société | Bidirectionnel | &lt; 1 s |
| Objet personnalisé | Unidirectionnel | &lt; 5 s |
| Activité | Unidirectionnel | &lt; 5 s |
| Appartenance Au Programme | Non synchronisé | — |
| Ressources | Non synchronisé | — |

Les leads et les sociétés se mettent à jour instantanément dans les deux directions sans créer de doublons de données. Les objets personnalisés se répliquent en quelques secondes, de sorte que les mises à jour de schéma dans Marketo Engage soient immédiatement exploitables dans un parcours actif. L’appartenance à un programme et Assets sont délibérément exclues de la synchronisation pour préserver la vitesse et l’intégrité du système.

Cette conception de latence quasi nulle signifie que les tableaux de bord d’analyse et les systèmes en aval sont alimentés en temps quasi réel, ce qui permet d’optimiser les campagnes en direct et d’effectuer un suivi rapide des prospects hautement prioritaires.

### Isolation et connexion des données

* Les données clients sont partagées entre Marketo Engage, Marketo Optimizer et Experience Platform dans le cadre de l’architecture d’analyse et de synchronisation des données du produit.
* Les données sont logiquement isolées par client et protégées par les contrôles de sécurité d’Adobe.
* Les données sont transférées sur des canaux sécurisés et chiffrés, puis stockées dans les services gérés par Adobe à l’aide du chiffrement standard et des contrôles d’accès.
* Selon le type de données, les informations peuvent être synchronisées entre Marketo Engage et Marketo Optimizer ou répliquées vers Experience Platform afin de prendre en charge les fonctionnalités de création de rapports et d’analyse, tout en préservant la sécurité et l’isolement des clients.
