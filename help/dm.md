---
title: DM
description: Pagina della guida del codice del rilevatore pattern
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
translation-type: tm+mt
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 7%

---

# DM {#dm}

Dynamic Media

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Il codice DM identifica l’utilizzo di AEM Assets Dynamic Media nell’implementazione corrente. La modalità Dynamic Media viene rilevata dalla modalità di esecuzione."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html" text="Sviluppo AEM - Linee guida e best practice"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html" text="Linee guida per lo sviluppo per AEM as a Cloud Service"

`DM` identifica l’utilizzo di AEM Assets Dynamic Media. La modalità Dynamic Media viene rilevata dalla modalità di esecuzione.

Con questo codice viene utilizzato un sottotipo:

* `dynamic.media.runmode`: Il valore associato di questo sottotipo, se fornito, è:
   * `dynamicmedia`: Dynamic Media - Modalità ibrida
   * `dynamicmedia_scene7`: Dynamic Media - Modalità Scene 7

## Possibili implicazioni e rischi {#implications-and-risks}

* `dynamic.media.runmode`
   * Potrebbero esserci problemi di aggiornamento relativi a Dynamic Media.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Guida all&#39;implementazione"
>abstract="AEM come Cloud Service supporta solo la modalità runmode dynamic_media_scene7. Controlla le impostazioni correnti e rivolgiti al team di supporto Adobe per assistenza e chiarimenti."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html" text="Impostazione di Dynamic Media"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"


* `dynamic.media.runmode`
   * Per ulteriori informazioni, consulta [Configurazione di Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html).

* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
