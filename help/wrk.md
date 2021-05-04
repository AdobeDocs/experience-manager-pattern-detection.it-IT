---
title: WRK
description: Pagina della guida del codice del rilevatore pattern
exl-id: 1be1db54-fc91-45d0-80b5-b2978eee1da8
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---

# WRK {#wrk}

Flusso di lavoro

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_overview"
>title="Flusso di lavoro"
>abstract="Il codice WRK identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento a AEM come Cloud Service. Con AEM come Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html" text="Microservizi per le risorse"

`WRK` identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento a AEM come Cloud Service.

Un sottotipo viene utilizzato per identificare il tipo di problema del flusso di lavoro attualmente rilevato.

* `custom.asset.workflow`: Rilevamento di un modello di flusso di lavoro delle risorse personalizzato o di un modulo di avvio.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_guidance"
>title="Guida all&#39;implementazione"
>abstract="Poiché i flussi di lavoro standard per le risorse sono supportati automaticamente dai miei microservizi per le risorse, Best Practice consiste nel rivedere tutti i modelli di flusso di lavoro per le risorse personalizzate o il modulo di avvio per verificare se sono necessari una volta che abbiamo effettuato la transizione al AEM come Cloud Service. Le personalizzazioni per i flussi di lavoro delle risorse richiedono la migrazione per poter lavorare con AEM come Cloud Service con l’aiuto dello strumento Asset Workflow Migration (Migrazione flussi di lavoro per risorse)"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html" text="Guida introduttiva - Microservizi per risorse"

* L’elaborazione delle risorse è tradizionalmente eseguita con i flussi di lavoro delle risorse in esecuzione sull’istanza di AEM Author. Con AEM come Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse. (Per ulteriori informazioni, consulta la [panoramica dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) .
* I flussi di lavoro delle risorse standard sono supportati automaticamente dai miei microservizi per le risorse.
* Le personalizzazioni ai flussi di lavoro delle risorse richiedono la migrazione per poter lavorare con AEM come Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_wrk_tools"
>title="Strumenti e risorse"
>abstract="Rivedi e pianifica l’esecuzione dello strumento Asset Workflow Migration (Migrazione flussi di lavoro per risorse) una volta identificato un modello di flusso di lavoro per risorse personalizzato o un modulo di avvio. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html" text="Strumento Asset Workflow Migration (Migrazione flussi di lavoro per risorse)"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Se è identificato un modello di flusso di lavoro per risorse personalizzate o un modulo di avvio, pianifica di eseguire [Asset Workflow Migration Tool](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Per ulteriori informazioni, consulta la [Guida introduttiva all’utilizzo dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) .
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
