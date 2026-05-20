---
title: IOI
description: Pagina della guida del codice di Pattern Detector.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 89b6489ff2881ae05bb98eb5a01b758501fddfdb
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 100%

---

# IOI {#ioi}

Internal Oak Import (importazione Oak interna)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import (importazione Oak interna)"
>abstract="Il codice IOI (Internal Oak Import) segnala che il cliente utilizza pacchetti Oak interni, importati tramite OSGi. Vengono esportati senza alcuna versione particolare. Li utilizzano solo i bundle Oak o i servizi AEM di basso livello."

`IOI` segnala che il cliente utilizza pacchetti Oak interni, importati tramite OSGi. Vengono esportati senza alcuna versione particolare. Li utilizzano solo i bundle Oak o i servizi AEM di basso livello.
Alcune di queste aree sono utilizzate da `com.adobe.granite.repository`, che imposta un archivio per AEM durante l’avvio. Un altro esempio è il bundle `com.adobe.granite.maintenance.oak` di Adobe, che racchiude e fornisce attività di manutenzione Oak.

## Possibili implicazioni e rischi {#implications-and-risks}

* In una versione futura di AEM le esportazioni interne potrebbero essere rimosse, causando dipendenze interrotte e bundle inattivi che dipendono direttamente da Oak.
* Le API nelle esportazioni interne potrebbe cambiare.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Guida all’implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato per individuare l’utilizzo di tali API ed eseguirne il refactoring per renderle compatibili con AEM as a Cloud Service. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza l’API per risorse Sling (o l’API JCR) invece di un accesso di basso livello.
* Evita le dipendenze da pacchetti interni che non fanno parte di alcuna API o SPI pubblica.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
