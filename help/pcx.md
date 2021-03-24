---
title: PCX
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# PCX {#pcx}

Complessità pagina

## Sfondo {#background}

`PCX` identifica le pagine che contengono un numero elevato di nodi nella loro struttura.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `page.complexity.medium`: Una pagina contiene un numero moderatamente elevato di nodi che possono influenzare le prestazioni di rendering.
* `page.complexity.high`: Una pagina contiene un numero molto elevato di nodi che probabilmente influenzeranno le prestazioni di rendering.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un numero elevato di nodi all’interno di una pagina può influire sulle prestazioni di rendering.

## Soluzioni possibili {#solutions}

* Adotta misure per ridurre il numero totale di nodi all’interno di una pagina, tra cui:
   * Verifica che non siano presenti contenitori non necessari.
   * Verifica se è possibile ottenere lo stesso layout con un numero inferiore di contenitori.
   * Semplifica il contenuto della pagina.
   * Ridurre la profondità della struttura del nodo.
   * Per semplicità, considera nuovamente i frammenti esperienza inclusi.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
