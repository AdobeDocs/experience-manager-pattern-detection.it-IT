---
title: NCC
description: Pagina della guida del codice di Pattern Detector.
exl-id: 4a374956-c64e-43fc-8279-ed25f6ed5cb0
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: ht
source-wordcount: '191'
ht-degree: 100%

---

# NCC {#ncc}

Modifiche non compatibili

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_overview"
>title="Modifiche non compatibili"
>abstract="NCC identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche di rilievo in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Note sulla versione di AEM as a Cloud Service"

`NCC` identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza modifiche non compatibili può essere interrotta e potrebbe non essere risolta correttamente.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ncc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere il codice personalizzato e assicurarsi che solo i componenti Sling compatibili siano sovrapposti o di riferimento. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/overlays#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Sovrapponi o fai riferimento solo ai componenti Sling compatibili.
* È consigliabile adattare le risorse provenienti da `/libs` o i bundle dopo un aggiornamento di AEM.
* Per risolvere eventuali dubbi o avere dei chiarimenti, contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
