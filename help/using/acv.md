---
title: ACV
description: Pagina della guida del codice di Pattern Detector.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: ht
source-wordcount: '475'
ht-degree: 100%

---

# ACV {#acv}

Assets Content Validator

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifica i nodi obbligatori mancanti nel contenuto delle risorse."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/overview" text="Modifiche di rilievo apportate a Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service: note sulla versione"

`ACV` La convalida del contenuto delle risorse identifica i nodi obbligatori mancanti ed eventuali violazioni nel contenuto delle risorse. Questo potrebbe causare errori in alcune funzionalità di Assets in Experience Manager as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `missing.jcrcontent`: identifica le cartelle con nodi obbligatori mancanti nell’archivio. L’identificazione di eventuali contenuti mancanti nell’archivio aiuta a prevenire eventuali funzioni o casi d’uso non funzionanti.
* `missing.original.rendition`: identifica le risorse con una rappresentazione originale obbligatoria mancante nell’archivio. L’anteprima delle pagine PDF non richiede la generazione di risorse secondarie in AEMaaCS. Pertanto, per le risorse PDF, viene soppressa la segnalazione di risorse secondarie con rappresentazione originale mancante.
* `metadata.descendants.violation`: identifica le risorse con più di 100 discendenti sotto il nodo dei metadati della risorsa nell’archivio.
* `conflict.node`: identifica la presenza di nodi di conflitto nell’archivio sotto il percorso /content/dam/.
* `psb.file.large`: identifica file PSB di grandi dimensioni (`dc:format : application/vnd.3gpp.pic-bw-small`) superiori a 2 GB.
* `invalid.asset.name`: identifica le risorse con caratteri non validi[`* / : [ \ ] | # % { } ? &`] nel nome.

## Possibili implicazioni e rischi {#implications-and-risks}

* Questo potrebbe causare l’errore di alcune funzionalità di Assets che dipendono dalle proprietà ereditate in Experience Manager as a Cloud Service.
* AEM Assets dipende dall’esistenza della rappresentazione originale. Se manca la rappresentazione originale, l’elaborazione delle risorse in Cloud Service dà luogo a un’esecuzione in loop. La generazione di risorse secondarie non è supportata in AEMaaCS.
* Un numero elevato di discendenti sotto un nodo di metadati potrebbe rallentare il download delle cartelle che contengono risorse interessate dalla violazione.
* La presenza di nodi di conflitto potrebbe causare un errore di acquisizione su AEM as a Cloud Service.
* Experience Manager potrebbe non elaborare file PSB ad alta risoluzione. Se utilizzi ImageMagick per l’elaborazione di file di grandi dimensioni, potresti riscontrare un impatto sulle prestazioni se non esegui un corretto benchmarking del server Experience Manager.
* I caratteri non validi nel nome della risorsa potrebbero causare errori durante la migrazione ad AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guida all’implementazione"
>abstract="Adobe consiglia di rivedere la struttura del contenuto per evitare flussi di lavoro interrotti che dipendono da proprietà ereditate. Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Analizza una cartella se presenta un nodo secondario mancante. Crea manualmente i nodi se il numero di cartelle è gestibile, altrimenti utilizza uno script.
* Se ci sono risorse in cui manca la rappresentazione originale, ricaricale o eliminale prima di eseguire la migrazione.
* Non è necessaria alcuna azione in caso di rappresentazioni originali mancanti per risorse secondarie.
* In caso di nodi di conflitto, è necessario risolverli o eliminarli prima di eseguire la migrazione a AEM as a Cloud Service.
* Se intendi elaborare molti file PSD o PSB di grandi dimensioni, contatta l’Assistenza clienti Adobe. Experience Manager potrebbe non elaborare file PSB con una risoluzione superiore a 30000x23000 pixel. Consulta la [documentazione](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick).
* Contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
