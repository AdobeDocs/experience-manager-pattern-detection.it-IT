---
title: CTEM
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 4%

---


# CTEM {#ctem}

Modello personalizzato

## Sfondo {#background}

`CTEM` identifica i modelli personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle migliori pratiche.

I modelli sono identificati da un valore di tipo principale &quot;cq:Template&quot;. Con questo codice viene utilizzato un sottotipo per identificare la categoria del modello:

* `custom.editable.template`: Il percorso del modello non inizia con &quot;/apps&quot;.
* `custom.static.template`: Il percorso del modello inizia con &quot;/apps&quot;.

## Possibili implicazioni e rischi {#implications-and-risks}

* Si consiglia di spostare tutti i modelli statici in modelli modificabili.

## Soluzioni possibili {#solutions}

* Utilizza gli [AEM strumenti di modernizzazione](https://opensource.adobe.com/aem-modernize-tools/) per migrare i modelli statici ai modelli modificabili.
* Per ulteriori informazioni sui modelli modificabili, consulta [Modelli](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
