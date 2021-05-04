---
title: CTEM
description: Pagina della guida del codice del rilevatore pattern
exl-id: cd70486c-8e21-4c31-89bf-928b80fa8772
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---

# CTEM {#ctem}

Modello personalizzato

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_overview"
>title="Modello personalizzato"
>abstract="CTEM identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle migliori pratiche"

`CTEM` identifica i modelli personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle migliori pratiche.

I modelli sono identificati da un valore di tipo principale &quot;cq:Template&quot;. Con questo codice viene utilizzato un sottotipo per identificare la categoria del modello:

* `custom.editable.template`: Il percorso del modello non inizia con &quot;/apps&quot;.
* `custom.static.template`: Il percorso del modello inizia con &quot;/apps&quot;.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di spostare tutti i modelli statici in modelli modificabili. I clienti possono utilizzare gli strumenti di modernizzazione AEM esistenti per migrare i modelli statici ai modelli modificabili."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html" text="Modelli modificabili"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti di modernizzazione AEM"

* Si consiglia di spostare tutti i modelli statici in modelli modificabili.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ctem_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto di AEM Suite di modernizzazione, i clienti possono manipolare la struttura di una pagina da una definizione statica a un modello modificabile. L’obiettivo è aiutare i clienti a passare dalle funzionalità limitate delle funzioni legacy alle AEM robuste e moderne. Questi strumenti sono configurabili, compatibili con la configurazione ed estensibili. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/page-structure.html" text="Convertitore struttura pagina"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza gli [AEM strumenti di modernizzazione](https://opensource.adobe.com/aem-modernize-tools/) per migrare i modelli statici ai modelli modificabili.
* Per ulteriori informazioni sui modelli modificabili, consulta [Modelli](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/templates/templates.html).
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
