---
title: Composants de contenu
description: 'Concevez des e-mails, des pages de destination et des fragments avec des composants de contenu : ajoutez des boutons, du texte, des images, des formulaires et des conteneurs dans Marketo Optimizer.'
feature: Content Design Tools
role: User
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '2828'
ht-degree: 7%

---

# Composants de contenu {#content-components}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_content_components_email"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour concevoir un e-mail."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_content_components_landing_page"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour concevoir une page de destination."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_content_components_fragment"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour concevoir un fragment."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_content_components_template"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour concevoir un modèle."

Lorsque vous concevez du contenu pour des e-mails, des pages de destination, des modèles et des fragments visuels, utilisez les [!UICONTROL composants de contenu] pour ajouter des éléments de conception visuelle.

Vous pouvez ajouter autant de composants de contenu que nécessaire dans un ou plusieurs [composants de structure](./structure-components.md), ce qui permet de définir la disposition.

## Bibliothèque de contenus

La section **[!UICONTROL Contenu]** de la bibliothèque de composants affiche les composants de contenu disponibles :

| Icône | Composant | Description |
| --------- | ---- | ----------- |
| ![Icône de conteneur](../assets/do-not-localize/icon-content-component-container.svg) | [Conteneur](#container) | Ajoutez ce composant à votre conception afin d’inclure un conteneur rectangulaire que vous pouvez utiliser pour regrouper les composants ou appliquer un style d’arrière-plan ou de bordure à une zone. |
| ![Icône Bouton](../assets/do-not-localize/icon-content-component-button.svg) | [Bouton](#button) | Ajoutez ce composant à votre conception pour inclure un élément bouton cliquable. |
| ![Icône Texte](../assets/do-not-localize/icon-content-component-text.svg) | [Texte](#text) | Ajoutez ce composant à votre conception pour inclure un corps de texte. |
| ![Icône Diviseur](../assets/do-not-localize/icon-content-component-divider.svg) | [Diviseur](#divider) | Ajoutez ce composant à votre conception afin d’inclure une ligne horizontale pour séparer les zones de votre contenu. |
| ![Icône ](../assets/do-not-localize/icon-content-component-html.svg) | [HTML](#html) | Ajoutez ce composant à votre conception pour copier-coller les différentes parties de votre HTML existante. Utilisez ce composant pour créer un bloc HTML modulaire libre afin de réutiliser du contenu externe. |
| ![ Icône Image ](../assets/do-not-localize/icon-content-component-image.svg) | [Image](#image) | Ajoutez ce composant à votre conception pour insérer un fichier image. |
| ![ Icône Social ](../assets/do-not-localize/icon-content-component-social.svg) | [Social](#social) | Ajoutez ce composant à votre conception pour insérer des liens vers des pages de réseaux sociaux. |
| ![Icône de formulaire](../assets/do-not-localize/icon-content-component-form.svg) | [Form](#form) (Formulaire) | **_Disponible uniquement pour les pages de destination._** Ajoutez ce composant à votre conception pour insérer un formulaire créé. |

## Barres d’outils des composants de contenu

Chaque type de composant de contenu affiche une barre d’outils lorsque vous le sélectionnez dans la zone de travail. Les outils disponibles, qui varient selon le type de composant, permettent d’utiliser facilement le composant directement dans le contenu rendu. La barre d’outils comprend des fonctionnalités de formatage et fonctionnelles applicables au type de composant.

![Barre d’outils du composant de contenu](../assets/do-not-localize/toolbar-content.png){width="450"}

### Outils de formatage

+++Modifier le style de texte

<table>
    <tr>
        <th style="width: 30%;">Outil</th>
        <th style="width: 50%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="120px" src="../assets/do-not-localize/toolbar-button-text-styles.png" alt="Outil Modifier le style de texte"></td>
        <td>Appliquez le gras, l’italique, le soulignement, le trait barré, l’exposant ou l’indice à la chaîne de texte sélectionnée.</td>
        <td><li>Bouton <li>Texte</td>
    </tr>
</table>

+++

+++Alignement horizontal

<table>
    <tr>
        <th style="width: 30%;">Outil</th>
        <th style="width: 50%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="120px" src="../assets/do-not-localize/toolbar-button-horizontal-alignment.png" alt="Outil d'alignement horizontal"></td>
        <td>Appliquez un type d’alignement horizontal au contenu du composant. Choisissez gauche, centré, droite ou justifié. </td>
        <td><li>Bouton <li>Texte</td>
    </tr>
</table>

+++

+++Créer une liste

<table>
    <tr>
        <th style="width: 30%;">Outil</th>
        <th style="width: 50%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="120px" src="../assets/do-not-localize/toolbar-button-create-list.png" alt="Outil Créer une liste"></td>
        <td>Appliquez une mise en forme de liste ordonnée ou non au texte du composant.</td>
        <td><li>Texte</td>
    </tr>
</table>

+++

+++Définir le titre

<table>
    <tr>
        <th style="width: 20%;">Outil</th>
        <th style="width: 60%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="60px" src="../assets/do-not-localize/toolbar-button-set-heading.png" alt="Définir l’outil de titre"></td>
        <td>Appliquez une mise en forme au niveau du titre au paragraphe pour l'emplacement du curseur.</td>
        <td><li>Bouton <li>Texte</td>
    </tr>
</table>

+++

+++Taille de la police

<table>
    <tr>
        <th style="width: 20%;">Outil</th>
        <th style="width: 60%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="60px" src="../assets/do-not-localize/toolbar-button-font-size.png" alt="Outil Taille de police"></td>
        <td>Appliquer la taille de police à un texte sélectionné. Cliquez sur l’outil et choisissez la taille ou saisissez la valeur px.</td>
        <td><li>Bouton <li>Texte</td>
    </tr>
</table>

+++

+++Couleur de police

<table>
    <tr>
        <th style="width: 40%;">Outil</th>
        <th style="width: 40%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="200px" src="../assets/do-not-localize/toolbar-button-font-color.png" alt="Outil Couleur de police"></td>
        <td>Appliquer une couleur de police au texte sélectionné. Sélectionnez une couleur dans le sélecteur et utilisez le curseur de couleur et le champ de couleur pour sélectionner la couleur. Vous pouvez également saisir une valeur RGB, HSL, HSB ou hexadécimale connue. </td>
        <td><li>Bouton <li>Texte</td>
    </tr>
</table>

+++

+++Insérer un lien

<table>
    <tr>
        <th style="width: 40%;">Outil</th>
        <th style="width: 40%;">Utilisation</th>
        <th style="width: 20%;">Composants</th>
    </tr>
    <tr>
        <td><img width="200px" src="../assets/do-not-localize/toolbar-button-insert-link.png" alt="Outil Insérer un lien"></td>
        <td>Créez un lien cliquable pour le texte ou l’élément sélectionné. <li>Contenu de l’e-mail - Spécifiez une URL externe ou une page de destination.<li>Contenu de la page de destination : indiquez un lien externe.</td>
        <td><li>Bouton <li>Texte <li>Image </td>
    </tr>
</table>

+++

+++Supprimer le lien

<table>
    <tr>
        <th style="width: 15%;">Outil</th>
        <th style="width: 60%;">Utilisation</th>
        <th style="width: 25%;">Composants</th>
    </tr>
    <tr>
        <td><img width="80px" src="../assets/do-not-localize/toolbar-button-remove-link.png" alt="Supprimer l’outil de lien"></td>
        <td> Supprimez le lien cliquable pour le texte ou l’élément sélectionné.</td>
        <td><li>Bouton <li>Texte <li>Image </td>
    </tr>
</table>

+++

### Outils fonctionnels

| Outil | Nom | Utilisation |
| ---- | ---- | ----- |
| ![Ajouter une personnalisation](../assets/do-not-localize/toolbar-button-add-personalization.png){width="40"} | Ajouter une personnalisation | Utilisez l’éditeur de personnalisation pour insérer des jetons de personnalisation dans le contenu du composant. [En savoir plus](./email-authoring.md#personalize-content) |
| ![Afficher le code source](../assets/do-not-localize/toolbar-button-show-source-code.png){width="40"} | Afficher le code source | Affichez le code source HTML du composant dans une fenêtre contextuelle en lecture seule. <br/>![Afficher le code HTML](assets/content-components-show-source-code.png){width="200"} |
| ![Activer le contenu conditionnel](../assets/do-not-localize/toolbar-button-enable-conditional-content.png){width="40"} | Activer le contenu conditionnel | (E-mails et fragments) Activez les variantes conditionnelles pour le composant. |
| ![Dupliquer](../assets/do-not-localize/toolbar-button-duplicate.png){width="40"} | Dupliquer | Créez une copie du composant et ajoutez-la directement sous . |
| ![Supprimer](../assets/do-not-localize/toolbar-button-delete.png){width="40"} | Supprimer | Supprimez le composant . |

## Ajouter un composant de contenu à votre conception

1. Dans l’espace de conception visuelle, utilisez un modèle existant ou ajoutez les composants de structure nécessaires dans une zone de travail vide pour définir la disposition.

1. Dans la bibliothèque **[!UICONTROL Composants]**, saisissez la _Poignée de glisser_ ![Poignée de glisser](../assets/do-not-localize/icon-drag-handle.svg) pour le composant de contenu de votre choix, puis faites-la glisser et déposez-la sur les composants de structure.

   Vous pouvez ajouter plusieurs composants dans un seul composant de structure et dans chaque colonne d’un composant de structure.

   ![Faites glisser le composant de contenu dans le composant de structure](assets/content-components-drag.png){width="600" zoomable="yes"}

1. Ajustez l’affichage du composant à l’aide des onglets **[!UICONTROL Paramètres]** et **[!UICONTROL Styles]** sur la droite, ou de la barre d’outils contextuelle affichée dans la zone de travail.

   Par exemple, vous pouvez modifier le style de texte, la marge intérieure ou la marge du composant.

   ![Définissez les paramètres et les styles du composant de contenu](assets/content-components-settings-styles.png){width="600" zoomable="yes"}

Lorsque vous travaillez sur votre conception, vous pouvez également supprimer ou dupliquer un composant à l’aide des outils **Supprimer** et **Dupliquer** dans la section [Outils fonctionnels](#functional-tools).

## Paramètres et styles des composants de contenu

Après avoir ajouté un composant, il est sélectionné dans l’espace de conception visuelle et ses propriétés s’affichent dans le panneau de droite. Vous pouvez également sélectionner un composant à tout moment pour modifier les paramètres et les styles. De nombreux paramètres et styles sont spécifiques au composant, mais vous pouvez appliquer certains paramètres et styles standard aux composants de contenu sélectionnés.

### Options d’affichage

Si vous souhaitez exclure le composant de l’affichage du bureau ou de l’appareil mobile, modifiez le paramètre **[!UICONTROL Options d’affichage]**. La valeur par défaut, _[!UICONTROL Afficher sur tous les appareils]_, active l’affichage sur tous les appareils. Choisissez un autre paramètre pour rendre le composant exclusif par type d’appareil :

* _[!UICONTROL Afficher uniquement sur les appareils de bureau]_ - Sélectionnez ce paramètre lorsque vous souhaitez afficher le composant sur les appareils de bureau et l’exclure pour les appareils mobiles.
* _[!UICONTROL Afficher uniquement sur les appareils mobiles]_ - Sélectionnez ce paramètre lorsque vous souhaitez afficher le composant sur les appareils mobiles, tels que les téléphones et les tablettes, et l’exclure pour les ordinateurs de bureau.

![Options d’affichage du composant de contenu](assets/content-components-display-options.png){width="400" zoomable="yes"}

### Conteneur {#container}

Utilisez un conteneur pour appliquer un style spécifique à un groupe de composants de contenu. Ajoutez un composant [!UICONTROL Conteneur], puis ajoutez d’autres composants de contenu à l’intérieur. Ce composant est similaire à la manière dont vous pouvez utiliser un élément `div` dans HTML. Vous pouvez appliquer au conteneur un style distinct qui diffère du style appliqué aux composants de contenu qu’il contient.

Par exemple, ajoutez un composant _[!UICONTROL Conteneur]_, puis ajoutez un composant _[!UICONTROL Bouton]_ à l’intérieur de ce conteneur. Vous pouvez utiliser un style de zone spécifique pour le conteneur et appliquer un style au bouton et à son arrière-plan selon vos besoins.

![Styles des composants de contenu de conteneur](assets/content-components-container.png){width="600" zoomable="yes"}

+++Contexte

{{styles-background}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

### Bouton {#button}

Utilisez le composant [!UICONTROL Button] pour insérer un ou plusieurs boutons cliquables dans votre contenu. Utilisez des boutons pour rediriger les visiteurs de pages ou les destinataires d’e-mails vers le contenu complémentaire (page de destination publiée ou lien externe).

#### Ajouter le texte du bouton

Lorsque le composant Bouton s’affiche dans la zone de travail, la barre d’outils comprend des options de mise en forme de texte, ainsi que des options de personnalisation et des variantes conditionnelles. Pour plus d’informations sur les options de la barre d’outils de l’éditeur, voir [ Barres d’outils des composants de contenu ](#content-component-toolbars).

Lorsque vous saisissez le texte du libellé du bouton et définissez la mise en forme, le bouton se redimensionne pour s’adapter au contenu.

![Composant bouton affiché dans la barre d’outils](assets/content-components-button.png){width="500" zoomable="yes"}

#### Définir les options de lien {#button-set-link-options}

Dans l’onglet _[!UICONTROL Paramètres]_, utilisez les options **[!UICONTROL Lien]** pour définir le texte du bouton, la destination du lien et le comportement du navigateur pour charger la page cible.

1. Définissez le **[!UICONTROL Type]** pour le lien :

   * **[!UICONTROL Lien externe]** - Choisissez ce type pour utiliser une URL standard comme destination du lien.

     Dans **[!UICONTROL Url]**, saisissez l’URL de destination du lien. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation en tant que paramètre dans l’URL.

     ![Définir un lien externe pour un composant Bouton](assets/component-button-link-options-external.png){width="200"}

   * **Page de destination** - Choisissez ce type pour sélectionner une page de destination publiée dans <!-- Journey Optimizer B2B Edition (_Beta_) or -->l’instance Marketo Engage connectée.

     Pour l’option **[!UICONTROL Page de destination]**, sélectionnez la page de destination publiée. Cliquez sur l’icône _Sélectionner une page_ ( ![Afficher l’icône des liens](../assets/do-not-localize/icon-landing-page-select.svg) ) et [sélectionnez la page de destination publiée](./landing-pages.md#link-to-landing-page).

     ![Définir un lien vers une page de destination pour un composant Bouton](assets/component-button-link-options-landing-page.png){width="200"}

1. Pour **[!UICONTROL Libellé]**, saisissez le texte à afficher dans le bouton.

   Le dimensionnement du bouton s’ajuste en fonction du texte et du style que vous avez définis.

1. Pour **[!UICONTROL Target]**, choisissez comment la destination liée est redirigée à partir de l’e-mail ou de la page :

   * _[!UICONTROL Aucune]_ - Ouvre le lien à l’aide du navigateur par défaut ou du comportement du client (par défaut).
   * _[!UICONTROL Vide]_ - Ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * _[!UICONTROL Self]_ - Ouvre le lien dans le même cadre.
   * _[!UICONTROL Parent]_ - Ouvre le lien dans le cadre parent.
   * _[!UICONTROL Haut]_ - Ouvre le lien dans le corps complet de la fenêtre.

#### Définition des styles

Personnalisez le style du bouton dans l’onglet **[!UICONTROL Styles]**.

+++Contexte

{{styles-background}}

+++

+++Texte

{{styles-text}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Alignement

{{styles-alignment-h-v}}

+++

+++Marge du bouton

{{styles-margin}}

+++

+++Marge du conteneur

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### Texte {#text}

Utilisez le composant Texte pour insérer un bloc de texte dans votre contenu. Lorsque le composant de texte est sélectionné dans la zone de travail, saisissez le texte et utilisez les options de la barre d’outils pour ajouter une mise en forme et des options intégrées, y compris des jetons de personnalisation et des variantes conditionnelles.

Personnalisez le style du composant de texte dans l’onglet **[!UICONTROL Styles]**.

+++Contexte

{{styles-background}}

+++

+++Texte

Ces styles sont appliqués à l’ensemble du bloc de texte. Vous pouvez appliquer un style intégré à une chaîne de texte sélectionnée.

{{styles-text}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### Diviseur {#divider}

Ajoutez un composant _Diviseur_ pour incorporer une division linéaire entre les sections de votre contenu.

+++Contexte

{{styles-background}}

+++

+++Ligne

Dans le panneau de droite avec l’onglet _[!UICONTROL Styles]_ sélectionné, développez la section **[!UICONTROL Ligne]** et définissez les options de hauteur et de largeur du composant :

* **[!UICONTROL Couleur]** - Cliquez sur le carré de couleur pour choisir une couleur dans le sélecteur. Vous pouvez choisir une couleur en entrant une valeur RGB, HSL, HSB ou hexadécimale connue. Vous pouvez également utiliser le curseur de couleur et le champ de couleur pour sélectionner la couleur.

* **[!UICONTROL Hauteur]** - Cliquez sur les icônes fléchées vers le haut et vers le bas pour augmenter ou réduire le nombre de pixels. Une valeur vide (Auto) est la valeur par défaut et dimensionne la hauteur de l’élément en fonction de son contenu.

* **[!UICONTROL Largeur]** - Utilisez le bouton (bascule) pour définir la largeur en pixels ou en pourcentage.

  * Pour un pourcentage de largeur, utilisez le curseur pour définir la valeur de pourcentage. Le pourcentage détermine la taille de l’élément en fonction de la zone de contenu du bloc conteneur, ce qui exclut la marge intérieure et les bordures. Par exemple, une valeur de 50 définit la largeur de l’élément sur 50 % de la largeur du contenu du bloc qui le contient.

  ![Définition du style de ligne pour un composant diviseur](assets/component-divider-line-options.png){width="250"}

  * Pour une largeur en pixels, cliquez sur les icônes fléchées vers le haut et vers le bas pour augmenter ou réduire le nombre de pixels. Une valeur vide (Auto) est la valeur par défaut et dimensionne la largeur de l’élément en fonction de son contenu.

* **[!UICONTROL Style]** - Sélectionnez une valeur dans la liste des valeurs de `line-style` CSS standard, telles que _Continu_, _Pointillé_ et _Tiret_.

+++

+++Taille

{{styles-size}}

+++

+++Alignement

{{styles-alignment-h}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### HTML {#html}

Utilisez le composant HTML pour ajouter des parties de votre HTML existant. Ce composant permet de créer facilement des éléments modulaires d’HTML qui réutilisent votre contenu externe.

1. Sélectionnez le composant sur la zone de travail et cliquez sur l’icône _Afficher le code source_ dans la barre d’outils.

   ![Ouvrez l’éditeur de code pour ajouter HTML](assets/content-components-html-show-code.png){width="450"}

1. Collez l’HTML dans la zone de texte, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![ Boîte de dialogue Modifier HTML ](assets/content-components-html-edit-dialog.png){width="600" zoomable="yes"}

   Si l’HTML est valide, elle effectue le rendu de l’élément sur la zone de travail. S’il s’agit d’un élément qui correspond à l’un des autres composants de contenu, vous pouvez modifier les paramètres et les styles dans le panneau de droite en fonction du type de composant. Dans le cas contraire, il reste en tant que composant HTML.

Pour un composant HTML, vous pouvez définir les styles suivants pour l’ensemble du composant HTML dans le panneau de droite :

+++Contexte

{{styles-background}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Alignement

{{styles-alignment-h-v}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### Image {#image}

Utilisez le composant [!UICONTROL Image] pour insérer une ressource image dans votre contenu. Lorsque le composant _Image_ est sélectionné dans la zone de travail, vous pouvez ajouter ou modifier le fichier de ressource image affiché.

![Composant d’image affiché avec la barre d’outils](assets/content-components-image.png){width="400" zoomable="yes"}

#### Ajout de la ressource image {#add-image-asset}

Choisissez une méthode pour ajouter la ressource image :

* **[!UICONTROL Sélectionner une ressource]** - Choisissez ce type pour parcourir et sélectionner une ressource image dans la bibliothèque Assets [!DNL Marketo Optimizer].

  ![Parcourir les ressources d’image disponibles](./assets/dam-assets-internal-image-selected.png){width="700" zoomable="yes"}

  Dans la boîte de dialogue, vous pouvez choisir une image dans le référentiel sélectionné. Cliquez sur **[!UICONTROL Sélectionner]** pour ajouter la ressource.

  Plusieurs outils sont disponibles pour vous aider à localiser la ressource dont vous avez besoin :

  * Cliquez sur l’icône _Filtrer_ en haut à gauche pour filtrer les éléments affichés en fonction de vos critères.

  * Saisissez du texte dans le champ _Rechercher_ pour filtrer les éléments affichés afin qu’ils correspondent au nom de la ressource.

* **[!UICONTROL Importer un média]** - Choisissez ce type pour sélectionner un fichier dans votre système et l’importer dans la bibliothèque de ressources [!DNL Marketo Optimizer].

  Dans la boîte de dialogue _[!UICONTROL Télécharger l’image]_, effectuez un glisser-déposer d’un fichier de votre système dans la zone de fichier. La taille de fichier maximale est de 100 Mo.

  ![Importer un fichier image dans la bibliothèque de ressources](assets/email-designer-image-upload.png){width="450"}

  Les noms de fichier des images sélectionnées s’affichent dans la boîte de dialogue. Les noms de fichiers de ressources doivent être uniques (dans plusieurs dossiers) et, si un fichier portant ce nom existe déjà, un message s’affiche. Les noms peuvent contenir au maximum 100 caractères et ne peuvent pas contenir de caractères spéciaux (par exemple `;`, `:`, `\` et `|`).

  Cliquez sur **[!UICONTROL Importer]**.

Vous pouvez ajouter un titre d’image et un texte secondaire pour l’image dans le panneau de droite.

![Paramètres d’image](./assets/dam-assets-image-settings.png){width="250"}

#### Définir les options de lien {#image-set-link-options}

Dans l’onglet _[!UICONTROL Paramètres]_, utilisez les options **[!UICONTROL Lien]** pour lier l’image à une destination et le comportement du navigateur pour charger la page cible.

1. Définissez le **[!UICONTROL Type]** pour le lien :

   * **[!UICONTROL Lien externe]** - Choisissez ce type pour utiliser une URL standard comme destination du lien.

     Dans **[!UICONTROL Url]**, saisissez l’URL de destination du lien. Cliquez sur l’icône _Personnaliser_ ( ![Icône Personnaliser](../assets/do-not-localize/icon-personalize.svg) ) pour utiliser un jeton de personnalisation en tant que paramètre dans l’URL.

     ![Définir un lien externe pour un composant d’image](assets/component-button-link-options-external.png){width="250"}

   * **Page de destination** - Choisissez ce type pour sélectionner une page de destination publiée dans <!-- Journey Optimizer B2B Edition (_Beta_) or -->l’instance Marketo Engage connectée.

     Pour l’option **[!UICONTROL Page de destination]**, sélectionnez la page de destination publiée. Cliquez sur l’icône _Sélectionner une page_ ( ![Afficher l’icône des liens](../assets/do-not-localize/icon-landing-page-select.svg) ) et [sélectionnez la page de destination publiée](./landing-pages.md#link-to-landing-page).

     ![Définir un lien vers une page de destination pour un composant d’image](assets/component-button-link-options-landing-page.png){width="250"}

1. Pour **[!UICONTROL Libellé]**, vous pouvez éventuellement saisir un texte descriptif pour le lien de l’image.

1. Pour **[!UICONTROL Target]**, choisissez comment la destination liée est redirigée à partir de l’e-mail ou de la page :

   * _[!UICONTROL Aucune]_ - Ouvre le lien à l’aide du navigateur par défaut ou du comportement du client (par défaut).
   * _[!UICONTROL Vide]_ - Ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * _[!UICONTROL Self]_ - Ouvre le lien dans le même cadre.
   * _[!UICONTROL Parent]_ - Ouvre le lien dans le cadre parent.
   * _[!UICONTROL Haut]_ - Ouvre le lien dans le corps complet de la fenêtre.

#### Définition des styles

Définissez les styles du composant d’image dans le panneau de droite.

+++Contexte

{{styles-background}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Alignement

{{styles-alignment-h}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### Social {#social}

Utilisez le composant _Social_ pour insérer des liens vers des pages de réseaux sociaux dans votre contenu. Il comprend trois types de médias sociaux par défaut, mais vous pouvez les ajouter ou les supprimer en fonction de vos besoins.

![Nouveau composant social avec les types par défaut](./assets/content-components-social-settings.png){width="600" zoomable="yes"}

* Pour ajouter un type de réseau social, cliquez sur l’icône _Ajouter_ ( **+** ) et choisissez un type de réseau social à ajouter.

  ![Cliquez sur + pour ajouter un type de réseau social](./assets/content-components-social-settings-add-type.png){width="250"}

* Pour supprimer un type de réseau social, cliquez sur le **X** en regard de l’icône de réseau social.

Développez la carte pour chaque type de réseau social afin de définir les options :

* **[!UICONTROL URL]** - Saisissez l’URL du réseau social que vous souhaitez lier au graphique ou à l’icône du réseau social.
* **** - Si vous souhaitez utiliser votre propre image au lieu de la valeur par défaut, choisissez une ressource d’image. Vous pouvez sélectionner une image dans la bibliothèque Assets ou importer un fichier image à partir de votre système. Pour plus d’informations sur la sélection et l’importation de ressources d’image](#add-the-image-asset) consultez les informations sur les composants d’image [.
* **[!UICONTROL Texte secondaire]** - Saisissez le texte secondaire de l’image affichée.

![Paramètres du type de réseau social développé](./assets/content-components-social-settings-for-type.png){width="250"}

Pour définir une taille d’affichage cohérente pour tous les graphiques des réseaux sociaux, définissez la **[!UICONTROL Taille des images]**.

Vous pouvez définir les options de style suivantes pour le composant _Social_ :

+++Contexte

{{styles-background}}

+++

+++Bord

{{styles-border}}

+++

+++Taille

{{styles-size}}

+++

+++Alignement

{{styles-alignment-h}}

+++

+++Marge

{{styles-margin}}

+++

+++Remplissage

{{styles-padding}}

+++

+++Advanced

{{styles-advanced}}

+++

### Formulaire (pages de destination uniquement) {#form}

Utilisez le composant _Formulaire_ pour ajouter un formulaire publié à une page de destination ou à un modèle de page de destination. Pour plus d&#39;informations sur la création et la publication de formulaires, voir [](./forms.md).

1. Cliquez sur l’outil _Formulaire_ dans la barre d’outils du composant, ou utilisez les propriétés **[!UICONTROL Incorporer le formulaire]** à droite pour sélectionner le formulaire publié.

   ![Sélectionnez le formulaire publié](assets/content-design-add-form-properties.png){width="600"}

1. Si vous souhaitez remplacer le **[!UICONTROL type de suivi]** par défaut pour le formulaire, modifiez le paramètre en fonction des exigences de la page ou du modèle.

   Cette page est également appelée _page de remerciement_ pour le formulaire. Ce paramètre détermine ce qui se passe lorsqu’un visiteur envoie le formulaire :

   * **[!UICONTROL Rester sur la page]** - Sélectionnez cette option pour que le visiteur reste sur la même page lors de l’envoi du formulaire.

   * **[!UICONTROL Page de destination]** - Sélectionnez cette option pour sélectionner n’importe quelle page de destination [!DNL Marketo Optimizer] ou Marketo Engage comme suite.

   * **[!UICONTROL URL externe]** - Sélectionnez cette option pour spécifier n’importe quelle URL comme page de suivi. Une fois que le visiteur a envoyé le formulaire, le navigateur charge l’URL désignée.

     >[!TIP]
     >
     >Si vous souhaitez utiliser le formulaire pour télécharger un fichier, vous pouvez spécifier une URL pour le fichier hébergé. Avec cette configuration, le bouton d’envoi fonctionne comme un bouton de téléchargement.

     ![Modifier le paramètre de relance](assets/content-design-add-form-follow-up.png){width="280"}

Si nécessaire, sélectionnez l’onglet **[!UICONTROL Styles]** dans le panneau de droite pour définir les marges du formulaire dans le composant de structure.

{{styles-margin}}
