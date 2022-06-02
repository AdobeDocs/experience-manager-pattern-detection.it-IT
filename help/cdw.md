---
title: CDW
description: Pagina della guida del codice di Pattern Detector
source-git-commit: 04709ba74eedad903669aae589c605542e1e3b09
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 44%

---

# CDW {#cdw}

Widget finestra di dialogo personalizzata

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_overview"
>title="Widget finestra di dialogo personalizzata"
>abstract="CDW identifica i Widget della finestra di dialogo personalizzata che devono essere aggiornati per renderli compatibili con AEM as a Cloud Service."

`CDW`  I widget di finestra di dialogo personalizzati identificano i widget di dialogo personalizzati CoralUI e Classic. Questi devono essere aggiornati per renderli compatibili con AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `custom.coral.widget`: Identifica i widget di dialogo personalizzati in base a CoralUI 2 o CoralUI 3.
* `custom.classic.widget`: Identifica i widget di dialogo personalizzati in base a ExtJs.

## Possibili implicazioni e rischi {#implications-and-risks}

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cdw_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I widget per finestra di dialogo classica personalizzati devono essere convertiti da ExtJS a [CoralUI](https://developer.adobe.com/experience-manager/reference-materials/6-5/coral-ui/coralui3/getting-started.html).
* I widget della finestra di dialogo Coral personalizzati devono essere valutati per l&#39;aggiornamento a CoralUI 3.
* Per eventuali domande o dubbi, contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
