---
title: SCR
description: Pagina della guida del codice di Pattern Detector.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# SCR {#scr}

## Informazioni di base {#background}

SIF identifica un utilizzo di AEM Screens incompatibile con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `screens.bundles.detected` - Questi bundle verranno disinstallati durante l&#39;aggiornamento.
* `screens.packages.detected` - Questi pacchetti verranno eliminati durante l&#39;aggiornamento.
* `screens.packages.dependency` - Rimuovi qualsiasi dipendenza da Screens dai pacchetti personalizzati.
* `screens.configs.detected` - Assicurarsi di non utilizzare alcuna proprietà di configurazione Screens nel codice personalizzato.
* `screens.users.detected` - Assicurarsi di non utilizzare gli utenti del servizio Screens nel codice personalizzato.
* `screens.paths.detected` - Rimuovere i percorsi Screens dopo aver verificato che non siano utilizzati in AEM.
* `screens.resource.type.detected` - Rimuovi l&#39;utilizzo del tipo di risorsa Screens.
* `screens.usage` - Rimuovi le API Screens dal codice personalizzato.