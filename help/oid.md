---
title: OID
description: Pagina della guida del codice del rilevatore pattern
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# OID {#oid}

Definizione dell&#39;indice Oak

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_overview"
>title="Definizione dell&#39;indice Oak"
>abstract="OID identifica i problemi relativi alle definizioni dell&#39;indice Oak. Identifica le modifiche apportate alle definizioni standard dell&#39;indice Oak. Inoltre identifica le definizioni personalizzate dell&#39;indice Oak incompatibili con AEM come Cloud Service. Il messaggio per ogni risultato OID identificherà l’indice e fornirà informazioni aggiuntive."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#how-to-use" text="Linee guida sull’indicizzazione dei contenuti"

`OID` identifica i problemi relativi alle definizioni dell&#39;indice Oak. Identifica le modifiche apportate alle definizioni standard dell&#39;indice Oak. Inoltre identifica le definizioni personalizzate dell&#39;indice Oak incompatibili con AEM come Cloud Service. Il messaggio relativo a ciascun risultato `OID` identificherà l&#39;indice e fornirà informazioni aggiuntive.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `custom.index.violation`: Un&#39;incompatibilità dell&#39;indice Oak personalizzato con AEM come Cloud Service.
* `standard.index.modification`: Modifica a un indice Oak standard.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_guidance"
>title="Guida all&#39;implementazione"
>abstract="La best practice prevede di rivedere tutti gli indici personalizzati e ridotti in base alle linee guida per l’indicizzazione dei contenuti. Utilizza Index Converter per migrare le definizioni di indici Oak personalizzati esistenti per AEM come definizione di indici Oak personalizzati compatibili con il Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html#oak-indexes" text="Linee guida per gli imballaggi"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools" text="Convertitore indice"

* Le modifiche alle definizioni standard dell&#39;indice Oak possono andare perse durante un aggiornamento AEM.
* Le definizioni Oak non sono modificabili, devono essere inserite nel pacchetto con il codice del progetto del cliente e devono essere distribuite solo utilizzando Cloud Manager.
* Tutte le definizioni dell&#39;indice Oak devono seguire la convenzione di denominazione e altre regole per gli indici Oak in AEM come Cloud Service. Quelli che non lo fanno possono causare un comportamento indesiderato.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_oid_tools"
>title="Strumenti e risorse"
>abstract="Controlla il progetto legacy WKND per capire come possono essere risolte le violazioni OID nel tuo progetto. Inoltre, rivedi l’esempio di violazione OID su Github per capire come gli indici legacy possono essere convertiti utilizzando lo strumento Convertitore indice e resi compatibili con AEM come Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid" text="Progetto legacy WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid" text="Esempio di violazione OID - Github"

* Risolvere le violazioni della regola dell&#39;indice identificate nel messaggio.
* Segui AEM come Cloud Service [linee guida sul packaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/aem-project-content-package-structure.html) per distribuire definizioni di indici Oak nuove o personalizzate.
* Gli indici standard personalizzati AEM e le nuove definizioni degli indici Oak personalizzati devono seguire le [linee guida sull&#39;indicizzazione dei contenuti](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html#preparing-the-new-index-definition) per AEM come Cloud Service.
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/oid) e scopri come [le violazioni OID](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/oid) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
* Utilizza il [Convertitore indice](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/moving/refactoring-tools/index-converter.html#refactoring-tools) per migrare le definizioni di indice Oak personalizzato esistenti in AEM come definizioni di indice Oak personalizzato compatibile con il Cloud Service.
