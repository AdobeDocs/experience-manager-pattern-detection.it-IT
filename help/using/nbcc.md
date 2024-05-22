---
title: NBCC
description: Pagina della guida del codice di Pattern Detector.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 67%

---

# NBCC {#nbcc}

OBSOLETO: Non-Backwards Compatible Changes (modifiche non compatibili con versioni precedenti) (sostituito da NCC, Non-Compatible Changes, modifiche non compatibili)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (Modifiche non compatibili con versioni precedenti)"
>abstract="NBCC identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche di rilievo in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Note sulla versione di AEM as a Cloud Service"

`NBCC`  Identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza Modifiche non compatibili con le versioni precedenti può essere interrotta e potrebbe non essere risolta correttamente.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guida all’implementazione"
>abstract="Una buona pratica consiste nel rivedere il codice personalizzato e assicurarsi di sovrapporre o fare riferimento solo a componenti Sling compatibili con le versioni precedenti. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Sovrapponi o fai riferimento solo a componenti Sling compatibili.
* È consigliabile adattare le risorse provenienti da `/libs` o bundle dopo un aggiornamento AEM.
* Per eventuali dubbi o chiarimenti, contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
