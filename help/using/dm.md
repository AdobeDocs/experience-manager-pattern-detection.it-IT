---
title: DM
description: Scopri come il codice di Pattern Detector identifica l’utilizzo di AEM Assets Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Il codice DM identifica l’utilizzo di AEM Assets Dynamic Media nell’implementazione corrente. La modalità Dynamic Media viene rilevata dalla modalità di esecuzione."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Sviluppo AEM: linee guida e best practice"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Linee guida per lo sviluppo in AEM as a Cloud Service"

`DM` (Dynamic Media) identifica l’utilizzo di AEM Assets Dynamic Media. La modalità Dynamic Media viene rilevata da quella di esecuzione.

Con questo codice viene utilizzato un sottotipo:

* `dynamic.media.runmode`: il valore associato di questo sottotipo, se fornito, è:
   * `dynamicmedia`: Dynamic Media: modalità ibrida
   * `dynamicmedia_scene7`: Dynamic Media: modalità Scena 7

## Possibili implicazioni e rischi {#implications-and-risks}

* `dynamic.media.runmode`
   * Potrebbero esserci problemi di aggiornamento relativi a Dynamic Media.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Guida all’implementazione"
>abstract="AEM as a Cloud Service supporta solo la modalità di esecuzione dynamicmedia_scene7. Rivedi le impostazioni correnti e rivolgiti al team di supporto Adobe per assistenza e chiarimenti."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configurazione di Dynamic Media"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"


* `dynamic.media.runmode`
   * Per ulteriori informazioni, consulta [Configurazione di Dynamic Media](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
