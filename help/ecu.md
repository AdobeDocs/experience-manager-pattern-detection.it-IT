---
title: ECU
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 2391ad7851d4e6634a7bacd684b08db44a9c78e8
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---


# ECU {#ecu}

OBSOLETO: Utilizzo di contenuti estranei (sostituito da CAV, Violazione dell’area contenuto)

## Sfondo {#background}

`ECU` identifica il pattern in cui vengono utilizzate diverse aree di contenuto in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste Sling definisce come viene utilizzato il contenuto di una risorsa, in particolare la relativa proprietà `sling:resourceType`, per determinare lo script che verrà utilizzato per il rendering del contenuto. (Consulta [Individuazione dello script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html#locating-the-script) per ulteriori informazioni.) Sling fornisce anche tecniche per accedere e unire le risorse tramite &quot;Sovrapposizioni&quot; e &quot;Sovrapposizioni&quot;. Questi sono descritti come parte di [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html) e in [Overlay](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html).

Per rendere più sicuro e facile per i clienti capire quali aree di `/libs` sono sicure da utilizzare e sovrapporre il contenuto in `/libs` è stato classificato con le proprietà &quot;mixin&quot;: Pubblico, astratto, finale e interno. Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Per una descrizione dettagliata, consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html) .

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evitare di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare le modifiche provenienti da `/libs` dopo AEM aggiornamenti, installazioni ServicePack o CumulativeFixPack.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
