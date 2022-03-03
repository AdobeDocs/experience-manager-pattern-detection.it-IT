---
title: PCX
description: Pagina della guida del codice di Pattern Detector
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: ht
source-wordcount: '227'
ht-degree: 100%

---

# PCX {#pcx}

Complessità della pagina

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complessità della pagina"
>abstract="PCX identifica le pagine che contengono un gran numero di nodi nella loro struttura."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM as a Cloud Service: note sulla versione"

`PCX` identifica le pagine che contengono un numero elevato di nodi nella struttura.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `page.complexity.medium`: una pagina contiene un numero moderatamente elevato di nodi che possono influenzare le prestazioni di rendering.
* `page.complexity.high`: una pagina contiene un numero molto elevato di nodi che probabilmente influenzeranno le prestazioni di rendering.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un numero elevato di nodi all’interno di una pagina può influire sulle prestazioni di rendering.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere la struttura del contenuto per ridurre la complessità delle pagine, il che contribuirebbe a migliorarne le prestazioni di rendering. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Puoi adottare misure per ridurre il numero totale di nodi all’interno di una pagina, tra cui:
   * Verifica che non siano presenti contenitori non necessari.
   * Verifica se è possibile ottenere lo stesso layout con un numero inferiore di contenitori.
   * Semplifica il contenuto della pagina.
   * Riduci la profondità della struttura del nodo.
   * Per semplicità, esegui il refactoring dei Frammenti di esperienza inclusi.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
