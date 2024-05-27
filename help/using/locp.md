---
title: LOCP
description: Pagina della guida del codice di Pattern Detector.
exl-id: a9993b58-7925-47c0-b774-b9ca8a4ee052
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---

# LOCP {#locp}

/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_overview"
>title="/libs Overwriting Custom Packages (/libs sovrascrive pacchetti personalizzati)"
>abstract="LOCP identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a `/libs`; si tratta di un anti-pattern (tranne nel caso di ACL)."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Aggiornamenti sostenibili"
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`LOCP` identifica il rilevamento di un pacchetto personalizzato che fornisce contenuti a `/libs`; si tratta di un anti-pattern (tranne nel caso di ACL).

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice cliente potrebbe venire eliminato o sostituito da eventuali aggiornamenti principali, CFP o SP di AEM.
* In alcuni casi i nuovi contenuti potrebbero non venire installati correttamente.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_locp_guidance"
>title="Guida all’implementazione"
>abstract="I clienti devono rivedere il proprio codice personalizzato e i pacchetti per verificare che il contenuto venga consegnato a `/libs`. Se necessario, esegui il refactoring per fare affidamento sulla sovrapposizione del contenuto in /apps per renderlo compatibile con AEM as a Cloud Service. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sovrapposizioni"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* I pacchetti del cliente devono distribuire i contenuti in `/apps` anziché `/libs`.
* Per eventuali chiarimenti o dubbi, rivolgiti al [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
