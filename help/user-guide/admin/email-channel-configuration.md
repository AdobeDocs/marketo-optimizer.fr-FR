---
title: Configuration du canal e-mail
description: Créez et gérez des configurations de canal e-mail qui lient l’identité de l’expéditeur, le sous-domaine, le groupe d’adresses IP, le type d’adresse e-mail et le suivi des URL pour Marketo Optimizer.
feature: Administration
role: Admin
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 0%

---

# Configuration du canal e-mail

Une configuration de canal est l’objet central qui lie votre identité d’expéditeur, votre sous-domaine, votre groupe d’adresses IP et vos paramètres de suivi. Les actions d’e-mail dans les parcours font référence à une configuration de canal pour savoir comment envoyer le message. Avant de créer une configuration, effectuez la [délégation de sous-domaine et configuration du groupe d’adresses IP](../start/email-deliverability.md).

* **Canal:** E-mail.
* **Type d’e-mail :** marketing ou transactionnel. Ce paramètre détermine si des règles de suppression s’appliquent (Marketing les applique ; Transactionnel contourne par défaut la suppression des plaintes pour spam pour les messages transactionnels légitimes).
* **Paramètres d’en-tête :** Nom de l’expéditeur, Adresse électronique de l’expéditeur, Nom de la personne à laquelle répondre, Adresse électronique de la personne à laquelle répondre, Adresse électronique d’erreur.
* **Sous-domaine :** sous-domaine délégué utilisé pour l’envoi. L’e-mail de l’expéditeur doit utiliser ce sous-domaine.
* **Groupe d’adresses IP :** groupe d’adresses IP utilisé pour diffuser le message.
* **Tracking des URL :** activer ou désactiver le tracking des clics et des ouvertures ; configurer le domaine de tracking.
* **Balises :** balises pour l’organisation et la recherche.

## Créer une configuration de canal e-mail {#create-email-channel-configuration}

>[!PREREQUISITES]
>
>* Au moins un [sous-domaine](../start/email-deliverability.md#subdomain-delegation) doit être délégué et actif.
>* Au moins un [pool d’adresses IP](../start/email-deliverability.md#ip-pools) doit être affecté à votre organisation.
>* Vous avez besoin du rôle Administrateur.
>* Examinez [limitations actuelles](../start/email-deliverability.md#limitations) — les groupes d’adresses IP dédiés ne sont pas disponibles dans Beta.

1. Dans le volet de navigation de gauche [!DNL Adobe Marketo Optimizer], développez **[!UICONTROL Administration]** et sélectionnez **[!UICONTROL Canaux]**.
1. Dans le panneau, développez **[!UICONTROL Paramètres d’e-mail]** et sélectionnez **[!UICONTROL Configurations de canal]**.
1. Cliquez sur **[!UICONTROL Créer une configuration de canal]**.
1. Saisissez un Nom (par exemple, _Contoso B2B Marketing — Amérique du Nord_) et une Description facultative.
1. Sélectionnez le canal **[!UICONTROL e-mail]**.
1. (Facultatif) Sélectionnez des balises pour catégoriser la configuration.
1. Dans la section **[!UICONTROL Type d’e-mail]**, choisissez Marketing ou Transactionnel.
1. Dans la section **[!UICONTROL Sous-domaine]**, sélectionnez un sous-domaine précédemment délégué.
1. Dans la section **[!UICONTROL Groupe d’adresses IP]**, sélectionnez un groupe d’adresses IP actives.

   Chez Beta, seul le pool d’adresses IP partagées est disponible. Vous pouvez pointer sur les adresses IP pour afficher les enregistrements PTR.

1. Configurez les **[!UICONTROL paramètres d’en-tête]** :
   * Nom de l’expéditeur (par exemple, « Marketing Contoso »).
   * E-mail de l&#39;expéditeur — doit utiliser le sous-domaine sélectionné (par exemple, `marketing@mail.contoso.com`).
   * Nom de la réponse et Adresse électronique de la réponse : si ce champ est vide, la valeur par défaut est _De_.
   * E-mail d&#39;erreur : adresse qui reçoit les notifications de non-diffusion.
1. Activez le **[!UICONTROL tracking des URL]** et sélectionnez le domaine de tracking.
1. Cliquez sur **[!UICONTROL Envoyer]**.

>[!NOTE]
>
>Après l’envoi, le système exécute la validation : statut du sous-domaine, enregistrement MX, alignement SPF/DKIM/DMARC, préparation du groupe d’adresses IP, enregistrement FBL. La configuration passe par le statut Brouillon → Traitement → actif.

>[!NOTE]
>
>Si la validation échoue, la configuration passe au statut **[!UICONTROL Échec]**. Ouvrez la configuration pour afficher la raison de l’échec : les causes courantes sont l’échec de la validation des enregistrements MX, des adresses IP du pool ne correspondant pas à la configuration ou un mauvais alignement du DMARC. Résoudre et renvoyer.

## Modification ou suppression d’une configuration de canal {#edit-channel-configuration}

Vous pouvez modifier les configurations de canal après leur création, mais avec une contrainte importante : **Le canal ne peut pas être modifié.** Une configuration est liée à son canal .

Lorsque vous modifiez une configuration en cours d’utilisation :

* **Pour les parcours publiés :** la modification est appliquée à la prochaine périodicité ou à la prochaine exécution. Les exécutions en cours se poursuivent avec les paramètres précédents.
* **Pour les messages transactionnels ou en temps réel :** modifications se propagent en cinq minutes environ.

>[!WARNING]
>
>La suppression d’une configuration de canal est permanente. Vous ne pouvez pas supprimer une configuration référencée par un parcours actif. Supprimez ou réaffectez d’abord toutes les actions e-mail.

Pour supprimer une configuration, supprimez ou mettez à jour chaque action d’e-mail qui y fait référence dans [Ajouter des e-mails aux parcours &#x200B;](../marketing/email-channel.md#define-email-properties). [!DNL Marketo Optimizer] ne supprime pas une configuration actuellement utilisée par un parcours actif.

## Configurations de plusieurs canaux {#multiple-channel-configurations}

La plupart des entreprises B2B utilisent plusieurs configurations de canal pour séparer les marques, les régions ou les types d’envoi. Modèles courants :

* Une configuration marketing distincte par unité opérationnelle (par exemple, *Marketing BU-A*, *Marketing BU-B*).
* Une configuration transactionnelle dédiée avec Type d’e-mail = Transactionnel pour les notifications de produit ou de contrat.
* Configurations spécifiques à une région utilisant des sous-domaines spécifiques à une région (par exemple, `mail.eu.contoso.com`, `mail.us.contoso.com`) pour s’aligner sur les FAI régionaux et la conformité.

>[!TIP]
>
>Nommez vos configurations selon une convention claire et structurée, par exemple : *[Marque] - [Région] - [Type]*. Cela devient critique une fois que vous disposez d’une douzaine de configurations ou plus.
