---
title: CIF
description: Pagina della guida del codice del rilevatore pattern
exl-id: 500e0d32-e75e-4abe-a96b-0692ce40c086
source-git-commit: 84aea5b24e51ce5672826bad4ec126074bf24a09
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica come Cloud Service la versione classica dell’utilizzo di Commerce Integration Framework incompatibile con AEM."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/introduction.html" text=" Contenuto e commercio"

`CIF` CIF identifica come Cloud Service la versione classica dell’utilizzo di Commerce Integration Framework incompatibile con AEM. Il messaggio relativo a ciascun risultato `CIF` identificherà l’utilizzo e fornirà ulteriori informazioni.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `commerce.integration.framework.detected`: Versione classica dell’incompatibilità di Commerce Integration Framework con AEM come Cloud Service.


## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di esaminare tutta la versione classica dell’utilizzo di Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/changes.html" text="Modifiche di rilievo apportate a CIF"

* La versione classica di Commerce Integration Framework non è più supportata su AEM come Cloud Service. Bloccherebbe l&#39;aggiornamento a AEM come Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Strumenti e risorse"
>abstract="Questa guida aiuta a identificare le aree da aggiornare per la migrazione degli Experienci Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/migration.html" text="Guida alla migrazione per CIF"

* Ad Experience Manager, come Cloud Service, il componente aggiuntivo CIF è l’unica soluzione di integrazione Commerce supportata per le soluzioni Commerce di Adobe e Commerce di terze parti. Il componente aggiuntivo CIF viene distribuito automaticamente per i clienti su Experience Manager come Cloud Service, non è necessaria alcuna distribuzione manuale. Consulta [Guida introduttiva a Commerce as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content-and-commerce/storefront/getting-started.html) .
* Per supportare i progetti che implementano CIF Adobe fornisce [AEM componenti core CIF](https://github.com/adobe/aem-core-cif-components).
* Il componente aggiuntivo CIF è disponibile per AEM 6.5 e tramite il [portale di distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html). È compatibile e fornisce le stesse caratteristiche del componente aggiuntivo CIF, ad Experience Manager come Cloud Service - non sono necessarie regolazioni.
* Classic CIF con le sue dipendenze non è più disponibile. Il codice che si basa su questa versione CIF e utilizza le API Java com.adobe.cq.commerce.api deve essere aggiornato al componente aggiuntivo CIF e ai relativi principi.
