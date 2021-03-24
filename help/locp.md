---
title: LOCP
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---


# LOCP {#locp}

/libs Sovrascrittura di pacchetti personalizzati

## Sfondo {#background}

`LOCP` identifica il rilevamento di un pacchetto personalizzato che distribuisce contenuti a  `/libs`, che è un anti-pattern (tranne nel caso ACL).

## Possibili implicazioni e rischi {#implications-and-risks}

* Il codice cliente potrebbe essere eliminato o sostituito per qualsiasi CFP, SP o aggiornamento AEM principale.
* In alcuni casi il nuovo contenuto potrebbe non essere installato correttamente.

## Soluzioni possibili {#solutions}

* I pacchetti cliente devono distribuire il contenuto in `/apps` invece di `/libs`.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
