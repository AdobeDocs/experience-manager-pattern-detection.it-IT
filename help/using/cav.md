---
title: CAV
description: Pagina della guida del codice di Pattern Detector.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 100%

---

# CAV {#cav}

Violazione dell’area contenuto

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Violazione dell’area contenuto"
>abstract="Il codice CAV identifica il pattern in cui aree di contenuto diverse vengono utilizzate in modo da violare le regole di classificazione dei contenuti. Questa violazione fornisce una panoramica sulle sovrapposizioni e sui contenuti soggetti a limitazioni che potrebbero richiedere modifiche nel passaggio ad AEM as a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`CAV` identifica il pattern in cui diverse aree di contenuto vengono utilizzate in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste sling definisce come il contenuto di una risorsa, in particolare la relativa proprietà `sling:resourceType`, viene utilizzato per determinare lo script che verrà impiegato per il rendering del contenuto. Per ulteriori informazioni. consulta l’[individuazione dello script](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script). Sling fornisce anche tecniche per accedere alle risorse e unirle tramite sovrapposizioni e sostituzioni. Queste tecniche sono descritte come parte di [Sling Resource Merger](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e in [Sovrapposizioni](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Per rendere più sicuro e facile far comprendere alla clientela quali aree di `/libs` si possono utilizzare in sicurezza e sovrapporre, il contenuto in `/libs` è stato classificato con proprietà “mixin”:

* Pubblico
* Astratto
* Finale
* Interno

Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) per una descrizione dettagliata.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Guida all’implementazione"
>abstract="È necessario rivedere i pattern identificati con CAS in cui si verificano violazioni per aree di contenuto diverse. È necessario evitare aree di classificazione dei contenuti finale e interna. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Aggiornamenti sostenibili"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evita di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare i cambiamenti provenienti da `/libs` dopo gli aggiornamenti AEM, Service Pack o le installazioni Cumulative Fix Pack.
* Contatta il [team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
