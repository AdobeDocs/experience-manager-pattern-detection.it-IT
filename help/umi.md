---
title: UMI
description: Pagina della guida del codice di Pattern Detector
exl-id: 04efa760-61f5-4690-8b4e-89fa756c5b64
source-git-commit: e72ddc20578f8ca736da198e626478816e7ca641
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 83%

---

# UMI {#umi}

Problema di configurazione errata dell’aggiornamento

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_overview"
>title="Problema di configurazione errata dell’aggiornamento"
>abstract="UMI identifica le modifiche ad alcune configurazioni OSGi che causeranno problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/aem-cloud-changes.html?lang=it" text="Modifiche importanti in AEM as a Cloud Service"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=it" text="AEM as a Cloud Service: note sulla versione"

`UMI` identifica le modifiche ad alcune configurazioni OSGi che causeranno problemi durante l’aggiornamento, come un aggiornamento non riuscito o funzionalità ridotte.

Le seguenti configurazioni vengono verificate per la modifica:
* `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName`
* `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`
* `org.apache.sling.engine.impl.auth.SlingAuthenticator`
* `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory`
* `com.day.cq.commons.impl.ExternalizerImpl`

## Possibili implicazioni e rischi {#implications-and-risks}

* La modifica o la rimozione delle configurazioni può causare i seguenti problemi:
   * L’aggiornamento potrebbe bloccarsi (ad esempio `org.apache.jackrabbit.oak.security.user.RandomAuthorizableNodeName` mancante ma presente in `org.apache.jackrabbit.oak.security.internal.SecurityProviderRegistration.requiredServicePids`).
   * Dopo l’aggiornamento possono verificarsi problemi di autorizzazione (`org.apache.sling.engine.impl.auth.SlingAuthenticator`).
   * Alcune funzionalità potrebbero non funzionare come previsto. Ad esempio, la modifica di `org.apache.sling.scripting.java.impl.JavaScriptEngineFactory` può causare la mancata compilazione di alcuni file JSP, che alla fine porta a una perdita di funzionalità.
   * Valori della configurazione dell&#39;esternalizzatore `com.day.cq.commons.impl.ExternalizerImpl` sono impostate dalle variabili di ambiente cloud manager in AEM as a Cloud Service.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_umi_guidance"
>title="Guida all’implementazione"
>abstract="Si consiglia di rivedere le configurazioni correnti e ripristinare eventuali modifiche apportate alle configurazioni citate per evitare problemi futuri di aggiornamento. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Non modificare o rimuovere le quattro configurazioni sopra menzionate.
* Se le configurazioni sono state modificate, è necessario riportarle ai valori previsti. Questi valori sono indicati nei messaggi `UMI`.
* Per `com.day.cq.commons.impl.ExternalizerImpl`, fai riferimento a [documentazione](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developer-tools/externalizer.html?lang=en) per impostare la configurazione dell’esternalizzatore utilizzando le variabili di ambiente cloud manager in AEM as a Cloud Service.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
