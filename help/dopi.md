---
title: DOPI
description: Pagina della guida del codice del rilevatore pattern
exl-id: ae4df44d-43ca-438c-8373-11381b916af3
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# DOPI {#dopi}

Indice obsoleto delle proprietà ordinate

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_overview"
>title="Indice obsoleto delle proprietà ordinate"
>abstract="Il codice DOPI identifica l&#39;uso delle definizioni dell&#39;indice delle proprietà ordinate (primaryType=oak:QueryIndexDefinition AND type=&quot;ordered&quot;), che sono state rimosse dal 6.1 e sono state rimosse in 6.2."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html?lang=en#the-ordered-index" text="Indice ordinato - Obsoleto"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/indexing.html" text="Indicizzazione - AEM come Cloud Service"

`DOPI` identifica l&#39;uso delle definizioni dell&#39;indice delle proprietà ordinate (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), che sono state rimosse a partire dalla versione 6.1 e nella versione 6.2.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di rivedere tutti gli indici ordinati obsoleti e spostarli nella forma supportata degli indici lucene per evitare problemi di prestazioni significativi o requisiti cliente non funzionali."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/practices/best-practices-for-queries-and-indexing.html" text="Tecniche consigliate - Query e indicizzazione"

* Alcune query potrebbero non rispondere.
* La funzionalità del cliente potrebbe non funzionare correttamente.
* Avvertenze di passaggio o anche errori e significative sanzioni sulle prestazioni in quanto gli indici obsoleti non hanno alcun effetto.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dopi_tools"
>title="Strumenti e risorse"
>abstract="Rivedi il progetto WKND-legacy per capire come le violazioni DOPI possono essere rese compatibili con AEM Cloud Service. Inoltre, Rivedi l’esempio di violazione DOPI su Github per capire come gli indici ordinati legacy possono essere convertiti in indici basati su Lucene supportati in AEM come Cloud Service."
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi" text="Progetto legacy WKND"
>additional-url="https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi" text="Esempio di violazione DOPI - Github"

* Modificare la definizione dell&#39;indice in modo che diventi o sostituisca l&#39;indice con una definizione di indice supportata. (Consulta [Query e indicizzazione Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e scopri come [violazioni DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
