---
title: OID
description: Pagina della guida del codice di Pattern Detector
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 100%

---

# OID {#oid}

Definizione dell’indice Oak

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definizione dell’indice Oak"
>abstract="OID identifica i problemi relativi alle definizioni dell’indice Oak. Identifica le modifiche apportate alle definizioni standard dell’indice Oak. Inoltre, identifica le definizioni personalizzate dell’indice Oak incompatibili con AEM as a Cloud Service. Il messaggio di ogni risultato OID identificherà l’indice e fornirà informazioni aggiuntive."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=it#how-to-use" text="Linee guida sull’indicizzazione dei contenuti"

`OID` identifica i problemi relativi alle definizioni dell’indice Oak. Identifica le modifiche apportate alle definizioni standard dell’indice Oak. Inoltre, identifica le definizioni personalizzate dell’indice Oak incompatibili con AEM as a Cloud Service. Il messaggio di ogni risultato `OID` identificherà l’indice e fornirà ulteriori informazioni.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `index.rule.violation`: incompatibilità dell’indice Oak personalizzato con AEM as a Cloud Service.
* `standard.index.modification`: modifica a un indice Oak standard.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Guida all’implementazione"
>abstract="È buona abitudine rivedere tutti gli indici personalizzati e ristrutturarli in base alle linee guida per l’indicizzazione dei contenuti. Sfrutta il convertitore di indice per migrare le definizioni di indice Oak personalizzato esistenti verso la definizione di indice Oak personalizzato compatibile con AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=it#oak-indexes" text="Linee guida per la creazione pacchetti"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=it#refactoring-tools" text="Convertitore indice"

* Le modifiche alle definizioni standard dell’indice Oak possono andare perse durante un aggiornamento AEM.
* Le definizioni Oak non sono modificabili, devono essere inserite nel pacchetto con il codice del progetto del cliente e devono essere distribuite solo utilizzando Cloud Manager.
* Tutte le definizioni dell’indice Oak devono seguire la convenzione di denominazione e altre regole per gli indici Oak in AEM as a Cloud Service. Se non la seguono, possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Strumenti e risorse"
>abstract="Controlla il progetto precedente WKND per capire come possono essere risolte le violazioni OID nel tuo progetto. Inoltre, rivedi l’esempio di violazione OID su Github per capire come gli indici precedenti possono essere convertiti utilizzando lo strumento Convertitore indice e resi compatibili con AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Esempio di violazione OID - Github"

* Risolvi le violazioni della regola dell’indice identificate nel messaggio.
* Segui le [linee guida sulla creazione pacchetti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html?lang=it) di AEM as a Cloud Service per distribuire definizioni di indici Oak nuove o personalizzate.
* Gli indici standard personalizzati AEM e le nuove definizioni di indici Oak personalizzati devono seguire le [linee guida sull’indicizzazione dei contenuti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=it#preparing-the-new-index-definition) di AEM come Cloud Service.
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e scopri come le [violazioni OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
* Sfrutta il [Convertitore indice](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html?lang=it#refactoring-tools) per migrare le definizioni degli indici Oak personalizzati esistenti in definizioni degli indici Oak personalizzati compatibili con AEM as a Cloud Service.
