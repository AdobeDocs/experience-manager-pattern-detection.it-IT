---
title: MI
description: Pagina della guida del codice di Pattern Detector
source-git-commit: aa05ebcb54c6945a903c76add4f31e3279cd05b5
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 30%

---

# MI {#mi}

Problema di configurazione errata

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema di configurazione errata"
>abstract="MI (Misconfiguration Issue, Problema di configurazione) individua eventuali problemi di configurazione nell’istanza AEM"

`MI`  Configurazione errata Il problema identifica i problemi di configurazione nell’istanza AEM.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `sling.job.max.parallel`: identifica i processi sling in cui la configurazione parallela massima è impostata su -1.
* `missing.maintenance.configuration`: identifica le configurazioni di attività di manutenzione mancanti.

## Possibili implicazioni e rischi {#implications-and-risks}

* `sling.job.max.parallel`
   * Il valore -1 viene sostituito con il numero di processori disponibili. Questo potrebbe causare problemi di prestazioni nell’istanza AEM.
* `missing.maintenance.configuration`
   * Le configurazioni delle attività di manutenzione mancanti possono causare la perdita di prestazioni o il danneggiamento dell’istanza.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* `sling.job.max.parallel`
   * È consigliabile impostare il valore su 0,5 per utilizzare la metà dei processori disponibili.
* `missing.maintenance.configuration`
   * Pulizia revisioni: fare riferimento a [Pulizia revisioni](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html). La parte importante riguardante la configurazione è questa: [Pulizia revisioni: configurazione coda e compattazione completa](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/revision-cleanup.html#how-to-configure-full-and-tail-compaction).
   * Pulizia binary di Lucene: fare riferimento a [Dashboard operazioni - Pulizia binary di Lucene](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-dashboard.html#lucene-binaries-cleanup).
   * Data Store Garbage Collection: consulta [Raccolta oggetti inattivi dell’archivio dati](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/data-store-garbage-collection.html).
   * Eliminazione del flusso di lavoro: consulta [Rimozione regolare delle istanze del flusso di lavoro](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/workflows-administering.html?lang=it#regular-purging-of-workflow-instances).
   * Attività di manutenzione del registro di controllo: consulta [Manutenzione del registro di controllo](https://experienceleague.adobe.com/docs/experience-manager-65/administering/operations/operations-audit-log.html).
* Per eventuali domande o dubbi, contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).