---
title: ACV
description: Pagina della guida del codice del rilevatore pattern
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: 57e33b97aba253bad62cf95dcca9ef6885d263e6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ACV {#acv}

Convalida del contenuto delle risorse

## Sfondo {#background}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_overview&quot;
>title=&quot;Convalida del contenuto delle risorse&quot;
>abstract=&quot;ACV identifica i nodi obbligatori mancanti nel contenuto delle risorse.&quot;
>add-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html&quot; text=&quot;Modifiche di rilievo - Experience Manager come Cloud Service&quot;
>additional-url=&quot;https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html&quot; text=&quot;Experience Manager as a Cloud Service - Note sulla versione&quot;

`ACV`  La funzione di convalida del contenuto delle risorse identifica i nodi obbligatori mancanti nel contenuto delle risorse. Questo potrebbe causare l’errore di alcune funzionalità di Assets all’Experience Manager come Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `assets.sanity.missing.jcrcontent`: Identifica le cartelle con nodi obbligatori mancanti nel repository. L’identificazione di eventuali contenuti mancanti nell’archivio aiuta a prevenire eventuali funzioni o casi d’uso non funzionanti.

## Possibili implicazioni e rischi {#implications-and-risks}

Questo potrebbe causare l’errore di alcune funzionalità di Assets che dipendono dalle proprietà ereditate in Experience Manager come Cloud Service.

## Soluzioni possibili {#solutions}

>[!INFO]
>id=&quot;aemcloud_bpa_acv_Guidance&quot;
>title=&quot;Guida all&#39;implementazione&quot;
>abstract=&quot;Adobe consiglia di rivedere la struttura del contenuto per evitare flussi di lavoro interrotti che dipendono dalle proprietà ereditate. Contatta l’Assistenza clienti per ricevere assistenza&quot;.
>add-url=&quot;https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html&quot; text=&quot;Supporto Experience Cloud&quot;

* Analizza una cartella se presenta un nodo figlio mancante. Crea manualmente i nodi se il numero di cartelle è gestibile, altrimenti utilizza uno script.
* Rivolgiti al nostro [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per affrontare i problemi.
