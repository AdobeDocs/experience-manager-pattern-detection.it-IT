---
title: REP
description: Pagina della guida del codice di Pattern Detector.
exl-id: e788deba-a301-404f-8e90-51f721409e69
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 100%

---

# [!DNL REP] {#rep}

Agente di replica

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_overview"
>title="Agente di replica"
>abstract="REP identifica gli agenti di replica abilitati. Questi vengono segnalati a causa di potenziali problemi che dovrebbero essere risolti durante l’aggiornamento ad AEM as a Cloud Service. AEM as a Cloud Service utilizza la distribuzione dei contenuti Sling per distribuire i contenuti dagli ambienti di authoring a quelli di pubblicazione. Questa operazione viene eseguita al di fuori del runtime di AEM utilizzando il servizio della pipeline di Adobe I/O Runtime su Adobe Developer. Il flusso di lavoro viene configurato automaticamente nell’ambiente AEM as a Cloud Service fornito."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents" text="Modifiche di rilievo in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents" text="Linee guida per lo sviluppo"

`REP` identifica gli agenti di replica abilitati. Questi vengono segnalati a causa di potenziali problemi che dovrebbero essere risolti durante l’aggiornamento ad AEM as a Cloud Service.

I sottotipi vengono utilizzati per identificare diversi tipi di informazioni:

* `forward.replication`: identifica gli agenti di replica in avanti abilitati.
* `reverse.replication`: identifica gli agenti di replica inversa abilitati.
* `standard.replication.agent.modification`: identifica gli agenti di replica standard abilitati che sono stati modificati.
* `custom.replication.agent.detection`: identifica gli agenti di replica personalizzati abilitati.

AEM as a Cloud Service utilizza la [Distribuzione dei contenuti Sling](https://sling.apache.org/documentation/bundles/content-distribution.html) per distribuire i contenuti dagli ambienti di authoring a quelli di pubblicazione. Questa operazione viene eseguita al di fuori del runtime di AEM utilizzando il servizio della pipeline di Adobe I/O Runtime su Adobe Developer. Il flusso di lavoro viene configurato automaticamente nell’ambiente AEM as a Cloud Service fornito.

## Possibili implicazioni e rischi {#implications-and-risks}

* La configurazione della replica è cambiata con AEM as a Cloud Service. Tutti gli agenti di replica correnti devono essere rivisti. La revisione consente di vedere:
   * quali sono quelli che la funzionalità standard può sostituire,
   * quali configurazioni devono essere spostate nel codice
   * e quali non sono supportate.
* Qualsiasi utilizzo degli agenti di replica nel codice personalizzato o nei flussi di lavoro deve essere rivisto durante l’aggiornamento ad AEM as a Cloud Service.
* La replica inversa non è inizialmente supportata in AEM as a Cloud Service.
* Non è necessario configurare un agente di svuotamento del dispatcher separato. Invece, questo viene configurato automaticamente nell’ambiente AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_rep_guidance"
>title="Guida all’implementazione"
>abstract="La best practice prevede di rivedere, rieseguire il factoring e ottimizzare le funzionalità personalizzate direttamente dipendenti dagli agenti di replica e renderle compatibili con AEM as a Cloud Service. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication" text="Replica in AEM as a Cloud Service"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Consulta le [Linee guida per lo sviluppo](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines#no-reverse-replication-agents) di AEM as a Cloud Service e le note sulla versione degli [agenti di replica](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes#replication-agents).
* Rivedi, riesegui il factoring e ottimizza le funzionalità direttamente dipendenti dagli agenti di replica per eseguire attività aziendali.
* Scopri come la [replica](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/deploying/overview#replication) è interessata dalla distribuzione in AEM as a Cloud Service.
* Per risolvere eventuali dubbi o avere dei chiarimenti, contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
