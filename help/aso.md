---
title: ASO
description: Pagina della guida del codice di Pattern Detector
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: a3b610f2028c4923344672dd71c2bd5d252a35c4
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 77%

---

# ASO {#aso}

Panoramica del sistema AEM

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Panoramica del sistema AEM"
>abstract="Il codice ASO identifica informazioni generali sull’istanza di AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema, e può essere utile per la pianificazione della migrazione e le iniziative di refactoring."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service: note sulla versione"

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
* `vanity.url.count`: numero di URL di reindirizzamento a microsito.

## Possibili implicazioni e rischi {#implications-and-risks}

* La versione AEM, i conteggi dei nodi, l’appartenenza al gruppo, l’archivio dei nodi, i tipi di implementazione dell’archivio dati, il conteggio dei tag CQ, il conteggio dei tag avanzati, la versione del componente core, AEM tipo di istanza e il conteggio delle risorse non elaborate sono forniti a scopo informativo.
* Il numero più elevato di URL personalizzati (>1000) può caricare Dispatcher e i server di pubblicazione con query costose.
* L’applicazione personalizzata può basarsi su prodotti o funzionalità non disponibili in AEM as a Cloud Service.
* L’aggiornamento con funzioni non supportate potrebbe impedire l’aggiornamento o il corretto funzionamento di un’applicazione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guida all’implementazione"
>abstract="Le informazioni esposte tramite codice ASO sono generiche per l’ambiente AEM, tra cui versione, componenti aggiuntivi per prodotti e informazioni a livello di sistema, e devono essere verificate per eventuali prodotti o funzionalità non supportati in AEM as a Cloud Service. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Gli aggiornamenti di AEM con prodotti o funzionalità non supportati non sono consigliati e potrebbero non essere supportati.
* Le risorse non elaborate devono essere elaborate e la proprietà dam:assetState sul nodo jcr:content della risorsa deve essere impostata su &quot;elaborati&quot; o rimuovere queste risorse dal set di migrazione prima di migrare ad AEMaaCS.
* Gli URL personalizzati possono essere sostituiti con Apache Rewrites.
* Consulta le [note sulla versione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it) per scoprire le ultime modifiche implementate in AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
