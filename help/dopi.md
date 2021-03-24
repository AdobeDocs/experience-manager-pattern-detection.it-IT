---
title: DOPI
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# DOPI {#dopi}

Indice obsoleto delle proprietà ordinate

## Sfondo {#background}

`DOPI` identifica l&#39;uso delle definizioni dell&#39;indice delle proprietà ordinate (`primaryType=oak:QueryIndexDefinition` AND  `type="ordered"`), che sono state rimosse a partire dalla versione 6.1 e nella versione 6.2.

## Possibili implicazioni e rischi {#implications-and-risks}

* Alcune query potrebbero non rispondere.
* La funzionalità del cliente potrebbe non funzionare correttamente.
* Avvertenze di passaggio o anche errori e significative sanzioni sulle prestazioni in quanto gli indici obsoleti non hanno alcun effetto.

## Soluzioni possibili {#solutions}

* Modificare la definizione dell&#39;indice in modo che diventi o sostituisca l&#39;indice con una definizione di indice supportata. (Consulta [Query e indicizzazione Oak](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/deploying/queries-and-indexing.html)).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/dopi) e scopri come [violazioni DOPI](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/dopi) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
