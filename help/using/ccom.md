---
title: CCOM
description: Pagina della guida del codice di Pattern Detector.
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
source-git-commit: 982ad1a6f43a29f2ee2284219757c8fc11b31ce0
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 92%

---

# CCOM {#ccom}

Componente personalizzato

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizzato"
>abstract="CCOM identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle best practice"

`CCOM` identifica i componenti personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle best practice.

Questo codice utilizza un sottotipo per identificare la categoria del componente:

* `custom.core`: un supertipo nella catena di supertipi del componente contiene “core/wcm/components/”, che indica che eredita da un componente di base.
* `custom.foundation`: un supertipo nella catena di supertipi del componente contiene “core/wcm/components/”, che indica che eredita da un componente di base.
* `custom.overlay.foundation`: il percorso del componente contiene “wcm/foundation/components/” o “foundation/components/”, che indica che sovrappone un componente di base.
* `custom`: il componente personalizzato non eredita o sovrappone un componente core o di base.

## Possibili implicazioni e rischi {#implications-and-risks}

* La best practice prevede di ridurre al minimo il numero di componenti personalizzati, sfruttare i componenti core e utilizzarli con il sistema di stili per ridurre il debito tecnico.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Guida all’implementazione"
>abstract="La best practice prevede di ridurre al minimo il numero di componenti personalizzati, sfruttare i componenti core e utilizzarli con il sistema di stili per ridurre il debito tecnico."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it" text="Componenti core"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=it#page-authoring" text="Sistema di stili"

* Per ulteriori informazioni sui componenti core, consulta [Introduzione ai componenti core](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it).
* Per ulteriori informazioni sul sistema di stili, consulta [Utilizzo del sistema di stili](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=it#page-authoring).
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
