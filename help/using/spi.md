---
title: SPI
description: Pagina della guida del codice di Pattern Detector.
source-git-commit: e050b9190f67fd6ccfac31490c4bf2a60d47731f
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# SPI {#spi}

## Informazioni di base {#background}

SIF identifica l’utilizzo di Search and Promote che è incompatibile con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `searchpromote.bundles.detected` - Questi bundle verranno disinstallati durante l&#39;aggiornamento
* `earchpromote.packages.detected` - Questi pacchetti verranno eliminati durante l&#39;aggiornamento
* `searchpromote.packages.dependency` - Rimuovi eventuali dipendenze di Search&amp;Promote dei pacchetti personalizzati
* `searchpromote.usage` - Rimuovi le API Search&amp;Promote dal codice personalizzato
* `searchpromote.users.detected` - Non utilizzare gli utenti del servizio Search&amp;Promote nel codice personalizzato
* `searchpromote.configs.detected` - Non utilizzare le proprietà di configurazione Search&amp;Promote nel codice personalizzato.