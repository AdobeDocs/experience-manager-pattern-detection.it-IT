---
title: MODULO
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: 9a02482d023ce1a6cbbff24b8e6509c91ddd2a6b
workflow-type: tm+mt
source-wordcount: '1136'
ht-degree: 0%

---


# [!DNL FORMS] {#form}

[!DNL Adobe Experience Manager Forms]

## Sfondo {#background}

`FORMS` Identifica i potenziali problemi relativi alla migrazione da  [!DNL Adobe Experience Manager Forms] a  [!DNL Adobe Experience Manager Form]s come  [!DNL Cloud Service]. Risolvere questi problemi prima di eseguire la migrazione a [!DNL Cloud Service].

I sottotipi seguenti consentono di identificare i diversi tipi di problemi:

* `modified.feature`: Queste funzioni, risorse o API sono state aggiornate o modificate per Cloud Service. Prima di eseguire la migrazione al Cloud Service, esegui l’utility di migrazione per rendere queste funzioni e risorse compatibili con il Cloud Service.
* `unavailable.feature`: L’ambiente dispone di funzioni e risorse non disponibili o rimosse dal Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service.
* `unsupported.feature`: L’ambiente utilizza alcune funzioni non ancora supportate al Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili.
* `unsupported.api`: Nel Cloud Service sono presenti alcune API non ancora supportate. Prima di eseguire la migrazione al Cloud Service, disattiva, sostituisci o rimuovi queste API dal codice. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili.

Consulta le sezioni [Possibili implicazioni e rischi](#implications-and-risks) e [Soluzioni possibili](#solutions) per informazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzionalità e API compatibili con il Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

Risolvere i seguenti problemi, prima di eseguire la migrazione a [!DNL Adobe Experience Manager Forms as a Cloud Service]. Quando non vengono affrontati le implicazioni e i rischi elencati di seguito, alcune funzioni non funzionano come previsto nell’ambiente di Cloud Service.

* La funzionalità editor di codice della funzione editor di regole non è disponibile. (CODE_EDITOR)

* Per impostazione predefinita, il supporto e-mail (porta SMTP) è disattivato. (EMAIL_SERVICE_CONFIGURATION)

* L&#39;azione di invio **[!UICONTROL E-mail PDF]** non è disponibile.(EMAIL_PDF_SUBMIT_ACTION)

* Forms adattivo basato su XFA non è ancora supportato. (XFA_BASED_FORM, XDP_BASED_FORM)

* Al momento dell’invio del modulo viene richiamata immediatamente un’azione di invio, anziché attendere che tutti i firmatari completino la firma. Pertanto, il PDF del contratto Adobe Sign inviato ai firmatari non è disponibile per l’invio di azioni da utilizzare o elaborare. (FORM_SIGN_INTEGRATION)

* Il passaggio Firma non è disponibile. (SIGNATURE_STEP)

* Il passaggio Verifica non è disponibile. (VERIFY_STEP)

* La funzione Forms Portal e **[!UICONTROL Forms Portal Submit Action]** non sono ancora disponibili. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L&#39;azione **[!UICONTROL Invia a Forms Workflow]** Invia non è disponibile. Nelle versioni [!DNL AEM 6.5 Forms] e precedenti, l’azione Invia è stata utilizzata per inviare dati del modulo adattivo a flussi di lavoro e LiveCycli Workflow [!DNL AEM Forms on JEE] legacy. (LC_WORKFLOW_SUBMISSION)

* La funzionalità di comunicazione interattiva non è disponibile.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Al momento non sono supportate le funzioni Salva come]** bozza e  **[!UICONTROL Salva automaticamente]** i moduli adattivi. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Il pannello a soffietto metadati non è disponibile. (METADATA_ACCORDION_FORM_CONTAINER)

* Il componente CAPTCHA ora utilizza il servizio Google reCAPTCHA per convalidare CAPTCHA, per impostazione predefinita. L’opzione per utilizzare Adobe Experience Manager per convalidare CAPTCHA è obsoleta. (FORMS_CAPTCHA)

* [!DNL AEM Forms] app non disponibile per  [!DNL Cloud Services]. (AEM_FORMS_APP)

* [I passaggi ](https://experienceleague.adobe.com/docs/experience-manager-65/forms/install-aem-forms/osgi-installation/install-configure-document-services.html?lang=en#deployment-topology) dei servizi documenti non sono disponibili nei flussi di lavoro AEM. (WORKFLOW_DOCSERVICES)

## Soluzioni possibili {#solutions}

* Utilizza l&#39;utilità di migrazione per convertire tutti gli script di regole nel tuo ambiente in funzioni riutilizzabili. È possibile utilizzare le funzioni riutilizzabili con l&#39;editor di regole visive per continuare a ottenere i risultati ottenuti con gli script di regole. (CODE_EDITOR)

* Contatta il team di supporto per abilitare la funzionalità e-mail (porta SMTP aperta) per il tuo ambiente. Per impostazione predefinita sono abilitate solo le connessioni HTTP e HTTPS in uscita. (passaggio EMAIL_SERVICE_CONFIGURATION, Email)

* Utilizza **[!UICONTROL E-mail]** Invia azione invece di **[!UICONTROL Invia e-mail PDF]**. L’ **[!UICONTROL Azione di invio e-mail]** fornisce opzioni per l’invio di allegati e l’invio tramite e-mail di documenti di record (DoR). (EMAIL_PDF_SUBMIT_ACTION)

* I dati inviati contengono l&#39;ID contratto Adobe Sign. Se necessario, è possibile utilizzare l’ID contratto di firma per recuperare un PDF del contratto di firma.  (FORM_SIGN_INTEGRATION)

* Rimuovi il passaggio Firma da un modulo adattivo esistente. Configura il modulo adattivo per utilizzare [esperienza di firma nel browser](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). Mostra il consenso di Adobe Sign alla firma del contratto all’interno del browser all’invio di un modulo adattivo. L’esperienza di firma nel browser consente di migliorare l’esperienza di firma e di risparmiare tempo per il firmatario. (SIGNATURE_STEP)

* Rimuovi il passaggio di verifica dal Forms adattivo esistente prima di spostare tali moduli in un ambiente [!DNL Cloud Service]. (VERIFY_STEP)

* Modifica i moduli adattivi esistenti per utilizzare [Invia all’endpoint REST](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-to-rest-endpoint), [Invia e-mail](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#send-email), [Invia tramite Form Data Model](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#submit-using-form-data-model) e [Richiama un flusso di lavoro AEM](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Invia azioni. L’azione di invio di Forms Portal e Forms Portal non è ancora disponibile. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* È possibile sviluppare un flusso di lavoro AEM e modificare i moduli adattivi esistenti per utilizzare [AEM Flusso di lavoro](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html#invoke-an-aem-workflow) Invia azione per inviare dati a un flusso di lavoro AEM invece di utilizzare l’ **[!UICONTROL Invia a Forms Workflow]** Invia azione. È possibile sviluppare un’azione di invio personalizzata per inviare dati, allegati o documenti di record (DoR) a un processo di LiveCycle invece di utilizzare l’ [!UICONTROL Invia a Forms Workflow]. (LC_WORKFLOW_SUBMISSION)

* Per informazioni sulla disponibilità della funzione di comunicazione interattiva, consultare le note sulle versioni mensili. Non eseguire la migrazione delle comunicazioni interattive, delle lettere e dei dizionari correlati in un ambiente di Cloud Service fino a quando la funzione non sarà disponibile. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Disattiva l&#39;opzione **[!UICONTROL Salva come bozza]** e **[!UICONTROL Abilita salvataggio automatico]** nel Forms adattivo prima di migrarli al Cloud Service. È possibile abilitare queste opzioni una volta rilasciata la funzione Forms Portal per il Cloud Service. Per informazioni sulla disponibilità delle funzioni, consultare le note sulla versione mensili. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Non viene effettuata alcuna sostituzione del pannello a soffietto metadati. Rimuovi dai moduli prima di migrarli al Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilizza Google reCaptcha invece del servizio CAPTCHA fornito da Adobe Experience Manager. (FORMS_CAPTCHA)

* Adaptive Forms offre un design reattivo. Questi moduli modificano l’aspetto, la progettazione e l’interattività in base al dispositivo sottostante. Puoi continuare a utilizzare l&#39;Adaptive Forms sui dispositivi mobili. Per informazioni sulla disponibilità dell’app [!DNL AEM Forms], consulta le note sulla versione mensili. (AEM_FORMS_APP)

* Non eseguire la migrazione di un modello di flusso di lavoro AEM che utilizza un passaggio Flusso di lavoro di Document Services. Inoltre, non eseguire la migrazione o l’aggiornamento di Forms adattivo che inviano dati utente a un modello di flusso di lavoro che utilizza i passaggi del flusso di lavoro di Document Services oppure modificare l’azione di invio in un [supportato](https://experienceleague.adobe.com/docs/experience-manager-forms-cloud-service/forms/create-an-adaptive-form/configure-submit-actions-and-metadata-submission/configuring-submit-actions.html) prima di eseguire la migrazione del modulo. (WORKFLOW_DOCSERVICES)

* Il supporto per Forms adattivo basato su XFA non è pronto all&#39;uso. Se desideri utilizzare Forms adattivo basato su XFA, contatta il Supporto Adobe con i dettagli del caso d’uso e i requisiti specifici.(XFA_BASED_FORM, XDP_BASED_FORM)

Rivolgiti a [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
