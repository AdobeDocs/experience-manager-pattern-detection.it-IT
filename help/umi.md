---
title: UMI
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# UMI {#umi}

Problema di configurazione errata dell’aggiornamento

## Sfondo {#background}

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

* Non modificare o rimuovere le quattro configurazioni sopra menzionate.
* Se le configurazioni sono state modificate, è necessario ripristinarle ai valori previsti. Questi valori sono indicati nei messaggi `UMI` .
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
