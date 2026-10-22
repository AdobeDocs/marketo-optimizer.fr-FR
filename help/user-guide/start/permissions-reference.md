---
title: Autorisations de produit
description: Liste de référence des autorisations Experience Platform qui contrôlent l’accès aux fonctionnalités de Marketo Optimizer, avec des descriptions et des autorisations recommandées pour les utilisateurs administrateurs, en accès complet et en lecture seule.
TQID: https://experienceleague.adobe.com/Q4HnGxPkiE0dsZUjIgPvVJHgs0dPwLJiOKVSL1edS4Y
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
    internal-label: Marketo Optimizer
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
    internal-label: Setup
  - id: a659ad61-de21-559d-a901-02e2fb329ff5
    internal-label: Administration
subfeature_v2:
  - id: b6434e31-d7bb-5416-960c-1c77bb1a2e8d
    internal-label: User Access
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
autotag-review: '2026-10-20T17:03:48.312Z'
source-git-commit: a33f749c32631dcd77ecf2892bdc3b1a5e06cd66
workflow-type: tm+mt
source-wordcount: '1556'
ht-degree: 6%
---
# Autorisations de produit

Les autorisations suivantes contrôlent l’accès aux fonctionnalités de [!DNL Adobe Marketo Optimizer]. Ajoutez-les aux rôles dans la zone _[!UICONTROL Autorisations]_ de [!DNL Adobe Experience Platform]. Pour plus d’informations sur la création de rôles et leur affectation à des utilisateurs, voir [_Accès et autorisations utilisateur_](./user-management.md).

Les trois dernières colonnes indiquent les autorisations recommandées pour chacun des [types d’utilisateurs suggérés](#suggested-user-types) : Admin, Tous les utilisateurs avec accès et Utilisateur avec accès en lecture seule. Une coche (✔) signifie que l’autorisation est recommandée pour ce type d’utilisateur et un tiret (-) signifie que ce n’est pas le cas. Ajustez les recommandations en fonction de votre organisation.

>[!IMPORTANT]
>
>[!DNL Marketo Optimizer] accès nécessite l’activation d’un sandbox spécifique configuré selon la convention de nommage suivante : `Mktoaep` + préfixe d’abonnement [!DNL Marketo Engage]. Par exemple, si le préfixe de votre abonnement [!DNL Marketo Engage] lié est _AcmeAssoc_, le sandbox requis pour l’accès [!DNL Marketo Optimizer] est _MktoaepAcmeAssoc_. Ajoutez ce sandbox à chaque rôle.

>[!NOTE]
>
>Vous devez être administrateur système pour voir la mosaïque _[!UICONTROL Autorisations]_ dans Experience Platform.

Certaines autorisations s’appliquent aux fonctionnalités qui ne sont pas encore disponibles dans le produit. Les administrateurs peuvent ajouter ces autorisations maintenant afin que les utilisateurs disposent de l’accès applicable lorsque les fonctionnalités seront disponibles.

## Types d’utilisateurs suggérés {#suggested-user-types}

Utilisez les recommandations d’autorisations dans les tableaux de cette page comme point de départ pour les rôles que vous créez. Voici des suggestions pour chaque type d’utilisateur. Ajustez-les en fonction de votre organisation.

| Attribut | Administration | All Access User | Utilisateur d&#39;accès en lecture seule |
| --- | ----- | --------------- | --------------------- |
| **À qui est-ce destiné** | Les personnes qui configurent et gèrent les [!DNL Marketo Optimizer] pour votre équipe. | Les professionnels du marketing et les opérateurs qui travaillent chaque jour sur [!DNL Marketo Optimizer]. | Les personnes qui ont besoin de voir des [!DNL Marketo Optimizer], mais qui n’ont rien à changer, comme les cadres, les analystes et les auditeurs. |
| **Ce qu&#39;ils peuvent faire** | Tout, y compris les paramètres d’installation et d’administration. | Utilisez toutes les fonctionnalités : parcours, programmes, contenu, listes, rapports et l’assistant. | Affichez les parcours, les programmes, le contenu, les listes et les rapports, et posez des questions à l&#39;assistant. |
| **Autorisations à attribuer** | Chaque autorisation sur cette page (sélectionnez **[!UICONTROL Ajouter tout]** dans l’éditeur de rôles). | Autorisations avec un ✔ dans la colonne _Tous les accès_ des tables de cette page. | Autorisations avec un ✔ dans la colonne _Lecture seule_ des tableaux de cette page. |
| **Non inclus** | – | <li>Configurations d’administration<li>Configurations de canal, y compris les paramètres d’e-mail, les paramètres prédéfinis de formulaire, les paramètres de page de destination et les paramètres prédéfinis et les paramètres WhatsApp<li>Types de programmes (affichage et gestion) | <li>Création, modification, suppression, publication ou exportation (toutes les autorisations _Gérer_ et _Publier_, à l’exception de l’accès aux conversations)<li>Activation des audiences vers les destinations<li>Configurations d’administration et configurations de canal, y compris l’affichage des paramètres d’e-mail et des préréglages de formulaire<li>Affichage des types de programmes |
| **Groupe d’utilisateurs suggéré** | Groupe d’administrateurs Marketo Optimizer | Groupe d’utilisateurs Marketo Optimizer | Groupe d’utilisateurs en lecture seule Marketo Optimizer |
| **Rôle suggéré** | Administrateur Marketo Optimizer | Utilisateur Marketo Optimizer All Access | Utilisateur d’accès en lecture seule Marketo Optimizer |

Pour connaître la procédure de création de ces groupes et rôles, voir [&#x200B; Création de groupes d’utilisateurs et de rôles pour les types d’utilisateurs suggérés &#x200B;](./user-management.md#create-suggested-roles).

## Contenu et ressources {#content-assets}

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Assets B2B | Gestion d’Assets B2B | Créer, modifier et supprimer des fichiers de ressources. | ✔ | ✔ | – |
| | Gérer Les E-Mails B2B | Créer, modifier et supprimer des e-mails. | ✔ | ✔ | – |
| | Gérer le Forms B2B | Créer, modifier et supprimer des formulaires. | ✔ | ✔ | – |
| | Gestion des fragments B2B | Créer, modifier et supprimer des fragments de contenu. | ✔ | ✔ | – |
| | Gérer la page de destination B2B | Créer, modifier et supprimer des pages de destination. | ✔ | ✔ | – |
| | Gérer L’Exportation Des Messages B2B | Exportez les rapports de messages sous la section _E-mail_. | ✔ | ✔ | – |
| | Gestion des modèles B2B | Créer, modifier et supprimer des modèles de contenu. | ✔ | ✔ | – |
| | Gérer Les Webinaires B2B | Créer, modifier et supprimer des webinaires interactifs. | ✔ | ✔ | – |
| | Publication de Forms B2B | Publiez des formulaires à utiliser dans des pages de destination. | ✔ | ✔ | – |
| | Publication De Fragments B2B | Publiez des fragments de contenu à utiliser dans des modèles, des e-mails et des pages de destination. | ✔ | ✔ | – |
| | Publier une page de destination B2B | Publiez des pages de destination. | ✔ | ✔ | – |
| | Afficher Assets B2B | Affichez les détails de la bibliothèque et du fichier de ressource Assets. | ✔ | ✔ | ✔ |
| | Afficher les e-mails B2B | Afficher les e-mails. | ✔ | ✔ | ✔ |
| | Afficher le Forms B2B | Affichez les formulaires. | ✔ | ✔ | ✔ |
| | Afficher les fragments B2B | Affichez la liste et les détails des fragments de contenu. | ✔ | ✔ | ✔ |
| | Afficher la page de destination B2B | Affichez les pages de destination. | ✔ | ✔ | ✔ |
| | Afficher les modèles B2B | Afficher la liste et les détails des modèles de contenu. | ✔ | ✔ | ✔ |
| | Afficher les webinaires B2B | Visionnez des webinaires interactifs. | ✔ | ✔ | ✔ |

## Configuration et administration des canaux {#channels-admin}

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Configurations de l’administration B2B | Gérer les configurations d’administration B2B | Configurez les paramètres d’administration, tels que les connexions de gestion des ressources numériques, les référentiels de ressources et les événements. | ✔ | – | – |
| Configurations du canal B2B | Gérer les configurations des canaux B2B | Accès à l’élément de menu _Canaux_ dans le volet de navigation de gauche et à toutes les opérations de configuration des canaux. | ✔ | – | – |
| | Gérer les paramètres d’e-mail B2B | Configurez les paramètres d’e-mail. Ces paramètres sont requis avant que les utilisateurs puissent envoyer des e-mails. | ✔ | – | – |
| | Gérer les paramètres prédéfinis de Forms B2B | Créer, modifier et supprimer des paramètres prédéfinis de formulaire. | ✔ | – | – |
| | Gérer Les Paramètres De La Page De Destination B2B | Configurez les paramètres de la page de destination, tels que les sous-domaines. | ✔ | – | – |
| | Gestion des paramètres prédéfinis WhatsApp B2B | Créer, afficher et supprimer des préréglages de messages WhatsApp et les paramètres SMS associés. | ✔ | – | – |
| | Gérer les paramètres WhatsApp B2B | Configurez les paramètres du canal WhatsApp. | ✔ | – | – |
| | Publication D’Un Préréglage Forms B2B | Publiez des paramètres prédéfinis de formulaire. | ✔ | – | – |
| | Afficher les paramètres d’e-mail B2B | Affichez les paramètres d’e-mail (sous-domaines, enregistrements PTR, groupes d’adresses IP, listes de suppression, listes de contrôle, plans de préchauffage d’adresses IP). | ✔ | – | – |
| | Afficher le paramètre prédéfini Forms B2B | Affichage des paramètres prédéfinis de formulaire. | ✔ | – | – |

## Parcours, programmes et dossiers {#journeys-programs}

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Jetons de dossier B2B | Gérer les jetons de dossier B2B | Créer, modifier et supprimer des jetons dans des dossiers. Les modifications s’appliquent à tous les éléments du dossier. Affectez-les donc séparément de _Gérer les dossiers B2B_. | ✔ | ✔ | – |
| | Affichage Des Jetons De Dossier B2B | Afficher les jetons définis sur les dossiers. | ✔ | ✔ | ✔ |
| Dossiers B2B | Gestion des dossiers B2B | Créer, modifier et supprimer des dossiers. | ✔ | ✔ | – |
| | Afficher les dossiers B2B | Afficher les dossiers. | ✔ | ✔ | ✔ |
| Parcours B2B | Gestion du contrôle du trafic du Parcours B2B | Configurez le contrôle du trafic de parcours, y compris en simulant son effet. | ✔ | ✔ | – |
| | Gérer Les Parcours De Personnes B2B | Accès à la liste Parcours de personne _et à toutes les opérations de parcours de personne._ | ✔ | ✔ | – |
| | Publier des Parcours de personne B2B | Publiez les parcours de personne. | ✔ | ✔ | – |
| | Afficher le contrôle du trafic du Parcours B2B | Affichez les paramètres de contrôle du trafic du parcours. | ✔ | ✔ | ✔ |
| | Afficher les rapports de Parcours de personnes B2B | Affichez les rapports de parcours de personne, y compris le rapport _Personne Parcours Individu_. | ✔ | ✔ | ✔ |
| | Afficher les Parcours de personne B2B | Accès en lecture seule à la liste Parcours de personne _et aux détails du parcours._ | ✔ | ✔ | ✔ |
| Jetons de programme B2B | Gérer Les Jetons De Programme B2B | Créer, modifier et supprimer des jetons sur les programmes et les types de programmes. | ✔ | ✔ | – |
| | Affichage Des Jetons De Programme B2B | Afficher les jetons définis sur les programmes et les types de programmes. | ✔ | ✔ | ✔ |
| Types de programmes B2B | Gérer les types de programmes B2B | Créer, modifier et supprimer des types de programmes marketing. | ✔ | – | – |
| | Afficher les types de programmes B2B | Affichez les types de programmes marketing. | ✔ | – | – |
| Programmes B2B | Gestion des programmes B2B | Créer, modifier et supprimer des programmes marketing. | ✔ | ✔ | – |
| | Afficher les programmes B2B | Afficher les programmes marketing. | ✔ | ✔ | ✔ |

## Audiences, intention et destinations {#audiences-intent}

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Destinations B2B | Activer les destinations B2B | Activez les audiences vers des destinations B2B. | ✔ | ✔ | – |
| | Gérer les destinations B2B | Créer, modifier et supprimer des destinations B2B. | ✔ | ✔ | – |
| | Afficher les destinations B2B | Accès en lecture seule aux destinations B2B. | ✔ | ✔ | ✔ |
| Configuration de l’intention B2B | Gérer la configuration d’intention B2B | Créez, modifiez et supprimez des configurations d’intention. | ✔ | ✔ | – |
| | Afficher la configuration d’intention B2B | Affichez les configurations d’intention (modèles de pondération d’intention). | ✔ | ✔ | ✔ |
| Règles d’organisation B2B | Gestion des règles d’organisation B2B | Créer, modifier et supprimer des règles d’organisation. | ✔ | ✔ | – |
| | Afficher les règles d’organisation B2B | Afficher les règles d&#39;organisation. | ✔ | ✔ | ✔ |
| Listes de personnes B2B | Gérer Les Listes De Personnes B2B | Créer, modifier et supprimer des listes de personnes et gérer l’appartenance à une liste. | ✔ | ✔ | – |
| | Afficher Les Listes De Personnes B2B | Affichez des listes de personnes statiques et dynamiques. | ✔ | ✔ | ✔ |

## Rapports, laboratoires et conversations {#reports-labs-chat}

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Expérience de conversation B2B | Gérer L’Expérience Conversationnelle B2B | Accès au panneau de conversation et à l’assistant. Les actions du panneau nécessitent également l’autorisation de la fonctionnalité correspondante. Par exemple, la création d’un parcours nécessite _Gérer les Parcours de personne B2B_. Voir [Autorisations de conversation](#chat-permissions). | ✔ | ✔ | ✔ |
| Laboratoires B2B | Gestion des laboratoires B2B | Activez et configurez les fonctionnalités de Labs. | ✔ | ✔ | – |
| | Afficher les laboratoires B2B | Affichez les fonctionnalités de Labs disponibles et activées. | ✔ | ✔ | ✔ |
| Rapports B2B | Affichage des rapports incorporés B2B | Affichez les rapports dans l’onglet _Rapports_. | ✔ | ✔ | ✔ |
| | Afficher les rapports d’intention B2B | Afficher les rapports d’intention. | ✔ | ✔ | ✔ |

## Autorisations de conversation {#chat-permissions}

Les autorisations de conversation suivent les autorisations au niveau des fonctionnalités. [!DNL Coworker for Marketo Optimizer] vérifie chaque compétence ou action dans la conversation par rapport à la même autorisation dont la fonctionnalité a besoin en dehors de la conversation : _Gérer_ autorisations de création, de modification ou de publication, et _Afficher_ autorisations pour les compétences en lecture seule. Si un utilisateur ne dispose pas de l’autorisation de fonctionnalité, [!DNL Coworker] ne pouvez pas effectuer cette action pour lui. Par exemple, la création d’un parcours nécessite _Gérer les Parcours de personne B2B_ et la liste des formulaires nécessite _Afficher le Forms B2B_.

<!--
_Manage B2B Conversational Experience_ gives access to the [!DNL CX Coworker] chat panel, but it does not grant access to any feature functions.

Per wiki: 
Update 10/02: We are no longer mapping b2b-conversational-experience read or write to any tools. It was decided that chat will be available for all users without permissions, but what they can do within the chat (i.e. tools they can use) will be defined by other permissions.
-->

## Autorisations des destinations externes {#external-destinations-permissions}

Pour permettre aux utilisateurs d’[!DNL Marketo Optimizer] d’accéder aux destinations externes, les autorisations suivantes sont requises. Les colonnes suivent les mêmes recommandations pour chaque type d’utilisateur décrit dans [Types d’utilisateur suggérés](#suggested-user-types).

| Catégorie | Autorisation | Description | Administration | Tous les accès | Lecture seule |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Tableaux de bord | Gestion des tableaux de bord standard | Ajoutez des attributs personnalisés qui ne se trouvent pas encore dans l’entrepôt de données. | ✔ | ✔ | – |
| | Afficher les tableaux de bord standard | Accès en lecture seule aux tableaux de bord _Profils_, _Destinations_ et _Segments_. Permet également d’accéder à _Tableaux de bord_ dans le volet de navigation de gauche. | ✔ | ✔ | ✔ |
| Destinations | Activation des destinations | Activez les données vers des destinations actives. _Afficher les destinations_ ou _Gérer les destinations_ est également obligatoire. | ✔ | ✔ | – |
| | Activer un segment sans mappage | Activez les audiences vers des destinations existantes sans l’étape de mappage. Les utilisateurs et utilisatrices peuvent ajouter et supprimer des audiences dans les workflows d’activation, mais ne peuvent pas ajouter ni supprimer des identités ou des attributs mappés. _Afficher les destinations_ est également obligatoire. | ✔ | ✔ | – |
| | Création de destinations | Créez des destinations à l’aide d’Experience Platform Destination SDK. | ✔ | ✔ | – |
| | Gérer et activer la destination du jeu de données | Affichez, créez, modifiez et désactivez les flux d’exportation des jeux de données, et activez les données dans les jeux de données. _Afficher les destinations_ est également obligatoire. | ✔ | ✔ | – |
| | Gestion des destinations | Afficher, créer et supprimer des connexions de destinations et des comptes de destination. | ✔ | ✔ | – |
| | Affichage des destinations | Affichez les destinations disponibles dans l’onglet _Catalogue_ et les destinations authentifiées dans l’onglet _Parcourir_. | ✔ | ✔ | ✔ |
| Gouvernance des données | Gérer les libellés d’utilisation de la suppression B2B | Afficher, créer et supprimer des libellés d’utilisation des données (DULE) appliqués aux jeux de données et aux schémas. | ✔ | ✔ | – |
| | Gestion des politiques d’utilisation des données | Afficher, créer, modifier et supprimer des politiques d’utilisation des données. | ✔ | ✔ | – |
| | Affichage des politiques d’utilisation des données | Accès en lecture seule aux politiques d’utilisation des données appartenant à votre organisation. | ✔ | ✔ | ✔ |
| Ingestion de données | Gestion des sources | Afficher, créer, modifier et désactiver des sources. | ✔ | ✔ | – |
| | Affichage des sources | Affichez les sources disponibles dans l’onglet _Catalogue_ et les sources authentifiées dans l’onglet _Parcourir_. | ✔ | ✔ | ✔ |
| Gestion des profils | Gérer les paramètres de profil | Afficher et modifier tous les paramètres de profil. | ✔ | ✔ | – |
| | Afficher les paramètres de profil | Accès en lecture seule à tous les paramètres de profil. | ✔ | ✔ | ✔ |

<!-- 

## Planned permissions {#planned-permissions}

The following permissions are for features that are not yet available in [!DNL Marketo Optimizer]. Adobe Marketo Qualifier permissions are not currently enforced. The estimated enforcement date is November 2026. Accounts and buying groups are targeted for delivery in Q1 2027.

| Category | Permission | Description | Admin | All Access | Read Only |
| -------- | ---------- | ----------- | :---: | :--------: | :-------: |
| Marketo Qualifier Configurations | Manage Marketo Qualifier Configurations | Create, edit, and delete Marketo Qualifier configurations. | ✔ | – | – |
| | View Marketo Qualifier Configurations | View Marketo Qualifier configurations. | ✔ | ✔ | ✔ |
| Marketo Qualifier Outbound | View Marketo Qualifier Outbound | View Marketo Qualifier outbound workflows and outbound reporting. | ✔ | ✔ | ✔ |
| Marketo Qualifier Research | Manage Marketo Qualifier Research | Use and manage research capabilities. | ✔ | ✔ | – |
| | View Marketo Qualifier Research | View research: conversational interface, prospect view, and account and lead research. | ✔ | ✔ | ✔ |
| B2B Account Lists | Manage B2B Account Lists | Create, edit, and delete account lists, including adding, removing, and importing accounts. | ✔ | ✔ | – |
| B2B Buying Groups | Manage B2B Buying Groups | Create, edit, and delete buying groups. | ✔ | ✔ | – |
| | Manage B2B Role Templates | Manage the role templates used in buying groups. | ✔ | ✔ | – |
| | Manage B2B Solution Interests | Manage the solution interests used in buying groups. | ✔ | ✔ | – |
| | Manage B2B Stages | Manage buying group stages. | ✔ | ✔ | – |
| | View B2B Buying Groups | View buying groups. | ✔ | ✔ | ✔ |

-->
