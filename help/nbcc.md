---
title: NBCC
description: Pagina della guida del codice di Pattern Detector
exl-id: fa6bdd3c-4deb-41ec-878d-4ea5dc1ddf60
source-git-commit: fdc3e8bdef27de971743a9ecb04d3912cf8e60ad
workflow-type: ht
source-wordcount: '233'
ht-degree: 100%

---

# NBCC {#nbcc}

OBSOLETO: Non-Backwards Compatible Changes (modifiche non compatibili con versioni precedenti) (sostituito da NCC, Non-Compatible Changes, modifiche non compatibili)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_overview"
>title="Non-Backwards Compatible Changes (Modifiche non compatibili con versioni precedenti)"
>abstract="NBCC identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="Note sulla versione per AEM as a Cloud Service"

`NBCC` identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* Le funzionalità che dipendono da un componente che utilizza modifiche non compatibili con le versioni precedenti possono risultare interrotte e non essere risolte correttamente.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_nbcc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere il codice personalizzato e assicurarsi di utilizzare o dare riferimento solo a componenti Sling compatibili con le versioni precedenti. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=it#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza o fai riferimento solo a componenti Sling compatibili con le versioni precedenti.
* È consigliabile adattare le risorse provenienti da `/libs` o i bundle dopo un aggiornamento AEM.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
