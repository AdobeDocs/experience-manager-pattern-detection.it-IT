---
title: MODULO
description: Pagina della guida del codice del rilevatore pattern
exl-id: ac28760b-b0ab-4082-b7ce-730cddc4ad83
source-git-commit: 127f6ee2268d27d78067f030ef343da50a625004
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Sfondo {#background}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_overview"
>title="Forms"
>abstract="Il codice Forms identifica i potenziali problemi relativi alla migrazione da Adobe Experience Manager Forms ad Adobe Experience Manager Forms as a Cloud Service. Esamina le potenziali implicazioni e i rischi associati e risolvi questi problemi prima di migrare al Cloud Service."
>additional-url="https://experienceleague.adobe.com/docs/experience-manager-pattern-detection/table-of-contents/forms.html#implications-and-risks" text="Possibili implicazioni e rischi"

`FORMS` Identifica potenziali problemi relativi alla migrazione da [!DNL Adobe Experience Manager Forms] a [!DNL Adobe Experience Manager Form]s come [!DNL Cloud Service]. Risolvere questi problemi prima di eseguire la migrazione a [!DNL Cloud Service].

I sottotipi seguenti consentono di identificare i diversi tipi di problemi:

* `modified.feature`: Queste funzioni, risorse o API sono state aggiornate o modificate per Cloud Service. Prima di eseguire la migrazione al Cloud Service, esegui l’utility di migrazione per rendere queste funzioni e risorse compatibili con il Cloud Service.
* `unavailable.feature`: L’ambiente dispone di funzioni e risorse non disponibili o rimosse dal Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service.
* `unsupported.feature`: L’ambiente utilizza alcune funzioni non ancora supportate al Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili.
* `unsupported.api`: Nel Cloud Service sono presenti alcune API non ancora supportate. Prima di eseguire la migrazione al Cloud Service, disattiva, sostituisci o rimuovi queste API dal codice. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili.

Consulta la sezione [Possibili implicazioni e rischi](#implications-and-risks) e [Soluzioni possibili](#solutions) sezioni per informazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzioni e API compatibili con il Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

Risolvere i seguenti problemi, prima di eseguire la migrazione a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando non vengono affrontati le implicazioni e i rischi elencati di seguito, alcune funzioni non funzionano come previsto nell’ambiente di Cloud Service.

* La funzionalità editor di codice della funzione editor di regole non è disponibile. (CODE_EDITOR)

* Per impostazione predefinita, il supporto e-mail (porta SMTP) è disattivato. (EMAIL_SERVICE_CONFIGURATION)

* La **[!UICONTROL E-mail PDF]** L’azione Invia non è disponibile.(EMAIL_PDF_SUBMIT_ACTION)

* Forms adattivo basato su XFA non è ancora supportato. (XFA_BASED_FORM, XDP_BASED_FORM)

* Al momento dell’invio del modulo viene richiamata immediatamente un’azione di invio, anziché attendere che tutti i firmatari completino la firma. Pertanto, l’accordo di Adobe Sign inviato ai firmatari non è disponibile per l’utilizzo o l’elaborazione delle azioni di invio da parte di PDF. (FORM_SIGN_INTEGRATION)

* Il passaggio Firma non è disponibile. (SIGNATURE_STEP)

* Il passaggio Verifica non è disponibile. (VERIFY_STEP)

* La **[!UICONTROL Invia al Forms Workflow]** L’azione Invia non è disponibile. Nelle versioni AEM 6.5 Forms e precedenti, l’azione Invia è stata utilizzata per inviare dati del modulo adattivo ad AEM Forms legacy su flussi di lavoro e LiveCycli Workflow JEE. (LC_WORKFLOW_SUBMISSION)

* La funzionalità di comunicazione interattiva non è disponibile.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* Il pannello a soffietto metadati non è disponibile. (METADATA_ACCORDION_FORM_CONTAINER)

* Il componente CAPTCHA ora utilizza il servizio Google reCAPTCHA per convalidare CAPTCHA, per impostazione predefinita. L’opzione per utilizzare Adobe Experience Manager per convalidare CAPTCHA è obsoleta. (FORMS_CAPTCHA)

* [!DNL AEM Forms] app non disponibile per [!DNL Cloud Services]. (AEM_FORMS_APP)

* [Servizi basati su documenti](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) i passaggi non sono disponibili nei flussi di lavoro AEM. (WORKFLOW_DOCSERVICES)

## Soluzioni possibili {#solutions}

>[!CONTEXTUALHELP]
>id="aemcloud_bpa_forms_guidance"
>title="Guida all&#39;implementazione"
>abstract="Le informazioni esposte tramite il codice FORMS possono fornire indicazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzioni e API compatibili con il Cloud Service. Contatta il supporto Adobe per assistenza e chiarimenti"
>additional-url="https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html" text="Supporto Experience Cloud"

* Utilizza l&#39;utilità di migrazione per convertire tutti gli script di regole nel tuo ambiente in funzioni riutilizzabili. È possibile utilizzare le funzioni riutilizzabili con l&#39;editor di regole visive per continuare a ottenere i risultati ottenuti con gli script di regole. (CODE_EDITOR)

* Contatta il team di supporto per abilitare la funzionalità e-mail (porta SMTP aperta) per il tuo ambiente. Per impostazione predefinita sono abilitate solo le connessioni HTTP e HTTPS in uscita. (passaggio EMAIL_SERVICE_CONFIGURATION, Email)

* Utilizzo **[!UICONTROL E-mail]** Invia azione invece di **[!UICONTROL E-mail PDF]**. La **[!UICONTROL E-mail]** L’azione di invio fornisce opzioni per l’invio di allegati e allega documento di record (DoR) con e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* I dati inviati contengono l&#39;ID contratto Adobe Sign. Se necessario, è possibile utilizzare l’ID contratto di firma per recuperare un PDF Sign Agreement.  (FORM_SIGN_INTEGRATION)

* Rimuovi il passaggio Firma da un modulo adattivo esistente. Configurare il modulo adattivo da utilizzare [esperienza di firma nel browser](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Mostra il consenso di Adobe Sign alla firma del contratto all’interno del browser all’invio di un modulo adattivo. L’esperienza di firma nel browser consente di migliorare l’esperienza di firma e di risparmiare tempo per il firmatario. (SIGNATURE_STEP)

* Rimuovi il passaggio di verifica dal Forms adattivo esistente prima di spostare tali moduli in un [!DNL Cloud Service] ambiente. (VERIFY_STEP)

* Modificare i moduli adattivi esistenti da utilizzare [Invia all’endpoint REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Invia e-mail](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Invia utilizzando il modello dati del modulo](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model)e [Richiamare un flusso di lavoro AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Inviare Azioni.

* Puoi sviluppare un flusso di lavoro AEM e modificare i moduli adattivi esistenti da utilizzare [Flusso di lavoro AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Invia un’azione per inviare dati a un flusso di lavoro AEM invece di utilizzare la funzione **[!UICONTROL Invia al Forms Workflow]** Invia azione. È possibile sviluppare un’azione di invio personalizzata per inviare dati, allegati o documenti di record (DoR) a un processo di LiveCycle invece di utilizzare il [!UICONTROL Invia al Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Per informazioni sulla disponibilità della funzione di comunicazione interattiva, consultare le note sulle versioni mensili. Non eseguire la migrazione delle comunicazioni interattive, delle lettere e dei dizionari correlati in un ambiente di Cloud Service fino a quando la funzione non sarà disponibile. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Non viene effettuata alcuna sostituzione del pannello a soffietto metadati. Rimuovi dai moduli prima di migrarli al Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilizza Google reCaptcha invece del servizio CAPTCHA fornito da Adobe Experience Manager. (FORMS_CAPTCHA)

* Non eseguire la migrazione di un modello di flusso di lavoro AEM che utilizza un passaggio Flusso di lavoro di Document Services. Inoltre, non eseguire la migrazione o l’aggiornamento di Forms adattivo che inviano dati utente a un modello di flusso di lavoro che utilizza i passaggi del flusso di lavoro di Document Services o modificare l’azione di invio in un modello [uno supportato](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) prima della migrazione del modulo. (WORKFLOW_DOCSERVICES)

* Adaptive Forms offre un design reattivo. Questi moduli modificano l’aspetto, la progettazione e l’interattività in base al dispositivo sottostante. Puoi continuare a utilizzare l&#39;Adaptive Forms sui dispositivi mobili. Per informazioni sulla disponibilità della [!DNL AEM Forms] app. (AEM_FORMS_APP)

* Il supporto per Forms adattivo basato su XFA non è pronto all&#39;uso. Se desideri utilizzare Forms adattivo basato su XFA, contatta il Supporto Adobe con i dettagli del caso d’uso e i requisiti specifici.(XFA_BASED_FORM, XDP_BASED_FORM)

Rivolgiti a [Supporto Adobe](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) ottenere chiarimenti o affrontare le preoccupazioni.
