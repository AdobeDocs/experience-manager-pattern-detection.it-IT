---
title: URS
description: Pagina della guida del codice di Pattern Detector.
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: b77a168fc8c075e8e41149a38df4d83fd2504a14
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 66%

---

# URS {#urs}

Struttura dell’archivio non supportata

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Struttura dell’archivio non supportata"
>abstract="URS identifica casi di URS (Unsupported Repository Structure) e caratteristiche del nodo. Mette in evidenza informazioni per evitare conflitti tra il codice prodotto AEM e il codice del cliente, in quanto il contenuto viene ristrutturato da `/etc` in altre cartelle del repository e altro ancora."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring" text="Ristrutturazione dell’archivio"

## Informazioni di base {#background}

`URS`  Identifica casi di URS (Unsupported Repository Structure) e caratteristiche del nodo. A partire dalla versione AEM 6.4 sono state fornite linee guida per la ristrutturazione del contenuto dell’archivio. Delineando chiaramente le gerarchie per codice prodotto AEM e codice cliente, ed evitando conflitti tra di loro, il contenuto viene ristrutturato da `/etc` in altre cartelle del repository. In questo modo, rispetta le seguenti regole di alto livello:

* Il codice del prodotto AEM è sempre inserito in `/libs` il codice personalizzato non deve essere sovrascritto.
* Il codice personalizzato deve essere inserito in `/apps`, `/content` e `/conf`.
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
* I pacchetti con contenuto sia mutabile che immutabile probabilmente causeranno problemi durante la distribuzione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guida all’implementazione"
>abstract="La best practice prevede la revisione del progetto di codice. Assicurati che sia conforme alle linee guida sulla struttura dei progetti dell’AEM ed evita che il codice si basi su percorsi di archivio precedenti o non supportati che possano causare comportamenti indesiderati in AEM as a Cloud Service. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure" text="Linee guida sulla struttura dei progetti AEM"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Per indicazioni sulla preparazione per AEM as a Cloud Service, consulta [Ristrutturazione dell’archivio](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/restructuring/repository-restructuring).
* Consulta anche [Struttura del progetto AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) per ulteriori informazioni sulle aree mutabili e immutabili dell’archivio.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
* Utilizza il [Modernizzatore dell’archivio](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/migration-journey/refactoring-tools/repo-modernizer#refactoring-tools) per ristrutturare i pacchetti di progetto esistenti separando il contenuto e il codice in pacchetti diversi, in modo che siano compatibili con la struttura di progetto definita per Adobe Experience Manager as a Cloud Service.
