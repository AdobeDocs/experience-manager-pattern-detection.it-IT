---
title: INST
description: Pagina della guida del codice di Pattern Detector.
exl-id: 9b8129d7-63d7-4975-a68b-9ba704d01532
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 100%

---

# INST {#inst}

Artefatto installato

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_overview"
>title="Artefatto installato"
>abstract="INST identifica i pacchetti e i bundle personalizzati e di terze parti che sono stati installati in AEM dal cliente. Questi vengono segnalati per aiutare a caratterizzare lo stato del sistema e l’ambito generale di un’attività di aggiornamento. Qualsiasi pacchetto di terze parti deve rispettare le linee guida per lo sviluppo e la creazione di pacchetti di AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Linee guida per lo sviluppo in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package" text="Linee guida per la creazione di pacchetti in AEM as a Cloud Service"

`INST` identifica pacchetti e bundle personalizzati e di terze parti installati in AEM dal cliente. Questi vengono segnalati per aiutare a caratterizzare lo stato del sistema e l’ambito generale di un’attività di aggiornamento.

Quando sono state installate più versioni di un pacchetto, viene segnalata solo la versione più recente.

I pacchetti e i bundle rilevati non sono stati necessariamente ottimizzati per AEM as a Cloud Service. La compatibilità di qualsiasi pacchetto di terze parti con AEM as a Cloud Service deve essere verificata con il suo creatore o con Adobe.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `custom.bundle`: bundle che è stato installato in AEM.
* `custom.package`: pacchetto che è stato installato in AEM.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_guidance"
>title="Guida all’implementazione"
>abstract="I clienti non possono più installare pacchetti di terze parti utilizzando Gestione pacchetti CRX. È quindi necessario esaminare gli artefatti installati e fare in modo che siano strutturati e ottimizzati per funzionare con AEM as a Cloud Service. Verifica la compatibilità di AEM as a cloud service con qualsiasi pacchetto di terze parti, confrontandoti con il suo creatore o con Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embeddeds" text="Incorporazione di pacchetti secondari nel pacchetto contenitore"


* L’installazione di pacchetti di terze parti tramite Gestione pacchetti CRX non è possibile in AEM as a Cloud Service.
* Le applicazioni dipendenti da pacchetti di terze parti potrebbero non funzionare come previsto fino a quando non vengono distribuite correttamente per AEM as a Cloud Service.
* I pacchetti di fornitori terze parti, se non ottimizzati per AEM as a Cloud Service, possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_inst_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND precedente per comprendere come le violazioni INST possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione INST su GitHub per capire come può essere corretto e distribuito in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst" text="Esempio di violazione INST: Github"

* I pacchetti di terze parti devono essere distribuiti in AEM come parte del progetto utilizzando il [processo di distribuzione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deployment-process) di Cloud Manager.
* Esamina come [incorporare pacchetti di terze parti](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure#embedding-3rd-party-packages) nel progetto per AEM as a Cloud Service.
* I pacchetti di terze parti devono rispettare le linee guida di [sviluppo](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines) e [creazione pacchetti](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/repository-structure-package) di AEM as a Cloud Service.
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/inst) e scopri come [le violazioni INST](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/inst) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
