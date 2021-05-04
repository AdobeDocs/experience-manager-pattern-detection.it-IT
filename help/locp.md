---
title: LOCP
description: Pagina della guida del codice del rilevatore pattern
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# LOCP {#locp}

/libs Sovrascrittura di pacchetti personalizzati

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Sovrascrittura di pacchetti personalizzati"
>abstract="LOCP identifica il rilevamento di un pacchetto personalizzato che consegna il contenuto a /libs, che è un anti-pattern (tranne nel caso ACL)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Aggiornamenti sostenibili"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling Resource Merger"

`LOCP` identifica il rilevamento di un pacchetto personalizzato che distribuisce contenuti a  `/libs`, che è un anti-pattern (tranne nel caso ACL).

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice cliente potrebbe essere eliminato o sostituito per qualsiasi CFP, SP o aggiornamento AEM principale.
* In alcuni casi il nuovo contenuto potrebbe non essere installato correttamente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guida all&#39;implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato e i pacchetti per identificare se il contenuto viene consegnato a /libs e refattelo per fare affidamento sulla sovrapposizione del contenuto sotto /apps e renderlo compatibile con AEM come Cloud Service. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I pacchetti cliente devono distribuire il contenuto in `/apps` invece di `/libs`.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
