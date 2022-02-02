---
title: ASO
description: Pagina della guida del codice del rilevatore pattern
exl-id: 2ba416b7-80c1-4ec5-a6bf-d80f6d625b07
source-git-commit: d45c6b561a9665cbac39bfd8d9ce6eb2658c24e8
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 4%

---

# ASO {#aso}

Panoramica del sistema AEM

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_overview"
>title="Panoramica del sistema AEM"
>abstract="Il codice ASO identifica le informazioni generali sull&#39;istanza AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema che possono essere utili per la pianificazione e il refactoring della migrazione."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html" text="AEM as a Cloud Service - Note sulla versione"

`ASO` identifica informazioni generali sull&#39;istanza AEM. Ogni risultato fornisce un valore di un particolare tipo di informazioni di sistema.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `aem.version`: Versione AEM.
* `aem.product`: Rilevamento dell’uso di un prodotto AEM (Commerce, Forms, ecc.).
* `node.count`: Conteggio approssimativo dei nodi di un determinato tipo (Pagina, Risorsa, ecc.) e il totale complessivo dei nodi.
* `node.store`: Il tipo di implementazione dell&#39;archivio nodi (SegmentNodeStore, DocumentNodeStore) e le relative dimensioni.
* `data.store`: Tipo di implementazione dell’archivio dati (FileDataStore, S3DataStore, AzureDataStore).
* `maintenance.task`: Attività di manutenzione.
* `slow.query`: Query lenta.
* `group.membership`: Il numero di utenti e sottogruppi ( solo membri diretti/dichiarati ) in un gruppo.
* `cqtag.count`: Il numero di risorse con tag CQ.
* `smarttag.count`: Il numero di risorse con tag avanzati.
* `ccom.version`: Versione del pacchetto del componente core.
* `instance.type`: Il tipo di istanza AEM (author|publish).

## Possibili implicazioni e rischi {#implications-and-risks}

* La versione AEM, i conteggi dei nodi, l’appartenenza al gruppo, l’archivio dei nodi, i tipi di implementazione dell’archivio dati, il conteggio dei tag CQ, il conteggio dei tag avanzati, la versione del componente core e AEM tipo di istanza sono forniti a scopo informativo.
* L’applicazione personalizzata può basarsi su prodotti o funzionalità non disponibili in AEM as a Cloud Service.
* L’aggiornamento con funzioni non supportate potrebbe causare un errore di aggiornamento e un’applicazione non funzionante.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_aso_guidance"
>title="Guida all&#39;implementazione"
>abstract="Le informazioni esposte tramite codice ASO forniscono informazioni generali per l’ambiente AEM, tra cui versione, componenti aggiuntivi per prodotti, informazioni a livello di sistema, che devono essere esaminate per tutti i prodotti o le funzionalità non supportati in AEM as a Cloud Service. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Gli aggiornamenti AEM con prodotti o funzionalità non supportati non sono consigliati e potrebbero non essere supportati.
* Consulta la sezione [note sulla versione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it) per scoprire le ultime modifiche in AEM as a Cloud Service.
* Per favore, contatta il nostro [Team di supporto AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) ottenere chiarimenti o affrontare le preoccupazioni.
