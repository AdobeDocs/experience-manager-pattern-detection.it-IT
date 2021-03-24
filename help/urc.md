---
title: URC
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: ae3e162da40441fba39e6e9d283c495d15f40ba1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# URC {#urc}

Configurazione della modalità di esecuzione non supportata

## Sfondo {#background}

`URC` identifica l&#39;utilizzo di configurazioni basate su un nome di modalità runmode non supportato in AEM come Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

* L&#39;insieme di nomi che possono essere utilizzati per le modalità di esecuzione in AEM come Cloud Service è limitato.
* Le configurazioni basate su nomi di modalità di esecuzione non supportati non avranno alcun effetto se distribuite in AEM come Cloud Service.

## Soluzioni possibili {#solutions}

* Controlla l&#39;utilizzo di questa configurazione per determinare se è necessario.
* Rinomina la configurazione per utilizzare uno dei [nomi di modalità runmode supportati](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#custom-runmodes) e segui le [linee guida per la risoluzione in modalità runmode](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/configuring-osgi.html#runmode-resolution).
* Rivedi il progetto [wknd-legacy](https://github.com/adobe/aem-guides-wknd-legacy/tree/code/urc) e scopri come [le violazioni dell&#39;URC](https://github.com/adobe/aem-guides-wknd-legacy/compare/main...code/urc) possono essere corrette e rese compatibili con AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
