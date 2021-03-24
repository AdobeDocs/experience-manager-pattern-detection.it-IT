---
title: ASO
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 4%

---


# ASO {#aso}

Panoramica del sistema AEM

## Sfondo {#background}

`ASO` identifica informazioni generali sull&#39;istanza AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `aem.version`: Versione AEM.
* `aem.product`: Rilevamento dell’uso di un prodotto AEM (Commerce, Forms, ecc.).
* `node.count`: Numero approssimativo di nodi di un determinato tipo (Pagina, Risorsa, ecc.).
* `node.store`: Il tipo di implementazione dell&#39;archivio nodi (SegmentNodeStore, DocumentNodeStore).
* `data.store`: Tipo di implementazione dell’archivio dati (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Attività di manutenzione.
* `slow.query`: Query lenta.

## Possibili implicazioni e rischi {#implications-and-risks}

* I tipi di implementazione della versione AEM, dei conteggi dei nodi, dell’archivio nodi e dell’archivio dati sono forniti a scopo informativo.
* L’applicazione personalizzata può basarsi su prodotti o funzionalità non disponibili in AEM come Cloud Service.
* L’aggiornamento con funzioni non supportate potrebbe causare un errore di aggiornamento e un’applicazione non funzionante.

## Soluzioni possibili {#solutions}

* Gli aggiornamenti AEM con prodotti o funzionalità non supportati non sono consigliati e potrebbero non essere supportati.
* Consulta le [note sulla versione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it) per scoprire le ultime modifiche in AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
