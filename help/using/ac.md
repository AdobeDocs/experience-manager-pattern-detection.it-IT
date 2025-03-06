---
title: AC
description: Pagina della guida del codice di Pattern Detector.
source-git-commit: 8dd9a42a3bba63d62fa2469b0f78ca15a608b4f9
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# AC {#ac}

## Informazioni di base {#background}

AC identifica l’utilizzo del bundle di Assets che è incompatibile con AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `asset.bundles.detected` - Il bundle verrà disinstallato durante l&#39;aggiornamento.
* `asset.usage` - Rimuovere dal codice personalizzato tutte le dipendenze dei componenti Asset Rating e Asset Catalog. Se applicabile, modificare il codice per utilizzare la nuova API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected` - È necessario rimuovere le sovrapposizioni create sui componenti Assets Rating e Catalog.
* `asset.resource.type.detected` - Rimuovi eventuali utilizzi del tipo di risorsa del componente di valutazione Assets nel codice personalizzato.
* `asset.paths.detected` - Sposta il contenuto del cliente presente in questi percorsi e rimuovi questi percorsi dopo aver verificato che non siano utilizzati in AEM.