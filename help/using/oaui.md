---
title: OAUI
description: Pagina della guida del codice di Pattern Detector.
exl-id: 326144d6-705a-4b2c-ac35-403fd4c2259f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '228'
ht-degree: 100%

---

# OAUI {#oaui}

Istanza utenti OAuth

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_overview"
>title="Istanza utenti OAuth"
>abstract="Il codice OAUI identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta. OAuth è configurato per gli utenti quando c’è un sottonodo chiamato oauth direttamente sotto un nodo rep:AuthorizableId nella forma di /home/user-path/user-node/oauth"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: note sulla versione"

`OAUI` identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta.

OAuth è configurato per gli utenti quando è presente un sottonodo denominato `oauth` direttamente sotto il nodo `rep:AuthorizableId` sotto forma di `/home/user-path/user-node/oauth`.

Un esempio è: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possibili implicazioni e rischi {#implications-and-risks}

* Gli utenti esterni configurati con OAuth non potranno accedere alle istanze di authoring/pubblicazione finché non saranno stati riconfigurati con la procedura seguente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oaui_guidance"
>title="Guida all’implementazione"
>abstract="Gli utenti esterni configurati con OAuth non potranno accedere alle istanze di authoring/pubblicazione finché non saranno stati riconfigurati per essere compatibili con AEM as a Cloud Service. AEM as a Cloud Service offre il supporto per l’autenticazione IMS solo per gli utenti con privilegi di autore, amministratore e sviluppatore, e per l’integrazione basata su SAML per gli ambienti di pubblicazione. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/security/ims-support" text="Supporto IMS per AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/authoring/personalization/user-and-group-sync-for-publish-tier#integration-with-an-idp" text="Integrazione SAML: pubblicazione"

* Contatta il rappresentante Adobe per discutere le opzioni per la migrazione degli utenti.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
