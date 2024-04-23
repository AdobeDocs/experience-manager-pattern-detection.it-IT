---
title: UMI
description: Pagina della guida del codice di Pattern Detector.
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 616fa84f6237893243cffc8af28c7cbe76bf32d7
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 41%

---

# UMI {#umi}

Problema di configurazione errata dell’aggiornamento

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema di configurazione errata dell’aggiornamento"
>abstract="UMI identifica le modifiche ad alcune configurazioni OSGi che causano problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service - Note sulla versione"

UMI identifica le modifiche ad alcune configurazioni OSGi che causano problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte.

Le seguenti configurazioni vengono verificate per la modifica:

* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`
* `org.apache.sling.commons.log.LogManager.factory.config`: identifica se la proprietà `org.apache.sling.commons.log.file` dei logger personalizzati rimanda a qualcosa di diverso dal file `logs/error.log`.

## Possibili implicazioni e rischi {#implications-and-risks}

* La modifica o la rimozione delle configurazioni può causare i seguenti problemi:
   * L’aggiornamento potrebbe bloccarsi (ad esempio `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` mancante ma presente in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Dopo l’aggiornamento possono verificarsi problemi di autorizzazione (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Alcune funzionalità potrebbero non funzionare come previsto. Ad esempio, modifica `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` potrebbero causare la mancata compilazione di alcuni file JSP, che alla fine porta a una perdita di funzionalità.
   * I valori della configurazione di Externalizer `com.day.cq.commons.impl.ExternalizerImpl` sono impostate dalle variabili dell’ambiente cloud manager in AEM as a Cloud Service.
   * AEM as a Cloud Service non supporta i file di registro personalizzati. I registri scritti in registri con nomi personalizzati non sono accessibili da AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere le configurazioni correnti e ripristinare eventuali modifiche apportate alle configurazioni citate per evitare problemi futuri di aggiornamento. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it" text="Supporto Experience Cloud"

* Non modificare o rimuovere le quattro configurazioni sopra menzionate.
   * Se si verifica la seguente violazione:\
     &quot;Proprietà richieste per la configurazione OSGi `xyz-configuration` sono mancanti: &#39;[property-1,property-2...]&quot;.&quot;\
     Conferma se queste eliminazioni sono legittime o meno perché queste configurazioni OSGI sono OOTB e potrebbero non essere mai state modificate/salvate dal gestore di configurazione OSGi.
* Se le configurazioni sono state modificate, è necessario riportarle ai valori previsti. Questi valori sono indicati nei messaggi `UMI`.
* Per `com.day.cq.commons.impl.ExternalizerImpl`, vedi [documentazione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) per impostare la configurazione di Externalizer utilizzando le variabili di ambiente di Cloud Manager in AEM as a Cloud Service.
* Per `org.apache.sling.commons.log.LogManager.factory.config`, modifica la configurazione OSGi per inviare il logger personalizzato al file `logs/error.log`. Consulta [documentazione](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) per il riposizionamento al `logs/error.log` file.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
