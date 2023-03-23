---
title: CDW
description: Pagina della guida del codice di Pattern Detector
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: d12f2613493d9bf379464d9c089ad376532c4de2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 100%

---

# CDW {#cdw}

Custom Dialog Widget (CDW, widget per finestre di dialogo personalizzati)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Custom Dialog Widget (CDW, widget per finestre di dialogo personalizzati)"
>abstract="CDW identifica i widget per finestre di dialogo personalizzati che devono essere aggiornati per renderli compatibili con AEM as a Cloud Service."

I widget per finestre di dialogo personalizzati `CDW` identificano i widget per finestre di dialogo CoralUI e Classic personalizzati. Questi devono essere aggiornati per renderli compatibili con AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `custom.coral.widget`: identifica i widget per finestre di dialogo personalizzati basati su CoralUI 2 o CoralUI 3.
* `custom.classic.widget`: identifica i widget per finestre di dialogo personalizzati basati su ExtJs.

## Possibili implicazioni e rischi {#implications-and-risks}

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I widget per finestre di dialogo classici personalizzati devono essere convertiti da ExtJS a [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* I widget per finestre di dialogo Coral personalizzati devono essere valutati per l’aggiornamento a CoralUI 3.
* Per eventuali domande o dubbi, contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
