---
title: DG
description: Pagina della guida del codice di Pattern Detector.
exl-id: 7ee3b177-bd79-41cd-abaf-ece3ae98ce03
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 100%

---

# DG {#dg}

Developer Guidelines (Linee guida per gli sviluppatori)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_overview"
>title="Developer Guidelines (Linee guida per gli sviluppatori)"
>abstract="Il codice DG individua deviazioni dalle specifiche linee guida di sviluppo per AEM 6.5 e AEM as a Cloud Service. Seguendo le best practice è possibile migliorare la manutenzione e le prestazioni del sistema. Queste deviazioni potrebbero non essere un problema in altri contesti applicativi, incluse versioni precedenti di AEM; tuttavia possono causare problemi se vengono utilizzate con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Sviluppo AEM: linee guida e best practice"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Linee guida per lo sviluppo in AEM as a Cloud Service"


`DG` identifica deviazioni da specifiche linee guida di sviluppo per [AEM 6.5](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices) e [AEM as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines). Seguendo le best practice è possibile migliorare la manutenzione e le prestazioni del sistema. Queste deviazioni potrebbero non essere un problema in altri contesti applicativi, incluse versioni precedenti di AEM; tuttavia possono causare problemi se vengono utilizzate con AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare diversi tipi di violazioni rilevate:

* `java.io.inputstream`: utilizzo di `java.io.InputStream` nel codice dell’applicazione.
* `maintenance.task.configuration`: configurazione di una certa attività di manutenzione periodica.
* `sling.commons.scheduler`: utilizzo dell’API Sling Commons Scheduler per un’attività pianificata.
* `unsupported.asset.api`: utilizzo delle API di Asset Manager non supportate nel codice dell’applicazione.
* `javax.jcr.observation.EventListener`: utilizzo di un listener di eventi nel codice dell’applicazione.
* `custom.guava.cache`: l’utilizzo della cache Guava nel codice dell’applicazione.

## Possibili implicazioni e rischi {#implications-and-risks}

* `java.io.inputstream`
   * Lo streaming di dati binari con `java.io.InputStream` può sfruttare le risorse di memoria al punto di influire sulle prestazioni. Questo diventa un problema a causa della memoria limitata disponibile nei contenitori utilizzati in AEM as a Cloud Service.

* `maintenance.task.configuration`
   * Alcune attività di manutenzione che in precedenza richiedevano una configurazione esplicita vengono ora configurate e gestite automaticamente in AEM as a Cloud Service.
   * La configurazione dell’attività di manutenzione in AEM as a Cloud Service deve essere spostata nel controllo del codice sorgente.

* `sling.commons.scheduler`
   * Le applicazioni dipendenti da attività in background che utilizzano [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) potrebbero non funzionare come previsto perché la loro esecuzione non è garantita in AEM as a Cloud Service.
   * Secondo le linee guida per [attività in background e processi con tempi di esecuzione lunghi](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#background-tasks-and-long-running-jobs), per il codice eseguito come attività pianificata si dovrebbe presupporre che in qualsiasi momento si potrebbe verificare un’interruzione dell’istanza su cui il codice è in esecuzione. Pertanto, il codice deve essere resiliente e ripristinabile.

* `unsupported.asset.api`
   * Le seguenti API di AssetManager sono contrassegnate come non supportate in AEM as a Cloud Service.
      * createAssetForBinary
      * getAssetForBinary
      * removeAssetForBinary
      * createAsset

* `javax.jcr.observation.EventListener`
   * Le applicazioni dipendenti dal listener di eventi potrebbero non funzionare come previsto perché l’esecuzione non può essere garantita.

* `custom.guava.cache`
   * L’utilizzo della cache Guava può causare problemi di prestazioni in AEM.


## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dg_guidance"
>title="Guida all’implementazione"
>abstract="Esamina le tue implementazioni sull’utilizzo del Modulo di pianificazione Sling Commons. Ristrutturale in Processi Sling, ristrutturane le attività di manutenzione del sistema, rivedi lo streaming di eventuali dati binari ed esegui il refactoring del codice per renderlo conforme ad AEM as a Cloud Service."
>additional-url="https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing" text="Processi Sling"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/operations/maintenance" text="Attività di manutenzione in AEM as a Cloud Service"

* `java.io.inputstream`
   * Utilizza un approccio di caricamento binario diretto in cui i dati binari vengono aggiunti direttamente al datastore.
   * Per i casi di utilizzo relativi alle risorse, consulta [aem-upload](https://github.com/adobe/aem-upload). Per altri tipi di dati binari, la logica di caricamento personalizzata può essere modellata secondo lo stesso schema.

* `maintenance.task.configuration`
   * Consulta la documentazione sulle [Attività di manutenzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/operations/maintenance) in AEM as a Cloud Service.
   * Assicurati che la [configurazione delle attività di manutenzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/overview#maintenance-tasks-configuration-in-source-control) sia inclusa nel controllo del codice sorgente.

* `sling.commons.scheduler`
   * Sostituisci l’uso di [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) con [processi Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), che dispongono di una garanzia di esecuzione “almeno una volta”.
   * I processi di lunga durata dovrebbero essere evitati.

* `unsupported.asset.api`
   * Anziché utilizzare le API non supportate di Asset Manager, consulta [aem-upload](https://github.com/adobe/aem-upload).

* `javax.jcr.observation.EventListener`
   * Invece di utilizzare il listener di eventi, si consiglia di eseguire il refactoring del meccanismo di gestione degli eventi con [Processi Sling](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing) per essere sicuri che il processo venga eseguito.

* `custom.guava.cache`
   * Se necessario, le cache devono essere create al di fuori di AEM. Potrebbe essere utile una soluzione di memorizzazione in cache esterna.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
