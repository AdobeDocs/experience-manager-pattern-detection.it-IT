---
title: CAV
description: Pagina della guida del codice di Pattern Detector.
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 45%

---

# CAV {#cav}

Violazione dell’area contenuto

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Violazione dell’area contenuto"
>abstract="Il codice CAV identifica il pattern in cui aree di contenuto diverse vengono utilizzate in modo da violare le regole di classificazione dei contenuti. Questa violazione fornisce una panoramica sulle sovrapposizioni, sui contenuti limitati che potrebbero dover essere modificati dopo lo spostamento nell’as a Cloud Service AEM."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger#platform" text="Sling Resource Merger"

`CAV` Identifica il pattern in cui diverse aree di contenuto vengono utilizzate in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste Sling definisce il modo in cui il contenuto di una risorsa, `sling:resourceType` in particolare, viene utilizzato per determinare lo script utilizzato per il rendering del contenuto. Consulta [Individuazione dello script](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) per ulteriori informazioni. Sling fornisce anche tecniche per accedere e unire le risorse tramite “sovrapposizioni” e “sovrascritture”. Sono descritti come parte di [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e [Sovrapposizioni](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Per rendere più sicuro e facile per i clienti capire quali aree di `/libs` sono sicuri da usare e sovrapporre al contenuto in `/libs` è stato classificato con proprietà &quot;mixin&quot;: pubblico, astratto, finale e interno. Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) per una descrizione dettagliata.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Guida all’implementazione"
>abstract="È necessario rivedere i pattern identificati con CAS in cui esistono diverse violazioni dell’area di contenuto. È necessario evitare le aree di classificazione dei contenuti finale e interna. Per assistenza o chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades" text="Aggiornamenti sostenibili"
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evita di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare i cambiamenti provenienti da `/libs` dopo aggiornamenti AEM, Service Pack o installazioni Cumulative Fix Pack.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
