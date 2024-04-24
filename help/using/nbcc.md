---
title: NBCC
description: Pagina della guida del codice di Pattern Detector.
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 54%

---

# NBCC {#nbcc}

OBSOLETO: Non-Backwards Compatible Changes (modifiche non compatibili con versioni precedenti) (sostituito da NCC, Non-Compatible Changes, modifiche non compatibili)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (Modifiche non compatibili con versioni precedenti)"
>abstract="NBCC identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Note sulla versione per AEM as a Cloud Service"

`NBCC`  Identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* Le funzionalità che dipendono da un componente che utilizza modifiche non compatibili con le versioni precedenti possono risultare interrotte e non essere risolte correttamente.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere il codice personalizzato e assicurarsi che solo i componenti Sling compatibili con le versioni precedenti siano sovrapposti o di riferimento. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Sovrapponi o fai riferimento solo a componenti Sling compatibili con le versioni precedenti.
* È consigliabile adattare le risorse provenienti da `/libs` o i bundle dopo un aggiornamento AEM.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
