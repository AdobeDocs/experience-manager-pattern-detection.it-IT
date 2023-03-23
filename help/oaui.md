---
title: OAUI
description: Pagina della guida del codice di Pattern Detector
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 100%

---

# OAUI {#oaui}

Istanza utenti OAuth

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Istanza utenti OAuth"
>abstract="Il codice OAUI identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta. OAuth è configurato per gli utenti quando c’è un sottonodo chiamato oauth direttamente sotto un nodo rep:AuthorizableId nella forma di /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM as a Cloud Service: note sulla versione"

`OAUI` identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta.

OAuth è configurato per gli utenti quando è presente un sottonodo denominato `oauth` direttamente sotto il nodo `rep:AuthorizableId` sotto forma di `/home/user-path/user-node/oauth`.

Un esempio è: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possibili implicazioni e rischi {#implications-and-risks}

* Gli utenti esterni configurati con OAuth non potranno accedere alle istanze di authoring/pubblicazione finché non saranno riconfigurati con la procedura seguente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guida all’implementazione"
>abstract="Gli utenti esterni configurati con OAuth non potranno accedere alle istanze di authoring/pubblicazione finché non saranno riconfigurati per essere compatibili con AEM as a Cloud Service. AEM as a Cloud Service offre il supporto per l’autenticazione IMS solo per gli utenti Author, Admin e Dev e l’integrazione basata su SAML per gli ambienti di pubblicazione. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=it" text="Supporto IMS per AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/personalization/user-and-group-sync-for-publish-tier.html?lang=it#integration-with-an-idp" text="Integrazione SAML: pubblicazione"

* Contatta il tuo rappresentante di Adobe per discutere le opzioni per la migrazione degli utenti.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
