---
title: REP
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 7d05067fc624571e6fe520e2a1addd5dff8acbd8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---


# [!DNL REP] {#rep}

Agente replica

## Sfondo {#background}

`REP` identifica gli agenti di replica abilitati. Questi vengono segnalati a causa del potenziale di problemi che devono essere risolti quando si esegue l’aggiornamento a AEM come Cloud Service.

AEM as a Cloud Service utilizza [Sling Content Distribution](https://sling.apache.org/documentation/bundles/content-distribution.html) per distribuire i contenuti dall&#39;autore agli ambienti di pubblicazione. Questa operazione viene eseguita al di fuori del runtime AEM utilizzando il servizio pipeline di Adobe I/O. Questo viene configurato automaticamente nel AEM predisposto come ambiente di Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

* La configurazione della replica è cambiata con AEM come Cloud Service. Tutti gli agenti di replica correnti devono essere rivisti per vedere quali sono sostituiti dalla funzionalità standard, quali configurazioni devono essere spostate nel codice e quali non sono supportate.
* Qualsiasi utilizzo di agenti di replica nel codice personalizzato o nei flussi di lavoro deve essere rivisto durante l&#39;aggiornamento a AEM come Cloud Service.
* La replica inversa non è inizialmente supportata in AEM come Cloud Service.
* Non è necessario configurare un agente di flush del dispatcher separato. Questa viene configurata automaticamente in AEM come ambiente di Cloud Service.

## Soluzioni possibili {#solutions}

* Consulta le AEM come Cloud Service [Linee guida per lo sviluppo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html#no-reverse-replication-agents) e le note sulla versione per [agenti di replica](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html#replication-agents).
* Rivedi, refattori e ottimizza le funzionalità direttamente dipendenti dagli agenti di replica per eseguire attività aziendali.
* Scopri in che modo [replica](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html#replication) è interessata dalla distribuzione in AEM come Cloud Service.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
