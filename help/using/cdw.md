---
title: CDW
description: Pagina della guida del codice di Pattern Detector.
exl-id: a9e9dae8-0aa2-4679-a3c1-418cab01cfda
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 87%

---

# CDW {#cdw}

Custom Dialog Widget (CDW, widget per finestre di dialogo personalizzati)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Custom Dialog Widget (CDW, widget per finestre di dialogo personalizzati)"
>abstract="CDW identifica i widget per finestre di dialogo personalizzati che devono essere aggiornati per renderli compatibili con AEM as a Cloud Service."

I widget per finestre di dialogo personalizzati `CDW` identificano i widget per finestre di dialogo classici personalizzati. Questi devono essere aggiornati per renderli compatibili con AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare le informazioni, ad esempio:

* `custom.classic.widget`: identifica i widget per finestre di dialogo personalizzati basati su ExtJs.

## Possibili implicazioni e rischi {#implications-and-risks}

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it" text="Supporto Experience Cloud"

* I widget per finestre di dialogo classici personalizzati devono essere convertiti da ExtJS a [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* Contatta il [Experience Manager team di assistenza clienti](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
