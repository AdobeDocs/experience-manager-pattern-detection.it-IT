---
title: UMI
description: Pagina della guida del codice del rilevatore pattern
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
translation-type: tm+mt
source-git-commit: 76dc944f1592118920f89c513faf456b8aa443a9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 3%

---

# UMI {#umi}

Problema di configurazione errata dell’aggiornamento

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema di configurazione errata dell’aggiornamento"
>abstract="UMI identifica le modifiche ad alcune configurazioni OSGi che causeranno problemi durante l&#39;aggiornamento, tra cui un aggiornamento non riuscito o funzionalità ridotte."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html" text="Modifiche di rilievo - AEM come Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM come Cloud Service - Note sulla versione"

`UMI` identifica le modifiche ad alcune configurazioni OSGi che causeranno problemi durante l&#39;aggiornamento, tra cui un aggiornamento non riuscito o funzionalità ridotte.

Le seguenti configurazioni vengono verificate per la modifica:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`

## Possibili implicazioni e rischi {#implications-and-risks}

* La modifica o la rimozione delle configurazioni può causare i seguenti problemi:
   * L&#39;aggiornamento potrebbe bloccarsi (ad esempio `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` era mancante ma presente in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * I problemi di autorizzazione possono verificarsi dopo l’aggiornamento (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Alcune funzionalità potrebbero non funzionare come previsto. Ad esempio, la modifica di `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` potrebbe causare la mancata compilazione di alcuni file JSP, il che alla fine provocherà una perdita di funzionalità.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guida all&#39;implementazione"
>abstract="Si consiglia di rivedere le configurazioni correnti e ripristinare eventuali modifiche apportate alle configurazioni citate per evitare problemi futuri di aggiornamento. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Non modificare o rimuovere le quattro configurazioni sopra menzionate.
* Se le configurazioni sono state modificate, è necessario ripristinarle ai valori previsti. Questi valori sono indicati nei messaggi `UMI` .
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
