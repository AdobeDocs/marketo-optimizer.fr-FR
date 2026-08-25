---
title: Webinaires interactifs
description: Découvrez les concepts sous-jacents aux webinaires interactifs dans Marketo Optimizer, notamment le modèle de ressource du webinaire, les États membres, les jetons et les activités.
keywords: 
role: User
feature: Channels
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 75b481faf0d66210329f95c8afabdfa59e7bcb79
workflow-type: tm+mt
source-wordcount: 1085
ht-degree: 2%

---


# Webinaires interactifs

Les webinaires interactifs vous permettent de planifier, de promouvoir, de diffuser et de suivre un webinaire en direct ou en direct simulé sans quitter [!DNL Adobe Marketo Optimizer]. La diffusion s’exécute sur [!DNL Adobe Connect] automatiquement. Vous n’avez donc jamais à changer de produit pour concevoir une page d’inscription, héberger la session en direct ou extraire les données de présence.

>[!NOTE]
>
>Cette fonctionnalité nécessite une licence et est soumise à des conditions générales supplémentaires. Pour en savoir plus sur les conditions générales supplémentaires, consultez votre contrat ou contactez Adobe.

Vous pouvez créer un webinaire de deux manières :

* **Expérience de conversation** - Demandez au collègue de planifier, de promouvoir et de créer un rapport sur un webinaire en langage naturel. Voir [Créer des webinaires avec un collègue](../agents/webinar-creation.md).

* **Pointer-cliquer** - Utilisez l’espace de travail _[!UICONTROL Programmes]_ pour ajouter une ressource de webinaire, la concevoir, ajouter des co-hôtes et des présentateurs, créer des parcours de promotion et de suivi, et consulter les rapports. Voir [Création et conception d’un webinaire](create-webinar.md) et [parcours de promotion et de suivi de webinaires](webinar-journeys.md).

## Webinaire en tant que ressource

Un webinaire est une ressource appartenant à un [programme](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/prime/marketing-management/programs/programs), de la même manière qu’un e-mail ou une page de destination. L’ajout d’un webinaire à un programme l’y enregistre et rend ses jetons, attributs et activités disponibles pour chaque parcours et ressource de ce programme.

>[!IMPORTANT]
>
>Un programme peut actuellement posséder une ressource de webinaire. La prise en charge de plusieurs webinaires par programme est prévue pour une version ultérieure.

## Etats membres

Pour toute personne qui est membre d&#39;un programme qui contient un webinaire, trois états indépendants s&#39;appliquent en même temps. Chaque peut être référencé séparément dans les audiences et les conditions de parcours.

| État | Propriétaire | Valeurs |
|---|---|---|
| Statut de membre du programme | Programme | Configurable par [type de programme](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/prime/admin/program-types) |
| État du webinaire | Ressource de webinaire | Invité, Inscrit, Participé, Pas d&#39;affichage, Sur demande |
| état du parcours | Parcours | Nœud actuel, en pause, terminé et autres états d’exécution de parcours |

### Statut du webinaire

Le statut du webinaire comporte cinq valeurs. [!DNL Adobe Connect] définit normalement la valeur automatiquement, mais vous pouvez également définir le statut avec une action de parcours si vous devez la remplacer. Pour refléter l’assiduité enregistrée dans un autre système, par exemple, vous pouvez définir le statut dans votre parcours.

| Statut | Méthode de définition | Source |
|---|---|---|
| Invité | Un nœud de parcours _Prendre une mesure_, généralement lorsque l’e-mail d’invitation envoie | Contrôlé par l’auteur |
| Inscrit | Nœud de parcours _Prendre une action_ lorsque la personne s’enregistre. Cela déclenche également la [!DNL Adobe Connect] de générer l’URL de recrutement de la personne | Contrôlé par l’auteur |
| A participé | Un événement de [!DNL Adobe Connect] après l’exécution du webinaire en direct | Contrôlé par le système, avec remplacement de l’auteur disponible via un parcours |
| Ne Pas Afficher | Un événement de [!DNL Adobe Connect] après l’exécution du webinaire en direct | Contrôlé par le système, avec remplacement de l’auteur disponible via un parcours |
| A participé à la demande | Un événement de [!DNL Adobe Connect] où une personne qui n&#39;était pas présente regarde l&#39;enregistrement en direct plus tard | Contrôlé par le système, avec remplacement de l’auteur disponible via un parcours |

>[!IMPORTANT]
>
>Qu’il soit défini automatiquement ou à partir d’un parcours, le statut du webinaire ne bouge que dans une seule direction, de la même manière que le [statut du programme](./programs.md#statuses). Une personne peut passer à un état ultérieur (par exemple, _Enregistré_ à _Terminé_), mais pas revenir à un état antérieur. Planifiez le remplacement de l’auteur en gardant à l’esprit cette progression linéaire.

Pour déplacer une personne entre les états d’un parcours, utilisez l’action **[!UICONTROL Modifier le statut du membre du webinaire]**. Voir parcours de promotion et de suivi de webinaires](webinar-journeys.md).[

## Jetons de webinaire

Les jetons de webinaire sont disponibles partout où vous personnalisez le contenu d’un e-mail (objet, corps, pré-titre et expéditeur). Recherchez-les dans l’éditeur de personnalisation sous **_Contexte > Webinaire_**.

Les jetons au niveau de la ressource se trouvent directement dans le dossier du webinaire :

- Titre
- Description
- Start datetime, end datetime
- Durée
- Fuseau horaire
- Présentateurs et présentatrices
- URL d’enregistrement

>[!NOTE]
>
>Les co-hôtes sont affichés dans la section Équipe de webinaires de la page du webinaire, mais ne sont pas disponibles en tant que jeton de personnalisation.

Les jetons par destinataire résident dans un sous-dossier **Membre** :

- **Statut** - Statut actuel du webinaire du destinataire (Invité, Enregistré, Avec participation, Sans affichage ou Avec participation à la demande). Voir [ Statut du webinaire ](#webinar-status).
- **URL d’inscription** - Lien [!DNL Adobe Connect] personnel du destinataire. Ce problème est résolu uniquement après l’enregistrement de l’état du webinaire du destinataire, ou à une date ultérieure. Il se résout comme vide pour quiconque à un stade antérieur.
- **URL d’enregistrement** - Se résout après la publication de l’enregistrement après la session active et reste vide jusqu’à ce moment-là. Utilisez-le de manière conditionnelle dans les e-mails postérieurs au webinaire afin qu’un lien n’apparaisse pas avant qu’un enregistrement ne soit à afficher.

>[!NOTE]
>
>Les jetons de webinaire s’affichent actuellement dans le contenu de l’e-mail uniquement (objet, corps, pré-titre et expéditeur). La prise en charge des jetons de webinaire dans les pages de destination et les formulaires est prévue pour une version ultérieure.
>
>Comme ces jetons sont résolus comme vides plutôt que de générer une erreur, un e-mail ou une page qui y fait référence est rendu en toute sécurité à tout moment du cycle de vie du webinaire. Prévisualisez le contenu avant et après la disponibilité des valeurs pour confirmer que la mise en page s’affiche correctement, dans les deux cas.

## Activités de webinaire

Chaque webinaire signale automatiquement les activités que vous pouvez utiliser comme _Écouter l’événement_ les déclencheurs, _Chemin de partage_ les conditions, les filtres d’audience et les mesures de rapports :

* Pose une question
* Répond à une enquête
* Clique sur un lien
* Télécharge une ressource
* Lève une main

>[!NOTE]
>
>Les modifications du statut du webinaire (Invité, Inscrit, Avec participation, Sans affichage, Avec participation à la demande) ne sont actuellement pas disponibles en tant que leur propre filtre _Écouter l’événement_ déclencheur ou activité. Pour créer une branche d’un parcours selon le statut du webinaire, utilisez une condition _Chemin de partage_ directement sur l’état du webinaire (décrite dans [_Création d’un parcours après le webinaire_](webinar-journeys.md#build-post-webinar-journey)) plutôt que d’écouter une activité de changement d’état.

L’engagement des personnes qui regardent l’enregistrement après l’événement en direct est assimilé aux mêmes activités, balisées avec un mode À la demande. Contrairement aux activités, l’engagement à la demande crée un état de webinaire distinct : une personne qui n’a pas assisté en direct et qui regarde ensuite l’enregistrement passe de **Pas d’affichage** à **Participé à la demande**.

## Conditions préalables

Avant de commencer à créer un webinaire, assurez-vous que les éléments suivants sont en place.

| Prérequis | Détails |
|---|---|
| Un programme | Le webinaire est ajouté dans un programme existant. En règle générale, un analyste des opérations marketing commence par créer le programme. |
| Licence de webinaire (capacité) | Une licence pour webinaire, également appelée « droit de capacité », doit être disponible avant de pouvoir planifier un webinaire. Vous choisissez une capacité au moment de la configuration et des modules complémentaires de capacité supérieure peuvent être disponibles. Pour augmenter la capacité disponible, contactez votre équipe de compte Adobe. |
| [!DNL Adobe Connect] | La diffusion s’exécute en [!DNL Adobe Connect]. L’approvisionnement se produit automatiquement en arrière-plan. Vous n’avez pas besoin de quitter [!DNL Marketo Optimizer] pour créer ou héberger un webinaire. |

### Autorisations

L’accès aux fonctionnalités des webinaires dépend des autorisations que vous avez attribuées pour les webinaires.

| Rôle | Ce qu&#39;il accorde |
|---|---|
| Afficher les webinaires B2B | Consultez la liste des webinaires, ainsi qu’une configuration, des détails et des rapports de webinaire. Les contrôles de création, de conception, de modification et de saisie ne sont pas disponibles via cette autorisation, et vous ne pouvez pas être affecté à un webinaire en tant que co-hôte ou présentateur. |

<!-- 
| Manage B2B webinars | Full lifecycle access: create, design, configure, schedule, edit, deliver, host, and delete a webinar. The Create, Design, Edit, and Manage controls are available only for users with this role. |
| Webinar co-host | After you are added as a co-host, this permission enables you to design and enter that webinar with co-host controls. |
| Webinar presenter | After you are added as a presenter, this permission enables you to view and enter that webinar with presenter capabilities. It grants no authoring or design access on its own. |

>[!NOTE]
>
>Co-hosts and presenters are currently defined by entering a name and email rather than selected from a picker of role-eligible users — see [Add co-hosts and presenters](create-webinar.md#add-co-hosts-and-presenters). The _Webinar co-host_ and _Webinar presenter_**_ roles still govern what that person can do when they are added as a co-host or presenter.

-->
