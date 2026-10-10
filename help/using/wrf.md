---
title: WRF
description: Pagina della guida del codice di Pattern Detector.
exl-id: 36578498-d5b2-46d1-a274-a1646ceaa764
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%
---
# WRF {#wrf}

## Esperienza pregressa {#background}

WRF identifica un utilizzo di We-Retail incompatibile con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `weretail.bundles.detected` - Questi bundle verranno disinstallati durante l&#39;aggiornamento
* `weretail.packages.detected` - Questi pacchetti verranno eliminati durante l&#39;aggiornamento
* `weretail.configs.detected` - Non utilizzare le proprietà di configurazione We.Retail nel codice personalizzato
* `weretail.packages.dependency` - Rimuovi la dipendenza di qualsiasi pacchetto personalizzato in We.Retail
* `weretail.paths.detected` - Questi percorsi We.Retail possono essere eliminati dopo aver verificato che non si sta utilizzando social network
* `weretail.resource.type.detected` - Rimuovi utilizzo tipo di risorsa We.Retail
* `weretail.usage` - Rimuovi le API We.Retail dal codice personalizzato.
