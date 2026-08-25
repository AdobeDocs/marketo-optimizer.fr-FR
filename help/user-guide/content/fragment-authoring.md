---
title: Création de fragments
description: 'Créez des fragments de contenu réutilisables avec des outils de conception visuelle : ajoutez la structure, les ressources, la personnalisation, le contenu conditionnel et le suivi des URL liées pour les e-mails et les modèles dans Marketo Optimizer.'
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 3%

---

# Création de fragments

Après avoir [créé un fragment](./fragments.md#create-fragments), utilisez l’espace de conception visuelle pour créer les composants de structure et de contenu dans votre fragment.

## Ajouter la structure et le contenu {#design-fragment}

{{$include /help/_includes/content-design-components-prime.md}}

## Ajout de ressources {#add-assets}

Dans l’espace de conception visuelle, sélectionnez l’icône __ ( ![icône Assets](../assets/do-not-localize/icon-assets-me.svg) ) dans la barre de navigation de gauche pour parcourir et sélectionner des ressources d’image dans la bibliothèque de ressources d’[!DNL Marketo Optimizer].

Pour connaître les étapes de sélection, de remplacement ou de chargement de ressources d’image, consultez [Utilisation de ressources pour la création de contenu](./digital-asset-management.md#assets-authoring).

## Parcourir les calques, paramètres et styles {#navigate-layers-settings-styles}

{{$include /help/_includes/content-design-navigation.md}}

## Personnaliser le contenu {#personalize-content}

[!DNL Marketo Optimizer] utilise la syntaxe Handlebars pour la personnalisation. Les jetons sont remplacés au moment de l’envoi par des valeurs provenant des données de profil de chaque destinataire.

_Pour ajouter de la personnalisation :_

1. Sélectionnez le composant de texte et cliquez sur l’icône _Ajouter une personnalisation_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) dans la barre d’outils.
1. Dans la boîte de dialogue de personnalisation, parcourez l’arborescence du schéma à gauche et sélectionnez un attribut de profil. L’éditeur insère l’expression Handlebars correspondante, par exemple, `{{profile.firstName}}`.
1. Ajoutez une valeur de secours pour gérer les données manquantes, si nécessaire, par exemple, `{{profile.firstName | default: "there"}}`.
1. Cliquez sur **[!UICONTROL Confirmer]** ou **[!UICONTROL Insérer]**. L’expression apparaît en ligne dans le champ.

Pour plus d’informations sur les outils et la syntaxe de l’éditeur d’expression, voir [Éditeur ](./personalization-expressions.md).

## Modifier le tracking des URL liées {#edit-linked-url-tracking}

{{$include /help/_includes/content-design-links.md}}
