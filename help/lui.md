---
title: LUI
description: Pagina della guida del codice di Pattern Detector
exl-id: 742220d6-b37a-48ec-9f89-2f3f0ce6ff96
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: ht
source-wordcount: '554'
ht-degree: 100%

---

# LUI {#lui}

Interfaccia utente precedente

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_overview"
>title="Interfaccia utente precedente"
>abstract="LUI identifica l’uso di elementi obsoleti dell’interfaccia utente che non sono consigliati o non sono supportati nelle versioni successive di AEM e in AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"

`LUI` identifica l’utilizzo di elementi obsoleti dell’interfaccia utente che non sono consigliati o non sono supportati nelle versioni successive di AEM e in AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare i diversi tipi di elementi dell’interfaccia utente che possono o devono essere aggiornati:

* `legacy.dialog.classic`: le finestre di dialogo dell’interfaccia classica basate su ExtJS devono essere modificate in Coral.
   * Questo viene rilevato quando il nome della finestra di dialogo è “dialog” o “design_dialog” e quando
il valore della proprietà `jcr:primaryType` o il valore della proprietà `xtype` è “cq:Dialog”.
* `legacy.dialog.coral2`: le finestre di dialogo Coral 2 devono essere aggiornate per utilizzare Coral 3.
   * Questo viene rilevato quando la finestra di dialogo e i relativi nomi dei nodi di contenuto secondario sono “cq:dialog/content”,
“cq:design_dialog/content”, “cq:dialog.coral2/content” o “cq:design_dialog.coral2/content” e
il valore della proprietà `sling:resourceType` non contiene
“granite/ui/components/coral/foundation”.
* `legacy.custom.component`: i componenti che ereditano da `foundation/components`, devono essere aggiornati per utilizzare i componenti core.
   * Questo viene rilevato quando il valore della proprietà `jcr:primaryType` è “cq:Component” e il
      valore della proprietà `sling:resourceSuperType` contiene “foundation/components” o quando uno qualsiasi dei
      valori delle proprietà `sling:resourceSuperType` della catena di componenti del supertipo contiene
“foundation/components”.
* `legacy.static.template`: i modelli statici devono essere aggiornati a modelli modificabili.
   * Questo viene rilevato quando il valore della proprietà `jcr:primaryType` è “cq:Template”.

## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_guidance"
>title="Guida all’implementazione"
>abstract="L’interfaccia classica non è più disponibile in AEM as a Cloud Service e l’interfaccia standard per l’authoring è l’interfaccia touch. Si consiglia di convertire tutte le interfacce non supportate e di rieseguire il factoring delle personalizzazioni collegate alle funzioni/funzionalità più recenti, compatibili con AEM as a Cloud Service. I clienti possono sfruttare la suite di modernizzazione AEM esistente per ridurre lo sforzo necessario per modernizzare le implementazioni di AEM Sites."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/" text="Strumenti AEM Modernization Tools"

* L’interfaccia utente classica non è più disponibile in AEM as a Cloud Service. L’interfaccia standard per l’authoring è l’interfaccia touch.
* L’utilizzo di componenti personalizzati precedenti può aumentare i costi di manutenzione nel tempo.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_lui_tools"
>title="Strumenti e risorse"
>abstract="Con l’aiuto della Suite di modernizzazione AEM, i clienti possono convertire le finestre di dialogo Classic (ExtJS) in finestre di dialogo Coral. L’obiettivo è aiutare i clienti a passare dalle funzionalità non supportate o precedenti alle robuste e moderne offerte AEM. Questi strumenti sono configurabili, estensibili e tengono conto delle configurazioni. Inoltre, per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni, approfondisci la sostituzione dei componenti personalizzati con il set di componenti core standardizzati."
>additional-url="https://opensource.adobe.com/aem-modernize-tools/pages/tools/component.html" text="Convertitore componente"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it" text="Componenti core"

* Utilizza la [Suite di strumenti AEM Modernization Tools](https://opensource.adobe.com/aem-modernize-tools/) per ridurre lo sforzo necessario per modernizzare le implementazioni AEM Sites. Questi strumenti includono la conversione di:
   * Finestre di dialogo classiche (ExtJS) in finestre di dialogo Coral
   * Componenti di base in Componenti core
   * Modelli statici e controllo colonna in modelli modificabili e griglia reattiva
   * Progettazione e finestre di dialogo di progettazione in criteri di modelli modificabili
* Esamina la libreria di componenti personalizzati del tuo progetto e la transizione, se possibile, al set di componenti standardizzati [Componenti core](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it) per accelerare i tempi di sviluppo e ridurre i costi di manutenzione delle applicazioni.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
