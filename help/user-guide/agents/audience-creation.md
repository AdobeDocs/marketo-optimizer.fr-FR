---
title: Création d’audiences pour des programmes
description: Utilisez les compétences de création d’audience de Marketo Optimizer pour créer des listes de personnes, adapter les listes dynamiques Marketo Engage et modifier les règles de liste dans la conversation.
source-git-commit: c00dc1d3f3028ece56905f9f1018605147b0ac20
workflow-type: tm+mt
source-wordcount: '1464'
ht-degree: 1%

---

# Créer des audiences pour les programmes

Dans [!DNL Adobe Marketo Optimizer], les [_listes de personnes_](../audiences/people-lists.md) définissent l’audience des parcours de personnes, sous la forme de listes dynamiques basées sur des filtres qui se mettent à jour automatiquement ou de listes statiques à appartenance fixe. À partir de l’[interface de chat](./chat-interface.md), le _Création d’audience_ [compétences](./skills.md) crée, adapte et modifie les listes de personnes par le biais d’une conversation guidée.

* **Compétences** - `audience-creation` et `people-list-comparison`
* **Appel** - Décrivez directement les critères d’audience, chargez une liste dynamique [!DNL Marketo Engage] ou nommez une liste existante à modifier
* **Lit à partir de / écrit sur** - [!DNL Marketo Optimizer] ; lit les [!DNL Marketo Engage] lors de l’adaptation des listes dynamiques

## Workflows pris en charge {#workflows}

Coworker prend en charge trois workflows de création d’audience et détermine lequel s’applique à partir de votre requête. Si votre intention est ambiguë, il vous demande avant de continuer.

| Workflow | Quand l’utiliser | Exemple de prompt |
|---|---|---|
| **Créer en partant de zéro** | Vous souhaitez une nouvelle liste de personnes définie par critères ou appartenance. | _« Créez une liste dynamique de vice-présidents marketing dans les entreprises SaaS en Amérique du Nord. »_ |
| **Adaptation d’une liste [!DNL Marketo Engage] dynamique** | Vous disposez déjà d’une liste dynamique de [!DNL Marketo Engage] ou d’une campagne dynamique et souhaitez une liste de personnes équivalente. | _« Adaptez cette liste dynamique Marketo en liste de personnes.«_ (joindre la ressource) |
| **Modifier une liste existante** | Vous souhaitez ajouter ou remplacer des règles dans une liste que vous avez déjà. | _« Ajoutez une règle à ma liste &#39;Essais sur les entreprises&#39; pour un score de prospect supérieur à 50.«_ |

## Créer entièrement une liste de personnes {#create-from-scratch}

Avant de générer quoi que ce soit, Coworker confirme les quatre éléments suivants. Il demande toutes les données manquantes dans un seul message.

1. **Règles/critères** — Description en langage clair de la personne qui fait partie de la liste.
1. **Nom** — Comment appeler la liste.
1. **Emplacement** — Dans quel programme la liste doit se trouver. Indiquez un nom de programme que votre collègue trouve ; s’il existe plusieurs correspondances, il vous demande de choisir.
1. **Type** : dynamique (basée sur des filtres, mise à jour automatique) ou statique (appartenance fixe). Ceci est obligatoire — Mon collègue ne devinera pas ; si vous ne spécifiez pas, il demande.

### Listes dynamiques {#dynamic-lists}

Pour les listes dynamiques, Coworker suggère de manière proactive d’inclure des attributs de personnalisation pour rendre le ciblage plus riche. Ces attributs sont **_inclus par défaut — vous vous désinscrivez, pas dans_** :

| Attribut | Pourquoi cela est utile |
|---|---|
| **Persona dérivé** | persona acheteur déduit par l’IA pour le ciblage du contenu basé sur les personas. |
| **Intention dérivée** | Les intentions d’achat présumées signalent que les comptes sur le marché apparaissent. |
| **Niveau d’engagement** | Niveau d’engagement calculé qui donne la priorité aux contacts engagés. |

Informez votre collègue si vous souhaitez supprimer l&#39;un de ces éléments avant de continuer.

### Listes statiques {#static-lists}

* **Statique, aucun critère** — La liste est créée vide, prête pour que vous ajoutiez manuellement des membres.
* **Statique à partir de critères (instantané)** — Coworker crée l’ensemble correspondant et y copie ces personnes. La population est asynchrone — Un collègue confirme que la liste a été créée, mais note que l’affichage des personnes peut prendre quelques minutes. Il ne prétendra pas que la liste est prête immédiatement.

## Vérifier la carte {#review-card}

Rien n’est créé tant que vous ne l’avez pas approuvé. Après avoir décrit vos critères, Coworker présente une vignette interactive _Révision de la création de la liste de personnes_ (pour les adaptations à partir de [!DNL Marketo Engage] listes, la vignette est intitulée _Révision de la conversion de la liste de personnes_).

Chaque ligne de la carte représente une condition :

| Colonne | Signification |
|---|---|
| **Conditions requises** (ou le nom de la liste [!DNL Marketo Engage] pour les adaptations) | Votre demande d’origine ou le filtre Marketo source. |
| **(règle)** | Règle basée sur les attributs réelle générée pour cette condition. |
| **Include** | Case à cocher permettant de conserver ou de supprimer cette règle. |

**Niveaux de confiance :**

* **Degré de confiance élevé** les lignes sont correctement appariées et vérifiées par défaut.
* **Faible degré de confiance** les lignes (mappages approximatifs ou éléments marqués d’un indicateur) sont affichées avec un indicateur d’avertissement et ne sont pas cochées par défaut.
* Les lignes que le système n&#39;a pas pu mapper indiquent **« Aucun équivalent trouvé »** — elles n&#39;ont pas de règle et ne sont pas cochées.

Un _Résumé des conversions_ affiche _N degré de confiance élevé_ et _N degré de confiance faible_, avec un indice : les règles de confiance faible ne sont pas cochées par défaut ; cochez-les pour inclure, ou décrivez la modification que vous souhaitez apporter dans la conversation.

**Actions de carte :**

* **Continuer** — Crée la liste en utilisant uniquement les règles cochées.
* **Décrivez les modifications que vous souhaitez apporter dans le chat** — Préremplissez la saisie avec _« Je souhaite modifier : «_ pour que vous puissiez l’affiner ; Mon collègue régénère et affiche une nouvelle carte, en conservant les règles que vous avez déjà approuvées.

Vous pouvez également taper un suivi à tout moment (par exemple, _« également limiter aux entreprises de plus de 500 employés »_) et Coworker régénère la carte.

## Mappage des attributs {#attribute-mapping}

Lorsque vous décrivez des critères, Collègue convertit chaque condition en un attribut réel et connu au niveau de la personne. Trois résultats peuvent apparaître sur la carte Révision :

1. **Correspondance (degré de confiance élevé)** — Votre condition correspond directement à un attribut (par exemple, _« email is acme.com »_ correspond à l’attribut `email`). Activé par défaut.
1. **Approximatif (faible degré de confiance)** — L’attribut disponible le plus proche diffère par son nom ou son modèle de données (par exemple, un filtre Marketo _Montant_ approximatif sous la forme _Score du lead_). Affiché avec une note expliquant la différence ; non coché par défaut.
1. **Introuvable** — La condition n&#39;a pu être mappée à aucun attribut connu. Affiché comme _« Aucun équivalent trouvé »_ ; aucune règle n’est générée.

C’est pourquoi une liste que vous décrivez peut comporter moins de règles que de conditions que vous n’en avez spécifiées. Les conditions non correspondantes sont affichées explicitement au lieu d’être supprimées silencieusement. Si des critères importants tombent comme « introuvables », reformulez-les à l’aide du nom réel de l’attribut et Coworker tente de les reformuler.

>[!NOTE]
>
>Si vous mappez des colonnes de feuille de calcul à des champs (une carte Mappage de champs avec _Colonne_, _Champ cible_, un pourcentage de confiance et une liste _Colonnes non mappées_), il s’agit du flux d’importation de prospect, et non de la création d’audience. Voir la compétence [import-leads](./skills.md#audiences-people).

## Modification des règles d’une liste existante {#edit-rules}

Lorsque vous demandez à modifier des règles sur une liste que vous avez déjà, Coworker détermine la liste et le mode de modification :

* **Ajouter/ajouter** (par défaut pour _« ajouter des règles »_, _« ajouter plus de règles »_) — les nouvelles règles sont fusionnées avec les règles existantes.
* **Remplacer** (par défaut pour _« remplacer les règles »_, _« modifier les règles en »_) — les nouvelles règles remplacent toutes les règles existantes dans la liste.

Un collègue résume ce qui sera appliqué et indique clairement s’il s’agit d’un ajout ou d’un remplacement, puis vous demande de confirmer avant la validation. Après l’application, il indique le nombre total de règles et le nombre de règles ajoutées ou remplacées.

>[!NOTE]
>
>Les modifications utilisent un chemin d’accès prenant en charge les fusions afin qu’une opération d’« ajout » ne remplace jamais silencieusement vos règles existantes.

## Chevauchement d’audiences {#overlap}

Demandez à votre collègue de comparer deux listes de personnes (par exemple, _« Montrez-moi le chevauchement entre « Webinaire du 3e trimestre » et « Comptes d’entreprise »_) et il génère une carte _Chevauchement de listes de personnes_ :

* Badge d’en-tête affichant le nombre : **»{N} en commun. »**
* Une ligne de statistiques avec le nombre total de membres de chaque liste et le chevauchement comme **« X % de A · Y % de B »**
* Tableau des membres des personnes des deux listes, avec une colonne **Nom** et une seconde colonne que vous pouvez diriger : **E-mail** (par défaut), **Société** ou **Fonction** en fonction de ce que vous avez demandé.
* Cliquez sur un nom pour ouvrir cette personne dans l’espace de travail.
* S&#39;il n&#39;y a pas de chevauchement, la carte dit très clairement : _« Aucun membre en commun entre ces deux listes »_.

**Limitations :**

| Limite | Détail |
|---|---|
| **Taille du tableau** | Affiche jusqu’à 200 membres ; au-delà, il note _« Affichage de 200 sur N - demandez-moi d’affiner la requête pour limiter les résultats »_ |
| **Calcul de chevauchement** | Calculé sur l’adresse e-mail. Les personnes sans adresse e-mail sont exclues de l’intersection. |
| **Taille de la liste** | Lit jusqu’à environ 1 000 premiers membres de chaque liste. Pour les listes plus volumineuses, Coworker indique que les résultats sont partiels. |
| **Brouillons de listes dynamiques** | Comparaison impossible : une liste qui n’a pas été publiée ne comporte aucun segment actif. Un collègue vous demande de le publier en premier ou d’utiliser une liste statique à la place. |

## Validation du contrôle qualité {#qa-validation}

Après avoir créé ou mis à jour une liste, un collègue propose : _« Voulez-vous que je vérifie que la liste est correctement configurée ?«_ Si vous acceptez, il récupère à nouveau la liste et signale les vérifications suivantes :

| Vérifier | Résultat |
|---|---|
| Liste trouvée sous le programme/dossier correct | Réussite/échec |
| Le nombre de filtres correspond à ce qui a été appliqué. | _N_ filtres / incompatibilité |
| Attributs Personalization présents (le cas échéant) | Présent/manquant |
| Le nom de la liste correspond à ce que vous avez demandé | Réussite/échec |
| Nombre estimé de membres | _count_ ou N/A |

## Limites {#limitations}

| Limite | Détail |
|---|---|
| **Adaptation de liste statique depuis[!DNL Marketo Engage]** | Vous ne pouvez pas adapter une liste statique [!DNL Marketo Engage] (ou un e-mail ou une autre ressource qui n’est pas une ressource de filtre) en liste de personnes. Les listes statiques sont des identifiants de membre explicites qui ne peuvent pas être exprimés en tant que filtres ; un collègue demande plutôt une liste dynamique ou une campagne dynamique. |
| **Filtres basés sur les activités et les appartenances** | Lors de l’adaptation à partir de [!DNL Marketo Engage], des filtres tels que _E-mail ouvert_, _Page web visitée_, _Formulaire rempli_, _Membre de la liste_ et _Membre de la campagne intelligente_ n’ont pas d’équivalent dans la liste de personnes et sont renvoyés comme « Aucun équivalent trouvé ». |
| **Conditions au niveau de l’entreprise** | Traduit dans la mesure du possible dans l’attribut au niveau de la personne le plus proche (les listes de personnes fonctionnent sur les attributs de la personne) et marqué comme étant de faible confiance lorsque l’ajustement est lâche. |
| **Logique AND/OR profondément imbriquée** | Une logique imbriquée complexe peut se réduire en un ET/OU de niveau supérieur ; c’est ce que remarque un collègue lorsqu’elle se produit. |
| **Collisions de noms** | Non résolu automatiquement — si le nom est pris, Coworker vous en demande un autre plutôt que d&#39;ajouter silencieusement un suffixe. |
| **Approbation requise** | Un collègue ne crée ou ne modifie pas une liste tant que vous n’avez pas cliqué sur **[!UICONTROL Continuer]**, confirmé ou donné un feu vert clair (_« approuvé »_, _« semble correct »_, _« créer »_). |
| **Population d’instantanés statiques** | L’appartenance à des listes statiques créées à partir de critères prend plus de quelques minutes, et non instantanément. |

