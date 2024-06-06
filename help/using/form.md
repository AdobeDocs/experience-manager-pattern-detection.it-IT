---
title: FORM
description: Pagina della guida del codice di Pattern Detector.
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 0d693e3ccadc81b59852914f115bb2fa2ea166b0
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 100%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Informazioni di base {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="FORMS"
>abstract="Il codice FORMS identifica i potenziali problemi relativi alla migrazione da AEM (Adobe Experience Manager) Forms ad AEM Forms as a Cloud Service. Esamina le potenziali implicazioni e i rischi associati e risolvi questi problemi prima di migrare a Cloud Service."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-manager-pattern-detection/table-of-contents/forms#implications-and-risks" text="Possibili implicazioni e rischi"

`FORMS` identifica potenziali problemi relativi alla migrazione da [!DNL Adobe Experience Manager Forms] a [!DNL Adobe Experience Manager Forms] as a [!DNL Cloud Service]. Risolvi questi problemi prima di eseguire la migrazione a [!DNL Cloud Service].

I sottotipi seguenti consentono di identificare i diversi tipi di problemi:

* `modified.feature`: queste funzioni, risorse o API sono state aggiornate o modificate per Cloud Service. Prima di eseguire la migrazione a Cloud Service, esegui l’utility di migrazione per rendere queste funzioni e risorse compatibili.
* `unavailable.feature`: nell’ambiente ci sono funzioni e risorse non disponibili o rimosse da Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente Cloud Service.
* `unsupported.feature`: l’ambiente utilizza alcune funzioni non ancora supportate da Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente Cloud Service. Per informazioni sulla disponibilità delle funzioni, consulta le note sulla versione mensili.
* `unsupported.api`: in Cloud Service sono presenti alcune API non ancora supportate. Prima di eseguire la migrazione a Cloud Service, disattiva, sostituisci o rimuovi queste API dal codice. Per informazioni sulla disponibilità delle funzioni, consulta le note sulla versione mensili.

Consulta le sezioni [Possibili implicazioni e rischi](#implications-and-risks) e [Soluzioni possibili](#solutions) per informazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzioni e API compatibili con Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

Risolvi i seguenti problemi, prima di eseguire la migrazione a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando non vengono affrontati le implicazioni e i rischi elencati di seguito, alcune funzioni non vengono eseguite come previsto nell’ambiente di Cloud Service.

* La funzionalità editor di codice della funzione editor di regole non è disponibile. (CODE_EDITOR)

* Per impostazione predefinita, il supporto e-mail (porta SMTP) è disattivato. (EMAIL_SERVICE_CONFIGURATION)

* L’azione di invio **[!UICONTROL E-mail PDF]** non è disponibile. (EMAIL_PDF_SUBMIT_ACTION)

* I moduli adattivi basati su XFA non sono ancora supportati. (XFA_BASED_FORM, XDP_BASED_FORM)

* Al momento dell’inoltro del modulo viene richiamata immediatamente un’azione di invio, anziché attendere che tutti i firmatari completino la firma. Pertanto, l’accordo PDF di Adobe Acrobat Sign inviato ai firmatari non è disponibile per l’utilizzo o l’elaborazione delle azioni di invio. (FORM_SIGN_INTEGRATION)

* Il passaggio Firma non è disponibile. (SIGNATURE_STEP)

* Il passaggio Verifica non è disponibile. (VERIFY_STEP)

* L’azione di invio **[!UICONTROL Invia a Forms Workflow]** non è disponibile. In AEM 6.5 Forms e versioni precedenti, l’azione di invio veniva utilizzata per inviare i dati del modulo adattivo a versioni precedenti di AEM Forms con flussi di lavoro JEE e LiveCycle. (LC_WORKFLOW_SUBMISSION)

* La funzionalità di comunicazione interattiva non è disponibile. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* Il pannello a soffietto metadati non è disponibile. (METADATA_ACCORDION_FORM_CONTAINER)

* Il componente CAPTCHA ora per impostazione predefinita utilizza il servizio Google reCAPTCHA per la convalida. L’opzione per utilizzare Adobe Experience Manager per la convalida CAPTCHA è obsoleta. (FORMS_CAPTCHA)

* L’app [!DNL AEM Forms] non è disponibile per [!DNL Cloud Services]. (AEM_FORMS_APP)

* I passaggi relativi ai [Servizi basati su documenti](https://experienceleague.adobe.com/it/docs/experience-manager-65/content/forms/install-aem-forms/osgi-installation/install-configure-document-services#deployment-topology) non sono disponibili nei flussi di lavoro AEM. (WORKFLOW_DOCSERVICES)

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Guida all’implementazione"
>abstract="Le informazioni esposte tramite il codice FORMS possono fornire indicazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzioni e API compatibili con Cloud Service. Per ricevere assistenza o chiarimenti, contatta il servizio di assistenza Adobe."
>additional-url="https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza l’utilità di migrazione per convertire tutti gli script di regole nell’ambiente in funzioni riutilizzabili. È possibile sfruttare le funzioni riutilizzabili con l’editor di regole visive per continuare a ottenere gli stessi risultati degli script di regole. (CODE_EDITOR)

* Contatta il team di supporto affinché possa abilitare la funzionalità e-mail (porta SMTP aperta) per il tuo ambiente. Per impostazione predefinita sono abilitate solo le connessioni HTTP e HTTPS in uscita. (EMAIL_SERVICE_CONFIGURATION, passaggio e-mail)

* Utilizza l’azione Invia **[!UICONTROL e-mail]** invece di **[!UICONTROL E-mail PDF]**. L’azione Invia **[!UICONTROL e-mail]** fornisce opzioni per l’invio di allegati e inserisce un documento Record (DoR) nell’e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* I dati inviati contengono l’ID contratto di Adobe Acrobat Sign. Se necessario, è possibile utilizzare l’ID Firma accordo per recuperare un Firma accordo PDF. (FORM_SIGN_INTEGRATION)

* Rimuovi il passaggio Firma da un modulo adattivo esistente. Configura il modulo adattivo per utilizzare l’[esperienza di firma nel browser](https://blog.developer.adobe.com/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). All’invio di un modulo adattivo, mostra il consenso di Adobe Sign alla firma dell’accordo all’interno del browser. L’esperienza di firma nel browser consente di rendere più rapida l’operazione e di far risparmiare tempo al firmatario. (SIGNATURE_STEP)

* Rimuovi il passaggio di verifica dai moduli adattivi esistenti prima di spostarli in un ambiente [!DNL Cloud Service]. (VERIFY_STEP)

* Modifica i moduli adattivi esistenti per utilizzare le azioni di invio [Invia a endpoint REST](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-to-rest-endpoint), [Invia e-mail](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#send-email), [Invia utilizzando modello dati del modulo](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#submit-using-form-data-model) e [Richiama un flusso di lavoro AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow).

* Puoi sviluppare un flusso di lavoro AEM e modificare i moduli adattivi esistenti per utilizzare l’azione di invio [Flusso di lavoro AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions#invoke-an-aem-workflow) per inviare dati a un flusso di lavoro AEM invece di utilizzare l’azione **[!UICONTROL Invia a Forms Workflow]**. È possibile sviluppare un’azione di invio personalizzata per inviare dati, allegati o documenti Record (DoR) a un processo di LiveCycle invece di utilizzare [!UICONTROL Invia a Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Per informazioni sulla disponibilità della funzione di comunicazione interattiva, consulta le note sulla versione mensili. Non eseguire la migrazione di comunicazioni interattive, lettere e dizionari correlati in un ambiente di Cloud Service fino a quando la funzione non sarà disponibile. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Non viene effettuata alcuna sostituzione del pannello a soffietto metadati. Rimuovilo dai moduli prima di migrarli a Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilizza Google reCaptcha invece del servizio CAPTCHA fornito da Adobe Experience Manager. (FORMS_CAPTCHA)

* Non eseguire la migrazione di un modello di un flusso di lavoro AEM che utilizza un passaggio Flusso di lavoro di servizi per documenti. Inoltre, non eseguire la migrazione o l’aggiornamento di moduli adattivi che inviano dati utente a un modello di flusso di lavoro che utilizza passaggi di servizi basati su documenti e non modificare l’`Submit Action` a [uno supportato](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/forms/adaptive-forms-authoring/authoring-adaptive-forms-foundation-components/configure-submit-actions-and-metadata-submission/configuring-submit-actions) prima della migrazione. (WORKFLOW_DOCSERVICES)

* Forms adattivo offre un design responsive. Questi moduli modificano l’aspetto, la progettazione e l’interattività in base al dispositivo sottostante. Puoi continuare a utilizzare moduli adattivi sui dispositivi mobili. Per informazioni sulla disponibilità dell’app [!DNL AEM Forms] segui le note sulla versione mensili. (AEM_FORMS_APP)

* Il supporto per Forms adattivo basato su XFA non è immediatamente disponibile. Se desideri utilizzare Forms adattivo basato su XFA, contatta il Supporto Adobe con i dettagli del caso d’uso e i requisiti specifici.(XFA_BASED_FORM, XDP_BASED_FORM)

Per eventuali dubbi o chiarimenti, contatta l’[assistenza clienti Adobe](https://helpx.adobe.com/it/enterprise/using/support-for-experience-cloud.html).
