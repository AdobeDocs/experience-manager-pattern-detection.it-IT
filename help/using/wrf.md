---
title: WRF
description: Pagina della guida del codice di Pattern Detector.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# WRF {#wrf}

## Informazioni di base {#background}

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