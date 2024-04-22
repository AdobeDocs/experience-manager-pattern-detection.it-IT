---
title: URC
description: Pagina della guida del codice di Pattern Detector.
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 24%

---

# URC {#urc}

Configurazione modalità di esecuzione non supportata

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configurazione della modalità di esecuzione non supportata"
>abstract="L’URC identifica l’utilizzo di configurazioni basate su un nome di modalità di esecuzione non supportato in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes" text="Modalità di esecuzione supportate"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/overview#runmodes" text="Modalità di esecuzione"

L’URC identifica l’utilizzo di configurazioni basate su un nome di modalità di esecuzione non supportato in AEM as a Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di verificare se tutte le modalità di esecuzione utilizzate nell’applicazione sono supportate e assicurarsi che rispettino le linee guida per la risoluzione delle modalità di esecuzione"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#deploying" text="Linee guida per la risoluzione in modalità di esecuzione"

* L’insieme dei nomi che possono essere utilizzati per l’esecuzione di varie modalità in AEM as a Cloud Service è limitato.
* Le configurazioni basate su nomi di modalità di esecuzione non supportati non hanno alcun effetto se distribuite a AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto precedente WKND per comprendere come le violazioni dell’URC possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione dell’URC su GitHub per capire come è possibile aggiornare le configurazioni OSGi basate su modalità di esecuzione personalizzate in modo da rispettare gli as a Cloud Service AEM."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Esempio di violazione dell’URC: GitHub"

* Esamina l’utilizzo di questa configurazione in modo da poter determinare se è necessario.
* Rinomina la configurazione utilizzando una delle [nomi modalità di esecuzione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#custom-runmodes) e seguire [linee guida per la risoluzione della modalità di esecuzione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/deploying/configuring-osgi#runmode-resolution).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e scopri come le [Violazioni URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
