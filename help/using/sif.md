---
title: SIF
description: Pagina della guida del codice di Pattern Detector.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

---

# SIF {#sif}

## Informazioni di base {#background}

SIF identifica un utilizzo social incompatibile con AEM 6.5 LTS.

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `social.bundles.detected` - Questi bundle verranno disinstallati durante l&#39;aggiornamento
* `social.packages.detected` - Questi pacchetti verranno eliminati durante l&#39;aggiornamento
* `social.packages.dependency` - Rimuovere la dipendenza del pacchetto social dai pacchetti personalizzati
* `social.nodes.detected` - Aggiorna il codice personalizzato per non creare nodi social
* `social.configs.detected` - Non utilizzare le proprietà di configurazione social nel codice personalizzato
* `social.users.detected` - Non utilizzare utenti social nel codice personalizzato
* `social.overlays.detected` - Rimuovi utilizzo sovrapposizioni social network
* `social.paths.detected` - Rimuovi i percorsi social dopo aver verificato che non siano utilizzati in AEM
* `social.resource.type.detected` - Rimuovi utilizzo tipo di risorsa social network
* `social.usage` - Rimuovi le API social dal codice personalizzato.