---
title: Surveillance et débogage de la progression des Parcours
description: Découvrez comment utiliser les compétences d’observabilité des Parcours dans la conversation des collègues pour déboguer et surveiller la manière dont les personnes et les prospects se déplacent dans les parcours, les décisions de chemin partagé et le timing.
source-git-commit: 9db94582512d95f6c07d4e978a0a27291b471900
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Surveillance et débogage de la progression du parcours

La compétence [_Observabilité_ Parcours &#x200B;](./skills.md#journeys) de [!DNL Adobe Marketo Optimizer] répond aux questions en langage naturel sur la manière dont les personnes et les prospects se déplacent dans les parcours. Utilisez-le dans l’[interface de conversation de vos collègues](./chat-interface.md) pour suivre la progression, comprendre les décisions de chemin partagé, analyser les personnes au sein des nœuds de parcours et vérifier les mesures de minutage. Vous pouvez également interroger les utilisateurs sur les modèles de comportement dans les parcours.

* **Compétences** - `journey-observability`
* **Appel** - Posez une question en langage naturel ou utilisez une commande de barre oblique pour exécuter la compétence Observabilité du Parcours. Par exemple : _« Comment demo_ lead_24@company.com a-t-il parcouru le parcours LeadNurture ?« _
* **Lit à partir de** - [!DNL Marketo Optimizer] les données de parcours ; lit [!DNL Marketo Engage] listes statiques pour vérifier l’appartenance à la liste

## Afficher les détails d&#39;une personne ou d&#39;un lead {#person-details}

Demandez des détails de base en lecture seule sur une personne ou un prospect pour établir un contexte avant d’enquêter sur son parcours. Indiquez l’adresse e-mail, l’ID de lead ou le nom du lead de la personne.

* _« Donnez-moi des informations de base sur le lead demo_ lead_24@company.com.« _
* _« Quel est l&#39;intitulé du poste et le pays du profil john.doe@company.com ?«_
* _« Affichez-moi l’e-mail et le rôle de lead_ 01.« _

## Trace de la progression au travers d’un parcours {#journey-progression}

Demandez à une personne ou à un prospect comment il s’est déplacé dans un parcours pour afficher l’entrée, la sortie, la durée et le chemin d’accès au niveau du nœud. Indiquez l’adresse e-mail ou l’ID de prospect de la personne, ainsi que le nom du parcours.

* _« Comment demo_ lead_24@company.com a-t-il traversé le parcours LeadNurture ?« _
* _« Quels nœuds john.doe@company.com a-t-il transmis dans le parcours de démonstration du produit ?«_

## Comprendre les décisions relatives au chemin de division {#split-path-analysis}

Demandez pourquoi une personne ou un prospect a emprunté, ou n’a pas emprunté, un chemin spécifique au niveau d’un nœud partagé. L’observabilité du parcours explique la décision à l’aide des valeurs d’attribut évaluées à ce moment. Indiquez l’adresse e-mail ou l’ID de prospect de la personne, le nom du parcours et l’ID du nœud partagé.

* _« Pourquoi demo_ lead_24@company.com est-il allé sur le chemin « Hautement engagé » au nœud de division c764a9 ? »_
* _« Pourquoi john.doe@company.com n’a-t-il pas pris le chemin d’accès qualifié au nœud ab123f dans LeadNurtureJourney ?«_
* _« Comparez les raisons pour lesquelles lead_ 01 et lead_02 ont pris des chemins différents au niveau du nœud partagé x99f3b.« _

## Analyse des personnes dans les nœuds de parcours {#node-analysis}

Demandez des détails et le nombre de personnes ou de leads dans un nœud de parcours ou un chemin de division. Filtrez les résultats par personnage, rôle, emplacement ou niveau d’engagement. Fournissez l’identifiant du nœud.

* _« Donnez-moi toutes les personnes actuellement sur le chemin d’accès « Engagement élevé » du nœud node-459c7c. »_
* _« Combien y a-t-il de leads dans le nœud de qualification du parcours de démonstration ?«_
* _« Afficher les leads dans le chemin de division &#39;Faible intention&#39; filtré par rôle : Responsable marketing.«_

## Identification de modèles dans les parcours {#pattern-recognition}

Demandez à l’observabilité du Parcours d’identifier les chemins communs, les points de chute et les comportements répétés dans un parcours. Indiquez le nom du parcours et éventuellement un délai, une personne, un produit ou un compte pour limiter les résultats.

* _« Quels sont les chemins les plus suivis par les SDR dans le parcours de démonstration du produit ? »_
* _« Où les prospects diminuent-ils généralement dans le parcours LeadNurture ?«_
* _« Existe-t-il des retards inhabituels ou des cheminements inattendus dans le parcours nurture du 1er trimestre ? »_

## Vérifier le timing et les mesures opérationnelles {#operational-metrics}

Renseignez-vous sur les temps d’accès, les durées d’attente, la latence de transition et la progression bloquée d’un parcours. Indiquez le nom du parcours et, éventuellement, un identifiant de nœud ou un identifiant de personne.

* _« Quand john.doe@company.com est-il entré dans le parcours de suivi de la démonstration ?«_
* _« Combien de temps les prospects attendent-ils généralement au nœud de qualification dans LeadNurtureJourney ?«_
* _« Quelles sont les leads qui sont bloqués dans le parcours de suivi de démonstration depuis plus de sept jours ?«_

## Limites {#limitations}

| Limite | Détail |
|---|---|
| Modifier les attributs d’une personne ou d’un prospect | Non pris en charge. Mettez à jour les enregistrements de personne et de lead directement dans [!DNL Marketo Engage] ou [!DNL Marketo Optimizer]. |
| Création, modification, suspension ou reprise de parcours | Non pris en charge. Utilisez plutôt la zone de travail de parcours [&#128279;](../marketing/person-journeys.md) ou une compétence de modification de parcours dans [Compétences du collègue](./skills.md#journeys). |
| Modification de la logique de division ou de la configuration du parcours | Non pris en charge. Modifiez les chemins de partage directement dans la zone de travail de parcours [&#128279;](../marketing/split-merge-paths-nodes.md). |
| Composition des groupes d&#39;achat ou cumuls au niveau du compte | Hors de portée. Parcours des rapports d’observabilité au niveau de la personne et du prospect uniquement. |
| Modification des horaires ou de la durée des parcours | Non pris en charge. |
