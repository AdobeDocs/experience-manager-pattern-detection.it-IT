---
title: AC
description: Pagina della guida del codice di Pattern Detector.
exl-id: 4c6ac075-5ba6-4511-97c6-a9b496d4677a
source-git-commit: 9c2f5452ff694e11a49c7b38efa61acc65924dd6
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---

# AC {#ac}

## Esperienza pregressa {#background}

AC identifica l’utilizzo del bundle di Assets che è incompatibile con AEM 6.5 LTS

<!-- Alexandru: drafting for now ## Possible implications and risks {#implications-and-risks} -->

## Soluzioni possibili {#solutions}

Di seguito sono elencate le possibili soluzioni per i diversi sottotipi:

* `asset.bundles.detected` - Il bundle verrà disinstallato durante l&#39;aggiornamento.
* `asset.usage` - Rimuovere dal codice personalizzato tutte le dipendenze dei componenti Asset Rating e Asset Catalog. Se applicabile, modificare il codice per utilizzare la nuova API `List<Scene7ConfigSetting>` `com.day.cq.dam.scene7.api.model.Scene7ViewerConfig#getSettingsList()`.
* `asset.overlays.detected` - È necessario rimuovere le sovrapposizioni create sui componenti Assets Rating e Catalog.
* `asset.resource.type.detected` - Rimuovi eventuali utilizzi del tipo di risorsa del componente di valutazione Assets nel codice personalizzato.
* `asset.paths.detected` - Sposta il contenuto del cliente presente in questi percorsi e rimuovi questi percorsi dopo aver verificato che non siano utilizzati in AEM.

