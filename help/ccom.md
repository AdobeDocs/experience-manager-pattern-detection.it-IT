---
title: CCOM
description: Pagina della guida del codice del rilevatore pattern
exl-id: 59071538-56ec-44e7-8196-56e6525bb4b9
translation-type: tm+mt
source-git-commit: 4ad2fe0fa05b8252112df8a94958e65bb882482d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 6%

---

# CCOM {#ccom}

Componente personalizzato

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_overview"
>title="Componente personalizzato"
>abstract="CCOM identifica i componenti personalizzati installati in AEM. Queste informazioni sono fornite ai fini della valutazione delle migliori pratiche"

`CCOM` identifica i componenti personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle migliori pratiche.

Questo codice utilizza un sottotipo per identificare la categoria del componente:

* `custom.core`: Un supertipo nella catena di supertipi del componente contiene &quot;core/wcm/components/&quot;, che indica che eredita da un componente di base.
* `custom.foundation`: Un supertipo nella catena di supertipi del componente contiene &quot;core/wcm/components/&quot;, che indica che eredita da un componente di base.
* `custom.overlay.foundation`: Il percorso del componente contiene &quot;wcm/foundation/components/&quot; o &quot;foundation/components/&quot;, che indica che sovrappone un componente di base.
* `custom`: Il componente personalizzato non eredita o sovrappone un componente di base o di base.

## Possibili implicazioni e rischi {#implications-and-risks}

* La best practice prevede di ridurre al minimo il numero di componenti personalizzati, sfruttare i componenti core e utilizzare i componenti core con il sistema di stili per ridurre il debito tecnico.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ccom_guidance"
>title="Guida all&#39;implementazione"
>abstract="La best practice prevede di ridurre al minimo il numero di componenti personalizzati, sfruttare i componenti core e utilizzare i componenti core con il sistema di stili per ridurre il debito tecnico."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html" text="Componenti core"
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring" text="Sistema di stili"

* Per ulteriori informazioni sui componenti core, consulta [Introduzione ai componenti core](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it) .
* Per ulteriori informazioni sul sistema di stili, visita [Utilizzo del sistema di stili](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
