---
title: DG
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---


# DG {#dg}

Guida per sviluppatori

## Sfondo {#background}

`DG` identifica le deviazioni delle linee guida di sviluppo selezionate per  [AEM 6.5](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html) e  [AEM come Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html). Seguendo le best practice è possibile migliorare la manutenzione e le prestazioni del sistema. Anche se alcune di queste deviazioni potrebbero non essere un problema in altri contesti di applicazione, anche con le versioni precedenti di AEM, possono causare problemi quando vengono utilizzate con AEM come Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di violazioni rilevate:

* `java.io.inputstream`: L&#39;utilizzo di  `java.io.InputStream` nel codice dell&#39;applicazione.
* `maintenance.task.configuration`: La configurazione di una certa attività di manutenzione periodica.
* `sling.commons.scheduler`: Utilizzo dell’API di pianificazione Sling Commons per un’attività pianificata.

## Possibili implicazioni e rischi {#implications-and-risks}

* `java.io.inputstream`
   * Lo streaming di dati binari con `java.io.InputStream` può richiedere risorse di memoria al punto di influire sulle prestazioni. Questo è particolarmente un problema a causa della memoria limitata disponibile nei contenitori utilizzati in AEM come Cloud Service.

* `maintenance.task.configuration`
   * Alcune attività di manutenzione che in precedenza richiedevano una configurazione esplicita ora vengono configurate e gestite automaticamente all&#39;interno di AEM come Cloud Service.
   * La configurazione dell&#39;attività di manutenzione in AEM come Cloud Service deve essere spostata nel controllo del codice sorgente.

* `sling.commons.scheduler`
   * Le applicazioni dipendenti dalle attività in background che utilizzano [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) potrebbero non funzionare come previsto perché l&#39;esecuzione non può essere garantita in AEM come Cloud Service.
   * AEM come linee guida di sviluppo del Cloud Service per le [attività in background e i processi a lungo termine](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#background-tasks-and-long-running-jobs) suggeriscono che il codice eseguito come attività pianificata deve presupporre che l&#39;istanza su cui è in esecuzione possa essere disattivata in qualsiasi momento. Pertanto, il codice deve essere resiliente e riutilizzabile.

## Soluzioni possibili {#solutions}

* `java.io.inputstream`
   * Utilizza un approccio di caricamento binario diretto in cui il binario viene aggiunto direttamente al datastore.
   * Per i casi di utilizzo delle risorse, utilizza [aem-upload](https://github.com/adobe/aem-upload). Per altri tipi di binari, la logica di caricamento personalizzata può essere modellata dopo lo stesso pattern.

* `maintenance.task.configuration`
   * Rivedi la documentazione AEM come Cloud Service [Attività di manutenzione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/maintenance.html) .
   * Assicurati che [Configurazione attività di manutenzione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#maintenance-tasks-configuration-in-source-control) sia nel controllo del codice sorgente.

* `sling.commons.scheduler`
   * Sostituisci l&#39;utilizzo di [Sling Commons Scheduler](https://sling.apache.org/documentation/bundles/scheduler-service-commons-scheduler.html) con [Sling Jobs](https://sling.apache.org/documentation/bundles/apache-sling-eventing-and-job-handling.html#jobs-guarantee-of-processing), che hanno una garanzia di esecuzione almeno una volta.
   * Se possibile, si dovrebbero evitare lavori a lungo termine.

* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
