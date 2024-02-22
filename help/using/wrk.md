---
title: WRK
description: Pagina della guida del codice di Pattern Detector
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '330'
ht-degree: 100%

---

# WRK {#wrk}

Flusso di lavoro

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Flusso di lavoro"
>abstract="Il codice WRK identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento ad AEM as a Cloud Service. Con AEM as a Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=it" text="Microservizi per le risorse"

`WRK` identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento ad AEM as a Cloud Service.

Viene utilizzato un sottotipo per identificare il tipo di problema del flusso di lavoro attualmente rilevato.

* `custom.asset.workflow`: rilevamento di personalizzazioni di modello di flusso di lavoro delle risorse o modulo di avvio.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guida all’implementazione"
>abstract="Poiché i flussi di lavoro delle risorse standard sono supportati automaticamente dai microservizi per le risorse, le best practice consistono nel rivedere tutte le personalizzazioni di modello di flusso di lavoro per le risorse o modulo di avvio per verificare se sono necessari una volta effettuata la transizione ad AEM as a Cloud Service. Per poter funzionare con AEM as a Cloud Service, le personalizzazioni dei flussi di lavoro delle risorse devono essere migrate con l’aiuto dello strumento Migrazione flussi di lavoro delle risorse"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=it" text="Guida introduttiva ai microservizi per risorse"

* L’elaborazione delle risorse è tradizionalmente eseguita con i flussi di lavoro delle risorse sull’istanza di authoring AEM. Con AEM as a Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse. Consulta la [panoramica dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html?lang=it) per ulteriori informazioni.
* I flussi di lavoro delle risorse standard sono supportati automaticamente dai microservizi per le risorse.
* Le personalizzazioni ai flussi di lavoro delle risorse devono essere migrate per poter funzionare con AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Strumenti e risorse"
>abstract="Rivedi e pianifica l’esecuzione dello strumento Migrazione dei flussi di lavoro delle risorse una volta identificata una personalizzazione di modello di flusso di lavoro per risorse o modulo di avvio. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=it" text="Strumento Migrazione dei flussi di lavoro delle risorse"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Se viene identificata una personalizzazione di modello di flusso di lavoro di una risorsa o modulo di avvio, pianifica l’esecuzione dello [strumento Migrazione dei flussi di lavoro delle risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html?lang=it).
* Consulta la [Guida introduttiva all’utilizzo dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html?lang=it) per ulteriori informazioni.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
