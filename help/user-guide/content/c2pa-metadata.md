---
title: Métadonnées C2PA
description: Découvrez comment Adobe Marketo Optimizer applique automatiquement les métadonnées C2PA aux images générées avec l’IA générative, et ce que cela signifie pour votre contenu.
feature: Assets, Content
role: User
source-git-commit: c7d3546d075f5a58923134231217b2fd10fe4aca
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Métadonnées C2PA

Les organisations marketing sont plus que jamais préoccupées par la transparence du contenu, la divulgation de l’IA et la prévention de l’altération des ressources. Le Content Authenticity Initiative (CAI) d’Adobe crée des outils conformes à la norme technique C2PA ([ Coalition for Content Provenance and Authenticity](https://c2pa.org/specifications/specifications/1.1/specs/C2PA_Specification.html#_trust_model). Les _métadonnées C2PA_ sont des informations chiffrées et infalsifiables qui peuvent aider les utilisateurs à comprendre la traçabilité du contenu et à garantir l’intégrité des ressources de la marque. Ces informations incluent :

* Émetteur ou signataire : informations sur l’entité ou la société qui a émis la signature numérique pour certifier ou signer la ressource.
* Date d&#39;émission — Date à laquelle les métadonnées C2PA ont été appliquées à la ressource.
* Crédit et utilisation — Informations sur le producteur de l&#39;actif, y compris le nom, les identifiants de médias sociaux ou d&#39;autres informations relatives à l&#39;identité.
* Processus — Enregistrements de toute modification apportée à l&#39;actif.
* Détails de l’appareil : informations sur l’application ou l’appareil utilisé pour créer ou modifier la ressource.
* Outil d’IA utilisé : si l’IA générative a été utilisée pour créer la ressource, le nom du modèle utilisé peut être inclus.
* Autres informations pertinentes : des données supplémentaires sont également incluses pour aider à fournir plus de contexte sur l’historique d’une ressource.

Pour obtenir des informations complètes sur l’historique des ressources, vous pouvez utiliser l’outil [inspection](https://contentauthenticity.adobe.com/inspect) d’Adobe Content Authenticity.

Les métadonnées C2PA sont conservées avec le fichier image. Lorsqu’une image qui a été générée ou modifiée avec l’IA générative est chargée vers ou exportée à partir de [!DNL Adobe Marketo Optimizer], ses métadonnées C2PA sont conservées.

>[!NOTE]
>
>Certaines méthodes d’importation d’images dans votre contenu, telles que l’extraction d’une image à partir d’un PDF ou d’une source incorporée (base64), peuvent ne pas conserver les métadonnées C2PA d’origine. Dans ces cas, les métadonnées C2PA ne peuvent pas être lues à partir de la source et aucune n’est créée pour le résultat.

>[!BEGINSHADEBOX]

## Persistance des métadonnées C2PA par le biais de canaux {#channels}

Lorsque vous incluez des images dans vos e-mails ou messages WhatsApp, les métadonnées C2PA pour les images diffusées sont également conservées :

* **E-mail** - Lorsque vous utilisez une action de parcours _Envoyer un e-mail_, ajoutez l’image au contenu de votre e-mail à partir de la bibliothèque _Assets_. Lorsque l’e-mail est diffusé, le destinataire peut télécharger l’image à partir du message et les métadonnées C2PA sont intactes.
* **WhatsApp** - Ajoutez l&#39;image à votre modèle de message WhatsApp dans votre compte professionnel Meta. Vous pouvez l&#39;ajouter directement depuis votre système ou télécharger un fichier image à partir de la bibliothèque __. Utilisez le modèle pour une action de parcours _Send WhatsApp_. Lorsque le message WhatsApp est diffusé, le destinataire peut télécharger l&#39;image à partir du message et les métadonnées C2PA sont intactes.

>[!ENDSHADEBOX]

## Génération d’images {#generate}

>[!INFO]
>
>De nouvelles lois émergent autour de la transparence générative de l’IA, et Adobe s’efforce de répondre aux exigences applicables dans toutes les juridictions. Les métadonnées C2PA sont l’outil de provenance utilisé par Adobe pour répondre aux exigences de ces lois.

Lorsque vous utilisez l’IA générative pour créer une image pour le contenu de votre e-mail dans [!DNL Marketo Optimizer], les métadonnées C2PA sont automatiquement jointes à l’image générée et aucune action n’est requise de votre part. Les outils d’IA générative produisent un élément de métadonnées C2PA combiné pour les variantes d’images avec des métadonnées existantes, y compris la source d’origine.

>[!NOTE]
>
>[!DNL Marketo Optimizer] ne prend actuellement pas en charge les actions de modification manuelle d’images. Les workflows de métadonnées C2PA pour ces actions ne sont pas applicables à ce stade.
