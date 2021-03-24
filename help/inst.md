---
title: INST
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# INST {#inst}

Artifact installato

## Sfondo {#background}

`INST` identifica pacchetti e bundle personalizzati e di terze parti installati in AEM dal cliente. Questi sono segnalati per aiutare a caratterizzare lo stato del sistema e l&#39;ambito generale di uno sforzo di aggiornamento.

Quando sono state installate più versioni di un pacchetto, viene segnalata solo la versione più recente.

I pacchetti e i bundle rilevati non sono stati necessariamente ottimizzati per AEM come Cloud Service. Qualsiasi pacchetto di terze parti deve essere verificato con il suo creatore o Adobe per la compatibilità con AEM come Cloud Service.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `custom.bundle`: Un bundle installato in AEM.
* `custom.package`: Un pacchetto installato in AEM.

## Possibili implicazioni e rischi {#implications-and-risks}

* L&#39;installazione di pacchetti di terze parti che utilizzano CRX Package Manager non è possibile in AEM come Cloud Service.
* Le applicazioni dipendenti da pacchetti di terze parti potrebbero non funzionare come previsto fino a quando non vengono distribuite correttamente per funzionare con AEM come Cloud Service.
* I pacchetti fornitore di terze parti, se non ottimizzati per AEM as a Cloud Service, possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

* I pacchetti di terze parti devono essere distribuiti in AEM come parte del progetto utilizzando il processo di distribuzione di Cloud Manager [](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/using-cloud-manager/deploy-code.html#deployment-process).
* Rivedi come [incorporare pacchetti di terze parti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#embedding-3rd-party-packages) nel tuo progetto per AEM come Cloud Service.
* I pacchetti di terze parti devono attenersi alle linee guida di AEM come Cloud Service [sviluppo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html) e [packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/repository-structure-package.html).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e scopri come è possibile correggere [violazioni INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) e renderlo compatibile con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
