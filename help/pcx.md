---
title: PCX
description: Pagina della guida del codice del rilevatore pattern
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a0
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 3%

---

# PCX {#pcx}

Complessità pagina

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_overview"
>title="Complessità pagina"
>abstract="PCX identifica le pagine che contengono un gran numero di nodi nella loro struttura."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Modifiche di rilievo - AEM come Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM come Cloud Service - Note sulla versione"

`PCX` identifica le pagine che contengono un numero elevato di nodi nella loro struttura.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `page.complexity.medium`: Una pagina contiene un numero moderatamente elevato di nodi che possono influenzare le prestazioni di rendering.
* `page.complexity.high`: Una pagina contiene un numero molto elevato di nodi che probabilmente influenzeranno le prestazioni di rendering.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un numero elevato di nodi all’interno di una pagina può influire sulle prestazioni di rendering.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_pcx_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di rivedere la struttura del contenuto per ridurre la complessità delle pagine, il che contribuirebbe a migliorare le prestazioni di rendering delle pagine. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Adotta misure per ridurre il numero totale di nodi all’interno di una pagina, tra cui:
   * Verifica che non siano presenti contenitori non necessari.
   * Verifica se è possibile ottenere lo stesso layout con un numero inferiore di contenitori.
   * Semplifica il contenuto della pagina.
   * Ridurre la profondità della struttura del nodo.
   * Per semplicità, considera nuovamente i frammenti esperienza inclusi.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
