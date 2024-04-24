---
title: IOI
description: Pagina della guida del codice di Pattern Detector.
exl-id: b6c9d11f-5189-4799-98c0-c2699dfe3f40
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 64%

---

# IOI {#ioi}

Internal Oak Import (importazione Oak interna)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_overview"
>title="Internal Oak Import (importazione Oak interna)"
>abstract="Il codice IOI segnala che il cliente utilizza pacchetti Oak interni, importati tramite OSGi. Sono esportati senza alcuna versione particolare e sono destinati al consumo solo da altri bundle Oak o servizi AEM di basso livello."

`IOI`  Identifica l’utilizzo da parte del cliente di pacchetti Oak interni, importati tramite OSGi. Sono esportati senza alcuna versione particolare e sono destinati al consumo solo da altri bundle Oak o servizi AEM di basso livello.

Alcuni di questi sono utilizzati da `com.adobe.granite.repository`, che imposta un archivio per AEM durante l’avvio. Un altro esempio è il bundle `com.adobe.granite.maintenance.oak` di Adobe, che racchiude e fornisce attività di manutenzione Oak.

## Possibili implicazioni e rischi {#implications-and-risks}

* In una versione futura di AEM le esportazioni interne potrebbero essere rimosse, causando dipendenze interrotte e bundle inattivi che dipendono direttamente da Oak.
* Le API nelle esportazioni interne potrebbe cambiare.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ioi_guidance"
>title="Guida all’implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato per individuare l’utilizzo di tali API ed eseguirne il refactoring per renderle compatibili con AEM as a Cloud Service. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it" text="Supporto Experience Cloud"

* Utilizza l’API per risorse Sling (o l’API JCR) invece di un accesso di basso livello.
* Evita le dipendenze da pacchetti interni che non fanno parte di alcuna API o SPI pubblica.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
