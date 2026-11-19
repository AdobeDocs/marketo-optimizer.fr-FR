---
title: Modules de contenu
description: Découvrez comment ajouter et personnaliser des modules pour les e-mails, les pages de destination, les fragments visuels et les modèles d’e-mail. Utilisez des mises en page préparées pour créer des conceptions de contenu cohérentes.
feature: Content Design Tools
role: User
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
source-git-commit: 73e54767086a103c11dce78a0295ad435c07f2c0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 1%
---
# Modules de contenu

Utilisez des modules dans [!DNL Adobe Marketo Optimizer] pour assembler du contenu à partir de dispositions préparées. Chaque module combine [structure](./structure-components.md) et [composants de contenu](./content-components.md) avec du contenu par défaut que vous remplacez par votre propre texte, vos propres images et vos propres liens.

Contrairement aux composants de contenu individuels, les modules fournissent des sections complètes telles que les en-têtes, les bannières, les cartes et les pieds de page. Ajoutez un module à la zone de travail, puis personnalisez ses composants au lieu de créer chaque section à partir d’un espace vide.

Les modules sont différents des [fragments visuels](./fragments.md). Un module fait partie du contenu que vous êtes en train de concevoir. Un fragment visuel est une ressource de contenu enregistrée que vous pouvez réutiliser dans les e-mails et les modèles d’e-mail.

## Onglet Modules

Utilisez l’onglet **[!UICONTROL Modules]** dans l’espace de conception visuelle pour l’un des types de contenu suivants :

* E-mail - Voir [_Création de contenu d’e-mail_](./email-authoring.md).
* Page de destination : consultez la section [_Conception de page de destination_](./landing-page-design.md).
* Fragment visuel : consultez la section [_Création de fragments_](./fragment-authoring.md).
* Modèle d’e-mail - Voir [_Créer des modèles d’e-mail_](./templates-create.md#build-new).

![Catégories de modules affichées à côté de la zone de travail de conception visuelle](../../assets/modules-left-panel.png){width="600" zoomable="yes"}

## Catégories de module

Développez une catégorie pour choisir une mise en page. Ces dispositions fournissent différentes dispositions du contenu de la section, telles qu’une, deux ou trois colonnes.

| Catégorie | Utilisation |
| --- | --- |
| [!UICONTROL En-têtes] | Présentez votre contenu avec un logo, des liens de navigation et un texte d’introduction. |
| [!UICONTROL Bannière] | Mettez en surbrillance une annonce ou une promotion avec une section de bannière. |
| [!UICONTROL Témoignages] | Présentez les devis des clients dans une section stylisée. |
| [!UICONTROL Cartes] | Organisez les produits, les articles ou les autres éléments de contenu dans une grille. |
| [!UICONTROL Équipes] | Présentez les membres de l’équipe, les auteurs ou les conférenciers avec des photos, des noms et des rôles. |
| [!UICONTROL Pieds de page] | Complétez votre contenu avec des liens de navigation, des liens de réseaux sociaux et du texte juridique. |

## Ajout et personnalisation de modules

Commencez par un module correspondant à la section que vous souhaitez créer, puis adaptez son contenu et son style. Remplacez les liens et le texte par défaut par le contenu approprié à votre canal.

>[!NOTE]
>
>Pour les e-mails marketing, incluez un lien d’exclusion et [vérifiez les alertes par e-mail](../marketing/email-channel.md#alerts) avant de publier l’e-mail.

1. Ouvrez votre e-mail, page de destination, fragment visuel ou modèle d’e-mail dans l’espace de conception visuelle.

   À gauche de la zone de travail, l’onglet **[!UICONTROL Modules]** s’affiche par défaut.

1. Pour passer en revue les dispositions disponibles, développez une catégorie.

   Vous pouvez également utiliser le champ de recherche pour rechercher un module par nom.

1. Faites glisser un module sur la zone de travail.

   ![La liste des modules est filtrée par recherche et un module est glissé sur la zone de travail.](../../assets/modules-search-drag.png){width="600" zoomable="yes"}

1. Examinez les éléments dans le module .

   Chaque module comprend du contenu par défaut que vous pouvez modifier. Cliquez sur l’icône _Arborescence de navigation_ ( ![Icône d’arborescence de navigation](../assets/do-not-localize/icon-navigation-tree.svg) ) à gauche de la zone de travail pour afficher la structure et les éléments dans le module.

   ![L&#39;arborescence de navigation affiche la structure et les éléments du module sélectionné.](./assets/modules-navigation-tree.png){width="600" zoomable="yes"}

1. Sélectionnez un élément dans le module pour le personnaliser.

   Vous pouvez remplacer le texte par défaut, choisir des images dans vos ressources et mettre à jour les liens de votre contenu.

   Utilisez les onglets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** pour ajuster le composant sélectionné.

   ![Composant Texte sélectionné dans le module avec les options Styles affichées](../../assets/modules-select-element-styles.png){width="600" zoomable="yes"}

1. Pour ajouter un autre élément, sélectionnez l’onglet **[!UICONTROL Composants]** et faites glisser un [composant de contenu](./content-components.md) dans le module.

   Si vous ajoutez un composant à la structure du module, il hérite du style du module par défaut. Ajustez ses styles selon les besoins.

   ![Composant de texte déplacé vers la structure du module avec le texte d’espace réservé formaté affiché](./assets/modules-select-element-add-component.png){width="800" zoomable="yes"}

1. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer vos modifications.

>[!NOTE]
>
>Lorsqu’un thème de marque est appliqué au contenu d’e-mail, les modules héritent de ses styles. Choisissez le mode de style lorsque vous [concevez entièrement un e-mail](./email-authoring.md#design-from-scratch).

## Réutiliser le contenu de module personnalisé

Pour créer du contenu de module réutilisable, [créez un fragment visuel](./fragments.md#create-fragments) et ajoutez et personnalisez des modules dans l’espace de conception de fragment. Enregistrez et publiez le fragment pour qu’il puisse être utilisé dans les e-mails et les modèles d’e-mail.

Ensuite [insérez le fragment](./fragments.md#add-to-content) dans d&#39;autres e-mails ou modèles d&#39;e-mail.
