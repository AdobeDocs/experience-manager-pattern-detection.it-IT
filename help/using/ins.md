---
title: INS
description: Pagina della guida del codice di Pattern Detector
source-git-commit: e469b546a75a77e538a54de3ffc1ca385c8cf21d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 47%

---

# INS {#ins}

Spazio dei nomi non valido

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Spazio dei nomi non valido"
>abstract="INS identifica i problemi di spazio dei nomi nell’istanza AEM"

`INS`  Lo spazio dei nomi non valido identifica i problemi di spazio dei nomi nell’istanza AEM.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `uri`: identifica l’URI dello spazio dei nomi non valido in AEM.

## Possibili implicazioni e rischi {#implications-and-risks}

* Impossibile replicare il contenuto (su più livelli) o copiarlo (su più livelli) tramite `/crx/packMgr` o Content Copy).

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Correggi le definizioni dello spazio dei nomi in base a [Specifiche JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html). Segui i passaggi indicati [qui](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* Per eventuali domande o dubbi, contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).