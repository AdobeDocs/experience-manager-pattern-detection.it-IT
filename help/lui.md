---
title: LUI
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 4%

---


# LUI {#lui}

Interfaccia utente legacy

## Sfondo {#background}

`LUI` identifica come Cloud Service l’utilizzo di elementi obsoleti dell’interfaccia utente che non sono consigliati o non sono supportati nelle versioni successive di AEM e in AEM.

I sottotipi vengono utilizzati per identificare i diversi tipi di elementi dell’interfaccia utente che devono o devono essere aggiornati:

* `legacy.dialog.classic`: Le finestre di dialogo dell’interfaccia classica basate su ExtJS devono essere modificate in Coral.
   * Questo viene rilevato quando il nome della finestra di dialogo è &quot;dialog&quot; o &quot;design_dialog&quot; e quando
il valore della proprietà `jcr:primaryType` o il valore della proprietà `xtype` è &quot;cq:Dialog&quot;.
* `legacy.dialog.coral2`: Le finestre di dialogo Coral 2 devono essere aggiornate per utilizzare Coral 3.
   * Questo viene rilevato quando i nomi dei nodi del contenuto figlio e della finestra di dialogo sono &quot;cq:dialog/content&quot;,
&quot;cq:design_dialog/content&quot;, &quot;cq:dialog.coral2/content&quot;, o &quot;cq:design_dialog.coral2/content&quot;
e il valore della proprietà `sling:resourceType` non contiene
&quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: I componenti che ereditano da  `foundation/components` devono essere aggiornati per l’utilizzo dei componenti core.
   * Questo viene rilevato quando il valore della proprietà `jcr:primaryType` è &quot;cq:Component&quot; e
      `sling:resourceSuperType` il valore della proprietà contiene &quot;foundation/components&quot; o uno qualsiasi dei
      `sling:resourceSuperType` i valori delle proprietà della catena di componenti di supertipo contengono &quot;foundation/components&quot;.
* `legacy.static.template`: I modelli statici devono essere aggiornati a Modelli modificabili.
   * Questo viene rilevato quando il valore della proprietà `jcr:primaryType` è &quot;cq:Template&quot;.

## Possibili implicazioni e rischi {#implications-and-risks}

* L’interfaccia classica non è più disponibile in AEM come Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.
* L’utilizzo di componenti personalizzati legacy può aumentare i costi di manutenzione nel tempo.

## Soluzioni possibili {#solutions}

* Utilizza [AEM suite di strumenti di modernizzazione](https://opensource.adobe.com/aem-modernize-tools/) per ridurre lo sforzo necessario per modernizzare le tue implementazioni AEM Sites. Questi strumenti includono la conversione di:
   * Finestre di dialogo classiche (ExtJS) nelle finestre di dialogo Coral
   * Componenti di base in componenti core
   * Modelli statici e controllo colonna per modelli modificabili e griglia reattiva
   * Finestre di dialogo di progettazione e progettazione per i criteri dei modelli modificabili
* Esamina la libreria di componenti personalizzati del tuo progetto e la relativa transizione, se possibile, al set di [Componenti core ](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it) standardizzati per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle tue applicazioni.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
