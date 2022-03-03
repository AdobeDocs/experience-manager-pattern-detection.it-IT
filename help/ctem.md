---
title: CTEM
description: Pagina della guida del codice di Pattern Detector
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: ht
source-wordcount: '284'
ht-degree: 100%

---

# CTEM {#ctem}

Custom Template (modello personalizzato)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Custom Template (modello personalizzato)"
>abstract="CTEM identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle best practice"

`CTEM` identifica i modelli personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle best practice.

I modelli sono identificati da un valore di tipo primario “cq:Template”. Con questo codice viene utilizzato un sottotipo per identificare la categoria del modello:

* `custom.editable.template`: il percorso del modello non inizia con “/apps”.
* `custom.static.template`: il percorso del modello inizia con “/apps”.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di convertire tutti i modelli statici in modelli modificabili. I clienti possono utilizzare gli strumenti AEM Modernization Tools esistenti per migrare i modelli statici in modelli modificabili."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=it" text="Modelli modificabili"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti AEM Modernization Tools"

* Si consiglia di convertire tutti i modelli statici in modelli modificabili.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto della serie di strumenti AEM Modernization Suite, i clienti possono modificare la struttura di una pagina da definizione statica a modello modificabile. L’obiettivo è aiutare i clienti a passare dalle caratteristiche limitate delle funzionalità precedenti a quelle robuste e moderne di AEM. Questi strumenti sono configurabili, estensibili e tengono conto delle configurazioni. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Page Structure Converter"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Sfrutta gli strumenti [AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/) per migrare i modelli statici in modelli modificabili.
* Per ulteriori informazioni sui modelli modificabili, consulta [Modelli](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html?lang=it).
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
