---
title: OCU
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 4f94d4a1e0b8eb7bedbedba2c8a683f34655b527
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# OCU {#ocu}

Utilizzo del codice obsoleto

## Sfondo {#background}

`OCU` identifica la situazione in cui alcuni nodi JCR, come i componenti Sling o AEM o le esportazioni API OSGi, vengono modificati o rimossi in modo non compatibile. Il cliente potrebbe non essere a conoscenza di questa modifica prima di un aggiornamento. Possono essere aggiornati a una versione non compatibile o non sono disponibili.

Poiché le versioni precedenti non sono installate per impostazione predefinita, l&#39;applicazione del cliente potrebbe non funzionare correttamente.

## Possibili implicazioni e rischi {#implications-and-risks}

* La funzionalità che dipende da qualsiasi componente che utilizza componenti o API obsoleti può essere interrotta e potrebbe non essere risolta correttamente dopo un aggiornamento.
* Alcune funzionalità dell&#39;applicazione del cliente o alcune funzionalità AEM potrebbero non funzionare correttamente o potrebbero non essere attive dopo un aggiornamento.

## Soluzioni possibili {#solutions}

* A breve termine: Potrebbe essere utile installare un pacchetto di compatibilità.
* A lungo termine: Adatta il codice cliente per utilizzare la versione più recente di componenti o API AEM.
* Contatta il nostro [AEM team di supporto](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
