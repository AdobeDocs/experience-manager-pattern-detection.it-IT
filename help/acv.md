---
title: ACV
description: Pagina della guida del codice di Pattern Detector
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 09e6149b971dc975dff517d98f8b2faaa8138b51
workflow-type: ht
source-wordcount: '310'
ht-degree: 100%

---

# ACV {#acv}

Assets Content Validator

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifica i nodi obbligatori mancanti nel contenuto delle risorse."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html?lang=it" text="Modifiche di rilievo apportate a Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="Experience Manager as a Cloud Service: note sulla versione"

`ACV` Assets Content Validator identifica i nodi obbligatori mancanti ed eventuali violazioni nel contenuto delle risorse. Questo potrebbe causare errori in alcune funzionalità di Assets in Experience Manager as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `missing.jcrcontent`: identifica le cartelle con nodi obbligatori mancanti nell’archivio. L’identificazione di eventuali contenuti mancanti nell’archivio aiuta a prevenire eventuali funzioni o casi d’uso non funzionanti.
* `missing.original.rendition`: identifica le risorse con una rappresentazione originale obbligatoria mancante nell’archivio.
* `metadata.descendants.violation`: identifica le risorse con più di 100 discendenti sotto il nodo dei metadati della risorsa nell’archivio.

## Possibili implicazioni e rischi {#implications-and-risks}

* Questo potrebbe causare errori in alcune funzionalità di Assets che dipendono dalle proprietà ereditate in Experience Manager as a Cloud Service.
* AEM Assets dipende dall’esistenza della rappresentazione originale. Se manca la rappresentazione originale, l’elaborazione delle risorse in Cloud Service finirà in loop.
* Un numero elevato di discendenti sotto il nodo dei metadati potrebbe rallentare il caricamento di cartelle contenenti risorse interessate da questa violazione.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guida all’implementazione"
>abstract="Adobe consiglia di rivedere la struttura del contenuto per evitare flussi di lavoro interrotti che dipendono da proprietà ereditate. Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Analizza una cartella se presenta un nodo secondario mancante. Crea manualmente i nodi se il numero di cartelle è gestibile, altrimenti utilizza uno script.
* Se ci sono risorse in cui manca la rappresentazione originale, ricaricale o eliminale prima di eseguire la migrazione.
* Per eventuali domande o dubbi, contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
