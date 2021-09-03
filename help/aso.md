---
title: ASO
description: Pagina della guida del codice del rilevatore pattern
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: dc9d6c94d5a724cf24890378ba6a8af7396760c6
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 4%

---

# ASO {#aso}

Panoramica del sistema AEM

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Panoramica del sistema AEM"
>abstract="Il codice ASO identifica le informazioni generali sull&#39;istanza AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema che possono essere utili per la pianificazione e il refactoring della migrazione."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM come Cloud Service - Note sulla versione"

`ASO` identifica informazioni generali sull&#39;istanza AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `aem.version`: Versione AEM.
* `aem.product`: Rilevamento dell’uso di un prodotto AEM (Commerce, Forms, ecc.).
* `node.count`: Conteggio approssimativo dei nodi di un determinato tipo (Pagina, Risorsa, ecc.) e il totale complessivo dei nodi.
* `node.store`: Il tipo di implementazione dell&#39;archivio nodi (SegmentNodeStore, DocumentNodeStore) e le relative dimensioni.
* `data.store`: Tipo di implementazione dell’archivio dati (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Attività di manutenzione.
* `slow.query`: Query lenta.

## Possibili implicazioni e rischi {#implications-and-risks}

* I tipi di implementazione della versione AEM, dei conteggi dei nodi, dell’archivio nodi e dell’archivio dati sono forniti a scopo informativo.
* L’applicazione personalizzata può basarsi su prodotti o funzionalità non disponibili in AEM come Cloud Service.
* L’aggiornamento con funzioni non supportate potrebbe causare un errore di aggiornamento e un’applicazione non funzionante.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guida all&#39;implementazione"
>abstract="Le informazioni esposte tramite codice ASO forniscono informazioni generali per l’ambiente AEM, tra cui versione, componenti aggiuntivi per prodotti, informazioni a livello di sistema, che devono essere esaminate per tutti i prodotti o le funzionalità non supportati in AEM come Cloud Service. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Gli aggiornamenti AEM con prodotti o funzionalità non supportati non sono consigliati e potrebbero non essere supportati.
* Consulta le [note sulla versione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it) per scoprire le ultime modifiche in AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
