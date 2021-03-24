---
title: NBCC
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# CCN {#nbcc}

Modifiche non compatibili con le versioni precedenti

## Sfondo {#background}

`NBCC` identifica la situazione in cui alcuni nodi o bundle JCR vengono modificati in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza modifiche non compatibili con le versioni precedenti può essere interrotta e potrebbe non essere risolta correttamente.
* Alcune funzionalità dell&#39;applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente dopo un aggiornamento.

## Soluzioni possibili {#solutions}

* Sovrapponi o fai riferimento solo ai componenti Sling compatibili con le versioni precedenti.
* È consigliabile adattare le risorse provenienti da `/libs` o dai bundle dopo un aggiornamento AEM.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
