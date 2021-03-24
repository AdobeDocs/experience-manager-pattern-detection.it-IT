---
title: URS
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---


# URS {#urs}

Struttura dell’archivio non supportata

## Sfondo {#background}

`URS` identifica i casi di struttura dell&#39;archivio non supportata. A partire dal AEM 6.4 sono state fornite linee guida per la ristrutturazione del contenuto dell’archivio. delineando chiaramente le gerarchie per AEM codice prodotto e codice cliente ed evitare conflitti tra loro, il contenuto viene ristrutturato da `/etc` ad altre cartelle nell’archivio, in conformità alle seguenti regole di alto livello:

* AEM codice prodotto verrà sempre inserito in `/libs`, che non deve essere sovrascritto dal codice personalizzato Il codice personalizzato deve essere inserito in `/apps`, `/content` e `/conf`.
* Si raccomanda vivamente che tali linee guida siano seguite per AEM come Cloud Service.

I sottotipi vengono utilizzati per identificare i tipi specifici di problemi dell’archivio che devono essere risolti:
* `clientlibs.location`: Una libreria client che fa riferimento  `/etc` per percorso.
* `file.location`: Un file in  `/etc` che è stato modificato dopo l&#39;installazione.
* `node.location`: Un nodo sotto  `/etc` che è stato modificato dopo l&#39;installazione.
* `workflow.location`: Un modello di flusso di lavoro o un modulo di avvio in  `/etc/workflow`.
* `package.structure`: Un pacchetto che contiene sia contenuti mutabili che immutabili.

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice personalizzato che si basa su percorsi meno recenti può causare comportamenti indesiderati e influire sulle funzionalità del prodotto.
* I pacchetti contenenti contenuto sia mutabile che immutabile causeranno probabilmente problemi durante la distribuzione.

## Soluzioni possibili {#solutions}

* Fai riferimento a [Ristrutturazione dell&#39;archivio](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/restructuring/repository-restructuring.html) per informazioni su come prepararsi per AEM come Cloud Service.
* Per ulteriori informazioni sulle aree mutabili e immutabili dell’archivio, consulta anche [AEM Struttura del progetto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) .
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
* Utilizza il [Repository Modernizer](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/repo-modernizer.html#refactoring-tools) per ristrutturare i pacchetti di progetto esistenti separando il contenuto e il codice in pacchetti discreti in modo da essere compatibile con la struttura di progetto definita per Adobe Experience Manager come Cloud Service.