---
title: ECU
description: Pagina della guida del codice di Pattern Detector
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: cbd43bca20831c19eb30703cc1ec528c75f2a2ef
workflow-type: ht
source-wordcount: '264'
ht-degree: 100%

---

# ECU {#ecu}

OBSOLETO: Utilizzo di contenuti estranei (sostituito da CAV, Violazione dell’area contenuto)

## Sfondo {#background}

`ECU` identifica il pattern in cui diverse aree di contenuto vengono utilizzate in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste sling definisce come il contenuto di una risorsa, in particolare la sua proprietà `sling:resourceType`, viene utilizzato per determinare lo script che verrà utilizzato per il rendering del contenuto. (Consulta [Individuazione dello script](https://experienceleague.adobe.com/docs/experience-manager-65/developing/introduction/the-basics.html?lang=it#locating-the-script) per ulteriori informazioni). Sling fornisce anche tecniche per accedere e unire le risorse tramite “sovrapposizioni” e “sovrascritture”. Sono descritti come parte di [Sling Resource Merger](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/sling-resource-merger.html?lang=it) e [Sovrapposizioni](https://experienceleague.adobe.com/docs/experience-manager-65/developing/platform/overlays.html?lang=it).

Per rendere più sicuro e facile per i clienti capire quali aree `/libs` si possono utilizzare in sicurezza e sovrapporre il contenuto in `/libs` è stato classificato con proprietà “mixin”: pubblico, astratto, finale e interno. Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/docs/experience-manager-65/deploying/upgrading/sustainable-upgrades.html?lang=it) per una descrizione dettagliata.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evita di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare i cambiamenti provenienti da `/libs` dopo aggiornamenti AEM, installazioni ServicePack o CumulativeFixPack.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o risolvere dubbi.
