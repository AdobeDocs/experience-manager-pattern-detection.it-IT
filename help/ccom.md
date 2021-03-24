---
title: CCOM
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a2c7137dd5cb2479bc0c6134d3afa58111049a68
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# CCOM {#ccom}

Componente personalizzato

## Sfondo {#background}

`CCOM` identifica i componenti personalizzati installati in AEM. Tali informazioni sono fornite ai fini della valutazione delle migliori pratiche.

Questo codice utilizza un sottotipo per identificare la categoria del componente:

* `custom.core`: Un supertipo nella catena di supertipi del componente contiene &quot;core/wcm/components/&quot;, che indica che eredita da un componente di base.
* `custom.foundation`: Un supertipo nella catena di supertipi del componente contiene &quot;core/wcm/components/&quot;, che indica che eredita da un componente di base.
* `custom.overlay.foundation`: Il percorso del componente contiene &quot;wcm/foundation/components/&quot; o &quot;foundation/components/&quot;, che indica che sovrappone un componente di base.
* `custom`: Il componente personalizzato non eredita o sovrappone un componente di base o di base.

## Possibili implicazioni e rischi {#implications-and-risks}

* La best practice prevede di ridurre al minimo il numero di componenti personalizzati, sfruttare i componenti core e utilizzare i componenti core con il sistema di stili per ridurre il debito tecnico.

## Soluzioni possibili {#solutions}

* Per ulteriori informazioni sui componenti core, consulta [Introduzione ai componenti core](https://experienceleague.adobe.com/docs/experience-manager-core-components/using/introduction.html?lang=it) .
* Per ulteriori informazioni sul sistema di stili, visita [Utilizzo del sistema di stili](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/page-authoring/style-system-feature-video-use.html?lang=en#page-authoring).
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
