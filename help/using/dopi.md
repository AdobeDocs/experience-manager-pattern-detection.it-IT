---
title: DOPI
description: Pagina della guida del codice di Pattern Detector.
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 100%

---

# DOPI {#dopi}

Indice delle proprietà ordinate obsolete

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Indice delle proprietà ordinate obsolete"
>abstract="Il codice DOPI identifica l’utilizzo delle definizioni dell’indice delle proprietà ordinate (`primaryType=oak:QueryIndexDefinition` AND `type="ordered"`). La definizione è diventata obsoleta in AEM 6.1 ed è stata rimossa in AEM 6.2."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing#the-ordered-index" text="Indice ordinato: obsoleto"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/operations/indexing" text="Indicizzazione: AEM as a Cloud Service"

`DOPI` identifica l’utilizzo delle definizioni dell’ indice delle proprietà ordinate (`primaryType=oak:QueryIndexDefinition` AND `type="ordered"`). Le definizioni sono diventate obsolete in AEM 6.1 e sono state rimosse in AEM 6.2.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere tutti gli indici ordinati obsoleti e convertirli nella forma supportata degli indici Lucene, per evitare problemi di prestazioni significativi o requisiti cliente non funzionali."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/practices/best-practices-for-queries-and-indexing" text="Best practice: query e indicizzazione"

* Alcune query potrebbero non rispondere.
* La funzionalità del cliente potrebbe non funzionare correttamente.
* Si verificano avvisi o anche errori di traversal e significative penalizzazioni delle prestazioni in quanto gli indici obsoleti non hanno alcun effetto.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND precedente per comprendere come le violazioni DOPI possono essere rese compatibili con AEM Cloud Service. Inoltre, rivedi l’esempio di violazione DOPI su GitHub. Può aiutare a comprendere come gli indici ordinati precedenti possono essere convertiti in indici basati su Lucene, che sono supportati in AEM as a Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Progetto WKND precedente"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Esempio di violazione DOPI: GitHub"

* Modifica la definizione dell’indice in modo che diventi o venga sostituito con una definizione di indice supportata. Consulta [Query e indicizzazione Oak](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/deploying/queries-and-indexing).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e scopri come le [Violazioni DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) possono essere corrette e rese compatibili con AEM as a Cloud Service.
* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
