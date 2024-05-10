---
title: MI
description: Pagina della guida del codice di Pattern Detector.
exl-id: fa47ac63-1b5d-43b3-8acd-4a71c3fa714e
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '196'
ht-degree: 100%

---

# MI {#mi}

Problema di configurazione errata

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_overview"
>title="Problema di configurazione errata"
>abstract="MI (Misconfiguration Issue, Problema di configurazione) individua eventuali problemi di configurazione nell’istanza AEM"

`MI` (Problema di configurazione errata) identifica i problemi di configurazione nell’istanza AEM.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `sling.job.max.parallel`: identifica i processi Sling in cui la configurazione parallela massima è impostata su -1.
* `missing.maintenance.configuration`: identifica le configurazioni di attività di manutenzione mancanti.

## Possibili implicazioni e rischi {#implications-and-risks}

* `sling.job.max.parallel`
   * Il valore -1 viene sostituito con il numero di processori disponibili. Questo potrebbe causare problemi di prestazioni nell’istanza di AEM.
* `missing.maintenance.configuration`
   * Le configurazioni delle attività di manutenzione mancanti possono causare una perdita di prestazione o il danneggiamento dell’istanza.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_mi_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* `sling.job.max.parallel`
   * Adobe consiglia di impostare il valore su 0,5 per sfruttare la metà dei processori disponibili.
* `missing.maintenance.configuration`
   * Pulizia revisioni: consulta [Pulizia revisioni](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup). La parte importante riguardante la configurazione è questa: [Pulizia revisioni - Configurazione della coda e compattazione completa](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/deploying/revision-cleanup).
   * Pulizia dati binari di Lucene: consulta [Dashboard operazioni - Pulizia dati binari di Lucene](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/sites/administering/operations/operations-dashboard#lucene-binaries-cleanup).
   * Archivio dati raccolta oggetti inattivi: consulta [Archivio dati raccolta oggetti inattivi](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/sites/administering/operations/data-store-garbage-collection).
   * Eliminazione del flusso di lavoro: consulta [Eliminazione regolare delle istanze del flusso di lavoro](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/sites/administering/operations/workflows-administering#regular-purging-of-workflow-instances).
   * Attività di manutenzione del registro di controllo: consulta [Manutenzione del registro di controllo](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/sites/administering/operations/operations-audit-log).
* Contatta il [Team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
