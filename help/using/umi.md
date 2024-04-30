---
title: UMI
description: Pagina della guida del codice di Pattern Detector
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 94%

---

# UMI {#umi}

Problema di configurazione errata dell’aggiornamento

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema di configurazione errata dell’aggiornamento"
>abstract="UMI individua le modifiche ad alcune configurazioni OSGi che causano problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/aem-cloud-changes" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current" text="AEM as a Cloud Service: note sulla versione"

`UMI`  Identifica le modifiche ad alcune configurazioni OSGi che causano problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte.

Le seguenti configurazioni vengono verificate per rilevare eventuali modifiche:

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
   * Alcune funzionalità potrebbero non funzionare come previsto. Ad esempio, la modifica di `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` può causare la mancata compilazione di alcuni file JSP, che alla fine determina una perdita di funzionalità.
   * I valori della configurazione `com.day.cq.commons.impl.ExternalizerImpl` di Externalizer sono impostati dalle variabili di ambiente di Cloud Manager in AEM as a Cloud Service.
   * AEM as a Cloud Service non supporta i file di registro personalizzati. I registri scritti con file log e nomi personalizzati non saranno accessibili da AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere le configurazioni correnti e ripristinare eventuali modifiche apportate alle configurazioni citate per evitare in futuro problemi di aggiornamento. Contatta il supporto Adobe per ricevere assistenza o chiarimenti."
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html?lang=it" text="Supporto Experience Cloud"

* Non modificare o rimuovere le quattro configurazioni sopra menzionate.
   * Se si verifica la seguente violazione:\
     “Mancano le proprietà richieste per la configurazione OSGi `xyz-configuration`: ‘[proprietà-1, proprietà-2...]’.”\
     Conferma se queste eliminazioni sono legittime o meno, in quanto queste configurazioni OSGI sono integrate e potrebbero non essere mai state modificate o salvate dal gestore di configurazione OSGi.
* Se le configurazioni sono state modificate, è necessario riportarle ai valori previsti. Questi valori sono indicati nei messaggi `UMI`.
* Per `com.day.cq.commons.impl.ExternalizerImpl`, consulta la [documentazione](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developer-tools/externalizer) relativa all’impostazione della configurazione di Externalizer utilizzando le variabili di ambiente di Cloud Manager in AEM as a Cloud Service.
* Per `org.apache.sling.commons.log.LogManager.factory.config`, modifica la configurazione OSGi per inviare il logger personalizzato al file `logs/error.log`. Consulta la [documentazione](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/logs) per rimandare nuovamente al file `logs/error.log`.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
