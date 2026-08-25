---
title: Configuration de la page de destination
description: Espace réservé
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 42%

---


# Configuration des pages de destination

Les administrateurs doivent s’assurer que les configurations de la page de destination sont en place pour les marketeurs qui créent et publient ces pages. Deux types de configuration sont requis pour concevoir des pages de destination qui reflètent une marque et effectuent efficacement le suivi de l’engagement :

* **_Sous-domaines_** — Configurer l&#39;emplacement d&#39;hébergement des pages de destination. Gérez les sous-domaines de la page de destination pour déléguer, configurer ou annuler la délégation des paramètres de domaine.
* **_Préréglages_** — Définissez des configurations réutilisables (y compris des paramètres de sous-domaine et d’autres canaux) afin que les spécialistes marketing puissent créer et gérer des pages de destination de manière cohérente.

## Sous-domaines {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_admin_subdomain_lp_header"
>title="Déléguer un sous-domaine de page de destination"
>abstract="Configurez un sous-domaine pour une page de destination. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_admin_subdomain_lp"
>title="Déléguer un sous-domaine de page de destination"
>abstract="Vous devez configurer un sous-domaine de page de destination avant de créer un préréglage de page de destination. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou configurer un nouveau sous-domaine."

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_admin_config_lp_subdomain"
>title="Créer un préréglage de la page de destination"
>abstract="Pour créer un préréglage de la page de destination, vérifiez que vous avez déjà configuré au moins un sous-domaine de la page de destination à sélectionner dans la liste Nom du sous-domaine."

Pour passer en revue les sous-domaines de page de destination configurés, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**. Sous _[!UICONTROL Pages de destination]_ dans le volet de navigation, sélectionnez **[!UICONTROL Sous-domaines de la page de destination]**.

<!-- ![Channel configurations - landing page subdomains](./assets/config-channels-landing-pages-subdomains.png){width="800" zoomable="yes"} -->

La colonne **Statut** fournit des informations sur le processus de création et de délégation de sous-domaine :

* _[!UICONTROL Brouillon]_ : la délégation de sous-domaine est enregistrée en tant que brouillon. Cliquez sur le nom du sous-domaine pour reprendre le processus de création.
* _[!UICONTROL Traitement]_ : le sous-domaine est en cours de réalisation via plusieurs contrôles de configuration, qui sont nécessaires avant de pouvoir être utilisé.
* _[!UICONTROL Succès]_ : le sous-domaine a passé les contrôles avec succès et peut être utilisé pour diffuser des messages.
* _[!UICONTROL Échec]_ : un ou plusieurs contrôles ont échoué après l&#39;envoi de la délégation de sous-domaine.

>[!NOTE]
>
>Avant de pouvoir [créer des préréglages de page de destination](#lp-presets), vous devez configurer les sous-domaines à utiliser pour les pages de destination. Vous pouvez utiliser un sous-domaine déjà délégué à Adobe ou en configurer un autre.

Une configuration de sous-domaine de page de destination est **commune à tous les environnements**. Par conséquent :

* Pour accéder aux sous-domaines de la page de destination et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gérer les sous-domaines de la page de destination]** dans le sandbox de production.

* Toute modification apportée à un sous-domaine de page de destination aura également un impact sur les sandbox de production.

<!-- 
### Use an existing subdomain {#lp-existing-subdomain}

To use a subdomain that is already delegated to Adobe:

1. Click **[!UICONTROL Set up landing page subdomain]**.

    ![](assets/lp_set-up-subdomain.png)

1. For _[!UICONTROL Configuration type]_, choose **[!UICONTROL Use delegated domain]**.

    ![](assets/lp_use-delegated-subdomain.png)

1. Enter the prefix that you want to display in the landing page URL.

    Only alpha-numeric characters and hyphens are allowed.

    >[!CAUTION]
    >
    >Do not use `cdn` or `data` prefixes as these are reserved for internal use. You should also avoid other restricted or reserved prefixes, such as `dmarc` or `spf`.

1. Select a delegated subdomain from the list.

    You cannot select a subdomain that is already used as landing page subdomain.
    
    ![](assets/lp_prefix-and-subdomain.png)

    You cannot use multiple delegated subdomains of the same parent domain. For example, if 'marketing1.yourcompany.com' is already delegated to Adobe for your landing pages, you cannot use 'marketing2.yourcompany.com'. However, when multi-level subdomains are supported for landing pages, you may proceed using a subdomain of 'marketing1.yourcompany.com' (such as 'email.marketing1.yourcompany.com'), or a different parent domain.

    >[!CAUTION]
    >
    >If you select a domain that was delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-setup), you must create the DNS record on your hosting platform. To generate the DNS record, the process is the same as when you configure a new landing page subdomain.

1. Click **[!UICONTROL Submit]**.

   The subdomain is displayed in the list with the _[!UICONTROL Processing]_ status. For more on subdomains' statuses, see TBD.

    ![](assets/lp_subdomain-processing.png)

   >[!IMPORTANT]
   >
   >The subdomain is not ready for use until Adobe performs the required checks, which can take **_up to 4 hours_**.

   When the checks are successful, the subdomain is listed with the _[!UICONTROL Success]_ status and it is ready to use for creating landing page presets.
-->

### Configurer un nouveau sous-domaine {#lp-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_admin_lp_subdomain_dns"
>title="Générer l’enregistrement DNS correspondant"
>abstract="Pour configurer un nouveau sous-domaine de page de destination, vous devez copier les informations du serveur de noms d’Adobe affichées dans l’interface B2B de Journey Optimizer et les coller dans votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant. Lorsque les vérifications sont effectuées, le sous-domaine est prêt à être utilisé pour créer des préréglages de page de destination."

1. Cliquez sur **[!UICONTROL Configurer le sous-domaine de la page de destination]**.

1. Pour _[!UICONTROL Type de configuration]_, choisissez **[!UICONTROL Ajouter votre propre domaine]**.

1. Spécifiez le sous-domaine à déléguer.

   >[!IMPORTANT]
   >
   >* Vous ne pouvez pas utiliser un sous-domaine de page de destination existant.
   >
   >* Les majuscules ne sont pas autorisées dans les sous-domaines.

   <!-- ![Landing page subdomain set up](./assets/config-channels-landing-pages-subdomain-setup.png){width="500" zoomable="yes"} -->

   La délégation d’un sous-domaine non valide à Adobe n’est pas autorisée. Veillez à saisir un sous-domaine valide détenu par votre entreprise, tel que marketing.votre_entreprise.com.

   Pour les pages de destination, les sous-domaines à plusieurs niveaux sont pris en charge. Vous pouvez, par exemple, utiliser `email.marketing.yourcompany.com`.

1. Copiez l’enregistrement affiché ou téléchargez un fichier CSV, puis accédez à votre solution d’hébergement de domaine pour générer l’enregistrement DNS correspondant.

   L’enregistrement à placer dans les serveurs DNS s’affiche.

1. Assurez-vous que l’enregistrement DNS a été généré dans votre solution d’hébergement de domaine.

   Si tout est correctement configuré, cochez la case de confirmation et cliquez sur **[!UICONTROL Envoyer]**.

   <!-- ![Landing page subdomain set up with DNS records](./assets/config-channels-landing-pages-subdomain-setup-dns.png){width="500" zoomable="yes"} -->

   Lorsque vous configurez un nouveau sous-domaine de page de destination, il pointe toujours vers un enregistrement CNAME.

   Lorsque la délégation de sous-domaine est envoyée, le sous-domaine s’affiche dans la liste avec le statut _[!UICONTROL Traitement]_.

   >[!IMPORTANT]
   >
   >Le sous-domaine n’est pas prêt à être utilisé tant qu’Adobe n’a pas effectué les vérifications requises, ce qui peut prendre **_jusqu’à 4 heures_**.

   Lorsque les vérifications sont réussies, le sous-domaine est répertorié avec le statut _[!UICONTROL Succès]_ et il est prêt à être utilisé pour créer des préréglages de page de destination.

   Le sous-domaine est marqué comme _[!UICONTROL Échec]_ si vous n’avez pas créé l’enregistrement de validation sur votre solution d’hébergement.

### Annuler la délégation d’un sous-domaine {#undelegate-subdomain}

1. Dans [!DNL Journey Optimizer], dépubliez toutes les pages de destination associées au sous-domaine.

1. Si le sous-domaine de la page de destination pointe vers un enregistrement CNAME, supprimez l’enregistrement CNAME de votre solution d’hébergement (ne supprimez pas le sous-domaine d’e-mail d’origine, le cas échéant).

   <!--
    >[!NOTE]
    >
    >A landing page subdomain can point to a CNAME record because it was either an [existing subdomain](#lp-use-existing-subdomain) delegated to Adobe using the [CNAME method](../configuration/delegate-subdomain.md#cname-subdomain-setup), or a [new landing page subdomain](#lp-configure-new-subdomain) that you configured. 
    -->

1. Contactez votre représentant Adobe avec le sous-domaine dont vous souhaitez annuler la délégation.

Une fois qu’Adobe a géré votre demande, la page d’inventaire des sous-domaines n’affiche plus le domaine non délégué.

<!-- 
old marketo way for Prime?

A landing page subdomain should help to identify the content type, product name, or campaign, and reinforce the page authenticity. Before you configure the subdomains, define one or more CNAMEs to use for your landing pages. For example:

* **product**.[CompanyDomain].com
* **go**.[CompanyDomain].com
* **signup**.[CompanyDomain].com

In these examples, the first part (in bold) is the `LandingPageCNAME`.

Add a new subdomain for each unique brand URL that you want to host on Adobe Journey Optimizer B2B Edition. You can add a maximum number of 50 subdomains.

>[!IMPORTANT]
>
>Delegating an invalid subdomain to Adobe is not allowed. Make sure you enter a valid subdomain that your organization owns, such as _marketing.yourcompany.com_.

To review your subdomains and add new ones, go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]**. Under _[!UICONTROL Landing Pages]_ in the navigation panel, select **[!UICONTROL Subdomains]**.

![Landing page subdomains](./assets/config-landing-pages-settings.png){width="800" zoomable="yes"}

_To add a landing page subdomain:_

1. Click **[!UICONTROL Add subdomain]** at the top right.

1. In the _[!UICONTROL Subdomain details]_, enter the subdomain information:

   * **[!UICONTROL Subdomain]** - The subdomain URL to use, such as `marketing.yourcompany.com`
   * **[!UICONTROL Default page]** - The URL for the default subdomain page, such as `marketing.yourcompany.com/products`
   * **[!UICONTROL Fallback page]** - The URL for the fallback page to be used if a landing page on the subdomain is not active, such as `marketing.yourcompany.com/expired`

   ![Add landing page subdomain](./assets/config-landing-pages-add-subdomain.png){width="700" zoomable="yes"}

1. Click **[!UICONTROL Save]**.

-->

## Préréglages {#lp-presets}

>[!CONTEXTUALHELP]
>id="ajo-b2b-prime_admin_config_lp_subdomain_header"
>title="Créer un préréglage de la page de destination"
>abstract="Pour créer une page de destination et l’utiliser via Journey Optimizer B2B Edition, vous devez créer un préréglage de page de destination qui inclura le sous-domaine à utiliser."

Lorsque les professionnels du marketing créent une page de destination, ils doivent sélectionner un préréglage de page de destination pour pouvoir créer la page de destination et l’exploiter via [!DNL Journey Optimizer B2B Edition]. Le préréglage comprend le sous-domaine à utiliser pour la page de destination.

Avant de configurer un préréglage, assurez-vous qu’au moins un sous-domaine de page de destination avec le statut _[!UICONTROL Succès]_ est configuré.

Pour passer en revue les préréglages de page de destination configurés, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]**. Sous _[!UICONTROL Pages de destination]_ dans le volet de navigation, sélectionnez **[!UICONTROL Préréglages de page de destination]**.

<!-- ![Channel configurations - landing page presets](./assets/config-channels-landing-pages-presets.png){width="800" zoomable="yes"} -->

Cliquez sur un nom de préréglage de page de destination pour en afficher les détails.

### Créer un préréglage de la page de destination {#lp-create-preset}

1. Cliquez sur **[!UICONTROL Créer un préréglage de page de destination]**.

1. Saisissez un nom et une description pour le préréglage.

   Les noms doivent commencer par une lettre (A-Z) et ne peuvent contenir que des caractères alphanumériques, un trait de soulignement `_`, un point`.` et un tiret `-`.

1. Sélectionnez un sous-domaine de page de destination.

   <!-- ![Landing page preset with name, description, and subdomain](./assets/config-channels-landing-pages-preset-create.png){width="500" zoomable="yes"} -->

   >[!NOTE]
   >
   >Avant de pouvoir sélectionner un sous-domaine, vous devez avoir configuré au moins un sous-domaine de page de destination.

   Les paramètres correspondant au sous-domaine sélectionné s’affichent.

1. Si vous souhaitez sélectionner le sous-domaine de page de destination comme **[!UICONTROL URL de suivi]**, cochez lʼoption **[!UICONTROL Identique au sous-domaine de page de destination]**.

   <!-- [Learn more about tracking](../email/message-tracking.md) -->

   <!-- ![Landing page preset with subdomain settings](./assets/config-channels-landing-pages-preset-subdomain-settings.png){width="500" zoomable="yes"} -->

   Par exemple, si l’URL de la page de destination est `pages.mail.luma.com` et que l’URL de suivi est `data.mail.luma.com`, vous pouvez choisir `pages.mail.luma.com`’utiliser comme sous-domaine de suivi.

   <!-- 
    >[!CAUTION]
    >
    >The selected landing page subdomain is used to specify the **[!UICONTROL Tracking URL]**and **[!UICONTROL Image Delivery URL]** if that subdomain was created using an [existing subdomain](#use-an-existing-subdomain).
    >
    >If the subdomain was created using the [Add your own domain](#configure-a-new-subdomain) option, the primary subdomain (such as the first delegated subdomain) is used instead. We don't have the existing option right now.
    -->

1. Cliquez sur **[!UICONTROL Envoyer]** pour confirmer la création du préréglage de page de destination.

   <!--You can also save the preset as draft and resume its configuration later on.-->

   Lorsque le préréglage de la page de destination est créé, il est affiché dans la liste avec le statut _[!UICONTROL Actif]_ et est prêt à être utilisé pour créer des pages de destination.