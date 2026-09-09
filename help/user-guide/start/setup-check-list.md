---
title: Liste de contrôle d'installation
description: Effectuez les tâches de configuration initiales pour votre instance Marketo Optimizer, y compris la configuration de l’accès utilisateur et l’infrastructure de délivrabilité des e-mails.
TQID: 'https://experienceleague.adobe.com/XEPKIa88-L7mdPz1opKegY1pdEF4Qyls0nLVJBQSaJk'
product_v2:
  - id: a8deb403-4b0c-4f5a-95c6-5e5bedc292ed
feature_v2:
  - id: 3cf5f37e-e87e-5179-812b-53ce05d7eebb
  - id: 64b90904-e4f0-5c1b-a871-8c6a40b204a1
source-git-commit: 43b1b5ba8415d7a7f3291c12c3db4cc333b673c4
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 10%

---

# Liste de contrôle de configuration

Effectuez ces tâches pour activer la fonctionnalité dans votre instance [!DNL Marketo Optimizer] configurée.

## Activer l’accès utilisateur {#enable-user-access}

Une fois la mise en service terminée et les sandbox liés, configurez l’accès [!DNL Journey Optimizer B2B Edition] pour votre équipe et les utilisateurs.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Fournir un accès et des autorisations de produit</strong> pour les utilisateurs</td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Création d’un profil de produit Journey Optimizer B2B edition dans Admin Console (configuration unique/initiale uniquement)</td>
<td><a href="./user-management.md#create-profile">Créer un profil</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’un groupe d’utilisateurs dans Admin Console</td>
<td><a href="./user-management.md#add-user-group">Ajouter un groupe d’utilisateurs</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Affectez le profil de produit au groupe d’utilisateurs dans l’Admin Console</td>
<td><a href="./user-management.md#assign-profile">Attribuer un profil de produit</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’utilisateurs au groupe d’utilisateurs dans Admin Console</td>
<td><a href="./user-management.md#add-users">Ajouter des utilisateurs et utilisatrices</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Modifier les rôles intégrés ou créer un rôle personnalisé avec des autorisations de produit</td>
<td><a href="./user-management.md#edit-role-permissions">Modifier les rôles</a> <br/> <a href="./user-management.md#create-a-custom-role">Créer un rôle personnalisé</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Ajout d’utilisateurs, d’utilisatrices ou de groupes à des rôles dans Adobe Experience Platform</td>
<td><a href="./user-management.md#add-users-to-a-role">Ajouter des utilisateurs</a> <br/><a href="./user-management.md#add-user-groups-to-a-role">Ajouter des groupes</a></td>
</tr>
</tbody>
</table>

## Délivrabilité des e-mails {#email-deliverability}

Avant que les professionnels du marketing puissent envoyer des e-mails à partir de parcours, configurez l’infrastructure d’envoi pour votre organisation, y compris la délégation de sous-domaines, l’authentification des e-mails et les paramètres de canal.

<table>
<thead>
<tr>
<th colspan="2">Tâche</th>
<th>Détails et instructions</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><strong>Configurer les paramètres de canal et de délivrabilité des e-mails</strong></td>
<td></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Déléguer un sous-domaine à Adobe (entièrement délégué ou CNAME)</td>
<td><a href="./email-deliverability.md#delegate-fully-delegated">Délégation complète</a> <br/> <a href="./email-deliverability.md#delegate-cname">CNAME</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Configuration de DMARC pour le sous-domaine</td>
<td><a href="./email-deliverability.md#configure-dmarc">Configuration de DMARC</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Vérification et affectation d’un groupe d’adresses IP</td>
<td><a href="./email-deliverability.md#review-ip-pool">Vérifier le groupe d’adresses IP</a></td>
</tr>
<tr>
<td><img src="../assets/do-not-localize/icon-checkbox.svg" width="25" alt="Case à cocher de la tâche"/></td>
<td>Créer une configuration de canal e-mail</td>
<td><a href="../admin/email-channel-configuration.md#create-email-channel-configuration">Configurer le canal e-mail</a></td>
</tr>
</tbody>
