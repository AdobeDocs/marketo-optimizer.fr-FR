---
title: Configuration de Forms
description: Espace réservé
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 30%

---

# Configurations de Forms

Avant que les marketeurs puissent créer et publier des formulaires à utiliser dans leurs pages de destination, un administrateur de produit doit créer un ou plusieurs paramètres prédéfinis dédiés. Chaque paramètre prédéfini définit le point d’entrée de connexion utilisé pour envoyer les données d’envoi du formulaire et le jeu de données utilisé pour stocker les données capturées.

Lorsque des données arrivent sur le point d’entrée de diffusion en continu, elles sont liées aux informations du jeu de données. À l’aide des connexions source/cible générées et du flux source, les données sont ensuite intégrées au jeu de données.

>[!BEGINSHADEBOX]

## Conditions préalables

Pour utiliser les formulaires web, vous devez disposer d’une ou de plusieurs connexions en continu d’API _**HTTP**_ définies dans Adobe Experience Platform. Assurez-vous que chaque connexion que vous souhaitez utiliser répond aux exigences suivantes :

* Le type de données doit être défini sur XDM (et non sur Données brutes).
* L&#39;authentification doit être désactivée (connexion non authentifiée)

Pour plus d’informations sur la création de connexions source par flux, consultez la documentation d’[__](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/streaming/http).

<!-- 
permissions coming in GA

Forms channel configuration in Journey Optimizer B2B Edition requires the following [permissions](../start/user-management.md#b2b-product-permissions):

* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL View Forms Presets]_ - Required to view forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Manage Forms Presets]_ - Required to create, update, and delete forms preset configurations.
* _[!UICONTROL B2B Channel Configurations]_ > _[!UICONTROL Publish Forms Presets]_ - Required to publish forms preset configurations.
-->

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
