---
title: ECU
description: Pagina della guida del codice di Pattern Detector.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: baa8f6dbf24b735348ed6b27f1e885b5078859ce
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 97%
---
# ECU {#ecu}

OBSOLETO: Utilizzo di contenuti estranei (sostituito da CAV, Violazione dell’area contenuto)

## Informazioni di base {#background}

`ECU` identifica il pattern di utilizzo di aree di contenuto diverse in modo tale da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste sling definisce come il contenuto di una risorsa, in particolare la relativa proprietà `sling:resourceType`, viene utilizzato per determinare lo script che verrà impiegato per il rendering del contenuto. Per ulteriori informazioni, vedere [Individuazione dello script](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script). Sling fornisce anche tecniche per accedere alle risorse e unirle tramite sovrapposizioni e sostituzioni. Queste tecniche sono descritte come parte di [Sling Resource Merger](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e in [Sovrapposizioni](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/implementing/developing/platform/overlays).

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

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evita di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare i cambiamenti provenienti da `/libs` dopo gli aggiornamenti AEM, Service Pack o le installazioni Cumulative Fix Pack.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per eventuali dubbi.
