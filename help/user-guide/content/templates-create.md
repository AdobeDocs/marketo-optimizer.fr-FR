---
title: Créer des modèles d’e-mail
description: 'Découvrez comment créer des modèles d’e-mail dans Marketo Optimizer : créez un nouveau modèle, enregistrez un e-mail à partir d’un parcours en tant que modèle ou convertissez une image de conception en modèle d’e-mail.'
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 1%

---


# Créer des modèles d’e-mail

Vous pouvez créer un modèle d’e-mail dans [!DNL Adobe Marketo Optimizer] de trois façons :

* **Créer un modèle** — Créez un modèle dans la bibliothèque de modèles à l&#39;aide de l&#39;espace visuel de conception d&#39;e-mail.
* **Enregistrer à partir d’un e-mail de parcours** — Enregistrez un e-mail que vous avez créé dans un parcours en tant que modèle réutilisable.
* **Convertir une image** — Chargez une image de conception et utilisez l’IA générative pour la convertir en modèle d’e-mail modifiable.

## Créer un nouveau modèle {#build-new}

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion de contenu]** et sélectionnez **[!UICONTROL Modèles]**.
1. Cliquez sur **[!UICONTROL Créer un modèle]**.
1. Saisissez un **[!UICONTROL Nom du modèle]** et un **[!UICONTROL Description]** facultatif.
1. Définissez le **[!UICONTROL Canal]** (type) du modèle.

   >[!NOTE]
   >
   >Dans cette version de Beta, seuls les modèles d’e-mail sont pris en charge.

   <!-- 1. Optionally add **[!UICONTROL Tags]** to categorize the template. -->

1. Cliquez sur **[!UICONTROL Créer]** pour ouvrir l’espace de conception d’e-mail.

1. Cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]** pour accéder à l’espace de conception de contenu.

   Voir [Création d’e-mails](email-authoring.md) pour plus d’informations sur la conception de contenu.

1. Vous pouvez éventuellement activer **[!UICONTROL Gouvernance]** et configurer [verrouillage de contenu](template-content-governance.md) pour limiter les parties du modèle que les auteurs et autrices peuvent modifier lors de l’application du modèle.

1. Cliquez sur **[!UICONTROL Enregistrer]**

## Enregistrer un e-mail en tant que modèle {#save-as-template}

Lorsque vous ouvrez le contenu de l’e-mail que vous souhaitez réutiliser, enregistrez-le directement dans la bibliothèque de modèles à partir de la page de contenu de l’e-mail.

1. Cliquez sur **[!UICONTROL Modèle de contenu]** en haut de la page.
1. Sélectionnez **[!UICONTROL Enregistrer comme modèle de contenu]**.
1. Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]** facultatif.
1. Ajoutez éventuellement des **[!UICONTROL Balises]**.
1. Cliquez sur **[!UICONTROL Créer]**.

L’e-mail de parcours d’origine n’est pas affecté. Le modèle enregistré est disponible dans la bibliothèque de modèles pour tous les utilisateurs dans le sandbox. Vous pouvez mettre à jour le modèle créé pour optimiser la réutilisation :

* Modifiez le texte et ajoutez des jetons [personnalisation](email-authoring.md#personalize-content).
* Mettez à jour ou remplacez des images et ajoutez des liens.
* Configurez [verrouillage de contenu](template-content-governance.md).

## Convertir une image en modèle {#image-to-template}

[!DNL Adobe Marketo Optimizer] pouvez convertir une image statique, telle qu’une maquette de Figma ou de Photoshop, en modèle d’e-mail modifiable à l’aide de l’IA générative. Cela élimine la nécessité de reconstruire manuellement les dispositions à partir des fichiers de conception et est idéal pour migrer les conceptions d’e-mail existantes à partir d’autres plateformes. Cette fonctionnalité est disponible uniquement pour les modèles de contenu d’e-mail.

>[!BEGINSHADEBOX]

### Conditions préalables

Avant de commencer :

* Votre entreprise doit avoir signé l’addendum Generative AI avec Adobe.
* Vous devez disposer de l’autorisation **[!UICONTROL Générer du contenu]** en plus de l’autorisation **[!UICONTROL Gérer les modèles de contenu]**.
* Le fichier image doit répondre aux spécifications suivantes :
  * Format : JPEG (.jpg, .jpeg) ou PNG (.png)
  * Taille de fichier maximale : 10 Mo
  * Largeur recommandée : 600 à 800 pixels
  * Image claire et de haute qualité avec texte lisible et éléments visuels distincts

>[!IMPORTANT]
>
>L’image ne doit pas contenir d’informations d’identification personnelle (PII) ni de données sensibles.

>[!ENDSHADEBOX]

### Création du modèle

1. Dans le volet de navigation de gauche, développez **[!UICONTROL Gestion de contenu]** et sélectionnez **[!UICONTROL Modèles]**.
1. Cliquez sur **[!UICONTROL Créer un modèle]**.
1. Saisissez un **[!UICONTROL Nom du modèle]** et un **[!UICONTROL Description]** facultatif.
1. Définissez le **[!UICONTROL Canal]** sur E-mail.

   <!--  Optionally add **[!UICONTROL Tags]** to categorize the template. -->

1. Cliquez sur **[!UICONTROL Créer]**.

### Générer le contenu du modèle

1. Dans la section **[!UICONTROL Convertir l’image en modèle]** :

   * Sélectionnez éventuellement un **[!UICONTROL thème de marque]** pour appliquer les couleurs, les polices et l’espacement de votre marque à la sortie générée.
   * Cochez la case accusé de réception pour confirmer que votre image ne contient aucune information d’identification personnelle (PII) ni d’autres données sensibles.
   * Cliquez sur **[!UICONTROL Télécharger l’image]** et sélectionnez votre fichier image.

   >[!CAUTION]
   >
   >Le chargement d’une image supprime tout contenu présent dans l’e-mail et le remplace par le modèle généré.

1. Si vous y êtes invité, consultez et acceptez les instructions d’utilisation d’Adobe Generative AI.

1. Cliquez sur **[!UICONTROL Ouvrir]** pour lancer le processus de conversion.

   La conversion se termine généralement en cinq minutes environ. Les images complexes ou volumineuses peuvent prendre jusqu’à dix minutes. La conversion s’exécute en arrière-plan : vous pouvez quitter la page et le brouillon de modèle est enregistré automatiquement une fois la conversion terminée.

1. Actualisez la page pour afficher le modèle terminé.

   >[!NOTE]
   >
   >Le résultat ne s’affiche pas automatiquement. Actualisez la page ou revenez à la bibliothèque de modèles pour afficher le modèle terminé.

1. Vous pouvez éventuellement utiliser la section **[!UICONTROL Commentaires du convertisseur d’images en modèles]** pour partager des suggestions avec Adobe.

1. Cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]** pour ouvrir le modèle converti dans l’espace de conception d’e-mail afin de le modifier.

1. Cliquez sur **[!UICONTROL Enregistrer]**

### Modification du contenu converti

Le contenu du modèle converti s’ouvre dans l’espace de conception sous la forme d’un modèle d’e-mail entièrement modifiable. Utilisez les outils de conception de contenu standard pour :

* Modifiez le texte et ajoutez des jetons [personnalisation](email-authoring.md#personalize-content).
* Mettez à jour ou remplacez des images et ajoutez des liens.
* Ajustez les couleurs, les polices et l’espacement.
* Ajouter, supprimer ou réorganiser des composants de contenu.
* Activez la gouvernance et configurez le [verrouillage de contenu](template-content-governance.md).

>[!IMPORTANT]
>
>L’IA générative produit une HTML statique basée sur l’image visuelle. Vérifiez tout le texte pour en assurer la précision et ajoutez manuellement la personnalisation, le contenu dynamique et le suivi après la conversion.

Le modèle converti est automatiquement enregistré dans la bibliothèque de modèles une fois la conversion terminée.

### Conseils pour obtenir de meilleurs résultats

Suivez les instructions suivantes pour obtenir les meilleurs résultats de la conversion d’une image en modèle :

**Avant la conversion :**

* Utilisez la version la plus haute résolution de votre fichier de conception.
* Concevez avec des largeurs d’e-mail standard (600 à 800 pixels) et incluez la disposition complète (de l’en-tête au pied de page) dans une seule image.
* Assurez-vous que le contraste entre le texte et l’arrière-plan est suffisant et utilisez des tailles de police lisibles.

**Concevoir pour une conversion précise :**

* Utilisez des dispositions simples et bien structurées, avec une séparation nette entre les sections.
* Suivez les modèles d’e-mail standard (en-tête, corps, appels à l’action, pied de page) plutôt que des conceptions à plusieurs couches complexes.
* Gardez les éléments visuels distincts afin que l’IA puisse identifier correctement les limites structurelles.

**Après la conversion :**

* Testez le rendu sur les clients de messagerie et les appareils avant d’utiliser le modèle dans un parcours.
* Vérifiez l’alignement avec les couleurs, les polices et les directives de style de la marque.
* Examiner et améliorer l’accessibilité, y compris le texte secondaire de l’image.
