---
title: CIF
description: Pagina della guida del codice di Pattern Detector.
exl-id: cf9d5f62-c9dd-4f56-982c-1b5b19c81506
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 76%

---

# CIF {#cif}

Commerce Integration Framework Classic

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_overview"
>title="Commerce Integration Framework Classic"
>abstract="CIF identifica l’utilizzo della versione classica di Commerce Integration Framework, non compatibile con AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/content-and-commerce/introduction" text=" Content and Commerce"

`CIF` identifica l’utilizzo della versione classica di Commerce Integration Framework, non compatibile con AEM as a Cloud Service. Nel messaggio per ogni risultato `CIF` viene identificato l’utilizzo e vengono fornite informazioni aggiuntive.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni:

* `commerce.integration.framework.detected`: incompatibilità della versione classic di Commerce Integration Framework con AEM as a Cloud Service.


## Possibili implicazioni e rischi {#implications-and-risks}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di esaminare ogni utilizzo della versione classic di Commerce Integration Framework."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/content-and-commerce/changes" text="Modifiche di rilievo apportate a CIF"

* La versione classic di Commerce Integration Framework non è più supportata in AEM as a Cloud Service. Bloccherebbe l’aggiornamento ad AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cif_tools"
>title="Strumenti e risorse"
>abstract="Questa guida aiuta a identificare le aree da aggiornare per la migrazione di Experience Manager Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/content-and-commerce/migration" text="Guida alla migrazione per CIF"

* Per Experience Manager as a Cloud Service il componente aggiuntivo CIF è l’unica soluzione di integrazione supportata per Adobe Commerce e per soluzioni commerce di terze parti. Il componente aggiuntivo CIF viene distribuito automaticamente ai clienti con Experience Manager as a Cloud Service, non è necessaria alcuna distribuzione manuale. Consulta [Guida introduttiva di AEM Commerce as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/content-and-commerce/storefront/getting-started).
* Per supportare i progetti che utilizzano CIF, Adobe fornisce [Componenti core CIF di AEM](https://github.com/adobe/aem-core-cif-components).
* Il componente aggiuntivo CIF è disponibile anche per AEM 6.5 tramite il [portale di distribuzione software](https://experience.adobe.com/#/downloads/content/software-distribution/it/aem.html). È compatibile e fornisce le stesse funzionalità del componente aggiuntivo CIF per Experience Manager as a Cloud Service, senza richiedere alcuna correzione.
* Classic CIF con le sue dipendenze non è più disponibile. Il codice che si basa su questa versione di CIF mediante le API Java™ com.adobe.cq.commerce.api deve essere regolato per il componente aggiuntivo CIF e per i relativi principi.

Di seguito sono riportate le possibili soluzioni per i diversi sottotipi:

* `commerce.bundles.detected` - Questi bundle verranno disinstallati durante l&#39;aggiornamento
* `commerce.packages.detected` - Questi pacchetti verranno eliminati durante l&#39;aggiornamento
* `commerce.packages.dependency` - Rimuovi qualsiasi dipendenza da Commerce dai pacchetti personalizzati
* `commerce.nodes.detected` - Aggiorna il codice personalizzato per non creare nodi CQ Commerce
* `commerce.configs.detected` - Non utilizzare le proprietà di configurazione di CQ Commerce nel codice personalizzato
* `commerce.users.detected` - Non utilizzare gli utenti del servizio CQ Commerce nel codice personalizzato
* `commerce.overlays.detected` - Rimuovi utilizzo sovrapposizioni CQ Commerce
* `commerce.paths.detected` - Rimuovi i percorsi commerce dopo aver verificato che non siano utilizzati in AEM
* `commerce.resource.type.detected` - Rimuovi utilizzo tipo di risorsa commerce
* `commerce.usage` - Rimuovi le API CQ Commerce nel codice personalizzato.
