---
title: ACV
description: Pagina della guida del codice di Pattern Detector.
exl-id: 1dd1af45-aa56-48da-8582-c4330cded489
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 67%

---

# ACV {#acv}

Assets Content Validator

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Assets Content Validator"
>abstract="ACV identifica i nodi obbligatori mancanti nel contenuto delle risorse."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview" text="Modifiche di rilievo apportate a Experience Manager as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="Experience Manager as a Cloud Service: note sulla versione"

`ACV` (Convalida del contenuto delle risorse) Identifica i nodi obbligatori mancanti e le violazioni nel contenuto delle risorse. Questo potrebbe causare errori in alcune funzionalità di Assets in Experience Manager as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `missing.jcrcontent`: identifica le cartelle con nodi obbligatori mancanti nell’archivio. L’identificazione di eventuali contenuti mancanti nell’archivio aiuta a prevenire eventuali funzioni o casi d’uso non funzionanti.
* `missing.original.rendition`: identifica le risorse con una rappresentazione originale obbligatoria mancante nell’archivio. Tieni presente che l’anteprima delle pagine PDF non richiede la generazione di risorse secondarie in AEMaaCS. Pertanto, per le risorse PDF, viene soppressa la segnalazione di risorse secondarie con rappresentazione originale mancante.
* `metadata.descendants.violation`: identifica le risorse con più di 100 discendenti sotto il nodo dei metadati della risorsa nell’archivio.
* `conflict.node`: identifica la presenza di nodi di conflitto nell’archivio sotto il percorso /content/dam/.
* `psb.file.large`: identifica file PSB di grandi dimensioni (dc:format : application/vnd.3gpp.pic-bw-small) aventi dimensioni superiori a 2 GB.
* `invalid.asset.name`: identifica le risorse con caratteri non validi [* / : [\] | # % { } ? &amp;] nel nome.

## Possibili implicazioni e rischi {#implications-and-risks}

* Questo potrebbe causare errori in alcune funzionalità di Assets che dipendono dalle proprietà ereditate in Experience Manager as a Cloud Service.
* AEM Assets dipende dall’esistenza della rappresentazione originale. L’elaborazione delle risorse nel Cloud Service viene ripetuta se manca la rappresentazione originale. La generazione di risorse secondarie non è supportata in AEMaaCS.
* Un numero elevato di discendenti sotto il nodo dei metadati potrebbe rallentare il download di cartelle contenenti risorse che violano questo criterio.
* La presenza di nodi di conflitto potrebbe causare un errore di acquisizione su AEM as a Cloud Service.
* L&#39;Experience Manager potrebbe non elaborare file PSB ad alta risoluzione. Se utilizzi ImageMagick per l’elaborazione di file di grandi dimensioni, potresti riscontrare un impatto sulle prestazioni se non esegui un corretto benchmarking del server Experience Manager.
* I caratteri non validi nel nome della risorsa potrebbero causare errori durante la migrazione ad AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guida all’implementazione"
>abstract="L’Adobe consiglia di rivedere la struttura del contenuto per evitare flussi di lavoro interrotti che dipendono da proprietà ereditate. Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it" text="Supporto Experience Cloud"

* Analizza una cartella se presenta un nodo secondario mancante. Crea manualmente i nodi se il numero di cartelle è gestibile, altrimenti utilizza uno script.
* Se ci sono risorse in cui manca la rappresentazione originale, ricaricale o eliminale prima di eseguire la migrazione.
* Non è necessaria alcuna azione in caso di rappresentazioni originali mancanti per risorse secondarie.
* In sono presenti nodi in conflitto che devono essere risolti o eliminati prima di migrare all’AEM as a Cloud Service.
* Contatta l’Assistenza clienti Adobe se intendi elaborare molti file PSD o PSB di grandi dimensioni. L&#39;Experience Manager non può elaborare file PSB ad alta risoluzione con una risoluzione superiore a 30000 x 23000 pixel. Consulta [documentazione](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/extending/best-practices-for-imagemagick).
* Contatta il [Experience Manager team di assistenza clienti](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
