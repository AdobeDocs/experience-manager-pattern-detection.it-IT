---
title: OCU
description: Pagina della guida del codice del rilevatore pattern
exl-id: cb28c727-415d-436c-ab74-cf7f1f34f7c7
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# OCU {#ocu}

Utilizzo del codice obsoleto

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_overview"
>title="Utilizzo del codice obsoleto"
>abstract="OCU identifica la situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non sono disponibili."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Modifiche di rilievo - AEM come Cloud Service"

`OCU` identifica la situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non sono disponibili.

Poiché le versioni precedenti non sono installate per impostazione predefinita, l&#39;applicazione del cliente potrebbe non funzionare correttamente.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza componenti o API obsoleti può essere interrotta e potrebbe non essere risolta correttamente dopo un aggiornamento.
* Alcune funzionalità dell&#39;applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente o potrebbero non essere attive dopo un aggiornamento.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ocu_guidance"
>title="Guida all&#39;implementazione"
>abstract="È consigliabile rivedere e adattare il codice cliente in modo da utilizzare la versione più recente dei componenti o delle API di AEM. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://javadoc.io/doc/com.adobe.aem/aem-sdk-api/latest/index.html" text="API SDK per Adobe Experience Manager"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* A breve termine: Potrebbe essere utile installare un pacchetto di compatibilità.
* A lungo termine: Adatta il codice cliente per utilizzare la versione più recente di componenti o API AEM.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
