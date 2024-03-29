---
title: DOPI
description: Pagina della guida del codice di Pattern Detector
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '255'
ht-degree: 100%

---

# DOPI {#dopi}

Indice delle proprietà ordinate obsolete

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Indice delle proprietà ordinate obsolete"
>abstract="Il codice DOPI identifica l’uso delle definizioni dell’indice delle proprietà ordinate (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), che sono state dichiarate obsolete dalla 6.1 e sono state rimosse nella 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=it#the-ordered-index" text="Indice ordinato: obsolete"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html?lang=it" text="Indicizzazione: AEM as a Cloud Service"

`DOPI` identifica l’uso delle definizioni dell’indice delle proprietà ordinate (`primaryType=oak:QueryIndexDefinition` E `type="ordered"`), che sono state dichiarate obsolete a partire dalla versione 6.1 e rimosse nella versione 6.2.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere tutti gli indici ordinati obsoleti e spostarli nella forma supportata degli indici lucene per evitare problemi di prestazioni significativi o requisiti cliente non funzionali."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html?lang=it" text="Best practice: query e indicizzazione"

* Alcune query potrebbero non rispondere.
* La funzionalità del cliente potrebbe non funzionare correttamente.
* Si verificano avvisi o anche errori di traversal e significative penalizzazioni delle prestazioni in quanto gli indici obsoleti non hanno alcun effetto.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND precedente per comprendere come le violazioni DOPI possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione DOPI su Github per capire come gli indici ordinati precedenti possono essere convertiti in indici basati su Lucene supportati in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Esempio di violazione DOPI: Github"

* Modifica la definizione dell’indice in modo che diventi, o venga sostituito con, una definizione di indice supportata. Consulta [Query e indicizzazione Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=it).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e scopri come le [Violazioni DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
