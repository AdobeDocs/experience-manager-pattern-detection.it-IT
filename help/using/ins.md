---
title: INS
description: Pagina della guida del codice di Pattern Detector.
exl-id: d89e1589-3195-4b2d-98f4-136bedaecb0b
source-git-commit: 2881b122773a8a5ad09fb9a14ae35b4a83dae20d
workflow-type: ht
source-wordcount: '109'
ht-degree: 100%

---

# INS {#ins}

Spazio dei nomi non valido

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_overview"
>title="Spazio dei nomi non valido"
>abstract="INS identifica problemi di spazio dei nomi nell’istanza AEM"

`INS` (Spazio dei nomi non valido) identifica i problemi relativi allo spazio dei nomi nell’istanza AEM.

I sottotipi vengono utilizzati per identificare i diversi tipi di informazioni, ad esempio:

* `uri`: identifica l’URI dello spazio dei nomi non valido in AEM.

## Possibili implicazioni e rischi {#implications-and-risks}

* Impossibile replicare il contenuto (su più livelli) o copiarlo (su più ambienti `env` tramite `/crx/packMgr` o Copia del contenuto).

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_ins_guidance"
>title="Guida all’implementazione"
>abstract="Contatta l’Assistenza clienti per ricevere aiuto."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Correggi le definizioni dello spazio dei nomi in base alle [specifiche JCR](https://developer.adobe.com/experience-manager/reference-materials/spec/jcr/1.0/4.5_Namespaces.html?lang=it). Segui i passaggi indicati [qui](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/how-can-i-delete-a-namespace-created-in-crx/td-p/225163)
* Contatta il [team di assistenza clienti di Experience Manager](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere dubbi.
