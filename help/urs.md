---
title: URS
description: Pagina della guida del codice di Pattern Detector
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 3e14d73acbe480dd861f492c24f67ffc37b1090d
workflow-type: ht
source-wordcount: '436'
ht-degree: 100%

---

# URS {#urs}

Struttura dell’archivio non supportata

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Struttura dell’archivio non supportata"
>abstract="URS identifica casi di struttura dell’archivio non supportata e caratteristiche dei nodi. Mette in evidenza informazioni che evitano conflitti tra codice prodotto AEM e codice del cliente: il contenuto viene ristrutturato da /etc ad altre cartelle nell’archivio e altro ancora."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=it" text="Ristrutturazione dell’archivio"

## Sfondo {#background}

`URS` identifica casi di struttura dell’archivio non supportata e caratteristiche del nodo. A partire dalla versione AEM 6.4 sono state fornite linee guida per la ristrutturazione del contenuto dell’archivio. Delineando chiaramente le gerarchie per codice prodotto AEM e codice del cliente ed evitando conflitti tra di loro, il contenuto viene ristrutturato da `/etc` ad altre cartelle nell’archivio, in conformità alle seguenti regole di alto livello:

* Il codice prodotto AEM verrà sempre inserito in `/libs`, che non deve essere sovrascritto dal codice personalizzato.
* Il codice personalizzato deve essere inserito in `/apps`, `/content` e `/conf`.
* AEM as a Cloud Service non supporta i nomi dei nodi lunghi (>150 byte).
* Si consiglia vivamente di seguire queste linee guida per AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i tipi specifici di problemi dell’archivio che devono essere risolti:
* `clientlibs.location`: libreria client che fa riferimento a `/etc` per percorso.
* `file.location`: file in `/etc` che è stato modificato dopo l’installazione.
* `node.location`: nodo sotto `/etc` che è stato modificato dopo l’installazione.
* `workflow.location`: modello di flusso di lavoro o modulo di avvio in `/etc/workflow`.
* `package.structure`: pacchetto che contiene sia contenuti mutabili che immutabili.
* `node.name.length`: nome di nodo con lunghezza non supportata.
* `node.size`: nodo con dimensioni non supportate.

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice personalizzato che si basa su percorsi meno recenti può causare comportamenti indesiderati e influire sulle funzionalità del prodotto.
* I pacchetti con contenuto sia mutabile che immutabile probabilmente causeranno problemi durante la distribuzione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guida all’implementazione"
>abstract="È consigliabile rivedere il progetto di codice e assicurarsi che sia conforme alle linee guida sulla struttura del progetto AEM ed evitare che il codice si basi su percorsi di archivio precedenti/non supportati che possano causare comportamenti indesiderati in AEM as a Cloud Service. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=it" text="Linee guida sulla struttura dei progetti AEM"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Fai riferimento a [Ristrutturazione dell’archivio](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html?lang=it) per indicazioni di preparazione per AEM as a Cloud Service.
* Fai riferimento anche a [Struttura del progetto AEM](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=it) per ulteriori informazioni sulle aree mutabili e immutabili dell’archivio.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
* Sfrutta il [Modernizzatore dell’archivio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html?lang=it#refactoring-tools) per ristrutturare i pacchetti di progetto esistenti separando il contenuto e il codice in pacchetti diversi in modo che siano compatibili con la struttura di progetto definita per Adobe Experience Manager as a Cloud Service.
