---
title: URC
description: Pagina della guida del codice di Pattern Detector
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# URC {#urc}

Configurazione della modalità di esecuzione non supportata

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configurazione della modalità di esecuzione non supportata"
>abstract="L’URC identifica l’utilizzo di configurazioni basate su un nome in modalità di esecuzione non supportato in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it#custom-runmodes" text="Modalità di esecuzione supportate"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=it#runmodes" text="Modalità di esecuzione"

`URC` identifica l’utilizzo di configurazioni basate su un nome in modalità di esecuzione non supportato in AEM as a Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di verificare se tutte le modalità di esecuzione utilizzate nell’applicazione sono supportate e assicurarsi che rispettino le linee guida di risoluzione della modalità di esecuzione"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=it#deploying" text="Linee guida per la risoluzione in modalità di esecuzione"

* L’insieme di nomi che possono essere utilizzati per le modalità di esecuzione in AEM as a Cloud Service è limitato.
* Le configurazioni basate su nomi di modalità di esecuzione non supportati non avranno alcun effetto se distribuite a AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto precedente WKND per comprendere come le violazioni dell’URC possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione dell’URC su Github per capire come è possibile aggiornare le configurazioni OSGi basate su modalità di esecuzione personalizzate in modo da rispettare AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Esempio di violazione dell’URC - Github"

* Controlla l’utilizzo di questa configurazione per determinare se è necessario.
* Rinomina la configurazione per utilizzare uno dei [nomi in modalità di esecuzione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it#custom-runmodes) supportati e segui le [linee guida per la risoluzione in modalità di esecuzione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html?lang=it#runmode-resolution).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e scopri come le [Violazioni URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
