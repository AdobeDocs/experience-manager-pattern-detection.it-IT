---
title: CIF
description: Pagina della guida del codice di Pattern Detector.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 98%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica l’utilizzo della versione classic di Commerce Integration Framework, incompatibile con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html?lang=it" text=" Content and Commerce"

`CIF` CIF identifica l’utilizzo della versione classica di Commerce Integration Framework, incompatibile con AEM as a Cloud Service. Il messaggio di ogni risultato `CIF` identificherà l’utilizzo e fornirà ulteriori informazioni.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `commerce.integration.framework.detected`: incompatibilità della versione classic di Commerce Integration Framework con AEM as a Cloud Service.


## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di esaminare ogni utilizzo della versione classic di Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html?lang=it" text="Modifiche di rilievo apportate a CIF"

* La versione classic di Commerce Integration Framework non è più supportata in AEM as a Cloud Service. Bloccherebbe l’aggiornamento ad AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Strumenti e risorse"
>abstract="Questa guida aiuta a identificare le aree da aggiornare per la migrazione di Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html?lang=it" text="Guida alla migrazione per CIF"

* Per Experience Manager as a Cloud Service il componente aggiuntivo CIF è l’unica soluzione di integrazione supportata per le soluzioni commerce di Adobe e di terze parti. Il componente aggiuntivo CIF viene distribuito automaticamente ai clienti con Experience Manager as a Cloud Service, non è necessaria alcuna distribuzione manuale. Consulta [Guida introduttiva di AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html?lang=it).
* Per supportare i progetti che utilizzano CIF, Adobe fornisce [Componenti core CIF di AEM](https://github.com/adobe/aem-core-cif-components).
* Il componente aggiuntivo CIF è disponibile anche per AEM 6.5 tramite il [portale di distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/it/aem.html). È compatibile e fornisce le stesse funzionalità del componente aggiuntivo CIF per Experience Manager as a Cloud Service, senza richiedere alcuna correzione.
* Classic CIF con le sue dipendenze non è più disponibile. Il codice che si basa su questa versione di CIF mediante le API Java com.adobe.cq.commerce.api deve essere regolato per il componente aggiuntivo CIF e ai relativi principi.
