---
title: Nœud d’attente
description: 'Configurez les nœuds d’attente dans Marketo Optimizer : mettez en pause la progression du parcours par durée, date ou planification avancée des jours et des heures.'
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Nœud d’attente

Utilisez un nœud _Attente_ lorsque vous souhaitez suspendre la progression du parcours pendant une certaine durée avant de passer à l’étape suivante.

Vous pouvez définir le temps d’attente de deux manières différentes :

* Date spécifique à laquelle vous souhaitez passer au nœud suivant du parcours
* Une durée relative (nombre de minutes, heures, jours, semaines ou mois)

## Ajouter le nœud d’attente {#add-wait-node}

1. Accédez à la zone de travail de parcours.

1. Cliquez sur l’icône plus ( **+** ) d’un chemin d’accès et choisissez **[!UICONTROL Attendre]**.

   ![Cliquez sur Ajouter une icône sur le chemin du parcours &#x200B;](./assets/person-journey-canvas-add-node.png){width="200"}

1. Pour définir le temps d’attente avant que le parcours ne passe au nœud suivant dans le chemin d’accès, utilisez les propriétés du nœud sur la droite pour définir le **[!UICONTROL Type]**.

   * **[!UICONTROL Durée]** - Définissez un nombre spécifique de jours, heures ou minutes entre l’entrée et la sortie du nœud d’attente.
   * **[!UICONTROL Date]** - Spécifiez la date et l’heure de sortie.

   ![Nœud de Parcours - attente](./assets/wait-node.png){width="500"}

## Paramètres avancés de l’attente {#advanced-wait-settings}

Activez l’option **[!UICONTROL Doit se terminer le]** pour configurer une _étape d’attente avancée_ et vous assurer que vos messages atteignent les personnes et les membres du compte au moment optimal. Cette configuration vous donne un contrôle précis sur le moment où une personne ou un compte quitte une étape d’attente et passe au nœud suivant dans le parcours. Plutôt qu’un nombre fixe d’heures ou de jours entre l’entrée et la sortie, vous pouvez planifier des actions qui se produisent à des heures spécifiques et à des jours spécifiques de la semaine.

Avec une _étape d’attente avancée_, vous définissez **_quand_** la personne ou le compte se ferme, et pas simplement combien de temps elle doit attendre.

![nœud de Parcours - étape d’attente avancée](./assets/wait-node-advanced.png){width="500"}

### Types d’attente {#wait-types}

| Type d’attente | Description | Configuration |
| --------- | ----------- | ------------- |
| **Heure spécifique de la journée** | Maintenir jusqu’à une heure spécifique (par exemple, à 9 h) | Réglez l’heure (heure et minute). Se ferme à l’occurrence suivante de cette heure (pour le fuseau horaire sélectionné). |
| **Jour spécifique de la semaine** | Attendre jusqu’à un jour particulier (tel que le mardi) | Sélectionnez un jour de la semaine. Si aucune heure n’est spécifiée, se ferme à minuit (pour le fuseau horaire sélectionné) le jour correspondant suivant. |
| **Période ou combinaison** | Conservez jusqu’à n’importe quel jour d’une plage (lundi-vendredi, par exemple) ou pendant l’un des jours spécifiés | Sélectionnez vos jours cibles. Si aucune heure n’est spécifiée, se ferme à minuit (pour le fuseau horaire sélectionné) le jour correspondant suivant. |
| **Combinaison Heure + Jour** | Combinez les deux pour une planification précise (par exemple, mardi à 10 h) | Sélectionnez vos jours cibles et définissez l’heure cible. Quitte à l’occurrence du jour/heure suivant (pour le fuseau horaire sélectionné). |

### Scénarios courants {#common-scenarios}

Les scénarios suivants illustrent comment appliquer des exemples typiques à la configuration de votre nœud d’attente :

+++Arrivée des e-mails pendant les heures d’ouverture

**Scénario :** vous commercialisez auprès des clients B2B qui lisent des e-mails pendant leur journée de travail. Vous souhaitez que tous les e-mails arrivent pendant les heures de bureau.

**Solution :** configurez votre étape d’attente pour libérer les prospects à 9 h du matin les jours de semaine (du lundi au vendredi). Quel que soit le moment où un prospect accède au nœud d’attente, il reçoit votre e-mail pendant les heures de bureau.

+++

+++Heures d’envoi cohérentes pour les audiences dynamiques

**Scénario :** votre audience change tous les jours à mesure que de nouveaux comptes ou prospects sont qualifiés. Vous souhaitez que tous les prospects reçoivent le premier e-mail en même temps, quelle que soit la date à laquelle ils remplissent les critères.

**Solution :** définissez l’étape d’attente pour qu’elle se termine à une heure spécifique (par exemple à 10 h). Toutes les pistes, qu&#39;elles se soient qualifiées à minuit ou à midi, sortent de l&#39;étape d&#39;attente ensemble à 10h00.

+++

+++Tâches de suivi conformes à SLA

**Scénario :** votre équipe des ventes dispose d’un SLA de deux jours ouvrables pour effectuer le suivi des prospects de compte qualifiés pour le marketing. Les week-ends sont exclus.

**Solution :** configurez l’étape d’attente pour libérer les prospects uniquement les jours ouvrables. Un prospect qualifié le vendredi est acheminé pour un suivi le lundi ou le mardi, et non le week-end.

+++

### Exemples d’entrée et de sortie {#entry-exit-examples}

| Configuration de l’attente | Entrées de compte/lead | Sorties de compte/prospect |
| ------------------ | ------------------- | ------------------ |
| 09:00, Tous les jours | Lundi 11:00 | Mardi 9:00 |
| 09:00, Tous les jours | Lundi 7:00 | Lundi 9:00 |
| Mardi, pas d&#39;heure fixée | Vendredi 15:00 | Mardi, 00:00 |
| 10 h, du lundi au vendredi | Samedi 14:00 | Lundi 10:00 |
| 10 h, du lundi au vendredi | Mercredi 8:00 | Mercredi 10:00 |
