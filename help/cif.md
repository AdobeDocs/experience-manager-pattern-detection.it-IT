---
title: CIF
description: Pagina della guida del codice del rilevatore pattern
source-git-commit: b611b595267e60df8a15511a8a2b4b30b601df1b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 3%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica la versione classica dell’utilizzo di Commerce Integration Framework incompatibile con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Contenuto e commercio"

`CIF` CIF identifica la versione classica dell’utilizzo di Commerce Integration Framework incompatibile con AEM as a Cloud Service. Messaggio per ogni `CIF` il risultato identificherà l’utilizzo e fornirà ulteriori informazioni.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `commerce.integration.framework.detected`: Versione classica dell’incompatibilità di Commerce Integration Framework con AEM as a Cloud Service.


## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di esaminare tutta la versione classica dell’utilizzo di Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Modifiche di rilievo apportate a CIF"

* La versione classica di Commerce Integration Framework non è più supportata in AEM as a Cloud Service. Bloccherebbe l&#39;aggiornamento a AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Strumenti e risorse"
>abstract="Questa guida aiuta a identificare le aree da aggiornare per la migrazione degli Experienci Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guida alla migrazione per CIF"

* Ad Experience Manager, as a Cloud Service, il componente aggiuntivo CIF è l’unica soluzione di integrazione Commerce supportata per le soluzioni commerce Adobe Commerce e di terze parti. Il componente aggiuntivo CIF viene distribuito automaticamente per i clienti su Experience Manager as a Cloud Service, non è necessaria alcuna distribuzione manuale. Vedi [Guida introduttiva a AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html).
* Per supportare i progetti che utilizzano CIF Adobe, fornisce [Componenti core CIF di AEM](https://github.com/adobe/aem-core-cif-components).
* Il componente aggiuntivo CIF è disponibile anche per AEM 6.5 tramite il [Portale di distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/it/aem.html). È compatibile e fornisce le stesse funzionalità del componente aggiuntivo CIF, ad Experience Manager as a Cloud Service, senza richiedere alcuna regolazione.
* Classic CIF con le sue dipendenze non è più disponibile. Il codice che si basa su questa versione CIF e utilizza le API Java com.adobe.cq.commerce.api deve essere aggiornato al componente aggiuntivo CIF e ai relativi principi.
