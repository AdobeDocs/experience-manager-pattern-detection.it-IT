---
title: INST
description: Pagina della guida del codice del rilevatore pattern
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# INST {#inst}

Artifact installato

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artifact installato"
>abstract="INST identifica i pacchetti e i bundle personalizzati e di terze parti che sono stati installati in AEM dal cliente. Questi sono segnalati per aiutare a caratterizzare lo stato del sistema e l&#39;ambito generale di uno sforzo di aggiornamento. Qualsiasi pacchetto di terze parti deve rispettare il AEM come guida Cloud Service per lo sviluppo e l&#39;imballaggio."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Orientamenti per lo sviluppo - AEM come Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html" text="Linee guida sugli imballaggi - AEM come Cloud Service"

`INST` identifica pacchetti e bundle personalizzati e di terze parti installati in AEM dal cliente. Questi sono segnalati per aiutare a caratterizzare lo stato del sistema e l&#39;ambito generale di uno sforzo di aggiornamento.

Quando sono state installate più versioni di un pacchetto, viene segnalata solo la versione più recente.

I pacchetti e i bundle rilevati non sono stati necessariamente ottimizzati per AEM come Cloud Service. Qualsiasi pacchetto di terze parti deve essere verificato con il suo creatore o Adobe per la compatibilità con AEM come Cloud Service.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `custom.bundle`: Un bundle installato in AEM.
* `custom.package`: Un pacchetto installato in AEM.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Guida all&#39;implementazione"
>abstract="I clienti non possono più installare pacchetti di terze parti utilizzando CRX Package Manager. I clienti devono rivedere questi artefatti installati e devono essere strutturati e ottimizzarli per lavorare con AEM come Cloud Service. Qualsiasi pacchetto di terze parti deve essere verificato con il suo creatore o Adobe per la compatibilità con AEM come Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embeddeds" text="Incorporazione di pacchetti secondari nel pacchetto contenitore"


* L&#39;installazione di pacchetti di terze parti che utilizzano CRX Package Manager non è possibile in AEM come Cloud Service.
* Le applicazioni dipendenti da pacchetti di terze parti potrebbero non funzionare come previsto fino a quando non vengono distribuite correttamente per funzionare con AEM come Cloud Service.
* I pacchetti fornitore di terze parti, se non ottimizzati per AEM as a Cloud Service, possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND-legacy per capire come le violazioni INST possono essere rese compatibili con AEM Cloud Service. Inoltre, Rivedi l&#39;esempio di violazione INST su Github per capire come può essere corretto e distribuito in AEM come Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Progetto legacy WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Esempio di violazione INST - Github"

* I pacchetti di terze parti devono essere distribuiti in AEM come parte del progetto utilizzando il processo di distribuzione di Cloud Manager [](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Rivedi come [incorporare pacchetti di terze parti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) nel tuo progetto per AEM come Cloud Service.
* I pacchetti di terze parti devono attenersi alle linee guida di AEM come Cloud Service [sviluppo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) e [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e scopri come è possibile correggere [violazioni INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) e renderlo compatibile con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
