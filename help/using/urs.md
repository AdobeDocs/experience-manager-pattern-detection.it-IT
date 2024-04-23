---
title: URS
description: Pagina della guida del codice di Pattern Detector.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 55%

---

# URS {#urs}

Struttura dell’archivio non supportata

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Struttura dell’archivio non supportata"
>abstract="URS identifica casi di struttura dell’archivio non supportata e caratteristiche dei nodi. Mette in evidenza informazioni che evitano conflitti tra codice prodotto AEM e codice del cliente: il contenuto viene ristrutturato da /etc ad altre cartelle nell’archivio e altro ancora."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Ristrutturazione dell’archivio"

## Sfondo {#background}

URS identifica casi di struttura dell’archivio non supportata e caratteristiche dei nodi. A partire dalla versione AEM 6.4 sono state fornite linee guida per la ristrutturazione del contenuto dell’archivio. Delineando chiaramente le gerarchie per codice prodotto AEM e codice del cliente ed evitando conflitti tra di loro, il contenuto viene ristrutturato da `/etc` ad altre cartelle nell’archivio, in conformità alle seguenti regole di alto livello:

* Il codice del prodotto AEM è sempre inserito in `/libs`, che non deve essere sovrascritto dal codice personalizzato.
* Il codice personalizzato deve essere inserito in `/apps`, `/content`, e `/conf`.
* Si consiglia vivamente di seguire queste linee guida per AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i tipi specifici di problemi dell’archivio che devono essere risolti:

* `clientlibs.location`: libreria client che fa riferimento a `/etc` per percorso.
* `file.location`: file in `/etc` che è stato modificato dopo l’installazione.
* `node.location`: nodo sotto `/etc` che è stato modificato dopo l’installazione.
* `workflow.location`: modello di flusso di lavoro o modulo di avvio in `/etc/workflow`.
* `package.structure`: pacchetto che contiene sia contenuti mutabili che immutabili.
* `node.size`: nodo con dimensioni non supportate.

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice personalizzato che si basa su percorsi meno recenti può causare comportamenti indesiderati e influire sulle funzionalità del prodotto.
* I pacchetti con contenuto sia mutabile che immutabile possono causare problemi durante la distribuzione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere il progetto di codice. Assicurati che sia conforme alle linee guida sulla struttura dei progetti dell’AEM ed evita che il codice si basi su percorsi di archivio precedenti/non supportati che possano causare comportamenti indesiderati negli as a Cloud Service AEM. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Linee guida sulla struttura dei progetti AEM"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Consulta [Ristrutturazione dell’archivio](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring) come guida per la preparazione all’AEM as a Cloud Service.
* Vedi anche [Struttura dei progetti AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) per ulteriori informazioni sulle aree mutabili e immutabili dell’archivio.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it) per ottenere chiarimenti o per fugare i dubbi.
* Utilizza il [Repository Modernizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) per ristrutturare i pacchetti di progetto esistenti separando il contenuto e il codice in pacchetti distinti in modo che siano compatibili con la struttura di progetto definita per Adobe Experience Manager as a Cloud Service.
