---
title: Configurer et analyser l’intention
description: Découvrez comment configurer les poids d’activité pour le modèle de score d’intention et analyser le motif au niveau du prospect avec des rapports de classement, de profil, de tendance et de comparaison.
TQID: 'https://experienceleague.adobe.com/BNzbM6v6ADSKyPR6jQMj1QdWMnLQQX-j3PNk8gF6PxY'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 46e599c6-e20f-5f67-9824-93415016f66b
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
topic_v2:
  - id: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 978
ht-degree: 0%

---


# Configurer et analyser l’intention

En [!DNL Adobe Marketo Optimizer], Coworker fournit deux compétences dans la catégorie _Intention_. Chaque client pèse les activités marketing différemment. Ces compétences vous permettent donc de configurer ce qui importe à votre entreprise. Vous pouvez ensuite valider ce que le pipeline d’intention a produit.

| Compétence | Commande | Ce qu&#39;il fait |
| --- | --- | --- |
| **Configuration de l’intention** | `/intent-configuration` (alias `/intent-config`) | Configurer les poids d’activité pour le modèle de score d’intention de la personne |
| **Intention d’analyse** | `/analyze-intent` | Interroger et valider le classement des intentions au niveau du prospect, la tendance, la taxonomie des produits et des mots-clés, ainsi que les rapports de comparaison |

La sélection d’une compétence insère sa description en tant qu’invite de démarrage dans l’entrée de conversation, que vous pouvez modifier avant l’envoi.

## Configuration du modèle de pondération {#configure-model}

Pour configurer les poids d’activité du modèle de score d’intention, procédez comme suit. Pour plus d’informations sur la configuration et la pondération de score, voir [_Configuration d’intention_](../audiences/intent-configuration.md).

1. Appelez la compétence (`/intent-configuration`) et appuyez sur **Entrée**.

   Coworker ouvre le panneau **[!UICONTROL Configuration de l’intention]** sous la forme d’un onglet d’espace de travail. Le panneau répertorie chaque activité d’intention du pipeline, en affichant un score **[!UICONTROL suggéré par l’IA]** et un score **[!UICONTROL pondération]** modifiable pour chacun. Il répertorie également les modèles qui existent déjà pour votre client . Un seul modèle peut être _[!UICONTROL actif]_ à tout moment : celui qui génère actuellement la notation.

1. Pour apporter des modifications, ouvrez un modèle _[!UICONTROL Brouillon]_ existant ou sélectionnez **[!UICONTROL Dupliquer]** sur le modèle _[!UICONTROL Actif]_ pour commencer à partir de son poids actuel.

1. Ajuster les poids ligne par ligne.

   Par exemple, marquez une activité à faible valeur comme **[!UICONTROL Ajouter à l’opportunité]** comme **[!UICONTROL Trivial]**, et donnez à **[!UICONTROL Cliquer sur l’e-mail]** ou **[!UICONTROL Cliquer sur le lien]** le statut **[!UICONTROL Important]** si ces activités sont plus importantes pour votre entreprise.

1. Sélectionnez **[!UICONTROL Enregistrer]**.

   L’enregistrement vous invite à activer le modèle maintenant. La confirmation du remplace le modèle _[!UICONTROL actif]_ actuel, qui est rétrogradé automatiquement.

## Notation de l’intention

Le score d’intention d’un prospect tient compte de trois éléments :

* **Poids configuré ici** pour chaque type d’activité.
* **Pertinence du contenu** : mots-clés extraits des ressources liées à chaque activité.
* **Fréquence** : nombre de fois où le prospect a interagi avec ce contenu.

Pour plus d’informations sur ces mesures, notamment le poids suggéré par l’IA, la pertinence du contenu et les limites, consultez [Configuration de l’intention](../audiences/intent-configuration.md).

## Rapports d’intention

Pour présenter les quatre types de rapports qu’il peut générer, appelez `/analyze-intent` pour inviter un collègue. Un collègue attend ensuite une demande de suivi nommant un prospect, un produit ou une comparaison. Chaque rapport s’ouvre sous son propre onglet dans le panneau de l’espace de travail et Coworker ajoute également une carte de résumé dans la conversation avec un bouton _[!UICONTROL Ouvrir le rapport]_.

### Rapport de classement d’intention

**Invite suggérée :** _« Afficher mes leads les plus intentionnés pour &lt;product>«_

Classe les prospects en fonction de l’intensité du signal d’intention pour un produit ou un mot-clé. Les colonnes comprennent le prospect, l’e-mail, le compte, le secteur, les produits, le score, le niveau d’intention et la source de la principale activité. La colonne delta _[!UICONTROL 7 jours]_ indique comment le score d’intention a évolué au cours de la dernière semaine. La colonne _[!UICONTROL Dernière mise à jour]_ indique la date de la dernière interaction du prospect, c’est-à-dire la date de la dernière modification du score. Les filtres pour le niveau de produit et d’intention sont des listes déroulantes dynamiques, vous n’êtes donc pas limité à ce que vous avez saisi dans l’invite. Les colonnes peuvent être triées.

Autres invites qui ouvrent le même rapport :

* « Classer les 10 premiers prospects par score d’intention pour Photoshop »
* « Répertorier les prospects présentant un haut degré d’intention pour Photoshop »
* « Montrez-moi les prospects dont le score d’intention pour Photoshop a le plus augmenté cette semaine »
* « Quels sont les leaders du secteur de la vente au détail qui démontrent une intention moyenne à élevée pour Creative Cloud ? »
* « Recherchez des prospects avec les scores d’intention générés par les téléchargements de ressources dans un webinaire. »
* « Répertorier les prospects à forte intention dont la source d’activité principale est le clic sur les e-mails »
* « Afficher les leads avec l’intention de contribuer par des visites web uniquement, à l’exclusion des téléchargements ou des webinaires »

### Rapport Profil d’intention

**Invite suggérée :** _« Afficher le profil d’intention de &lt;lead>«_

Un instantané rapide d’un prospect : les produits et mots-clés qui les intéressent et le score de chacun. Utilisez ce rapport une fois qu’un rapport de classement a fait apparaître un prospect qui mérite d’être étudié. Il vous aide à définir les parcours, les rôles et les groupes d’achat en fonction de l’intention réelle du produit de ce prospect.

Autres invites :

* « Quels produits &lt;lead> intéresse-t-il le plus ? »
* « Qu’est-ce qui intéresse &lt;lead> en ce moment ? »
* « Donnez-moi un résumé de tous les produits et mots-clés pour lesquels le lead X a montré son intention. »

### Rapport Tendance d’intention

**Invite suggérée :** _« Afficher l’historique du score d’intention de &lt;lead> pour &lt;product> au cours des 30 derniers jours »_

Trace le score d’intention d’un prospect pour un produit au fil du temps. Utilisez-la pour identifier les points d&#39;inflexion. Par exemple, un score qui reste constant pendant des semaines, puis qui chute brusquement, signale un changement d&#39;intérêt, et non pas des données non pertinentes. Vous pouvez ajuster la période à 7, 30 ou 100 jours.

Autres invites :

* « Quelle est l’augmentation prévue pour Acrobat cette semaine pour le prospect X ? »
* « Afficher la tendance d’intention d’un prospect ce mois-ci »
* « L’intention de lead X pour Acrobat a-t-elle augmenté ou diminué ce mois-ci ? »

### Rapport de comparaison d’intention

**Invite suggérée :** _« Comparez les tendances d’intention pour Photoshop par rapport à Illustrator pour tous les prospects au cours des 30 derniers jours »_

Compare l’intention au fil du temps pour deux prospects ou deux produits, sous la forme d’un graphique côte à côte et d’un tableau récapitulatif (score actuel, score il y a N jours, delta). La période peut être ajustée de la même manière que le rapport de tendance. L’intention peut changer tous les jours, d’une minute à l’autre ou toutes les heures, de sorte qu’une courte fenêtre plate ne signifie pas nécessairement qu’il ne se passe rien.

Autres invites :

* « Comparer l’intention d’Acrobat et de Photoshop au cours du dernier trimestre »
* « Comparer le prospect X et l’intention du prospect Y pour Creative Cloud »
* « Lequel a l’intention la plus élevée en moyenne : Photoshop ou Illustrator ? »
* « Comparer les profils pour Acrobat : qui a le taux de réussite le plus élevé ? »
* « Afficher l’intention côte à côte pour Photoshop dans les segments Retail et Finance »

## Suivi du rapport {#report-follow-up}

Les rapports d’intention sont en lecture seule et ne comportent aucune option d’exportation autonome. Pour agir sur la base des résultats d’un rapport, utilisez plutôt d’autres compétences.

* Invite avec la mention _« Répertorier les principaux prospects d’intention pour Creative Cloud »_ Un collègue utilise la compétence `/analyze-intent` pour produire la liste spécifiée.

* Invite indiquant _« Créer une liste de personnes à l’aide de cette liste »_ Un collègue remet l’ensemble de prospects à la [compétence de création d’audience](./audience-creation.md), qui crée directement la liste des personnes. Aucune étape d’exportation ou d’importation manuelle n’est nécessaire.
