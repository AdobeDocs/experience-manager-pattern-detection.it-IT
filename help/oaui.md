---
title: OAUI
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# OAUI {#oaui}

Istanza utenti OAuth

## Sfondo {#background}

`OAUI` identifica il pattern in cui è presente almeno un utente configurato relativo a OAuth che richiede la migrazione corretta.

OAuth è configurato per gli utenti quando esiste un sottonodo denominato `oauth` direttamente sotto un nodo `rep:AuthorizableId` sotto forma di `/home/user-path/user-node/oauth`.

Un esempio è: `/home/users/ims/0001/R80w6XaUCBq3jHE47xDN/oauth`.

## Possibili implicazioni e rischi {#implications-and-risks}

* Gli utenti esterni configurati con OAuth non potranno accedere alle istanze di authoring/pubblicazione finché non saranno riconfigurati con la procedura seguente.

## Soluzioni possibili {#solutions}

* Contatta il tuo rappresentante di Adobe per discutere le opzioni per la migrazione degli utenti.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
