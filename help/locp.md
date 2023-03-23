---
title: LOCP
description: Pagina della guida del codice di Pattern Detector
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 100%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)"
>abstract="LOCP identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a /libs; si tratta di un anti-pattern (tranne nel caso di ACL)."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=it" text="Aggiornamenti sostenibili"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=it#platform" text="Sling Resource Merger"

`LOCP` identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a `/libs`; si tratta di un anti-pattern (tranne nel caso di ACL).

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice del cliente potrebbe venire eliminato o sostituito da eventuali aggiornamenti principali, CFP o SP di AEM.
* In alcuni casi i nuovi contenuti potrebbero non venire installati correttamente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guida all’implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato e relativi pacchetti per verificare se vengono forniti contenuti a /libs, ed eseguirne il refactoring affinché i contentuti vengano inseriti in /apps per compatibilità con AEM as a Cloud Service. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=it#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I pacchetti del cliente devono distribuire i contenuti in `/apps` anziché `/libs`.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
