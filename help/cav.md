---
title: CAV
description: Pagina della guida del codice del rilevatore pattern
exl-id: b2282da2-a028-4be7-914c-17dcd5d2902a
translation-type: tm+mt
source-git-commit: 1966a3e83ab6b2247d9f1095c8965eac399e3b6e
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# CAV {#cav}

Violazione dell’area contenuto

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_overview"
>title="Violazione dell’area contenuto"
>abstract="Il codice CAV identifica il pattern in cui vengono utilizzate aree di contenuto diverse in modo da violare le regole di classificazione dei contenuti. Questa violazione ti darebbe una panoramica sulle sovrapposizioni, sui contenuti limitati che potrebbero richiedere modifiche una volta che passiamo a AEM come Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html#platform" text="Sling Resource Merger"

`CAV` identifica il pattern in cui vengono utilizzate diverse aree di contenuto in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste Sling definisce come viene utilizzato il contenuto di una risorsa, in particolare la relativa proprietà `sling:resourceType`, per determinare lo script che verrà utilizzato per il rendering del contenuto. Per ulteriori informazioni, consulta [Individuazione dello script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) . Sling fornisce anche tecniche per accedere e unire le risorse tramite &quot;Sovrapposizioni&quot; e &quot;Sovrapposizioni&quot;. Questi sono descritti come parte di [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) e in [Overlay](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Per rendere più sicuro e facile per i clienti capire quali aree di `/libs` sono sicure da utilizzare e sovrapporre il contenuto in `/libs` è stato classificato con le proprietà &quot;mixin&quot;: Pubblico, astratto, finale e interno. Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Per una descrizione dettagliata, consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) .

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_cav_guidance"
>title="Guida all&#39;implementazione"
>abstract="È necessario rivedere i pattern identificati con CAS in cui esistono diverse violazioni dell’area di contenuto. È necessario evitare aree di classificazione dei contenuti finali e interni. Per assistenza e chiarimenti, contatta il supporto Adobe."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html" text="Aggiornamenti sostenibili"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evitare di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare le modifiche provenienti da `/libs` dopo AEM aggiornamenti, installazioni ServicePack o CumulativeFixPack.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
