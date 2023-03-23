---
title: DM
description: Pagina della guida del codice di Pattern Detector
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: 54b121a6ec29ba6ff6fb33b402f1821c34d0763f
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 100%

---

# DM {#dm}

Dynamic Media

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Il codice DM identifica l’utilizzo di AEM Assets Dynamic Media nell’implementazione corrente. La modalità Dynamic Media viene rilevata dalla modalità di esecuzione."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/dev-guidelines-bestpractices.html?lang=it" text="Sviluppo AEM: linee guida e best practice"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/implementing/developing/development-guidelines.html?lang=it" text="Linee guida per lo sviluppo in AEM as a Cloud Service"

`DM` identifica l’utilizzo di AEM Assets Dynamic Media. La modalità Dynamic Media viene rilevata dalla modalità di esecuzione.

Con questo codice viene utilizzato un sottotipo:

* `dynamic.media.runmode`: il valore associato di questo sottotipo, se fornito, è:
   * `dynamicmedia`: Dynamic Media: modalità ibrida
   * `dynamicmedia_scene7`: Dynamic Media - modalità Scene7

## Possibili implicazioni e rischi {#implications-and-risks}

* `dynamic.media.runmode`
   * Potrebbero esserci problemi di aggiornamento relativi a Dynamic Media.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_guidance"
>title="Guida all’implementazione"
>abstract="AEM as a Cloud Service supporta solo la modalità di esecuzione dynamicmedia_scene7. Controlla le impostazioni correnti e rivolgiti al team di supporto Adobe per assistenza e chiarimenti."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=it" text="Configurazione di Dynamic Media"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"


* `dynamic.media.runmode`
   * Per ulteriori informazioni, consulta [Configurazione di Dynamic Media](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/administering-dynamic-media.html?lang=it).

* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
