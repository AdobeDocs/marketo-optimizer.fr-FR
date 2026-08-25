---
title: Accès utilisateur et autorisations
description: 'Gérer l’accès des utilisateurs et utilisatrices dans Adobe Admin Console : créer des groupes d’utilisateurs et d’utilisatrices, attribuer des profils de produit et définir des autorisations en fonction du rôle pour Marketo Optimizer.'
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '2279'
ht-degree: 45%

---

# Accès utilisateur et autorisations

Une fois la mise en service terminée et les sandbox liés, procédez comme suit pour fournir un accès [!DNL Marketo Optimizer] à votre équipe et aux utilisateurs.

1. [Créer un [!DNL Journey Optimizer B2B Edition] profil de produit](#create-profile) dans Admin Console (configuration unique/initiale uniquement).
1. [Ajoutez un groupe d’utilisateurs](#add-user-group) dans Admin Console.
1. [Attribuez le profil de produit](#assign-profile) au groupe d’utilisateurs dans Admin Console.
1. [Ajoutez des utilisateurs au nouveau groupe](#add-users) dans Admin Console.
1. [Modifiez les rôles intégrés](#edit-role-permissions) ou [créez un rôle personnalisé](#create-a-custom-role) avec des autorisations [!DNL Journey Optimizer B2B Edition] dans Adobe Experience Platform.
1. [Ajouter des utilisateurs](#add-users-to-a-role) des utilisatrices ou des [groupes](#add-user-groups-to-a-role) à des rôles dans Adobe Experience Platform.

## Configuration du profil de produit {#config-profile}

En tant qu’administrateur, vous pouvez effectuer ces tâches dans l’[!DNL Adobe Admin Console], qui constitue un emplacement central pour administrer et gérer vos licences de produit et utilisateurs Adobe. Dans Admin Console, vous pouvez créer et gérer des utilisateurs dans un emplacement unique, plutôt qu’au sein de vos différentes solutions. Pour en savoir plus sur ses fonctions et ses fonctionnalités, consultez la page de présentation d’Admin Console [&#128279;](https://helpx.adobe.com/business/enterprise/plan-your-deployment/basic-concepts/admin-console.html).

### Accès à Admin Console {#admin-console}

Avant de pouvoir utiliser Admin Console pour administrer les utilisateurs au sein de votre équipe, vous devez vous assurer que vous pouvez accéder à Admin Console et que vous disposez des autorisations appropriées.

1. En tant qu’administrateur système, vous devriez recevoir plusieurs e-mails d’Adobe dans le cadre du processus d’intégration.

   Recherchez l’e-mail de bienvenue qui fournit les informations sur le nom de l’organisation auquel vous avez accès.

1. Cliquez sur le lien **[!UICONTROL Commencer]** dans l’e-mail de bienvenue pour accéder à Admin Console.

   Si vous ne retrouvez pas l’e-mail en question, ouvrez un navigateur directement sur Admin Console à l’adresse [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Connectez-vous à l’aide de votre Adobe ID.

   Une fois la connexion établie, la page _Aperçu_ du Adobe Admin Console s’affiche.

1. Si vous avez accès à plusieurs organisations, vérifiez que vous vous êtes connecté à la bonne organisation.

   Pour modifier votre organisation, cliquez sur le nom de l’organisation dans le coin supérieur droit et sélectionnez l’organisation à laquelle vous avez besoin d’accéder.

1. Sélectionnez **[!UICONTROL Administrateurs]** dans la vignette _[!UICONTROL Utilisateurs]_ pour vérifier que vous êtes bien administrateur système.

   ![Présentation d’Admin Console - cliquez sur Administrateurs](./assets/admin-console-overview-administrators.png){width="800" zoomable="yes"}

1. Recherchez en saisissant votre adresse e-mail, votre nom d’utilisateur, votre prénom ou votre nom Adobe ID.

   * Si votre accès est correctement configuré, la recherche renvoie votre enregistrement.

   * Si la valeur de la colonne **[!UICONTROL RÔLE D’ADMINISTRATEUR]** s’affiche `System`, vous savez que vous (ou l’utilisateur affiché) êtes un administrateur ou une administratrice système.

### Créer le profil de produit [!DNL Journey Optimizer B2B Edition] {#create-profile}

Lorsque vous accordez aux utilisateurs l’accès à une solution Adobe, vous ne souhaitez pas nécessairement leur accorder un accès complet. Les profils de produit permettent à chaque solution d’avoir son propre jeu d’autorisations utilisateur. Utilisez Admin Console pour attribuer des profils de produit.

Pour plus d’informations sur l’utilisation des profils de produit pour les droits des utilisateurs, voir [_Gérer les profils de produit pour les utilisateurs d’entreprise_](https://helpx.adobe.com/business/enterprise/manage-products-and-entitlements/manage-products-and-product-profiles/manage-product-profiles.html){target="_blank"} dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou [!DNL Experience Platform] administrateur de produit peut effectuer les étapes suivantes à partir de [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Produits]**.

1. Ouvrez l’instance de [!DNL Journey Optimizer B2B Edition] où vous souhaitez ajouter le profil et cliquez sur **[!UICONTROL Nouveau profil]**.

   ![Experience Platform - profils de produit pour le groupe d’utilisateurs](./assets/admin-console-product-profiles.png){width="600" zoomable="yes"}

1. Saisissez un nom de profil de produit, tel que _Utilisateurs B2B_.

1. Cliquez sur **[!UICONTROL Suivant]** puis sur **[!UICONTROL Enregistrer]**.

### Ajouter un groupe d’utilisateurs {#add-user-group}

Un groupe d’utilisateurs est un ensemble d’utilisateurs auxquels est accordé un ensemble partagé d’autorisations. Vous pouvez ajouter ou supprimer des utilisateurs dans votre groupe d’utilisateurs. Les autorisations de groupe restent les mêmes tandis que les utilisateurs du groupe changent.

Pour plus d’informations sur l’utilisation des groupes d’utilisateurs pour gérer les autorisations, voir [Gérer les groupes d’utilisateurs](https://helpx.adobe.com/business/enterprise/manage-users/user-groups.html){target="_blank"} dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système peut effectuer les étapes suivantes à partir de [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Sélectionnez l’onglet **[!UICONTROL Utilisateurs]**.

1. Sélectionnez **[!UICONTROL Groupes d’utilisateurs]** dans le volet de navigation de gauche.

1. Cliquez sur **[!UICONTROL Nouveau groupe d’utilisateurs]** en haut à droite.

1. Saisissez le nom du groupe d’utilisateurs, par exemple _Utilisateurs B2B_ et cliquez sur **[!UICONTROL Enregistrer]**.

   ![Admin Console - Ajout d’un groupe d’utilisateurs](./assets/admin-console-new-user-group.png){width="600" zoomable="yes"}

### Attribuer le profil de produit {#assign-profile}

![Exigences du rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur de produit peut effectuer les étapes suivantes à partir de [https://adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Cliquez sur le groupe d’utilisateurs que vous avez créé.

1. Sélectionnez l’onglet **[!UICONTROL Profils de produit attribués]** et cliquez sur **[!UICONTROL Attribuer un profil]**.

1. Cliquez sur **+** et ajoutez chaque instance des produits suivants :

   * [!UICONTROL Adobe Journey Optimizer B2B edition - Profil des utilisateurs]
   * [!UICONTROL Adobe Experience Platform - AEP-Default-All-Users]
   * [!UICONTROL Collecte De Données Adobe Experience Platform - Collecte De Données Par Défaut Tous Les Accès]
   * [!UICONTROL Adobe Experience Platform - Accès Tous À La Production Par Défaut]

   ![Admin Console - profils de produit pour le groupe d’utilisateurs](./assets/admin-console-product-profiles.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]**

### Ajouter des utilisateurs au nouveau groupe {#add-users}

Pour plus d’informations sur la gestion des utilisateurs, voir [_Utilisateurs de_](https://helpx.adobe.com/business/enterprise/manage-users/users.html){target="_blank"} dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur de produit peut effectuer les étapes suivantes à partir de [https://adminconsole.adobe.com](https://adminconsole.adobe.com). Un administrateur ou une administratrice de produit ne peut ajouter que des utilisateurs et utilisatrices qui existent déjà dans son organisation.

1. Si les utilisateurs ne sont pas déjà membres de votre organisation, ajoutez chaque utilisateur :

   * Sous _[!UICONTROL Liens rapides]_, cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

   * Saisissez l’adresse électronique de l’utilisateur et cliquez sur **[!UICONTROL Ajouter en tant que nouvel utilisateur]**.

     ![Admin Console - Ajouter un profil utilisateur pour le nouveau groupe](./assets/admin-console-user-group-add-users.png){width="600" zoomable="yes"}

   * Saisissez le prénom et le nom, puis cliquez sur **[!UICONTROL Enregistrer]**.

1. Ajoutez chaque utilisateur au groupe :

   * Cliquez sur le nom d’utilisateur.

   * Dans la page des détails de l’utilisateur, faites défiler l’écran jusqu’à **[!UICONTROL Groupes d’utilisateurs]**.

   * Cliquez sur l’icône _Plus_ ( **...** ) à gauche et choisissez **[!UICONTROL Modifier les groupes d’utilisateurs]**.

   * Cliquez sur l’icône _Ajouter_ ( **+** ) sous **[!UICONTROL Groupes d’utilisateurs]**.

     ![Admin Console - Sélection du groupe d’utilisateurs pour l’utilisateur](./assets/admin-console-user-edit-user-groups.png){width="600" zoomable="yes"}

   * Sélectionnez le groupe d’utilisateurs que vous avez créé précédemment et cliquez sur **[!UICONTROL Appliquer]**.

   * Cliquez sur **[!UICONTROL Enregistrer]** pour les modifications de l’utilisateur.

## Attribuer des autorisations de produit {#assign-product-permissions}

Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations attribuées à un profil de produit. Chaque autorisation est regroupée sous une fonctionnalité, telle que des parcours de personne ou du contenu, représentant les fonctionnalités de [!DNL Marketo Optimizer].

La zone _Autorisations_ de Adobe Experience Platform permet aux administrateurs de définir des rôles d’utilisateur et des politiques d’accès afin de gérer les autorisations d’accès aux fonctionnalités et objets d’une application de produit. Dans cette application, vous pouvez créer et gérer des rôles, ainsi qu’attribuer les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les sandbox et les utilisateurs associés à un rôle spécifique.

Pour plus d’informations sur les autorisations des rôles dans Experience Platform, voir [Gérer les autorisations pour un rôle](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions){target="_blank"} dans la documentation d’Experience Platform.

1. Accédez à [experience.adobe.com](https://experience.adobe.com/).

1. Dans le panneau _[!UICONTROL Accès rapide]_, sélectionnez **[!UICONTROL Autorisations]**.

   >[!NOTE]
   >
   >Si vous ne voyez pas _[!UICONTROL Autorisations]_, vous devrez peut-être cliquer sur **[!UICONTROL Afficher tout]** et le sélectionner dans les applications disponibles.

   ![Experience Platform - Autorisations d’accès](./assets/aep-permissions.png){width="700" zoomable="yes"}

### Autorisations {#permissions}

Les autorisations suivantes contrôlent l’accès aux fonctionnalités de configuration des canaux, de gestion de contenu et de parcours des personnes dans [!DNL Marketo Optimizer] :

| Catégorie | Autorisation | Description |
| -------- | ----------- | ---------- |
| Configurations du canal B2B | Afficher les paramètres d’e-mail B2B | Affichez les paramètres d’e-mail (sous-domaines, enregistrements PTR, groupes d’adresses IP, listes de suppression, listes de contrôle, plans de préchauffage d’adresses IP). |
| | Gérer les paramètres d’e-mail B2B | Configurez les paramètres d’e-mail (sous-domaines, enregistrements PTR, groupes d’adresses IP, listes de suppression, listes de contrôle, plans de préchauffage d’adresses IP). Ces paramètres sont requis avant que les utilisateurs puissent envoyer des e-mails. |
| | Gérer les configurations des canaux B2B | Accès à l’élément de menu _Canaux_ dans le volet de navigation de gauche et à toutes les opérations de configuration des canaux. |
| | Gestion des paramètres prédéfinis WhatsApp B2B | Créer, afficher et supprimer des préréglages de messages WhatsApp et les paramètres SMS associés. |
| Parcours B2B | Gérer Les Parcours De Personnes B2B | Accès à la liste Parcours de personne _et à toutes les opérations de parcours de personne._ |
| Assets B2B | Affichage des modèles de contenu | Afficher la liste et les détails des modèles de contenu. |
| | Gestion des modèles B2B | Créer, modifier et supprimer des modèles de contenu. |
| | Afficher les fragments B2B | Affichez la liste et les détails des fragments de contenu. |
| | Gestion des fragments B2B | Créer, modifier et supprimer des fragments de contenu. |
| | Publication De Fragments B2B | Publiez des fragments de contenu à utiliser dans des modèles, des e-mails et des pages de destination. |
| | Afficher Assets B2B | Affichez les détails de la bibliothèque et du fichier de ressource Assets. |
| | Gestion d’Assets B2B | Créer, modifier et supprimer des fichiers de ressources. |
| | Afficher les e-mails B2B | Afficher les e-mails. |
| | Gérer Les E-Mails B2B | Créer, modifier et supprimer des e-mails. |
| | Gérer L’Exportation Des Messages B2B | Exportez les rapports de messages sous la section E-mail . |
| Bibliothèque Journey Optimizer | Gestion des éléments de bibliothèque B2B | Ajouter et supprimer des expressions enregistrées dans la bibliothèque. |
| Gouvernance des données | Gérer les libellés d’utilisation de la suppression B2B | Afficher, créer et supprimer des libellés d’utilisation des données (DULE) appliqués aux jeux de données et aux schémas. |
| Sandbox Administration | Gestion des packages B2B | Créer, exporter, importer, copier et supprimer des packages sandbox. |

Pour fournir une prise en charge des destinations externes dans [!DNL Marketo Optimizer], les autorisations suivantes sont requises :

| Catégorie | Autorisation | Description |
| -------- | ----------- | ---------- |
| Tableaux de bord | Afficher les tableaux de bord standard | Accès en lecture seule aux tableaux de bord _Profils_, _Destinations_ et _Segments_. Permet également d’accéder à _Tableaux de bord_ dans le volet de navigation de gauche et dans l’onglet Inventaire et intégrations de _Tableaux de bord_. |
| | Gestion des tableaux de bord standard | Ajoutez des attributs personnalisés qui ne se trouvent pas encore dans l’entrepôt de données. |
| Destinations | Affichage des destinations | Accès en lecture seule pour afficher les destinations disponibles dans l’onglet _Catalogue_ et les destinations authentifiées dans l’onglet _Parcourir_. |
| | Gestion des destinations | Afficher, créer et supprimer des connexions de destinations et des comptes de destination. |
| | Activation des destinations | Activez les données vers des destinations actives. Pour accéder à cette fonction _vous devez également utiliser les options_ Afficher les destinations ou _Gérer les destinations_. |
| | Activer un segment sans mappage | Activez les audiences vers des destinations existantes, sans afficher l’étape de mappage. Les utilisateurs et utilisatrices peuvent ajouter et supprimer des audiences dans les workflows d’activation, mais ne peuvent pas ajouter ni supprimer des identités ou des attributs mappés. L’autorisation _Afficher les destinations_ est également requise pour accéder à cette fonction. |
| | Gérer et activer la destination du jeu de données | Affichez, créez, modifiez et désactivez les flux d’exportation des jeux de données, et activez les données dans les jeux de données actifs. L’autorisation _Afficher les destinations_ est également requise pour accéder à cette fonction. |
| | Création de destinations | Possibilité de créer des destinations à l’aide de Adobe Experience Platform Destination SDK. |
| Gouvernance des données | Affichage des politiques d’utilisation des données | Accès en lecture seule aux politiques d’utilisation des données appartenant à votre organisation. |
| | Gestion des politiques d’utilisation des données | Afficher, créer, modifier et supprimer des politiques d’utilisation des données. |
| Ingestion de données | Affichage des sources | Accès en lecture seule aux sources disponibles dans l’onglet _Catalogue_ et aux sources authentifiées dans l’onglet _Parcourir_. |
| | Gestion des sources | Afficher, créer, modifier et désactiver des sources. |
| Gestion des profils | Afficher les paramètres de profil | Accès en lecture seule à tous les paramètres de profil. |
| | Gérer les paramètres de profil | Afficher et modifier tous les paramètres de profil. |

<!--

### B2B built-in roles {#b2b-built-in-roles}

When your organization has [!DNL Journey Optimizer B2B Edition] provisioned, Experience Platform includes a set of built-in (default) roles that you can use to manage access to the product capabilities:

| Role | Permissions |
| ---- | ----------- |
| B2B Journey Manager | <li>Manage B2B Journeys <li>Manage B2B Buying Groups <li>Manage B2B Account Lists <li>View B2B Engagement Dashboard <li>View B2B Insights Dashboard |
| B2B Channel Manager | <li>Manage B2B Assets <li>Manage B2B Templates <li>Manage B2B Fragments |
| B2B System Administrator | <li>Manage B2B Channels Configurations <li>Manage B2B Admin Configurations |
| B2B Sales User | <li>View B2B Engagement Dashboard <li>View B2B Buying Groups <li>Access In-CRM Insights |

-->

### Modifier les autorisations de rôle {#edit-role-permissions}

Pour les rôles intégrés ou personnalisés, vous pouvez décider à tout moment d’ajouter ou de supprimer des autorisations. Si vous modifiez un rôle par défaut ou personnalisé, cela a un impact sur chaque utilisateur affecté au rôle.

>[!IMPORTANT]
>
>[!DNL Marketo Optimizer] accès nécessite l’activation d’un sandbox spécifique configuré selon la convention de nommage suivante : préfixe d’abonnement Marketo Engage + Prime. Par exemple, si le préfixe de votre abonnement Marketo Engage lié est _AcmeAssoc_, le sandbox requis pour [!DNL Marketo Optimizer] accès est _AcmeAssocPrime_.

>[!NOTE]
>
>Un administrateur système Admin Console peut effectuer les étapes suivantes.

_Pour modifier les autorisations d&#39;un rôle :_

1. Sélectionnez **[!UICONTROL Rôles]** dans le volet de navigation de gauche.

1. Cliquez sur le nom du rôle **_Gestionnaire de canaux B2B_**.

1. Dans la page de détails, cliquez sur **[!UICONTROL Modifier]** en haut à droite.

   ![Experience Platform - modifiez le rôle](./assets/aep-permissions-role-prime-edit.png){width="800" zoomable="yes"}

   Dans l’éditeur de rôles, le menu _[!UICONTROL Ressources]_ affiche la liste des ressources qui s’appliquent aux applications Experience Cloud optimisées par Platform.

1. Sélectionnez le sandbox configuré pour l’accès [!DNL Marketo Optimizer] (`<Marketo subscription prefix>Prime`).

   ![Experience Platform - ajouter des sandbox pour le nouveau rôle](./assets/aep-permissions-role-prime-sandbox.png){width="800" zoomable="yes"}

1. Cliquez sur l’icône _Ajouter_ (**+**) pour chacune des ressources B2B.

   ![Experience Platform - Ressource Parcours B2B ajoutée au rôle de responsable de canal](./assets/aep-permissions-b2b-list.png){width="700" zoomable="yes"}

1. Ajoutez les autorisations spécifiques à chacune des ressources ou sélectionnez **[!UICONTROL Tout ajouter]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**

   <!-- ![Experience Platform - B2B Journeys permissions saved for Channel Manager role](assets/aep-permissions-role-edit-b2b-journeys-done.png){width="700" zoomable="yes"} -->

1. Cliquez sur **[!UICONTROL Fermer]** pour revenir à la page de détails.

### Ajouter des utilisateurs à un rôle {#add-users-to-a-role}

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur Experience Platform peut effectuer les étapes suivantes.

1. Ouvrez les détails du rôle et sélectionnez l’onglet **[!UICONTROL Utilisateurs]**.

   Cet onglet affiche une liste de tous les utilisateurs affectés au rôle.

1. Cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

   ![Experience Platform - ajouter des utilisateurs au rôle](./assets/aep-permissions-role-prime-add-users.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des utilisateurs]_, recherchez et sélectionnez les utilisateurs que vous souhaitez ajouter au rôle.

   * Vous pouvez utiliser l’outil de recherche pour filtrer la liste des utilisateurs.

   * Cochez la case correspondant à chaque personne.

   ![Experience Platform - Boîte de dialogue Ajouter des utilisateurs](assets/aep-permissions-role-add-users-dialog.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez sélectionné tous les utilisateurs à ajouter.

### Ajouter des groupes d’utilisateurs à un rôle {#add-user-groups-to-a-role}

Pour plus d’informations sur la gestion des utilisateurs, voir [_Utilisateurs de_](https://helpx.adobe.com/business/enterprise/manage-users/users.html){target="_blank"} dans la documentation d’Admin Console.

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur Experience Platform peut effectuer les étapes suivantes.

1. Ouvrez les détails du rôle et sélectionnez l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

   Cet onglet affiche la liste de tous les groupes d’utilisateurs affectés au rôle.

1. Cliquez sur **[!UICONTROL Ajouter des groupes]**.

   ![Experience Platform - ajouter des groupes au rôle](./assets/aep-permissions-role-prime-add-groups.png){width="800" zoomable="yes"}

1. Dans la boîte de dialogue _[!UICONTROL Ajouter des groupes]_, recherchez et sélectionnez les groupes à ajouter au rôle.

   * Vous pouvez utiliser l’outil Rechercher pour filtrer la liste des groupes d’utilisateurs.

   * Cochez la case de chaque groupe d’utilisateurs.

   ![Experience Platform - Boîte de dialogue Ajouter des groupes](assets/aep-permissions-role-add-groups-dialog.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez sélectionné tous les groupes à ajouter.

### Créer un rôle personnalisé {#create-a-custom-role}

![Exigences relatives au rôle d’administrateur](../assets/do-not-localize/icon-admin-user.svg){width="30"} Un administrateur système ou un administrateur Experience Platform peut effectuer les étapes suivantes.

1. Sélectionnez **[!UICONTROL Rôles]** dans le volet de navigation de gauche, puis sélectionnez **[!UICONTROL Créer un rôle]**.

1. Dans la boîte de dialogue _[!UICONTROL Créer un nouveau rôle]_, saisissez un nom pour le rôle, tel que _Spécialistes du marketing B2B_, ainsi qu’une description (facultatif).

1. Cliquez sur **[!UICONTROL Confirmer]**.

1. Sélectionnez le sandbox configuré pour l’accès [!DNL Marketo Optimizer] (`<Marketo subscription prefix>Prime`).

   ![Experience Platform - ajouter des sandbox pour le nouveau rôle](./assets/aep-permissions-role-prime-sandbox.png){width="800" zoomable="yes"}

1. Ajoutez les autorisations de produit B2B :

   Pour déterminer les fonctionnalités de produit souhaitées pour le rôle, reportez-vous à la liste des [autorisations de produit](#permissions).

   Dans la liste _[!UICONTROL Ressources]_ sur la gauche, localisez les éléments B2B et cliquez sur l’icône _Ajouter_ (**+**) pour ajouter chaque attribut que vous souhaitez activer pour le rôle.

   Vous pouvez saisir _B2B_ dans l’outil de recherche pour filtrer la liste de nombreuses autorisations de produits B2B.

   ![Experience Platform - Autorisations B2B](./assets/aep-permissions-b2b-list.png){width="700" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Enregistrer]** en haut à droite.

1. Accédez aux détails du rôle et sélectionnez l’onglet **[!UICONTROL Groupes d’utilisateurs]**.

1. Cliquez sur **[!UICONTROL Ajouter des groupes]**.

1. Cochez la case en regard du groupe d’utilisateurs que vous avez créé précédemment dans Admin Console.

1. Cliquez sur **[!UICONTROL Enregistrer]**

Votre rôle personnalisé est configuré et les utilisateurs du groupe affecté peuvent désormais accéder aux fonctionnalités [!DNL Marketo Optimizer] que vous avez sélectionnées.
