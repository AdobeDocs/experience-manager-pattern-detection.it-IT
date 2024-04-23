---
title: OAUI
description: Pagina della guida del codice di Pattern Detector.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 44%

---

# OAUI {#oaui}

Istanza utenti OAuth

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Istanza utenti OAuth"
>abstract="Il codice OAUI identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta. OAuth è configurato per gli utenti quando c’è un sottonodo chiamato oauth direttamente sotto un nodo rep:AuthorizableId nella forma di /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Note sulla versione"

OAUI identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta.

OAuth è configurato per gli utenti quando è presente un sottonodo denominato `oauth` direttamente sotto il nodo `rep:AuthorizableId` sotto forma di `/home/user-path/user-node/oauth`.

Un esempio è: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possibili implicazioni e rischi {#implications-and-risks}

* Gli utenti esterni configurati con OAuth non possono accedere alle istanze di authoring/pubblicazione finché non vengono riconfigurati con la procedura seguente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guida all’implementazione"
>abstract="Gli utenti esterni configurati con OAuth non possono accedere alle istanze di authoring/pubblicazione finché non vengono riconfigurati per essere compatibili con AEM as a Cloud Service. AEM as a Cloud Service offre il supporto per l’autenticazione IMS solo per gli utenti Author, Admin e Dev e l’integrazione basata su SAML per gli ambienti di pubblicazione. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/security/ims-support" text="Supporto IMS per AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Integrazione SAML: pubblicazione"

* Se hai bisogno di discutere delle opzioni di migrazione, contatta il rappresentante del tuo Adobe.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
