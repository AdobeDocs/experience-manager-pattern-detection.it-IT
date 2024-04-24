---
title: WRK
description: Pagina della guida del codice di Pattern Detector.
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 62%

---

# WRK {#wrk}

Flusso di lavoro

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Flusso di lavoro"
>abstract="Il codice WRK identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento ad AEM as a Cloud Service. Con AEM as a Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview" text="Microservizi per le risorse"

`WRK`  Identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento ad AEM as a Cloud Service.

Viene utilizzato un sottotipo per identificare il tipo di problema del flusso di lavoro attualmente rilevato.

* `custom.asset.workflow`: rilevamento di personalizzazioni di modello di flusso di lavoro delle risorse o modulo di avvio.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guida all’implementazione"
>abstract="I flussi di lavoro delle risorse standard sono supportati automaticamente dai microservizi per le risorse. Pertanto, è consigliabile rivedere tutti i modelli di flusso di lavoro delle risorse personalizzati o l’utilità di avvio per verificare se sono necessari dopo la transizione all’AEM as a Cloud Service. Le personalizzazioni dei flussi di lavoro delle risorse devono essere migrate per poter funzionare con AEM as a Cloud Service con l’aiuto dello strumento Asset Workflow Migration (Migrazione flussi di lavoro per risorse)"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use" text="Guida introduttiva ai microservizi per risorse"

* L’elaborazione delle risorse è tradizionalmente eseguita con i flussi di lavoro delle risorse sull’istanza di authoring AEM. Con AEM as a Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse. Consulta la [panoramica dei microservizi per le risorse](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/asset-microservices-overview) per ulteriori informazioni.
* I flussi di lavoro delle risorse standard sono supportati automaticamente dai microservizi per le risorse.
* Le personalizzazioni dei flussi di lavoro delle risorse richiedono la migrazione per poter funzionare con AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Strumenti e risorse"
>abstract="Rivedi e pianifica l’esecuzione dello strumento Migrazione dei flussi di lavoro delle risorse una volta identificata una personalizzazione di modello di flusso di lavoro per risorse o modulo di avvio. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool" text="Strumento Migrazione dei flussi di lavoro delle risorse"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Se viene identificata una personalizzazione di modello di flusso di lavoro di una risorsa o modulo di avvio, pianifica l’esecuzione dello [strumento Migrazione dei flussi di lavoro delle risorse](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/asset-workflow-migration-tool).
* Consulta la [Guida introduttiva all’utilizzo dei microservizi per le risorse](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-microservices-configure-and-use) per ulteriori informazioni.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
