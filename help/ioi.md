---
title: IOI
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# IOI {#ioi}

Importazione Oak interna

## Sfondo {#background}

`IOI` identifica l&#39;utilizzo da parte del cliente dei pacchetti Oak interni, importandoli tramite OSGi. Di solito sono esportati senza alcuna versione particolare e sono destinati al consumo solo da altri bundle Oak o servizi di AEM di basso livello.

Alcuni di questi sono utilizzati da `com.adobe.granite.repository`, che imposta un archivio per AEM durante l&#39;avvio. Un altro esempio è il bundle di Adobe `com.adobe.granite.maintenance.oak`, che racchiude e fornisce attività di manutenzione Oak.

## Possibili implicazioni e rischi {#implications-and-risks}

* In una versione futura AEM le esportazioni interne potrebbero essere rimosse causando dipendenze interrotte e bundle inattivi a seconda direttamente di Oak.
* L’API nelle esportazioni interne potrebbe cambiare.

## Soluzioni possibili {#solutions}

* Utilizza l’API della risorsa Sling (o l’API JCR) invece di un accesso di basso livello.
* Evita di dipendere da pacchetti interni che non fanno parte di alcuna API o SPI pubblica.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.