---
title: OID
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 5a83dd8d08da974a5d775032b8dbea2593be9d15
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# OID {#oid}

Definizione dell&#39;indice Oak

## Sfondo {#background}

`OID` identifica i problemi relativi alle definizioni dell&#39;indice Oak. Identifica le modifiche apportate alle definizioni standard dell&#39;indice Oak. Inoltre identifica le definizioni personalizzate dell&#39;indice Oak incompatibili con AEM come Cloud Service. Il messaggio relativo a ciascun risultato `OID` identificherà l&#39;indice e fornirà informazioni aggiuntive.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `custom.index.violation`: Un&#39;incompatibilità dell&#39;indice Oak personalizzato con AEM come Cloud Service.
* `standard.index.modification`: Modifica a un indice Oak standard.

## Possibili implicazioni e rischi {#implications-and-risks}

* Le modifiche alle definizioni standard dell&#39;indice Oak possono andare perse durante un aggiornamento AEM.
* Le definizioni Oak non sono modificabili, devono essere inserite nel pacchetto con il codice del progetto del cliente e devono essere distribuite solo utilizzando Cloud Manager.
* Tutte le definizioni dell&#39;indice Oak devono seguire la convenzione di denominazione e altre regole per gli indici Oak in AEM come Cloud Service. Quelli che non lo fanno possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

* Risolvere le violazioni della regola dell&#39;indice identificate nel messaggio.
* Segui AEM come Cloud Service [linee guida sul packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) per distribuire definizioni di indici Oak nuove o personalizzate.
* Gli indici standard personalizzati AEM e le nuove definizioni degli indici Oak personalizzati devono seguire le [linee guida sull&#39;indicizzazione dei contenuti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) per AEM come Cloud Service.
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e scopri come [le violazioni OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
* Utilizza il [Convertitore indice](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) per migrare le definizioni di indice Oak personalizzato esistenti in AEM come definizioni di indice Oak personalizzato compatibile con il Cloud Service.
