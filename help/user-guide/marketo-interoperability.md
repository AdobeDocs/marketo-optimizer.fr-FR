---
title: Interopérabilité avec Marketo Engage
description: Découvrez ce que Marketo Optimizer partage avec Marketo Engage, y compris les données, les activités et les audiences, et comment envoyer des e-mails à partir de l’un des produits dans vos parcours.
role: User, Admin
autotag-review: '2026-10-01T18:40:01.444Z'
TQID: 'https://experienceleague.adobe.com/7TB6JG9yiUT-l0VevNW4tvwieCyFjOypZwI0SlUzmmY'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
    internal-label: Audiences
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: a29661b8-f7a4-53d1-a9ac-fdec08c092e4
    internal-label: Programs
  - id: d4203578-d294-5145-b397-f26f4488a904
    internal-label: Channels
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
    internal-label: Customer journeys
source-git-commit: cd171c6ec89301ed315d8b882ac0fccac745809f
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%
---

# Interopérabilité avec Marketo Engage

[!DNL Adobe Marketo Optimizer] et [!DNL Adobe Marketo Engage] partagent des données, certaines activités et des audiences. Ils séparent les ressources. Comprenez ce que chaque produit partage pour décider où créer et envoyer votre marketing.

## Partagé entre les produits {#shared}

* [!DNL Marketo Engage] leads et les activités se propagent automatiquement dans [!DNL Marketo Optimizer].
* Les parcours peuvent écouter les activités [!DNL Marketo Engage].
* Les audiences basées sur un événement peuvent inclure des personnes qui effectuent des activités [!DNL Marketo Engage].
* Les actions de parcours peuvent interagir avec les [!DNL Marketo Engage]. Vous pouvez ajouter des personnes à une liste de [!DNL Marketo Engage] ou en supprimer et demander une campagne de [!DNL Marketo Engage].
* [!UICONTROL Scoring Studio] évalue les personnes par rapport aux activités [!DNL Marketo Engage] et [!DNL Marketo Optimizer]. Vous pouvez utiliser les scores dans [!DNL Marketo Engage].
* Les deux produits partagent des adresses IP et des sous-domaines.
* Le reporting conversationnel unifié couvre les deux produits.

## Conservé séparément {#separate}

* **Assets:** Les e-mails, modèles, programmes et images sont stockés dans des référentiels distincts.
* **Activités :** les activités [!DNL Marketo Optimizer] ne sont pas partagées avec [!DNL Marketo Engage].
* **Champs et limites :** les champs de persona que [!DNL Marketo Optimizer] dérive ne sont pas disponibles dans [!DNL Marketo Engage]. Les limites de communication sont définies séparément dans chaque produit.

Pour plus d’informations sur la synchronisation, voir [Synchronisation des entités](./data-architecture.md#entity-sync).

## Envoyer un e-mail à partir de Marketo Engage {#send-from-marketo}

Utilisez cette approche pour exécuter des parcours, des étapes d’attente et la prise de décision par l’IA dans [!DNL Marketo Optimizer] pendant que [!DNL Marketo Engage] envoie chaque e-mail.

1. Dans [!DNL Marketo Optimizer], créez un parcours qui inclut les étapes d’attente et la prise de décision par l’IA.
1. Pour chaque étape d’envoi, ajoutez l’action **[!UICONTROL Demander une campagne Marketo Engage]** et sélectionnez une campagne [!DNL Marketo Engage] correspondante.
1. Facultatif : ajoutez un programme global par défaut [!DNL Marketo Engage] d’agréger les rapports de succès dans le parcours.

Pour plus d’informations sur les actions, voir [Nœud d’action à exécuter](./marketing/action-nodes.md).

[!DNL Marketo Engage] envoie l’e-mail par le biais des paramètres de votre canal existant. Étant donné que [!DNL Marketo Engage] envoie l’e-mail, vous ne configurez pas de canaux ni d’e-mails dans [!DNL Marketo Optimizer]. En outre :

* Les envois, les ouvertures et les clics sont enregistrés dans [!DNL Marketo Engage].
* La gestion des désabonnements et la gouvernance des e-mails s’appliquent dans [!DNL Marketo Engage].
* L’activité E-mail alimente vos campagnes de notation de [!DNL Marketo Engage] existantes.
* Les campagnes de synchronisation Salesforce déclenchées par une activité s’exécutent comme prévu.
* Chaque envoi envoie des mappages à une campagne [!DNL Marketo Engage], de sorte que vous puissiez suivre l’adhésion au programme par campagne par e-mail et créer des rapports dans les programmes familiers.

## Envoyer un e-mail à partir de Marketo Optimizer {#send-from-optimizer}

Utilisez cette approche pour créer le parcours et envoyer un e-mail entièrement en [!DNL Marketo Optimizer]. [!DNL Marketo Engage] reste le système d’enregistrement pour la transmission à votre système de gestion de la relation client (GRC).

1. Configurez le canal e-mail . Créez des modèles d’e-mail et configurez l’adresse IP et le sous-domaine, les liens de désabonnement et les pages de destination. Voir [Délivrabilité des emails](./start/email-deliverability.md).
1. Définissez les limites de communication dans [!DNL Marketo Optimizer]. Les limites de communication partagées ne sont pas disponibles.
1. Créez le parcours avec les audiences, la prise de décision par l’IA et le meilleur chemin.
1. Envoyez un e-mail à partir de [!DNL Marketo Optimizer]. [!DNL Marketo Optimizer] enregistre les activités.
1. Notez les personnes dans [!UICONTROL Scoring Studio] pour créer un modèle dans l’activité [!DNL Marketo Engage] et [!DNL Marketo Optimizer]. Voir [&#x200B; Scoring Studio &#x200B;](./labs/scoring-studio.md).

Les désabonnements se synchronisent automatiquement avec les [!DNL Marketo Engage] partagés. [!DNL Marketo Optimizer] activité e-mail n’est pas renvoyée à [!DNL Marketo Engage], mais [!UICONTROL Scoring Studio] l’utilise toujours.

### Remettre les leads aux ventes {#hand-off}

[!DNL Marketo Optimizer] n’a pas d’intégration CRM directe. L’itinéraire mène à [!DNL Marketo Engage] avec l’une des méthodes suivantes :

* **Basé sur les scores :** le champ de score s’affiche en [!DNL Marketo Engage] et une campagne intelligente synchronise le prospect sur votre CRM.
* **Basé sur les activités :** un parcours [!DNL Marketo Optimizer] écoute l’activité et ajoute le prospect à une campagne intelligente [!DNL Marketo Engage].
* **Appartenance à un programme :** le parcours se trouve dans un programme [!DNL Marketo Optimizer], ce qui vous permet de suivre le statut du début à la fin.
