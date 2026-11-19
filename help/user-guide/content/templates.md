---
title: Modèles d’e-mail
description: Découvrez comment accéder aux modèles d’e-mail et les gérer dans Marketo Optimizer, notamment comment organiser les modèles à l’aide de dossiers.
TQID: 'https://experienceleague.adobe.com/PS1sj99Udmajg2M4JadFQCGYF7DL9JkkdU9-7FG-OzY'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
    internal-label: Journeys
  - id: 8881ff95-1653-5fea-82af-ce1549c0d99d
    internal-label: Content Management
source-git-commit: e48e778c3a62154297e2c4464f49c3010917d984
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 2%
---

# Modèles d’e-mail

Les modèles d&#39;e-mail dans [!DNL Adobe Marketo Optimizer] permettent aux spécialistes du contenu de créer des dispositions d&#39;e-mail réutilisables indépendamment, afin que les équipes marketing puissent réutiliser les conceptions sans les reconstruire à chaque fois.

>[!NOTE]
>
>Seuls les modèles d’e-mail sont actuellement pris en charge. Les modèles de page de destination ne sont actuellement pas disponibles.

Utilisez les [modules de contenu](./content-modules.md) lorsque vous [créez des modèles d’e-mail](./templates-create.md) pour assembler des dispositions à partir de sections préparées.

Lorsqu’un modèle est appliqué à un nouvel e-mail, le contenu est copié à ce stade. Les modifications apportées au modèle n’affectent pas les e-mails créés précédemment à partir de celui-ci.

>[!PREREQUISITES]
>
>L’utilisation de modèles nécessite les [autorisations](../start/permissions-reference.md) suivantes :
>
>* **[!UICONTROL Afficher les modèles B2B]** - Obligatoire pour afficher la liste et les détails des modèles.
>* **[!UICONTROL Gérer les modèles B2B]** - Requis pour créer, modifier et supprimer des modèles.

## Accès aux modèles d’e-mail {#access}

Accédez à **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Modèles]** dans le volet de navigation de gauche. La bibliothèque de modèles s’ouvre au format tableau, triée selon la dernière modification effectuée par défaut.

Basculez entre la vue Liste et la vue Grille (aperçu miniature) à l’aide des icônes situées en haut à droite de la bibliothèque.

### Rechercher et filtrer {#search-filter}

Utilisez la barre de recherche pour rechercher un modèle par nom. Cliquez sur un en-tête de colonne pour trier la liste. Cliquez sur **[!UICONTROL Filtres]** pour affiner la liste par balises ou pour afficher uniquement les modèles que vous avez créés.

Pour personnaliser les colonnes qui apparaissent dans le tableau, cliquez sur l’icône **[!UICONTROL Personnaliser le tableau]** et sélectionnez les colonnes à afficher.

## Organisation des modèles avec des dossiers {#folders}

Créez des dossiers pour regrouper les modèles par équipe, campagne, marque ou toute structure adaptée à votre workflow.

**Pour créer un dossier :**

1. Dans la bibliothèque de modèles, cliquez sur **[!UICONTROL Créer un dossier]**.
1. Saisissez un nom de dossier et cliquez sur **[!UICONTROL Confirmer]**.

**Pour déplacer un modèle dans un dossier :**

1. Cliquez sur l’icône **[!UICONTROL Plus]** ( ... ) en regard du modèle.
1. Sélectionnez **[!UICONTROL Déplacer vers le dossier]**.
1. Sélectionnez le dossier de destination et cliquez sur **[!UICONTROL Déplacer]**.

## Affichage des détails du modèle {#view-details}

Cliquez sur le nom d’un modèle pour ouvrir sa page de détails. À partir de là, vous pouvez consulter les propriétés telles que la date de création et l’historique des modifications, et voir quels e-mails de parcours utilisent le modèle dans l’onglet **[!UICONTROL Utilisé par]**.

## Gérer les modèles {#manage}

### Modification d’un modèle

Cliquez sur le nom d&#39;un modèle pour ouvrir la page de détails, puis cliquez sur **[!UICONTROL Modifier le modèle d&#39;e-mail]**. Vous pouvez également cliquer sur l’icône **[!UICONTROL Plus]** ( ... ) dans la liste des modèles et sélectionner **[!UICONTROL Modifier]**.

### Dupliquer un modèle

Cliquez sur l’icône **[!UICONTROL Plus]** ( ... ) à côté du modèle et sélectionnez **[!UICONTROL Dupliquer]**. La copie s’ouvre afin que vous puissiez la renommer et effectuer des réglages.

### Suppression d’un modèle

Cliquez sur l’icône **[!UICONTROL Plus]** ( ... ) à côté du modèle et sélectionnez **[!UICONTROL Supprimer]**. Confirmez la suppression lorsque vous y êtes invité.

>[!NOTE]
>
>La suppression d’un modèle n’affecte pas les e-mails de parcours qui ont déjà été créés à partir de celui-ci. Ces e-mails conservent leur propre copie indépendante du contenu.

### Suppression en bloc

Cochez la case en regard de chaque modèle à supprimer ou cochez la case en-tête pour sélectionner tous les modèles visibles. Cliquez sur **[!UICONTROL Supprimer]** dans la barre d’actions en bloc et confirmez.

## Utiliser un modèle dans un email {#use-in-journey}

Lors de la création d’un e-mail dans un parcours, la section **[!UICONTROL Sélectionner un modèle de conception]** vous permet de choisir parmi des modèles enregistrés ou des exemples de modèles. Cliquez sur une miniature de modèle pour la prévisualiser, puis cliquez sur **[!UICONTROL Utiliser ce modèle]** pour l&#39;appliquer. Pour plus d’informations sur l’utilisation de modèles dans votre workflow de création d’e-mail, voir [Création de contenu d’e-mail](./email-authoring.md#templates).
