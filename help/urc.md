---
title: URC
description: Pagina della guida del codice del rilevatore pattern
exl-id: 1be61351-3e3e-4e51-973f-93f8bf9bf932
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# URC {#urc}

Configurazione della modalità di esecuzione non supportata

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_overview"
>title="Configurazione della modalità di esecuzione non supportata"
>abstract="L’URC identifica l’utilizzo di configurazioni basate su un nome in modalità runmode non supportato in AEM come Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes" text="Modalità di esecuzione supportate"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#runmodes" text="Modalità di esecuzione"

`URC` identifica l&#39;utilizzo di configurazioni basate su un nome di modalità runmode non supportato in AEM come Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di verificare se tutte le modalità di esecuzione utilizzate nell&#39;applicazione sono supportate e assicurarsi che rispettino le linee guida di risoluzione della modalità runmode"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#deploying" text="Linee guida per la risoluzione in modalità di esecuzione"

* L&#39;insieme di nomi che possono essere utilizzati per le modalità di esecuzione in AEM come Cloud Service è limitato.
* Le configurazioni basate su nomi di modalità di esecuzione non supportati non avranno alcun effetto se distribuite in AEM come Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urc_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND-legacy per capire come le violazioni dell’URC possono essere rese compatibili con AEM Cloud Service. Inoltre, Rivedi l’esempio di violazione dell’URC su Github per capire come è possibile aggiornare le configurazioni OSGi basate su runmode personalizzate in modo da rispettare AEM come Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc" text="Progetto legacy WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc" text="Esempio di violazione dell’URC - Github"

* Controlla l&#39;utilizzo di questa configurazione per determinare se è necessario.
* Rinomina la configurazione per utilizzare uno dei [nomi di modalità runmode supportati](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) e segui le [linee guida per la risoluzione in modalità runmode](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e scopri come [le violazioni dell&#39;URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
