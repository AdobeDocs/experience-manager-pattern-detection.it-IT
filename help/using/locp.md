---
title: LOCP
description: Pagina della guida del codice di Pattern Detector.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 57%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)"
>abstract="LOCP identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a /libs; si tratta di un anti-pattern (tranne nel caso di ACL)."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Aggiornamenti sostenibili"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`LOCP`  Identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a `/libs`, che è un anti-pattern (tranne nel caso di ACL).

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice cliente potrebbe essere eliminato o sostituito per qualsiasi aggiornamento CFP, SP o AEM principale.
* A volte il nuovo contenuto potrebbe non essere installato correttamente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guida all’implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato e relativi pacchetti per verificare se vengono forniti contenuti a /libs, ed eseguirne il refactoring affinché i contentuti vengano inseriti in /apps per compatibilità con AEM as a Cloud Service. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I pacchetti del cliente devono distribuire i contenuti in `/apps` anziché `/libs`.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) se hai bisogno di chiarimenti o dubbi.
