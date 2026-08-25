---
title: Ajout d’une page CSS personnalisée pour votre contenu
description: Ajoutez une page CSS personnalisée aux e-mails et aux pages de destination pour un style avancé et un contrôle de conception précis allant au-delà des composants standard dans Marketo Optimizer.
feature: Content Design Tools, Email Authoring, Landing Pages
role: User
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# Ajout d’une page CSS personnalisée pour votre contenu

Vous pouvez ajouter votre propre CSS personnalisé directement dans l’espace de conception de l’e-mail ou de la page de destination. Utilisez le CSS personnalisé pour appliquer un style avancé et spécifique, pour une plus grande flexibilité et un meilleur contrôle de l’aspect de votre contenu.

La feuille de style CSS personnalisée est ajoutée à la section `<head>` dans une balise `<style>` à l’aide de l’attribut `data-name="global-custom"` . Cette structure garantit que les styles personnalisés sont appliqués globalement au contenu.

+++ Exemple d’implémentation

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++

>[!NOTE]
>
>Le CSS personnalisé n’est pas reflété ou validé dans le panneau _[!UICONTROL Styles]_ pour un composant sélectionné. Il est entièrement indépendant et ne peut être modifié que par le biais de l’option [!UICONTROL Ajouter un CSS personnalisé] au niveau du composant Corps.

## Ajouter votre CSS personnalisé

1. Après avoir ajouté au moins un composant de contenu dans la zone de travail, sélectionnez le composant **[!UICONTROL Corps]** dans le volet de navigation de gauche.

1. Sélectionnez l’onglet _Styles_ à droite et cliquez sur **[!UICONTROL Ajouter un CSS personnalisé]**.

   ![Accès aux styles de corps](assets/email-body-styles.png){width="800" zoomable="yes"}

   >[!NOTE]
   >
   >Le bouton _[!UICONTROL Ajouter un CSS personnalisé]_ n’est disponible que lorsque le composant _[!UICONTROL Corps]_ est sélectionné. Cependant, vous pouvez appliquer des styles CSS personnalisés à tous les composants qu’il contient.

   L’éditeur pop-up _[!UICONTROL Ajouter un CSS personnalisé]_ s’affiche avec des commentaires de code d’espace réservé.

1. Saisissez votre code CSS dans l’éditeur.

   Assurez-vous que le code CSS personnalisé est valide et suit la syntaxe appropriée. Si la page CSS saisie n’est pas valide, un message d’erreur s’affiche et la page CSS ne peut pas être enregistrée. Pour en savoir plus, voir [Validité CSS](#css-validity).

   ![Saisissez le CSS personnalisé dans l’éditeur](assets/content-design-add-custom-css.png){width="450"}

1. Cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer le fichier CSS personnalisé.

   La feuille de style personnalisée est appliquée au contenu existant. Vous pouvez vérifier que votre CSS personnalisé est appliqué en fonction de vos besoins. Pour plus d&#39;informations sur la façon d&#39;apporter des modifications et d&#39;ajuster l&#39;application de la feuille de style, voir [Dépannage](#troubleshooting).

   ![CSS personnalisé appliqué au contenu](assets/email-body-custom-css-applied.png){width="600" zoomable="yes"}

## Validité CSS {#css-validity}

>[!CAUTION]
>
>Les utilisateurs et utilisatrices sont responsables de la sécurité de leur CSS personnalisé. Assurez-vous que votre CSS n’introduit pas de vulnérabilité ou de conflit avec le contenu existant.
>
>Évitez d’utiliser du code CSS qui pourrait altérer involontairement la disposition ou la fonctionnalité du contenu.

+++ Exemples de CSS valides

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++

+++ Exemples de CSS non valides

L’utilisation de balises `<style>` n’est pas acceptée :

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Une syntaxe non valide, comme l’omission des accolades, n’est pas acceptée :

```css
body {
  background: red;
```

+++

## CSS dans le contenu importé {#imported-content}

Si vous souhaitez utiliser un CSS personnalisé avec du contenu importé dans l’espace de conception d’e-mail ou de page de destination, tenez compte des points suivants :

* Si vous importez du contenu HTML externe, y compris du contenu CSS, il est renseigné en [!UICONTROL mode de compatibilité] et la section [!UICONTROL styles CSS] n’est pas disponible.

* Si vous importez du contenu créé à l’origine dans l’espace de conception d’e-mail ou de page de destination à l’aide de l’option [!UICONTROL Ajouter un CSS personnalisé], le CSS appliqué est visible et modifiable à partir de la même option.

## Dépannage {#troubleshooting}

Si votre page CSS personnalisée n’est pas appliquée comme prévu, utilisez les outils de développement du navigateur pour inspecter le contenu et vérifier que votre page CSS cible les sélecteurs appropriés. Lorsque vous examinerez le code de style, tenez compte des points suivants :

* Vérifiez que votre CSS est valide et ne comporte pas d’erreurs de syntaxe (telles que des accolades manquantes, des noms de propriété incorrects).

* Vérifiez que votre CSS a été ajouté à la balise `<style>` avec l’attribut `data-name="global-custom"`.

* Vérifiez si la balise de style de `global-custom` possède l’attribut `data-disabled` défini sur true, par exemple :

  `<style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>`

* Vérifiez que votre CSS n’est pas remplacé à un endroit du contenu, par exemple par un style intégré.

* Ajoutez des `!important` à vos déclarations pour vous assurer qu’elles sont prioritaires, par exemple :

  ```
  .acr-Form {
  background: red !important;
  }
  ```
