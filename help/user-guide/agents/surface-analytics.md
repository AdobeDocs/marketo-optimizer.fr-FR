---
title: Génération de rapports Analytics
description: Découvrez comment utiliser les compétences Surface Analytics dans la conversation des collègues pour générer des rapports d’activité, d’e-mail, de prospect, de segment et de parcours à partir d’invites en langage naturel.
autotag-review: '2026-09-21T14:58:26.479Z'
TQID: 'https://experienceleague.adobe.com/BSDEihjdpz-YZjMWrYTmIuyjqtcjRHRrJdz4xPFZbHU'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 1650dadf-b034-5ac9-a309-77ad1e2f5035
    internal-label: Chat Interface
  - id: 3c1de303-7a7c-59a6-abca-8c534730e19c
    internal-label: Reporting
subfeature_v2:
  - id: b9e5c7f3-be30-563c-9e41-cc8ea76e2fee
    internal-label: Skills
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
source-git-commit: 1dcc3bcdc59114c7fc1e16178db8921ae173b955
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%
---
# Génération de rapports d’analyse

La compétence [_Surface Analytics_ &#x200B;](./skills.md#analytics-reporting) de [!DNL Adobe Marketo Optimizer] répond aux questions en langage naturel sur vos données. Utilisez-le dans l’[interface de conversation des collègues](./chat-interface.md) pour explorer les tendances des activités, les performances des e-mails, les données de prospect et de compte, l’appartenance à un segment et à une liste, ainsi que les mesures de parcours. Les résultats sont renvoyés sous forme de graphiques et de tableaux de bord, de sorte que vous n’avez pas besoin de créer manuellement une requête ou un tableau de bord.

* **Compétences** - `surface-analytics`
* **Appel** - Posez une question en langage naturel ou utilisez une commande de barre oblique pour exécuter la compétence Surface Analytics. Par exemple : _« Afficher le nombre d’activités quotidiennes pour les 30 derniers jours.«_
* **Lit à partir de** - [!DNL Marketo Optimizer] les données d’analyse ; lit les données d’analyse [!DNL Marketo Engage] pour les questions qui couvrent les deux produits.

>[!NOTE]
>
>Les données du rapport sont actualisées toutes les deux heures. Les résultats peuvent ne pas refléter l’activité des deux dernières heures.

## Afficher les tendances des activités {#activity-trends}

Renseignez-vous sur le nombre d’activités quotidiennes ou hebdomadaires et ventilez les résultats par type d’activité ou par zone de produit.

* _« Afficher le nombre d’activités quotidiennes au cours des 30 derniers jours._ »
* _« Quels sont les principaux types d’activités de la semaine ?«_
* _« Répartissez l’activité du mois dernier par zone d’application »_

## Vérifier les performances des e-mails {#email-performance}

Renseignez-vous sur le volume d’envoi, les taux d’ouverture et de clics, les bounces et les désabonnements pour vos programmes de messagerie.

* _« Quel est le taux d’ouverture des e-mails par parcours ?«_
* _« Afficher les taux de clics des 90 derniers jours.«_
* _« Combien de désabonnements avons-nous reçus la semaine dernière ?«_

## Analyse des données de lead et de compte {#lead-account-data}

Renseignez-vous sur la distribution des scores des prospects, les répartitions des rôles et les cumuls géographiques ou micrographiques.

* _« Montrez-moi la répartition des scores entre les prospects_. »
* _« Combien y a-t-il de personnes dans chaque compte ?«_
* _« Ventilez les leads par persona.«_

## Vérifier l’appartenance à un segment et à une liste {#segment-list-membership}

Demandez qui appartient à une liste ou à un segment spécifique.

* _« Combien de personnes figurent sur la liste des formations au 1er trimestre ?«_
* _« Quel segment a le plus de membres ?«_

## Explorer les mesures de parcours {#journey-metrics}

Renseignez-vous sur l’appartenance au parcours, les taux d’achèvement, le parcours transversal des nœuds et l’analyse funnel.

* _« Quel est le taux d’achèvement du parcours de suivi de la démonstration ?«_
* _« Combien y a-t-il de personnes dans chaque nœud du parcours LeadNurture ?«_

## Poser des questions sur plusieurs produits {#cross-product}

Surface Analytics peut répondre à des questions qui couvrent à la fois les données [!DNL Marketo Engage] et [!DNL Marketo Optimizer] dans une seule invite.

* _« Quelle est ma messagerie la plus performante dans LumaSecure et dans LumaStorage ? »_

## Limites {#limitations}

| Limite | Détail |
|---|---|
| Modifier ou créer des enregistrements | Non pris en charge. Surface Analytics ne lit et ne génère des rapports que sur les données existantes. |
| Noms lisibles par l’utilisateur dans les résultats | Pas toujours disponible. Certains rapports affichent un ID interne, tel qu’un ID de parcours ou d’e-mail, au lieu d’un nom. |
| Duplication de cartes de rapports | Une même question peut parfois renvoyer plusieurs cartes de rapports pour le même résultat. |
