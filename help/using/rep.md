---
title: REP
description: Pagina della guida del codice di Pattern Detector
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: f1e833bea35ef3b412936d529b14bff6f1cb35c1
workflow-type: ht
source-wordcount: '410'
ht-degree: 100%

---

# [!DNL REP] {#rep}

Agente di replica

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente di replica"
>abstract="REP identifica gli agenti di replica abilitati. Questi vengono segnalati a causa di potenziali problemi che devono essere risolti durante l’aggiornamento ad AEM as a Cloud Service. AEM as a Cloud Service utilizza la Distribuzione dei contenuti Sling per distribuire i contenuti dagli ambienti di authoring a quelli di pubblicazione. Questa operazione viene eseguita al di fuori del runtime AEM utilizzando il servizio pipeline di Adobe I/O. Viene configurato automaticamente nell’ambiente con provisioning AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it#replication-agents" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=it#no-reverse-replication-agents" text="Linee guida per lo sviluppo"

`REP` identifica gli agenti di replica abilitati. Questi vengono segnalati a causa di potenziali problemi che devono essere risolti durante l’aggiornamento ad AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `forward.replication`: identifica gli agenti di replica in avanti abilitati.
* `reverse.replication`: identifica gli agenti di replica inversa abilitati.
* `standard.replication.agent.modification`: identifica gli agenti di replica standard abilitati che sono stati modificati.
* `custom.replication.agent.detection`: identifica gli agenti di replica personalizzati abilitati.

AEM as a Cloud Service utilizza la [Distribuzione dei contenuti Sling](https://sling.apache.org/documentation/bundles/content-distribution.html) per distribuire i contenuti dagli ambienti di authoring a quelli di pubblicazione. Questa operazione viene eseguita al di fuori del runtime AEM utilizzando il servizio pipeline di Adobe I/O. Viene configurato automaticamente nell’ambiente con provisioning AEM as a Cloud Service.

## Possibili implicazioni e rischi {#implications-and-risks}

* La configurazione della replica è cambiata con AEM as a Cloud Service. Tutti gli agenti di replica correnti devono essere verificati per vedere quali sono sostituiti dalla funzionalità standard, quali configurazioni devono essere spostate nel codice e quali non sono supportate.
* Qualsiasi utilizzo degli agenti di replica nel codice personalizzato o nei flussi di lavoro deve essere rivisto durante l’aggiornamento ad AEM as a Cloud Service.
* La replica inversa non è inizialmente supportata in AEM as a Cloud Service.
* Non è necessario configurare un agente di scaricamento del dispatcher separato. Viene configurato automaticamente nell’ambiente AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Guida all’implementazione"
>abstract="La best practice prevede di rivedere, rieseguire il factoring e ottimizzare le funzionalità personalizzate direttamente dipendenti dagli agenti di replica e renderle compatibili con AEM as a Cloud Service. Per assistenza e chiarimenti, contatta il supporto Adobe"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=it#replication" text="Replica in AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Consulta le [Linee guida per lo sviluppo](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=it#no-reverse-replication-agents) di AEM as a Cloud Service e le note sulla versione degli [agenti di replica](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it#replication-agents).
* Rivedi, riesegui il factoring e ottimizza le funzionalità direttamente dipendenti dagli agenti di replica per eseguire attività aziendali.
* Scopri come la [replica](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/deploying/overview.html?lang=it#replication) è interessata dalla distribuzione in AEM as a Cloud Service.
* Per eventuali domande o dubbi, contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
