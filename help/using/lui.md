---
title: LUI
description: Pagina della guida del codice di Pattern Detector.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: ht
source-wordcount: '708'
ht-degree: 100%

---

# LUI {#lui}

Interfaccia utente precedente

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaccia utente precedente"
>abstract="LUI identifica l’utilizzo di elementi obsoleti dell’interfaccia utente. Questi elementi non sono consigliati o supportati nelle versioni successive di AEM e in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche di rilievo in AEM as a Cloud Service"

`LUI` identifica l’utilizzo di elementi obsoleti dell’interfaccia utente. Questi elementi non sono consigliati o supportati nelle versioni successive di AEM e in AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di elementi dell’interfaccia utente che possono o devono essere aggiornati:

* `legacy.dialog.classic`: le finestre di dialogo dell’interfaccia classica basate su ExtJS devono essere modificate in Coral.
   * Questo sottotipo viene rilevato quando il nome della finestra di dialogo è `dialog` o `design_dialog` e quando il valore della proprietà `jcr:primaryType` o `xtype` è `cq:Dialog`.
* `legacy.dialog.coral2`: le finestre di dialogo `Coral 2` devono essere aggiornate per utilizzare `Coral 3`.
   * Questo sottotipo viene rilevato quando la finestra di dialogo e i relativi nomi dei nodi di contenuto secondario sono
      * `cq:dialog/content`,
      * `cq:design_dialog/content`,
      * `cq:dialog.coral2/content`,
      * o `cq:design_dialog.coral2/content` e il valore della proprietà `sling:resourceType` non contiene `granite/ui/components/coral/foundation`.
* `legacy.custom.component`: i componenti che ereditano da `foundation/components` devono essere aggiornati per l’utilizzo dei componenti core.
   * Questo sottotipo viene rilevato quando il valore della proprietà `jcr:primaryType` è `cq:Component` e il
     valore della proprietà `sling:resourceSuperType` contiene “foundation / components”. Oppure, uno qualsiasi dei
     valori proprietà `sling:resourceSuperType` della catena di componenti del supertipo contiene “foundation / components.”
* `legacy.static.template`: i modelli statici devono essere aggiornati a modelli modificabili.
   * Questo sottotipo viene rilevato quando il valore della proprietà `jcr:primaryType` è `cq:Template`.
* `content.fragment.template`: i modelli per frammenti di contenuto devono creare modelli di frammenti in sostituzione dei modelli di frammenti.
   * I precedenti modelli per frammenti di contenuto si trovano nelle seguenti posizioni:
      * I precedenti modelli per frammenti di contenuto preconfigurati sono memorizzati in `/libs/settings/dam/cfm/templates`
      * Possono essere sovrapposti in  `/apps/settings/dam/cfm/templates`  o  `/conf/.../settings/dam/cfm/templates`(... = global o “tenant”)
* `translation.dictionary`: dizionario `I18n` che disponibile in `/apps`.
   * `/apps` non è modificabile in fase di esecuzione e il file translator.html non sarà più disponibile in AEM as a Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guida all’implementazione"
>abstract="L’interfaccia classica non è più disponibile in AEM as a Cloud Service e l’interfaccia standard per l’authoring è l’interfaccia touch. Si consiglia di convertire tutte le interfacce non supportate e di eseguire il refactoring delle personalizzazioni collegate alle funzioni/funzionalità più recenti, compatibili con AEM as a Cloud Service. È possibile utilizzare la suite di strumenti di modernizzazione AEM esistente per semplificare le attività necessarie per modernizzare le implementazioni di AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti AEM Modernization Tools"

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.
* L’utilizzo di componenti personalizzati precedenti può aumentare i costi di manutenzione nel tempo.
* I precedenti modelli per frammenti di contenuto sono stati sostituiti da nuovi modelli per frammenti di contenuto in AEM 6.3. Quando i frammenti di contenuto basati su modelli precedenti vengono migrati ad AEM as a Cloud Service, tali frammenti continueranno a funzionare, ma non è possibile creare nuovi frammenti basati sul modello precedente. Inoltre, non è possibile distribuire tali frammenti mediante AEM GraphQL, che richiede come schemi i modelli per frammenti di contenuto.
* /apps non è modificabile in fase di esecuzione e il file translator.html non sarà più disponibile in AEM as a Cloud Service. Pertanto, i dizionari `I18n` devono provenire da Git tramite la pipeline CI/CD.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto della suite di strumenti AEM Modernization, i clienti possono convertire le finestre di dialogo Classic (ExtJS) in finestre di dialogo Coral. L’obiettivo è aiutare i clienti a passare dalle funzionalità non supportate o precedenti alle robuste e moderne offerte AEM. Questi strumenti sono configurabili, estensibili e tengono conto delle configurazioni. Inoltre, per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni, approfondisci la sostituzione dei componenti personalizzati con il set di componenti core standardizzati."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Convertitore componente"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction" text="Componenti core"

* Per ridurre le attività necessarie per modernizzare le implementazioni di AEM Sites, utilizza la [suite di strumenti di modernizzazione AEM](https://opensource.adobe.com/aem-modernize-tools/). Questi strumenti includono la conversione di:
   * Finestre di dialogo classiche (ExtJS) in finestre di dialogo Coral
   * Componenti di base in Componenti core
   * Modelli statici e controllo colonna in modelli modificabili e griglia reattiva
   * Progettazione e finestre di dialogo di progettazione in criteri di modelli modificabili
* Esamina la libreria di componenti personalizzati del tuo progetto e la transizione, se possibile, al set di componenti standardizzati [Componenti core](https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction) per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni.
* Crea modelli per frammenti di contenuto con funzionalità equivalenti ai modelli precedenti e utilizzali in futuro per creare frammenti di contenuto. Per ulteriori dettagli, consulta [Modelli per frammenti di contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models).
* I dizionari `I18n` devono provenire da Git tramite la pipeline CI/CD. [Documentazione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
