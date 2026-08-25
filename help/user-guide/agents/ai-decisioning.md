---
title: Prise de décision par l’IA
description: Découvrez la prise de décision par l’IA dans Marketo Optimizer, la couche d’intelligence artificielle derrière le contrôle de trafic de parcours, le meilleur chemin suivant, l’optimisation de l’heure d’envoi et d’autres fonctionnalités qui remplacent les règles statiques par une automatisation axée sur les résultats.
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '808'
ht-degree: 2%

---


# Prise de décision par l’IA

La prise de décision par l’IA est la couche d’intelligence artificielle derrière Adobe Marketo Optimizer. Au lieu de précréer chaque branche sous la forme d’une règle statique, la prise de décision par l’IA évalue en permanence le contexte d’un profil, y compris l’appartenance au parcours, l’historique de l’engagement, les scores d’intention et le comportement en temps réel, afin de déterminer la meilleure action ou le meilleur parcours pour cette personne.

Cette évaluation continue déplace l’orchestration des règles statiques vers une automatisation axée sur les résultats : plutôt que de définir chaque condition à l’avance, vous décrivez le résultat que vous souhaitez et le système détermine comment y parvenir pour chaque personne.

## Fonctionnalités {#capabilities}

La prise de décision par l’IA comprend les fonctionnalités suivantes :

| Fonctionnalité | Ce qu’il décide |
|---|---|
| [Contrôle de trafic de Parcours ](../marketing/journey-traffic-control.md) | Dans quel parcours une personne doit-elle se trouver en ce moment ? Lorsqu’une personne est admissible pour plusieurs parcours, le contrôle de la circulation des parcours la réachemine au moment où son profil ou son comportement change, plutôt que de la laisser sur un chemin qui ne convient plus. |
| [Meilleur chemin suivant](../marketing/next-best-path.md) | Chemin le mieux adapté pour une personne au sein d’un parcours. Au lieu des conditions de filtre de codage en dur, vous décrivez l’intention en langage naturel, et le système dirige chaque personne vers le chemin le mieux adapté au bon moment. |
| [Optimisation de l’heure d’envoi](../marketing/email-send-time-optimization.md) | La meilleure fenêtre d’envoi pour chaque destinataire, basée sur l’engagement historique, plutôt qu’une planification fixe pour tout le monde. |
| Contenu contextuel | Variantes d’e-mail personnalisées générées automatiquement à partir d’un résumé de contenu, à utiliser comme une ressource d’e-mail personnalisée unique dans parcours. _Bientôt disponible._ |
| [](https://experienceleague.adobe.com/fr/docs/brand-concierge/content/home){target="_blank"} | Routage et réponse conversationnels en temps réel, tels que le chat et l’assistance en direct. Brand Concierge nécessite des droits de produit supplémentaires. |

Certaines de ces fonctionnalités résolvent différents problèmes dans le même parcours. Le contrôle du trafic sur les parcours décide quel parcours est prioritaire lorsque plusieurs parcours sont en concurrence pour impliquer la même personne en même temps. Les autres fonctionnalités déterminent ce qui se passe lorsqu’une personne se trouve déjà dans un parcours.

## Fractionner les chemins et le meilleur chemin suivant {#split-paths-next-best-path}

Les [chemins partagés](../marketing/split-merge-paths-nodes.md) permettent de définir des branches de parcours avec des conditions de filtrage explicites : si un score dépasse un seuil, envoyez une personne sur un chemin, sinon un autre. Cette logique basée sur des règles est précise et entièrement auditable, mais chaque nouvelle condition nécessite une nouvelle branche.

Le nœud [Meilleur chemin suivant](../marketing/next-best-path.md) applique la prise de décision par l’IA au même problème. Au lieu d’un seuil fixe, le modèle évalue ensemble l’engagement, le profil, l’intérêt du produit et l’étape funnel, prédit le meilleur résultat pour chaque personne et sélectionne automatiquement le chemin optimal.

## Entrées de données {#data-inputs}

La prise de décision par l’IA s’appuie sur les catégories de données suivantes :

| Catégorie | Exemples |
|---|---|
| Données démographiques et démographiques | Fonction, secteur et taille de l’entreprise |
| Psychographique | Score, urgence et priorité du lead |
| Engagement | Score, niveau, tendance, dernière activité et canal |
| Intention | Intention du produit ou du mot-clé, regroupée en intervalles élevé, moyen ou faible |
| Persona | Rôle dans l’affaire, le titre de la fonction et le persona |

## Cadence d’évaluation {#evaluation-cadence}

AI decisioning utilise deux plannings d’évaluation différents. Le profil sous-jacent d’une personne est recalculé par lots pendant la nuit. La décision elle-même est appliquée en temps réel à chaque interaction, en utilisant ce que le dernier profil nocturne indique. Ainsi, la partie continue de la prise de décision par l’IA décrit le moment de la décision, et non le taux d’actualisation du profil.

## Mécanismes de sécurisation et règles {#guardrails-rules}

Les règles ne couvrent que les conditions qu’une personne a explicitement écrites. Lorsque la réalité sort de cet arbre, comme un personnage hybride ou une combinaison de signaux que personne n’avait anticipée, les règles ne font rien jusqu’à ce que quelqu’un ajoute une nouvelle branche. L’IA decisioning évalue chaque personne en continu et génère à la place une meilleure action basée sur la confiance. Elle gère donc les combinaisons pour lesquelles personne n’a été explicitement programmé, et elle s’améliore lorsqu’elle voit plus de résultats, ce qu’une règle ne fait jamais.

Les règles sont explicables et instantanées pour le contrôle, tandis que la prise de décision par l’IA est évaluée par le degré de confiance plutôt que déterministe. Pour cette raison, les règles restent le meilleur outil lorsque :

* Une limite de conformité stricte ne doit jamais être franchie, comme la suppression des contacts exclus.
* Il n’y a pas encore assez de volume ou d’historique pour qu’un modèle puisse en tirer des enseignements.
* Chaque décision doit être pleinement explicable à la demande.

La plupart des configurations matures fonctionnent ensemble : les règles servent de mécanismes de sécurisation et les décisions de l’IA gèrent tout ce qui se situe entre les deux.

## Avantages {#benefits}

* Moins de complexité de parcours manuel, avec moins de branches de règles à gérer.
* Des expériences plus pertinentes sans créer des centaines de règles.
* Efficacité de la qualification supérieure.
* Identification plus rapide du meilleur engagement suivant pour chaque profil.

>[!BEGINSHADEBOX]

**Portée future : contexte de compte et de groupe d&#39;achat**

Actuellement indisponible dans Marketo Optimizer. La prise de décision par l’IA est prévue pour s’étendre au-delà du profil individuel aux éléments suivants :

* Contexte du compte — Signaux au niveau de la société et du compte comme entrée de prise de décision.
* Signaux de groupe d&#39;achat : rôle dans l&#39;accord, statut du décideur ou du praticien, et engagement global de toutes les personnes impliquées dans une décision d&#39;achat.
* Orchestration du parcours au niveau du compte : les décisions de routage et de contenu sont prises pour le compte ou le groupe d’achat en tant qu’unité, avec un contrôle du trafic du parcours coordonné entre les différentes personnes impliquées.

>[!ENDSHADEBOX]
