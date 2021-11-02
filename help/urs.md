---
title: URS
description: Pagina della guida del codice del rilevatore pattern
exl-id: 05c5b664-f034-42a2-918b-07772c8d480f
source-git-commit: 3e14d73acbe480dd861f492c24f67ffc37b1090d
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 3%

---

# URS {#urs}

Struttura dell’archivio non supportata

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_overview"
>title="Struttura dell’archivio non supportata"
>abstract="URS identifica casi di struttura dell’archivio non supportata e caratteristiche dei nodi. Questo consente di rimuovere informazioni per evitare conflitti tra AEM codice prodotto e codice cliente, il contenuto viene ristrutturato da /etc ad altre cartelle nell’archivio e altro ancora."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html" text="Ristrutturazione dell’archivio"

## Sfondo {#background}

`URS` identifica casi di struttura dell&#39;archivio non supportata e caratteristiche del nodo. A partire dal AEM 6.4 sono state fornite linee guida per la ristrutturazione del contenuto dell’archivio. delineando chiaramente le gerarchie per AEM codice prodotto e codice cliente ed evitare conflitti tra di loro, il contenuto viene ristrutturato `/etc` ad altre cartelle nel repository, in conformità alle seguenti regole di alto livello:

* AEM codice prodotto verrà sempre inserito in `/libs`, che non deve essere sovrascritto dal codice personalizzato.
* Il codice personalizzato deve essere inserito in `/apps`, `/content` e `/conf`.
* AEM as a Cloud Service non supporta i nomi dei nodi lunghi (>150 byte).
* Si consiglia vivamente di seguire queste linee guida per AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i tipi specifici di problemi dell’archivio che devono essere risolti:
* `clientlibs.location`: Una libreria client che fa riferimento a `/etc` per percorso.
* `file.location`: Un file in `/etc` che è stato modificato dopo l&#39;installazione.
* `node.location`: Un nodo sotto `/etc` che è stato modificato dopo l&#39;installazione.
* `workflow.location`: Un modello di flusso di lavoro o un modulo di avvio in `/etc/workflow`.
* `package.structure`: Un pacchetto che contiene sia contenuti mutabili che immutabili.
* `node.name.length`: Nome di nodo con lunghezza non supportata.
* `node.size`: Un nodo con dimensioni non supportate.

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice personalizzato che si basa su percorsi meno recenti può causare comportamenti indesiderati e influire sulle funzionalità del prodotto.
* I pacchetti contenenti contenuto sia mutabile che immutabile causeranno probabilmente problemi durante la distribuzione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_urs_guidance"
>title="Guida all&#39;implementazione"
>abstract="È consigliabile rivedere il progetto di codice e assicurarsi che sia conforme alle linee guida sulla struttura del progetto AEM ed evitare che il codice si basi su percorsi di archivio precedenti/non supportati che possano causare comportamenti indesiderati in AEM as a Cloud Service. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html" text="Linee guida per la struttura del progetto AEM"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Fai riferimento a [Ristrutturazione dell’archivio](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) per informazioni da preparare per AEM as a Cloud Service.
* Fai riferimento anche a [AEM struttura del progetto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=it) per ulteriori informazioni sulle aree mutabili e immutabili dell’archivio.
* Per favore, contatta il nostro [Team di supporto AEM](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) ottenere chiarimenti o affrontare le preoccupazioni.
* Sfruttare [Modernizzatore dell&#39;archivio](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) per ristrutturare i pacchetti di progetto esistenti separando il contenuto e il codice in pacchetti discreti in modo che siano compatibili con la struttura di progetto definita per Adobe Experience Manager as a Cloud Service.
