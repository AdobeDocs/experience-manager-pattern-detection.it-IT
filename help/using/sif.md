---
title: SIF
description: Pagina della guida del codice di Pattern Detector.
exl-id: c0a5c565-16e7-407b-befc-5a2966089da1
source-git-commit: 29d702c9662fd185ef806123fc4f4a03a70d64aa
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
