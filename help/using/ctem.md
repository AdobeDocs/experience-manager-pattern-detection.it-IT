---
title: CTEM
description: Pagina della guida del codice di Pattern Detector.
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 71%

---

# CTEM {#ctem}

Custom Template (modello personalizzato)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Custom Template (modello personalizzato)"
>abstract="CTEM identifica i componenti personalizzati installati su AEM. Queste informazioni sono fornite ai fini della valutazione delle best practice"

`CTEM`  Identifica i modelli personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle best practice.

I modelli hanno un valore di tipo primario di `cq:Template`, che ne facilita l&#39;identificazione. Con questo codice viene utilizzato un sottotipo per identificare la categoria del modello:

* `custom.editable.template`: il percorso del modello non inizia con `/apps`.
* `custom.static.template`: il percorso del modello inizia con `/apps`.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di convertire tutti i modelli statici in modelli modificabili. È possibile utilizzare gli strumenti AEM Modernization Tools esistenti per migrare i modelli statici in modelli modificabili."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/templates/templates" text="Modelli modificabili"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti AEM Modernization Tools"

* Si consiglia di convertire tutti i modelli statici in modelli modificabili.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto della serie di strumenti AEM Modernization Suite, i clienti possono modificare la struttura di una pagina da definizione statica a modello modificabile. L’obiettivo è aiutare i clienti a passare dalle caratteristiche limitate delle funzionalità precedenti a quelle robuste e moderne di AEM. Questi strumenti sono configurabili, estensibili e tengono conto delle configurazioni. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/structure/about.html" text="Page Structure Converter"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza gli [strumenti di modernizzazione AEM](https://opensource.adobe.com/aem-modernize-tools/) per migrare i modelli statici in modelli modificabili.
* Per ulteriori informazioni sui modelli modificabili, consulta [Modelli](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/templates/templates).
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
