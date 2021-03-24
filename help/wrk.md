---
title: WRK
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 1%

---


# WRK {#wrk}

Flusso di lavoro

## Sfondo {#background}

`WRK` identifica un risultato relativo a un modello di flusso di lavoro o a un modulo di avvio. Questi vengono segnalati perché è necessario eseguire la migrazione dei modelli di flusso di lavoro delle risorse personalizzate durante l’aggiornamento a AEM come Cloud Service.

Un sottotipo viene utilizzato per identificare il tipo di problema del flusso di lavoro attualmente rilevato.

* `custom.asset.workflow`: Rilevamento di un modello di flusso di lavoro delle risorse personalizzato o di un modulo di avvio.

## Possibili implicazioni e rischi {#implications-and-risks}

* L’elaborazione delle risorse è tradizionalmente eseguita con i flussi di lavoro delle risorse in esecuzione sull’istanza di AEM Author. Con AEM come Cloud Service, l’elaborazione delle risorse viene ora eseguita dai microservizi per le risorse. (Per ulteriori informazioni, consulta la [panoramica dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/asset-microservices-overview.html) .
* I flussi di lavoro delle risorse standard sono supportati automaticamente dai miei microservizi per le risorse.
* Le personalizzazioni ai flussi di lavoro delle risorse richiedono la migrazione per poter lavorare con AEM come Cloud Service.

## Soluzioni possibili {#solutions}

* Se è identificato un modello di flusso di lavoro per risorse personalizzate o un modulo di avvio, pianifica di eseguire [Asset Workflow Migration Tool](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/asset-workflow-migration-tool.html).
* Per ulteriori informazioni, consulta la [Guida introduttiva all’utilizzo dei microservizi per le risorse](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/asset-microservices-configure-and-use.html) .
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
