---
title: Configuration de Forms
description: Espace réservé
TQID: 'https://experienceleague.adobe.com/7X5-67hfrjRjWbGjq9duLu7mVjgfCs7tpAQLV8u6YKE'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: a659ad61-de21-559d-a901-02e2fb329ff5
    internal-label: Administration
  - id: d4203578-d294-5145-b397-f26f4488a904
    internal-label: Channels
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: f65df8d5e83eca29ffaaabf51e7c80ed223d175a
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 27%
---
# Configurations de Forms

Avant que les marketeurs puissent créer et publier des formulaires à utiliser dans leurs pages de destination, un administrateur de produit doit créer un ou plusieurs paramètres prédéfinis dédiés. Chaque paramètre prédéfini définit le point d’entrée de connexion utilisé pour envoyer les données d’envoi du formulaire et le jeu de données utilisé pour stocker les données capturées.

Lorsque des données arrivent sur le point d’entrée de diffusion en continu, elles sont liées aux informations du jeu de données. À l’aide des connexions source/cible générées et du flux source, les données sont ensuite intégrées au jeu de données.

>[!BEGINSHADEBOX]

## Conditions préalables

Pour utiliser les formulaires web, vous devez disposer d’une ou de plusieurs connexions en continu d’API _&#x200B;**HTTP**&#x200B;_ définies dans Adobe Experience Platform. Assurez-vous que chaque connexion que vous souhaitez utiliser répond aux exigences suivantes :

* Le type de données doit être défini sur XDM (et non sur Données brutes).
* L&#39;authentification doit être désactivée (connexion non authentifiée)

Pour plus d’informations sur la création de connexions source par flux, consultez la documentation d’[__](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

La configuration du canal Forms dans [!DNL Marketo Optimizer] nécessite les [autorisations](../start/permissions-reference.md) suivantes :

* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Afficher le paramètre prédéfini Forms B2B]_ - Obligatoire pour afficher les configurations de paramètre prédéfini de formulaire.
* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Gérer les paramètres prédéfinis de Forms B2B]_ - Requis pour créer, modifier et supprimer des configurations de paramètres prédéfinis de formulaire.
* _[!UICONTROL Configurations de canal B2B]_ > _[!UICONTROL Publication d’un paramètre prédéfini Forms B2B]_ - Obligatoire pour publier les configurations de paramètre prédéfini de formulaire.

>[!ENDSHADEBOX]

## Instructions de configuration relatives aux paramètres prédéfinis de formulaire

Lors de la création d’un paramètre prédéfini :

* Vous pouvez configurer plusieurs préréglages à l’aide de différentes combinaisons de jeux de données et de connexions en streaming.

* Vous pouvez réutiliser le même jeu de données ou la même connexion en continu sur plusieurs paramètres prédéfinis.

* Chaque connexion en continu génère automatiquement des ressources, telles que :

  * _Connexion Source_ - emplacement d’où proviennent les données.
  * _Connexion cible_ - emplacement de stockage ou d’utilisation des données.
  * _Flux Source_ - pipeline qui déplace les données de la connexion source vers Experience Platform. Il gère le mappage, la transformation et la validation.

## Créer un paramètre prédéfini de formulaire {#create-preset}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_connection"
>title="Sélectionner le point d’entrée à utiliser"
>abstract="Définissez le point d&#39;entrée de streaming où les données sont envoyées lors de l’envoi du formulaire."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="Créer une connexion de streaming d’API HTTP"

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_lp_form_dataset"
>title="Sélectionner un jeu de données"
>abstract="Définissez un jeu de données dans lequel les réponses au formulaire sont stockées et reflétées. Saisissez le nom d’un jeu de données pour le rechercher ou le sélectionner directement dans la liste."

1. Dans le volet de navigation de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**.

1. Sous _[!UICONTROL Paramètres de formulaire]_ dans le panneau de navigation, sélectionnez **[!UICONTROL Paramètres prédéfinis de formulaire]**.

   <!-- ![Access the form configurations](./assets/config-channels-forms.png){width="800" zoomable="yes"} -->

1. Cliquez sur **[!UICONTROL Créer un paramètre prédéfini de formulaire]**.

1. Saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif) pour la configuration.

   >[!NOTE]
   >
   >Les noms doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d’union `-`.

1. Sélectionnez la **[!UICONTROL Connexion en continu]**.

   Cette connexion est le point d’entrée de diffusion en continu utilisé pour envoyer les données lorsqu’une visionneuse web envoie un formulaire. Si la connexion en continu nécessaire n’apparaît pas dans la liste, vérifiez que les exigences sont remplies.

1. Cliquez sur l’icône _Sélectionner un jeu de données_ ( ![Icône Sélectionner un jeu de données](../assets/do-not-localize/icon-select-data.svg) ) pour lier un jeu de données au formulaire.

   Le jeu de données est l’endroit où les réponses du formulaire sont stockées et reflétées. Vous pouvez saisir une chaîne de texte pour rechercher un jeu de données spécifique ou le sélectionner dans la liste.

   <!-- ![Select datasets dialog](./assets/config-channel-forms-select-datasets.png){width="500" zoomable="yes"} -->

   >[!NOTE]
   >
   >Actuellement, seuls les jeux de données [Adobe Experience Platform activés et non activés pour Profil](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/overview) sont disponibles pour sélection. Vous pouvez sélectionner un jeu de données à la fois. Les jeux de données système ne peuvent pas être utilisés pour enregistrer les données de formulaire.

   Cochez la case du jeu de données et cliquez sur **[!UICONTROL Sélectionner]**.

1. Cliquez sur **[!UICONTROL Enregistrer comme brouillon]**.

## Publication d’un paramètre prédéfini de formulaire

1. Cliquez sur le nom du paramètre prédéfini de formulaire pour ouvrir la page de configuration.

   Si nécessaire, vous pouvez apporter des ajustements au brouillon.

1. Cliquez sur **[!UICONTROL Publier]**.

   Lorsque le paramètre prédéfini de formulaire est répertorié avec un statut _Publié_, il est disponible pour être utilisé lors de la création du formulaire.
