---
title: ECU
description: Pagina della guida del codice di Pattern Detector.
exl-id: fd061001-b00e-44ae-bd31-71bd2fa733cd
source-git-commit: 84c193b66fbf9c41f546e8575a0aa17e94043b9a
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 50%

---

# ECU {#ecu}

OBSOLETO: Utilizzo di contenuti estranei (sostituito da CAV, Violazione dell’area contenuto)

## Sfondo {#background}

`ECU`  Identifica il pattern in cui diverse aree di contenuto vengono utilizzate in modo da violare le regole di classificazione del contenuto.

L’elaborazione delle richieste Sling definisce il modo in cui il contenuto di una risorsa, `sling:resourceType` in particolare, viene utilizzato per determinare lo script utilizzato per il rendering del contenuto. (Consulta [Individuazione dello script](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/introduction/the-basics#locating-the-script) per ulteriori informazioni). Sling fornisce anche tecniche per accedere e unire le risorse tramite “sovrapposizioni” e “sovrascritture”. Sono descritti come parte di [Sling Resource Merger](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-resource-merger) e [Sovrapposizioni](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/overlays).

Per rendere più sicuro e facile per i clienti capire quali aree di `/libs` sono sicuri da usare e sovrapporre al contenuto in `/libs` è stato classificato con proprietà &quot;mixin&quot;: pubblico, astratto, finale e interno. Ogni classificazione implica regole su come il contenuto può essere utente, ereditato o sovrapposto. Consulta [Aggiornamenti sostenibili](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/deploying/upgrading/sustainable-upgrades) per una descrizione dettagliata.

## Possibili implicazioni e rischi {#implications-and-risks}

* Un aggiornamento AEM può causare problemi di rendering della pagina e altri comportamenti indesiderati.
* Gli aggiornamenti di sicurezza non sono efficaci.

## Soluzioni possibili {#solutions}

* Riduci al minimo l’utilizzo della sovrapposizione dei contenuti nei casi in cui è necessario.
* In particolare, evita di sovrapporre i contenuti soggetti a restrizioni (classificazione finale e classificazione interna).
* È consigliabile adattare i cambiamenti provenienti da `/libs` dopo aggiornamenti AEM, Service Pack o installazioni Cumulative Fix Pack.
* Contatta il [Team di supporto AEM](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per fugare i dubbi.
