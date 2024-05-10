---
title: PCX
description: Pagina della guida del codice di Pattern Detector.
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '198'
ht-degree: 100%

---

# PCX {#pcx}

Complessità della pagina

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complessità della pagina"
>abstract="PCX identifica le pagine che contengono un gran numero di nodi nella loro struttura."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche di rilievo in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: note sulla versione"

`PCX` identifica le pagine la cui struttura contiene numerosi nodi.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `page.complexity.medium`: una pagina contiene un numero moderatamente elevato di nodi che possono influenzare le prestazioni di rendering.
* `page.complexity.high`: una pagina contiene un numero elevato di nodi che possono influenzare le prestazioni di rendering.

## Possibili implicazioni e rischi {#implications-and-risks}

* Molti nodi all’interno di una pagina possono influire sulle prestazioni di rendering.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere la struttura del contenuto per ridurre la complessità delle pagine, il che contribuirebbe a migliorarne le prestazioni di rendering. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Riduci il numero totale di nodi all’interno di una pagina eseguendo la seguente azione:
   * Verifica che non siano presenti contenitori non necessari.
   * Verifica se è possibile ottenere lo stesso layout con un numero inferiore di contenitori.
   * Semplifica il contenuto della pagina.
   * Riduci la profondità della struttura del nodo.
   * Per semplicità, esegui il refactoring dei Frammenti di esperienza inclusi.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
