---
title: Types de programmes
description: Créez et gérez des types de programmes qui définissent les attributs et les flux de statut des membres pour les programmes dans Marketo Optimizer.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Types de programme

Les types de programme définissent des aspects importants des [programmes](../marketing/programs.md) et de leurs membres, et distinguent différents types de programmes marketing les uns des autres. Chaque type de programme définit les propriétés suivantes, qui sont héritées pour les programmes utilisant le type de programme :

* **Attributs** - Les attributs décrivent les aspects importants du type de programme, tels que les dates d’événement et les attributs d’emplacement.

* **Flux de statut du programme** - Chaque statut est affecté à une étape du type de programme (1, 2 ou 3, par exemple). Les membres d’un programme peuvent uniquement passer d’un statut avec le même numéro d’étape (par exemple, de _Non affiché_ à _Terminé_), ou à un statut avec un numéro d’étape plus élevé (par exemple, de _Invité_ à _Enregistré_).

  Les statuts de programme s’excluent mutuellement et sont linéaires. Ainsi, une personne ne peut avoir qu’une seule valeur de statut par programme. Lors de la conception des statuts, réfléchissez aux statuts entre lesquels vous souhaitez autoriser le mouvement. Par exemple, si une personne ne s’est pas présentée à un webinaire, mais a la possibilité d’y assister ultérieurement à la demande, vous souhaiteriez qu’elle ait le même numéro de statut ou qu’elle définisse le statut à la demande sur un numéro supérieur afin qu’un membre du programme puisse y accéder.

>[!NOTE]
>
>Si un type de programme est utilisé par au moins un programme, il ne peut pas être modifié.

_Pour définir un type de programme personnalisé :_

1. Dans le volet de navigation de gauche [!DNL Adobe Marketo Optimizer], développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Types de programme]**.

   ![Accéder à la liste des types de programmes](./assets/program-types-list.png){width="800" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Créer un type]** en haut à droite.

1. Saisissez un **[!UICONTROL Nom]** unique (obligatoire) et un **[!UICONTROL Description]** (facultatif).

   ![Créer un type de programme](./assets/program-type-create.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >L’inclusion d’une description est une bonne pratique qui facilite la gestion de votre bibliothèque de types de programmes.

1. Cliquez sur **[!UICONTROL Créer un type]**.

1. Ajoutez le **[!UICONTROL Attributs]** pour le type de programme.

   Pour chaque attribut que vous souhaitez ajouter :

   * Cliquez sur **[!UICONTROL Ajouter un attribut]**.
   * Choisissez le **[!UICONTROL nom de l’API]** et saisissez le **[!UICONTROL nom d’affichage]**.
   * Cliquez sur **[!UICONTROL Enregistrer]**

   ![ Attributs de type de programme ](./assets/program-type-attributes.png){width="600" zoomable="yes"}

1. Définissez les étapes pour les **[!UICONTROL statuts du programme]**.

   Définissez chaque étape à inclure dans le flux :

   * Cliquez sur **[!UICONTROL Ajouter une étape]**.
   * Saisissez un nom de statut.
   * (Facultatif) Cliquez sur **[!UICONTROL Ajouter un statut]** et saisissez un nom de statut supplémentaire à inclure pour l’étape.

   Cochez la case **[!UICONTROL Marquer comme réussi]** pour toute étape dont vous souhaitez effectuer le suivi en tant qu’exécution réussie du programme.

   ![Statuts des types de programmes](./assets/program-type-statuses.png){width="600" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Terminé]** pour enregistrer vos modifications et revenir à la liste des types de programmes.