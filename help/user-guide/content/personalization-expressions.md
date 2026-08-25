---
title: Éditeur Personalization
description: Découvrez comment utiliser l’éditeur de personnalisation dans Marketo Optimizer pour sélectionner, organiser, personnaliser et valider les jetons d’attribut de profil dans les e-mails, les messages WhatsApp, les pages de destination et les champs d’URL.
feature: Content Design Tools
role: User
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 55%

---

# Éditeur de personnalisation

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_personalization_editor"
>title="À propos de l’éditeur de personnalisation"
>abstract="L’éditeur de personnalisation vous permet de sélectionner, organiser, personnaliser et valider des attributs de profil pour créer du contenu personnalisé."

L’éditeur de personnalisation est l’élément central de la personnalisation dans [!DNL Marketo Optimizer]. Utilisez-le là où vous avez besoin de contenu dynamique (dans les e-mails, les messages WhatsApp, les landing pages et les champs d’URL).

Dans l’interface de l’éditeur de personnalisation, vous pouvez sélectionner, organiser, personnaliser et valider des attributs de profil afin de créer du contenu personnalisé.

![Personnalisation de l&#39;éditeur d&#39;expression](./assets/personalization-editor.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Seuls les attributs de profil sont disponibles dans l’éditeur de personnalisation dans cette version de Beta. La personnalisation au niveau du compte et les données d’objet personnalisé ne sont pas disponibles. Voir [Limites actuelles](../marketing/email-channel.md#limitations).

Vous pouvez ajouter de la personnalisation dans n’importe quel champ à l’aide de l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ). Développez les sections suivantes pour plus d’informations.

+++E-mails et messages WhatsApp

Dans les messages [e-mails](./email-authoring.md#personalize-content) et [WhatsApp](./whatsapp-authoring.md#personalize-message-content), la personnalisation peut être ajoutée à différents emplacements, tels que le champ **[!UICONTROL Objet]** dans un e-mail ou les paramètres dynamiques dans un modèle WhatsApp approuvé.

Il peut également être ajouté à d’autres sections de votre contenu, notamment au corps du texte de l’e-mail, aux pré-titres et aux URL des boutons.

+++

+++Espace de conception de contenu

Lors de la modification du contenu visuel, vous pouvez ajouter une personnalisation dans la plupart des éléments de texte à l’aide de l’icône dans la barre d’outils contextuelle.

<!-- ![](assets/perso_insert.png) -->

+++

+++URL

[!DNL Marketo Optimizer] vous permet également de personnaliser les **URL** dans vos messages. Les URL personnalisées orientent les destinataires vers des pages spécifiques dʼun site web ou vers un microsite personnalisé, en fonction des attributs du profil.

<!-- ![](assets/perso-url.png){width="50%"} -->

>[!NOTE]
>
>La personnalisation des URL est disponible pour les types de liens suivants : **Lien externe**, **Lien de désabonnement** et **Opt-out**.

+++

+++Configuration du canal e-mail

Lors de la création d’une [configuration du canal e-mail](../admin/email-channel-configuration.md), vous pouvez définir des valeurs personnalisées pour les sous-domaines, les en-têtes et les paramètres de tracking d’URL.

+++

## Ajouter une personnalisation {#add}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_perso_editor_autocomplete"
>title="Remplissage automatique"
>abstract="Activer cette option permet au système de suggérer et de remplir automatiquement le code au fur et à mesure que vous le tapez. Cette fonctionnalité est disponible uniquement pour les formats HTML et Texte et prend en charge les attributs de profil. Si vous désactivez cette option, l’éditeur fournit une saisie automatique du code HTML natif à la place."

C’est dans l’espace de travail central que vous créez votre syntaxe de personnalisation. Pour utiliser un attribut afin de personnaliser votre message, localisez-le dans le volet de navigation de gauche, puis cliquez sur le bouton `+` pour l’ajouter à l’expression.

<!-- ![](assets/personalization-add-attribute.png) -->

Le menu à trois points en regard de l’icône `+` vous permet d’obtenir plus de détails sur chaque attribut et d’ajouter ceux que vous utilisez le plus souvent à vos favoris. Vous pouvez accéder aux attributs ajoutés aux favoris à partir du menu **[!UICONTROL Favoris]** dans le volet de navigation.

>[!NOTE]
>
>Par défaut, le volet des attributs affiche uniquement les attributs renseignés. Pour afficher tous les attributs, sélectionnez le bouton **[!UICONTROL Paramètres]** dans le volet Attributs et désactivez l’option **[!UICONTROL Afficher uniquement les attributs renseignés]**.

De plus, vous pouvez définir un texte de remplacement par défaut qui s’affichera si un attribut de profil de type chaîne est vide. Pour ce faire, cliquez sur le bouton des points de suspension en regard de l’attribut et sélectionnez **[!UICONTROL Insérer avec un texte de remplacement]**. Rédigez le texte à afficher par défaut si la valeur de l’attribut est vide pour un profil, puis cliquez sur **[!UICONTROL Ajouter]**.

<!-- ![](assets/attribute-details.png) -->

Par exemple, vous pouvez saluer chaque destinataire par prénom en utilisant `{{profile.firstName}}` avec un secours lorsque la valeur est manquante : `{{profile.firstName | default: "there"}}`.

## Options de modification d’expressions {#options}

L’espace de travail central fournit divers outils pour vous aider à écrire votre expression de personnalisation.

<!-- ![](assets/perso-workspace.png) -->

Les options disponibles sont les suivantes :

1. **[!UICONTROL Rechercher]**/**[!UICONTROL Rechercher et remplacer]** : effectuez une recherche dans votre expression et remplacez automatiquement des parties de code.
1. **[!UICONTROL Annuler]** / **[!UICONTROL Rétablir]** : annulez ou rétablissez la dernière opération.
1. **[!UICONTROL Saisie automatique]** : suggère et remplit automatiquement le code au fur et à mesure que vous le tapez. Cette fonctionnalité est disponible uniquement pour les formats HTML et Texte et prend en charge les attributs de profil. Si vous désactivez cette option, l’éditeur fournit une saisie automatique du code HTML natif à la place.

   <!-- ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"} -->

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Texte]** : identifiez le format de votre code. Cela permet au système d’adapter la fonctionnalité de validation et de saisie automatique à la langue sélectionnée.
1. **[!UICONTROL Valider]** : vérifiez la syntaxe de votre expression.
1. **[!UICONTROL Taille de police]** : ajuste la taille de la police du contenu dans l’éditeur pour une meilleure lisibilité.
1. **[!UICONTROL Retour à la ligne]** : active ou désactive le retour à la ligne, ce qui permet aux expressions longues d’être affichées sur une seule ligne ou renvoyées à la ligne dans l’éditeur. Les options incluent :
   * **Désactivé** (par défaut) : aucun retour à la ligne. Les lignes longues s’étendent au-delà de la vue de l’éditeur et nécessitent un défilement horizontal.
   * **Activé** : adapte le retour à la ligne à la largeur de l’éditeur.
   * **Colonne renvoyée à la ligne** - Renvoie les lignes à la ligne lorsqu’une ligne atteint 80 caractères.
   * **Limité** : le retour à ligne s’adapte à la largeur de l’éditeur ou a lieu quand la ligne atteint 80 caractères, selon la valeur la plus petite.
1. **[!UICONTROL Pastilles]** : affichez les attributs sous la forme de « pastilles » compactes afin d’améliorer la lisibilité en masquant les chemins d’accès aux attributs longs. Cliquez sur un attribut pour afficher son chemin d’accès complet.

   >[!NOTE]
   >
   >Cette option n’est disponible que pour les attributs de profil.

Dans le volet de navigation, des fonctionnalités supplémentaires sont disponibles pour vous permettre de créer votre expression de personnalisation.

<!-- ![](assets/perso-features.png) -->

* **[!UICONTROL Fonctions d’assistance]** : les fonctions d’assistance vous permettent d’effectuer des opérations sur les données, comme des calculs, une mise en forme ou des conversions de données, des conditions, et de les manipuler dans le contexte de la personnalisation.

* **[!UICONTROL Favoris]** : les attributs que vous avez ajoutés aux favoris s’affichent dans cette liste. Vous pouvez ainsi accéder rapidement aux éléments les plus utilisés. Pour ajouter un attribut à vos favoris, cliquez sur le menu à trois points et sélectionnez **[!UICONTROL Ajouter aux favoris]**.

Il peut générer des expressions Handlebars à partir de descriptions en langage clair, expliquer des expressions existantes et identifier les problèmes potentiels.

Lorsque votre expression de personnalisation est prête, cliquez sur **[!UICONTROL Confirmer]** ou **[!UICONTROL Insérer]** pour l’ajouter à votre contenu.

## Mécanismes de validation {#validation-mechanisms}

La validation de votre expression s’exécute automatiquement lorsque vous cliquez sur **[!UICONTROL Confirmer]** ou **[!UICONTROL Insérer]** pour fermer l’éditeur. Vous pouvez également cliquer sur **[!UICONTROL Valider]** pour vérifier la syntaxe de votre personnalisation avant la fermeture.

Pour les alertes de contenu qui bloquent l’activation des parcours, voir [Validation du contenu de l’e-mail](./email-authoring.md#validation).

Développez la section suivante pour afficher les erreurs courantes qui peuvent se produire lors de la validation de la personnalisation.

+++Erreurs courantes

* **Chemin « XYZ » introuvable**

Cette erreur se produit lorsque vous référencez un champ qui n’est pas défini dans le schéma.

Dans ce cas **firstName1** n&#39;est pas défini comme un attribut dans le schéma du profil :

```handlebars
{{profile.firstName1}}
```

* **Incompatibilité de type pour la variable « XYZ ».: Tableau attendu. Chaîne trouvée.**

Cette erreur se produit lorsque vous essayez d’effectuer une itération sur une chaîne au lieu d’un tableau.

Dans ce cas **jobTitle** est une chaîne, pas un tableau :

```handlebars
{{#each profile.jobTitle as |item|}}
  {{item}}
{{/each}}
```

* **Syntaxe des barres de contrôle non valide.`'[XYZ}}'`** trouvé

Cette erreur se produit lorsque la syntaxe Handlebars utilisée est non valide.

```handlebars
{{[profile.firstName}}
```

+++
