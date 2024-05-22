---
title: CCOM
description: Pagina della guida del codice di Pattern Detector.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 58fdb55e1f0c067dacf6825c4076465bc8c5d821
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 100%

---

# CCOM {#ccom}

Componente personalizzato

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizzato"
>abstract="CCOM identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle best practice"

`CCOM` identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle best practice.

Questo codice utilizza un sottotipo per identificare la categoria del componente:

* `custom.core`: un supertipo nella catena di supertipi del componente contiene `core/wcm/components/`, che indica che eredita da un componente core.
* `custom.foundation`: un supertipo nella catena di supertipi del componente contiene `core/wcm/components/`, che indica che eredita da un componente core.
* `custom.overlay.foundation`: il percorso del componente contiene `wcm/foundation/components/` o `foundation/components/`, che indica che si sovrappone a un componente di base.
* `custom`: il componente personalizzato non eredita o sovrappone un componente core o di base.

## Possibili implicazioni e rischi {#implications-and-risks}

* La best practice prevede di ridurre al minimo il numero di componenti personalizzati, utilizzare i componenti core e e di farlo con il sistema di stili per ridurre il debito tecnico.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Guida all’implementazione"
>abstract="La best practice prevede di ridurre al minimo il numero di componenti personalizzati, utilizzare i componenti core e usarli con il sistema di stili per ridurre il debito tecnico."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction" text="Componenti core"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring" text="Sistema di stili"

* Per ulteriori informazioni sui componenti core, consulta [Introduzione ai componenti core](https://experienceleague.adobe.com/it/docs/experience-manager-core-components/using/introduction).
* Per ulteriori informazioni sul sistema di stili, consulta [Utilizzo del sistema di stili](https://experienceleague.adobe.com/it/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use#page-authoring).
* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
