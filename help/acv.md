---
title: ACV
description: Pagina della guida del codice del rilevatore pattern
exl-id: 7e3c1142-c349-4bce-b8de-8e91528f80a5
source-git-commit: d61fbb28fdf91fd9b356654d5cd2d50b156398c4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# ACV {#acv}

Convalida del contenuto delle risorse

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_overview"
>title="Convalida del contenuto delle risorse"
>abstract="ACV identifica i nodi obbligatori mancanti nel contenuto delle risorse."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/home.html" text="Modifiche di rilievo - Experience Manager come Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="Experience Manager come Cloud Service - Note sulla versione"

`ACV`  La funzione di convalida del contenuto delle risorse identifica i nodi obbligatori mancanti nel contenuto delle risorse. Questo potrebbe causare l’errore di alcune funzionalità di Assets all’Experience Manager come Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `assets.sanity.missing.jcrcontent`: Identifica le cartelle con nodi obbligatori mancanti nel repository. L’identificazione di eventuali contenuti mancanti nell’archivio aiuta a prevenire eventuali funzioni o casi d’uso non funzionanti.

## Possibili implicazioni e rischi {#implications-and-risks}

Questo potrebbe causare l’errore di alcune funzionalità di Assets che dipendono dalle proprietà ereditate in Experience Manager come Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_acv_guidance"
>title="Guida all&#39;implementazione"
>abstract="Adobe consiglia di rivedere la struttura del contenuto per evitare flussi di lavoro interrotti che dipendono da proprietà ereditate. Contatta l’Assistenza clienti per ricevere assistenza&quot;.
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Analizza una cartella se presenta un nodo figlio mancante. Crea manualmente i nodi se il numero di cartelle è gestibile, altrimenti utilizza uno script.
* Rivolgiti al nostro [Experience Manager Customer Care Team](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per affrontare i problemi.
