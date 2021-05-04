---
title: NBCC
description: Pagina della guida del codice del rilevatore pattern
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# CCN {#nbcc}

Modifiche non compatibili con le versioni precedenti

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Modifiche non compatibili con le versioni precedenti"
>abstract="NBCC identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Modifiche di rilievo - AEM come Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="Note sulla versione - AEM come Cloud Service"

`NBCC` identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza modifiche non compatibili con le versioni precedenti può essere interrotta e potrebbe non essere risolta correttamente.
* Alcune funzionalità dell&#39;applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di rivedere il codice personalizzato e assicurarsi che solo i componenti Sling compatibili con le versioni precedenti siano sovrapposti o a cui si fa riferimento. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Sovrapponi o fai riferimento solo ai componenti Sling compatibili con le versioni precedenti.
* È consigliabile adattare le risorse provenienti da `/libs` o dai bundle dopo un aggiornamento AEM.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
