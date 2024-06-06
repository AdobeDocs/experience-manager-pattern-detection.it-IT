---
title: URC
description: Pagina della guida del codice di Pattern Detector.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 100%

---

# URC {#urc}

Configurazione della modalità di esecuzione non supportata

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configurazione della modalità di esecuzione non supportata"
>abstract="URC identifica l’utilizzo di configurazioni basate su un nome della modalità di esecuzione non supportata in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modalità di esecuzione supportate"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modalità di esecuzione"

`URC` identifica l’utilizzo di configurazioni basate su un nome della modalità di esecuzione non supportata in AEM as a Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di verificare se tutte le modalità di esecuzione utilizzate nell’applicazione sono supportate. Inoltre, è opportuno assicurarsi che vengano seguite le linee guida per la risoluzione della modalità di esecuzione"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Linee guida per la risoluzione della modalità di esecuzione"

* L’insieme di nomi che possono essere utilizzati per le svariate modalità di esecuzione in AEM as a Cloud Service è limitato.
* Le configurazioni basate su nomi della modalità di esecuzione non supportati non avranno alcun effetto se distribuite in AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto precedente WKND per comprendere come le violazioni dell’URC possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione dell’URC su Github per capire come è possibile aggiornare le configurazioni OSGi basate su modalità di esecuzione personalizzate in modo da rispettare AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Esempio di violazione URC: GitHub"

* Controlla l’utilizzo di questa configurazione per determinare se è necessario.
* Rinomina la configurazione utilizzando uno dei [nomi delle modalità di esecuzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) supportati e segui le [linee guida per la risoluzione in modalità di esecuzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e scopri come le [Violazioni URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
