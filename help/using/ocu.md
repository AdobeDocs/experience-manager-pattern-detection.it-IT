---
title: OCU
description: Pagina della guida del codice di Pattern Detector.
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 93%

---

# OCU {#ocu}

OBSOLETO: Outdated Code Usage (utilizzo di codice obsoleto); sostituito da OU, Outdated Usage (utilizzo obsoleto)

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Outdated Code Usage (utilizzo di codice obsoleto)"
>abstract="OCU identifica una situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non essere disponibili."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"

`OCU` identifica una situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non essere disponibili.

Poiché le versioni precedenti non sono installate per impostazione predefinita, l’applicazione del cliente potrebbe non funzionare correttamente.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza componenti o API obsoleti può essere interrotta e potrebbe non essere risolta correttamente dopo un aggiornamento.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non venire eseguite correttamente o potrebbero non essere attive dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Guida all’implementazione"
>abstract="È consigliabile rivedere e adattare il codice del cliente in modo da utilizzare la versione più recente dei componenti o delle API di AEM. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API SDK di Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* A breve termine: potrebbe essere utile installare un pacchetto di compatibilità.
* A lungo termine: adatta il codice del cliente per utilizzare la versione più recente di componenti o API AEM.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
