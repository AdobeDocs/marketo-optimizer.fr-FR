---
title: Gouvernance du contenu pour les modèles
description: Utilisez les paramètres de gouvernance dans Marketo Optimizer pour verrouiller le contenu dans les modèles d’e-mail au niveau de la structure ou du composant, en contrôlant ce que les auteurs d’e-mail peuvent modifier.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---


# Gouvernance du contenu pour les modèles

Le verrouillage de contenu permet aux auteurs de modèles de définir des règles de gouvernance qui limitent les parties d&#39;un modèle d&#39;e-mail qui peuvent être modifiées lorsque le modèle est utilisé dans un e-mail. Cela permet aux équipes de marque et de conformité de protéger les éléments de conception clés, tels que les en-têtes, les logos et le contenu légal, tout en permettant aux équipes marketing de personnaliser le message au sein de la structure approuvée.

>[!NOTE]
>
>Le verrouillage de contenu est une fonctionnalité de gouvernance au niveau de l’éditeur. Il contrôle ce que les auteurs et autrices peuvent modifier dans l’espace de conception d’e-mail, mais n’empêche pas les modifications apportées par l’API.

Seuls les utilisateurs disposant de l’autorisation **[!UICONTROL Gérer les modèles de contenu]** peuvent configurer les paramètres de gouvernance.

## Activer la gouvernance {#enable}

>[!NOTE]
>
>Dans cette version de Beta, seuls les modèles d’e-mail sont pris en charge.

1. Ouvrez le modèle dans l’espace de conception.
1. Dans la zone de travail, cliquez sur le composant **[!UICONTROL Corps]** pour le sélectionner.
1. Sélectionnez l’icône _Paramètres_ pour le panneau de droite,
1. Activez **[!UICONTROL Gouvernance]**.
1. Pour **[!UICONTROL Mode]**, sélectionnez le type de gouvernance à appliquer :

   | Mode | Description |
   | ---- | ----------- |
   | **[!UICONTROL Verrouillage de contenu]** | Verrouiller sélectivement des structures ou des composants spécifiques. Les zones déverrouillées restent modifiables par les auteurs. |
   | **[!UICONTROL Lecture seule]** | Verrouillez le modèle entier. Les auteurs peuvent l’appliquer à un e-mail, mais ne peuvent pas modifier une partie de son contenu. |

1. Si vous avez sélectionné le mode de verrouillage Contenu , vous pouvez définir plus en détail la manière dont les utilisateurs peuvent interagir avec le modèle.

   Activez l’option Activer l’ajout de contenu et choisissez l’une des options suivantes :

   * **[!UICONTROL Autoriser l’ajout de structure et de contenu]** - Les utilisateurs et utilisatrices peuvent ajouter des structures entre des structures existantes et ajouter des composants de contenu ou des fragments dans des structures modifiables.

   * **[!UICONTROL Autoriser l’ajout de contenu uniquement]** - Les utilisateurs et utilisatrices peuvent ajouter des composants de contenu ou des fragments dans des structures modifiables, mais ne peuvent pas ajouter ni dupliquer de structures.

### Verrouiller une structure {#lock-structure}

1. Dans la zone de travail, sélectionnez la structure (mise en page des colonnes) à protéger.
1. Dans le rail de droite, activez le bouton (bascule) **[!UICONTROL Verrouiller la structure]**.

Tout le contenu imbriqué dans une structure verrouillée est automatiquement verrouillé. Pour permettre à un composant spécifique au sein d’une structure verrouillée de rester modifiable, sélectionnez le composant et activez **[!UICONTROL modifiable]** dans le rail de droite.

Par défaut, les auteurs ne peuvent pas supprimer une structure verrouillée. Pour autoriser la suppression, activez l’option **[!UICONTROL Autoriser la suppression]** dans le rail de droite.

### Verrouiller un composant {#lock-component}

Dans une structure modifiable, vous pouvez verrouiller des composants de contenu individuels.

1. Sélectionnez le composant sur la zone de travail.
1. Dans le rail de droite, activez le bouton (bascule) **[!UICONTROL Verrouiller le contenu]** et choisissez le type de verrouillage :

   | Type de verrouillage | Description |
   | --------- | ----------- |
   | **[!UICONTROL Verrouillé]** | Empêche les modifications de contenu et de style. Les auteurs ne peuvent pas modifier le texte ni modifier l’aspect du composant. |
   | **[!UICONTROL Contenu modifiable uniquement]** | Permet aux créateurs de modifier du texte et du contenu, mais empêche les modifications de style telles que les couleurs, les polices et l’espacement. |
   | **[!UICONTROL Modifiable]** | Permet des modifications complètes même dans une structure verrouillée. |

Par défaut, les auteurs ne peuvent pas supprimer un composant verrouillé. Pour autoriser la suppression, activez l’option **[!UICONTROL Autoriser la suppression]** dans le rail de droite.

### Autoriser les ajouts de contenu {#allow-additions}

Lors de l’utilisation du mode **[!UICONTROL Verrouillage de contenu]**, vous pouvez permettre aux créateurs et créatrices d’ajouter du nouveau contenu au modèle tout en conservant les éléments verrouillés protégés :

1. Activez **[!UICONTROL Autoriser l’ajout de contenu]**.
1. Choisissez si les auteurs peuvent ajouter à la fois des structures et des composants de contenu, ou uniquement des composants de contenu.

## Identification des éléments verrouillés {#identify}

L’**[!UICONTROL arborescence de navigation]** dans le rail de gauche affiche des icônes de verrouillage et de crayon pour aider les auteurs à identifier rapidement ce qu’ils peuvent ou ne peuvent pas modifier :

* Une **icône de verrouillage** indique un élément verrouillé.
* Une **icône en forme de crayon** indique un élément modifiable.

Pour améliorer davantage la visibilité, activez le bouton (bascule) **[!UICONTROL Mettre les zones modifiables en surbrillance]** pour distinguer visuellement les zones modifiables des zones verrouillées dans la zone de travail.

## Considérations

Les paramètres de gouvernance sont enregistrés avec le modèle. Tout e-mail créé à partir d’un modèle régi hérite de sa configuration de verrouillage au moment de son application. La mise à jour des paramètres de gouvernance sur un modèle n’affecte pas les e-mails créés précédemment à partir de celui-ci.
