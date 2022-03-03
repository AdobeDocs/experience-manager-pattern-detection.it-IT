---
title: OU
description: Pagina della guida del codice di Pattern Detector
exl-id: 6ec96fab-dd6e-46af-864f-05dad387cbb6
source-git-commit: 8b8d902dc5b5a8534475d256c199dc235bb35464
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# OU {#ou}

Utilizzo obsoleto

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_overview"
>title="Utilizzo obsoleto"
>abstract="OU identifica la situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non essere disponibili."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"

`OU` identifica la situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non essere disponibili.

Poiché le versioni precedenti non sono installate per impostazione predefinita, l’applicazione del cliente potrebbe non funzionare correttamente.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza componenti o API obsoleti può essere interrotta e potrebbe non essere risolta correttamente dopo un aggiornamento.
* Alcune funzionalità dell’applicazione del cliente o alcune funzionalità AEM potrebbero non venire eseguite correttamente o potrebbero non essere attive dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ou_guidance"
>title="Guida all’implementazione"
>abstract="È consigliabile rivedere e adattare il codice del cliente in modo da utilizzare la versione più recente dei componenti o delle API di AEM. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API SDK di Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* A breve termine: potrebbe essere utile installare un pacchetto di compatibilità.
* A lungo termine: adatta il codice del cliente per utilizzare la versione più recente di componenti o API AEM.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
