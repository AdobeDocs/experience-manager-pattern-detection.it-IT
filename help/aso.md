---
title: ASO
description: Pagina della guida del codice di Pattern Detector
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: 725a04c2d0c7f14673ac8cef9b62239ae3a5166c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ASO {#aso}

AEM System Overview

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="AEM System Overview"
>abstract="Il codice ASO identifica informazioni generali sull’istanza di AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema, e può essere utile per la pianificazione della migrazione e le iniziative di refactoring."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM as a Cloud Service - Note sulla versione"

`ASO` identifica informazioni generali sull’istanza di AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `aem.version`: versione di AEM.
* `aem.product`: rilevamento dell’uso di un prodotto AEM (Commerce, Forms, ecc.).
* `node.count`: conteggio approssimativo dei nodi di un determinato tipo (Pagina, Risorsa, ecc.) e il totale complessivo dei nodi.
* `node.store`: tipo di implementazione dell’archivio dei nodi (SegmentNodeStore, DocumentNodeStore) e relative dimensioni.
* `data.store`: tipo di implementazione dell’archivio dei dati (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: attività di manutenzione.
* `slow.query`: query lenta.
* `group.membership`: numero di utenti e sottogruppi (solo membri diretti/dichiarati) in un gruppo.
* `cqtag.count`: numero di risorse con tag CQ.
* `smarttag.count`: numero di risorse con tag avanzati.
* `ccom.version`: versione del pacchetto dei componenti core.
* `instance.type`: tipo di istanza di AEM (author|publish).
* `unprocessed.asset.count`: numero di risorse non elaborate.
* `vanity.url.count`: numero di URL personalizzati.
* `index.size`: dimensione totale dell’indice Lucene migrabile.
* `workflow.count`: Il numero di flussi di lavoro di authoring in esecuzione e in stato non aggiornato.

## Possibili implicazioni e rischi {#implications-and-risks}

* I seguenti dati sono forniti a scopo informativo: versione di AEM, numero di nodi, appartenenza ai gruppi, archivio nodi, tipi di implementazione dell’archivio dati, numero di tag CQ e di tag avanzati, versione dei componenti core, tipo di istanza di AEM e numero di risorse non elaborate.
* Un numero elevato di URL personalizzati (>1000) può comportare un carico notevole per Dispatcher e i server Publish con query costose.
* L’applicazione personalizzata può basarsi su prodotti o funzionalità non disponibili in AEM as a Cloud Service.
* L’aggiornamento con funzioni non supportate potrebbe impedire l’aggiornamento o il corretto funzionamento di un’applicazione.
* Un numero elevato di flussi di lavoro di authoring in esecuzione o in stato obsoleto potrebbe peggiorare le prestazioni.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guida all’implementazione"
>abstract="Le informazioni esposte tramite codice ASO sono generiche per l’ambiente AEM, tra cui versione, componenti aggiuntivi per prodotti e informazioni a livello di sistema, e devono essere verificate per eventuali prodotti o funzionalità non supportati in AEM as a Cloud Service. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Gli aggiornamenti di AEM con prodotti o funzionalità non supportati non sono consigliati e potrebbero non essere supportati.
* Le risorse non elaborate devono essere elaborate e la proprietà dam:assetState sul nodo jcr:content della risorsa deve essere impostata su “processed”; in alternativa, rimuovi queste risorse dal set di migrazione prima di migrare ad AEMaaCS.
* Gli URL personalizzati possono essere sostituiti con Apache Rewrite.
* Consulta le [note sulla versione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it) per scoprire le ultime modifiche implementate in AEM as a Cloud Service.
* Per eventuali domande o dubbi, contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
