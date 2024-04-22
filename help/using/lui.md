---
title: LUI
description: Pagina della guida del codice di Pattern Detector.
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 58%

---

# LUI {#lui}

Interfaccia utente precedente

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaccia utente precedente"
>abstract="LUI (Legacy User Interface) identifica l’uso di elementi obsoleti dell’interfaccia utente che non sono consigliati o supportati nelle versioni successive di AEM e in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche importanti in AEM as a Cloud Service"

LUI (Legacy User Interface) identifica l’uso di elementi obsoleti dell’interfaccia utente che non sono consigliati o supportati nelle versioni successive di AEM e in AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di elementi dell’interfaccia utente che possono o devono essere aggiornati:

* `legacy.dialog.classic`: le finestre di dialogo dell’interfaccia classica basate su ExtJS devono essere convertite per Coral.
   * Questo viene rilevato quando il nome della finestra di dialogo è &quot;dialog&quot; o &quot;design_dialog&quot; e quando `jcr:primaryType` valore della proprietà o `xtype` valore proprietà: `cq:Dialog`.
* `legacy.dialog.coral2`: `Coral 2` le finestre di dialogo devono essere aggiornate per utilizzare `Coral 3`.
   * Questo viene rilevato quando la finestra di dialogo e i relativi nomi dei nodi di contenuto figlio sono `cq:dialog/content`,
     `cq:design_dialog/content`, `cq:dialog.coral2/content`&quot;, o `cq:design_dialog.coral2/content`
e `sling:resourceType` il valore della proprietà non contiene &quot;granite/ui/components/coral/foundation&quot;.
* `legacy.custom.component`: i componenti che ereditano da `foundation/components` devono essere aggiornati per l’utilizzo dei componenti core.
   * Questo viene rilevato quando `jcr:primaryType` il valore della proprietà è &quot;`cq:Component`&quot; e
     `sling:resourceSuperType` il valore della proprietà contiene &quot;foundation/components&quot;. Oppure, uno qualsiasi dei
     valori delle proprietà `sling:resourceSuperType` della catena di componenti del supertipo contiene
“foundation/components”.
* `legacy.static.template`: i modelli statici devono essere aggiornati a modelli modificabili.
   * Questo viene rilevato quando `jcr:primaryType` il valore della proprietà è &quot;`cq:Template`&quot;.
* `content.fragment.template`: i precedenti modelli per frammenti di contenuto devono creare nuovi modelli di frammenti in sostituzione dei modelli di frammenti di vecchia generazione.
   * I precedenti modelli per frammenti di contenuto si trovano nelle seguenti posizioni:
      * I precedenti modelli per frammenti di contenuto preconfigurati sono memorizzati in `/libs/settings/dam/cfm/templates`
      * Possono essere sovrapposti in  `/apps/settings/dam/cfm/templates`  o  `/conf/.../settings/dam/cfm/templates`(... = global o “tenant”)
* `translation.dictionary`: `I18n` dizionario presente in /apps.
   * /apps non è modificabile in fase di esecuzione e il file translator.html non sarà più disponibile in AEM as a Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guida all’implementazione"
>abstract="L’interfaccia classica non è più disponibile in AEM as a Cloud Service e l’interfaccia standard per l’authoring è l’interfaccia touch. Si consiglia di spostare tutte le interfacce non supportate e di rieseguire il factoring delle personalizzazioni collegate alle funzioni/funzionalità più recenti, compatibili con AEM as a Cloud Service. I clienti possono utilizzare la suite di modernizzazione AEM esistente per ridurre lo sforzo necessario per modernizzare le implementazioni AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti AEM Modernization Tools"

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.
* L’utilizzo di componenti personalizzati precedenti può aumentare i costi di manutenzione nel tempo.
* I modelli per frammenti di contenuto sono stati sostituiti dai modelli per frammenti di contenuto in AEM 6.3. La migrazione di frammenti di contenuto basati su modelli precedenti a AEM as a Cloud Service mantiene questi frammenti come funzionali, ma non è possibile creare frammenti basati sul modello precedente. Inoltre, non è possibile distribuire questi frammenti utilizzando AEM GraphQL, che richiede come schemi i modelli per frammenti di contenuto.
* /apps non è modificabile in fase di esecuzione e il file translator.html non sarà più disponibile in AEM as a Cloud Service Pertanto, `I18n` I dizionari devono provenire da Git tramite la pipeline CI/CD.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto della suite di strumenti AEM Modernization, i clienti possono convertire le finestre di dialogo Classic (ExtJS) in finestre di dialogo Coral. L’obiettivo è aiutare i clienti a passare dalle funzionalità non supportate o precedenti alle robuste e moderne offerte AEM. Questi strumenti sono configurabili, estensibili e tengono conto delle configurazioni. Inoltre, per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni, approfondisci la sostituzione dei componenti personalizzati con il set di componenti core standardizzati."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/component/about.html" text="Convertitore componente"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction" text="Componenti core"

* Per ridurre lo sforzo necessario per modernizzare le implementazioni di AEM Sites, utilizza [Suite di strumenti di modernizzazione AEM](https://opensource.adobe.com/aem-modernize-tools/). Questi strumenti includono la conversione di:
   * Finestre di dialogo classiche (ExtJS) in finestre di dialogo Coral
   * Componenti di base in Componenti core
   * Modelli statici e controllo colonna in modelli modificabili e griglia reattiva
   * Progettazione e finestre di dialogo di progettazione in criteri di modelli modificabili
* Esamina la libreria di componenti personalizzati del tuo progetto e la transizione, se possibile, al set di componenti standardizzati [Componenti core](https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction) per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni.
* Crea modelli per frammenti di contenuto con funzionalità equivalenti ai modelli di vecchia generazione e utilizzali in futuro per creare frammenti di contenuto. Consulta [Modelli per frammenti di contenuto](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/content-fragments/content-fragments-models) per ulteriori dettagli.
* `I18n` I dizionari devono provenire da Git tramite la pipeline CI/CD. [Documentazione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#apps-libs-immutable)
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
