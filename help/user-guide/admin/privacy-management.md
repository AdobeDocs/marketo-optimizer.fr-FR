---
title: Gestion de la confidentialité
description: Découvrez comment vous conformer au RGPD, au CCPA et à d’autres règlements sur la confidentialité dans Marketo Optimizer, et comment envoyer des demandes à l’aide d’Adobe Privacy Service.
feature: Setup
role: Admin
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: 630
ht-degree: 6%

---


# Gestion de la confidentialité {#privacy-management}

[&#128279;](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/home){target="_blank"} fournit une API RESTful et une interface utilisateur pour vous aider à gérer les demandes de données des clients. Avec [!DNL Adobe Privacy Service], vous pouvez envoyer des demandes d’accès et de suppression de données clients personnelles des applications Adobe CX Enterprise, ce qui facilite l’automatisation de la conformité aux réglementations légales et organisationnelles en matière de confidentialité.

[!DNL Adobe Marketo Optimizer] fournit ces outils de confidentialité afin que vous puissiez répondre aux exigences mondiales en matière de protection des données. Utilisez des [!DNL Privacy Service] pour envoyer et gérer des demandes d’accès et de suppression pour les données que [!DNL Marketo Optimizer] collecte et stocke.

Vous pouvez soumettre des requêtes individuelles pour accéder aux données des clients et les supprimer de [!DNL Adobe Marketo Optimizer] de deux manières :

* L’interface utilisateur de [!DNL Privacy Service]
* L’API [!DNL Privacy Service]

## Règlements de confidentialité pris en charge {#regulations}

[!DNL Marketo Optimizer] outils de confidentialité vous aident à vous conformer à la réglementation par le biais de [!DNL Privacy Service]. Chaque règlement s’applique si vous détenez des données pour les personnes qui résident dans la région associée.

Pour obtenir la liste à jour des réglementations prises en charge, voir [_Présentation des réglementations de confidentialité_](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/regulations/overview){target="_blank"} dans la documentation de Privacy Service.

## Types de requêtes {#access-and-delete-requests}

[!DNL Marketo Optimizer] prend en charge deux types de demandes d’accès à des informations personnelles :

* **Accès aux données** - Une personne peut demander la confirmation que ses données personnelles sont en cours de traitement et recevoir une copie électronique gratuite de ces données.
* **Suppression des données** - Également appelé le _droit à l&#39;oubli_, une personne peut demander que vous effaciez ses données personnelles et que vous arrêtiez le traitement ultérieur.

## Affichage et gestion des demandes d’accès à des informations personnelles {#view-manage-requests}

>[!BEGINSHADEBOX]

![Icône Autorisations AEP &#x200B;](../assets/do-not-localize/icon_permissions-outline.svg) ces étapes nécessitent le profil de produit [!DNL Privacy Service] et les [autorisations suivantes pour le rôle d’utilisateur qui vous a été attribué dans Experience Platform &#x200B;](../start/user-management.md#permissions) :

* **[!UICONTROL Autorisations Privacy Service]** - `Privacy Read Permission` et `Privacy Write Permission`
* **[!UICONTROL Gouvernance des données]** - `View Privacy Console`

Voir [_Gestion des autorisations pour Privacy Service_](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/permissions){target="_blank"} dans le guide de [!DNL Privacy Service] pour plus d’informations.

>[!ENDSHADEBOX]

Pour afficher les traitements de demande d&#39;accès à des informations personnelles dans [!DNL Marketo Optimizer], développez **[!UICONTROL Confidentialité]** et sélectionnez **[!UICONTROL Demandes]**.

Utilisez l’option **[!UICONTROL Type de réglementation]** en haut à droite pour modifier la page affichée pour la réglementation que vous souhaitez gérer les tâches ou soumettre des demandes.

![Traitements de demande d&#39;accès à des informations personnelles, sélectionnez le type de réglementation](./assets/privacy-requests.png){width="800" zoomable="yes"}

### Envoi d’une requête {#submit-a-request}

1. Cliquez sur **[!UICONTROL Créer une demande]**.

1. Pour le **[!UICONTROL Type de traitement]**, sélectionnez le type de traitement :

   * **[!UICONTROL Accès]**

     Lorsque vous soumettez une demande d’**_accès_** qui comprend des [!DNL Marketo Optimizer], [!DNL Privacy Service] renvoie :

     * [!DNL Marketo Engage] activité associée au prospect.
     * [!DNL Marketo Optimizer] activité associée à la personne ou au compte.

   * **[!UICONTROL Supprimer]**

     Lorsque vous soumettez une demande **delete** pour [!DNL Marketo Engage] et [!DNL Marketo Optimizer], les enregistrements suivants sont supprimés :

     * Lead associé dans [!DNL Marketo Engage].
     * Enregistrements de compte et de personne créés dans [!DNL Marketo Optimizer].
     * Historique des conversations des collègues qui font référence aux informations personnelles de la personne.

1. Pour **[!UICONTROL Produits]**, sélectionnez **[!UICONTROL Marketo]**.

   ![Créer une demande d’accès à des informations personnelles en vertu du RGPD pour Marketo Engage et Marketo Optimizer](./assets/privacy-request-create-gdpr.png){width="450" zoomable="yes"}

   Cette sélection inclut les données de [!DNL Marketo Optimizer] et de votre instance [!DNL Marketo Engage].

1. Faites défiler la page jusqu’au bas de la boîte de dialogue et saisissez l’adresse e-mail de la personne dont vous souhaitez accéder aux données ou les supprimer.

1. Pour soumettre la demande, cliquez sur **[!UICONTROL Créer]**.

   [!DNL Privacy Service] renvoie un identifiant de requête que vous pouvez utiliser pour vérifier le statut de votre requête.

### Requêtes API {#api-requests}

Vous pouvez également envoyer des demandes d’accès à des informations personnelles à l’aide de l’API [!DNL Privacy Service]. Pour consulter la référence générale de l’API, voir la documentation de l’API Privacy Service [&#128279;](https://developer.adobe.com/experience-platform-apis/references/privacy-service){target="_blank"}.

>[!PREREQUISITES]
>
>Rassemblez les informations suivantes avant d’envoyer une requête :
>
>* L’identifiant d’organisation IMS de votre organisation (chaîne alphanumérique de 24 caractères se terminant par `@AdobeOrg`). Contactez l’assistance Adobe à l’adresse `gdprsupport@adobe.com` si vous ne connaissez pas votre ID d’organisation IMS.
>* Adresse e-mail de la personne dont vous souhaitez accéder aux données ou les supprimer.

Utilisez les valeurs de champ suivantes dans votre requête :

| Champ | Valeur |
|---|---|
| `companyContexts.namespace` | `imsOrgID` |
| `companyContexts.value` | Votre identifiant de l’organisation IMS |
| `users.action` | `access` ou `delete`. |
| `users.userIDs.namespace` | `Email` |
| `include` | `marketo` d’inclure les données [!DNL Marketo Optimizer] et [!DNL Marketo Engage] |
| `regulation` | Exemple : `ccpa` <br/>Certaines valeurs de réglementation sont modifiées pour inclure une abréviation d’état (par exemple, `ucpa_ut_usa`). Les anciennes valeurs restent valables pendant une période de transition. Pour obtenir la liste actuelle avant de créer des intégrations en fonction de ces valeurs[&#128279;](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/regulations/overview){target="_blank"} reportez-vous à la  Présentation des réglementations de confidentialité . |

L’exemple suivant soumet une requête de suppression en vertu du RGPD qui inclut des données [!DNL Marketo Optimizer].

```json
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "1231659F56A68A8B7F000101@AdobeOrg"
    }
  ],
  "users": [
    {
      "action": ["delete"],
      "userIDs": [
        {
          "namespace": "Email",
          "type": "standard",
          "value": "john.doe@adobe.com"
        }
      ]
    }
  ],
  "include": ["marketo"],
  "regulation": "gdpr"
}
```

[!DNL Privacy Service] renvoie une réponse similaire à ce qui suit.

```json
{
  "requestId": "16331241037112570RX-245",
  "totalRecords": 1,
  "jobs": [
    {
      "jobId": "997b01e3-9568-402c-904b-b4e60a437875",
      "customer": {
        "user": {
          "action": ["delete"],
          "userIDs": [
            {
              "namespace": "Email",
              "value": "john.doe@adobe.com",
              "type": "standard",
              "namespaceId": 6,
              "isDeletedClientSide": false
            }
          ]
        }
      }
    }
  ]
}
```
