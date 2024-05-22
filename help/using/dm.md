---
title: DM
description: Scopri come il codice di Pattern Detector identifica l’utilizzo di AEM Assets Dynamic Media.
exl-id: f077df57-f2bc-4875-a7de-41251a9d7f2f
source-git-commit: dd60fb9fb21d534e7b6f264826d3cc1477def421
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 81%

---

# DM {#dm}

Dynamic Media

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_dm_overview"
>title="Dynamic Media"
>abstract="Il codice DM identifica l’utilizzo di AEM Assets Dynamic Media nell’implementazione corrente. La modalità di esecuzione rileva la modalità Dynamic Medie."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/dev-guidelines-bestpractices" text="Sviluppo AEM: linee guida e best practice"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/implementing/developing/development-guidelines" text="Linee guida per lo sviluppo in AEM as a Cloud Service"

`DM` (Dynamic Media) identifica l’utilizzo di AEM Assets Dynamic Media. La modalità di esecuzione rileva la modalità Dynamic Medie.

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
>abstract="AEM as a Cloud Service supporta solo la modalità di esecuzione dynamicmedia_scene7. Controlla le impostazioni correnti e rivolgiti al team di supporto Adobe per assistenza e chiarimenti."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media" text="Configurazione di Dynamic Media"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"


* `dynamic.media.runmode`
   * Per ulteriori informazioni, consulta [Configurazione di Dynamic Media](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/assets/dynamicmedia/administering-dynamic-media).

* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
