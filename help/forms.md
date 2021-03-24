---
title: Forms
description: Pagina della guida del codice del rilevatore pattern
translation-type: tm+mt
source-git-commit: a6ba6e93c89644160650882ecbf17028bec35068
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---


# [!DNL FORMS] {#forms}

[!DNL Adobe Experience Manager Forms]

## Sfondo {#background}

`FORMS` identifica come Cloud Service i potenziali problemi relativi alla migrazione da Adobe Experience Manager Forms ad Adobe Experience Manager Forms. Risolvere questi problemi prima di eseguire la migrazione al Cloud Service.

I sottotipi seguenti consentono di identificare i diversi tipi di problemi:

* `modified.feature`: Queste funzioni, risorse o API sono state aggiornate o modificate per Cloud Service. Prima di eseguire la migrazione al Cloud Service, esegui l’utility di migrazione per rendere queste funzioni e risorse compatibili con il Cloud Service.
* `unavailable.feature`: L’ambiente dispone di funzioni e risorse non disponibili o rimosse dal Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service.
* `unsupported.feature`: L’ambiente utilizza alcune funzioni non ancora supportate al Cloud Service. Non eseguire la migrazione di tali funzionalità o risorse in un ambiente di Cloud Service. Controlla le note sulle versioni mensili per verificare la disponibilità delle funzioni.
* `unsupported.api`: Nel Cloud Service sono presenti alcune API non ancora supportate. Prima di eseguire la migrazione al Cloud Service, disattiva, sostituisci o rimuovi queste API dal codice. Controlla le note sulle versioni mensili per verificare la disponibilità delle funzioni.

Consulta le sezioni [Possibili implicazioni e rischi](#implications-and-risks) e [Soluzioni possibili](#solutions) per informazioni sulle sostituzioni e altre azioni necessarie per rendere alcune funzionalità e API compatibili con il Cloud Service

## Possibili implicazioni e rischi {#implications-and-risks}

Risolvi i seguenti problemi, prima di eseguire la migrazione ad Adobe Experience Manager Forms as a Cloud Service. Quando non vengono affrontati le implicazioni e i rischi elencati di seguito, alcune funzioni non funzionano come previsto nell’ambiente di Cloud Service.

* La funzionalità editor di codice della funzione editor di regole non è disponibile. (CODE_EDITOR)

* Per impostazione predefinita, il supporto e-mail (porta SMTP) è disattivato. (EMAIL_SERVICE_CONFIGURATION)

* L&#39;azione di invio **[!UICONTROL E-mail PDF]** non è disponibile.(EMAIL_PDF_SUBMIT_ACTION)

* I moduli adattivi basati su XDP non sono ancora supportati. (XDP_BASED_FORM)

* Al momento dell’invio del modulo viene richiamata immediatamente un’azione di invio, anziché attendere che tutti i firmatari completino la firma. Pertanto, il documento della firma del modulo adattivo (PDF del contratto Adobe Sign inviato ai firmatari) non è disponibile per le azioni di invio da utilizzare o elaborare. (FORM_SIGN_INTEGRATION)

* Il passaggio Firma non è disponibile. (SIGNATURE_STEP)

* Il passaggio Verifica non è disponibile. (VERIFY_STEP)

* La funzione Forms Portal e **[!UICONTROL Forms Portal submit action]** non sono disponibili. Non è possibile utilizzare Forms Portal per elencare i moduli, salvare le bozze o mostrare i moduli inviati. Non è possibile inviare (utilizzare **[!UICONTROL Forms Portal per inviare i dati di azione]** ) inviati a un modulo adattivo a un Forms Portal. [!UICONTROL Al momento non sono supportate le funzioni Salva come ] bozza e  [!UICONTROL Salva automaticamente ] i moduli adattivi. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL, DRAFT_AUTO_SAVE, DRAFT_SAVE)

* L&#39;azione di invio **[!UICONTROL Invia a flusso di lavoro Forms]** non è disponibile. Nelle versioni AEM 6.5 Forms e precedenti, l’azione Invia è stata utilizzata per inviare dati del modulo adattivo ad AEM Forms legacy su flussi di lavoro e LiveCycli Workflow JEE. (LC_WORKFLOW_SUBMISSION)

* La funzionalità di comunicazione interattiva non è disponibile.  (FP_PROFILE_INTERACTIVE_COMMUNICATIONS).

* **[!UICONTROL Al momento non sono supportate le funzioni Salva come]** bozza e  **[!UICONTROL Salva automaticamente]** i moduli adattivi. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Il pannello a soffietto metadati non è disponibile. (METADATA_ACCORDION_FORM_CONTAINER)

* Il componente CAPTCHA ora utilizza il servizio Google reCAPTCHA per convalidare CAPTCHA, per impostazione predefinita. L’opzione per utilizzare Adobe Experience Manager per convalidare CAPTCHA non è disponibile. (FORMS_CAPTCHA)

## Soluzioni possibili {#solutions}

* Utilizza l&#39;utilità di migrazione per convertire tutti gli script di regole nel tuo ambiente in funzioni riutilizzabili. È possibile utilizzare le funzioni riutilizzabili con l&#39;editor di regole visive per continuare a ottenere i risultati ottenuti con gli script di regole. (CODE_EDITOR)

* Contatta il team di supporto per abilitare la funzionalità e-mail (porta SMTP aperta) per il tuo ambiente. Per impostazione predefinita sono abilitate solo le connessioni HTTP e HTTPS in uscita. (EMAIL_SERVICE_CONFIGURATION)

* Utilizza l&#39;azione di invio **[!UICONTROL E-mail]** invece di **[!UICONTROL E-mail PDF]**. L’azione di invio **[!UICONTROL E-mail]** fornisce opzioni per l’invio di allegati e allega documento di record (DoR) con e-mail. (EMAIL_PDF_SUBMIT_ACTION)

* Non eseguire la migrazione dei moduli adattivi basati su XDP in un ambiente di Cloud Service. Controlla le note sulle versioni mensili per verificare la disponibilità delle funzioni. (XDP_BASED_FORM)

* I dati inviati contengono l’ID contratto di firma. Se necessario, è possibile utilizzare l’ID contratto di firma per recuperare un PDF del contratto di firma.  (FORM_SIGN_INTEGRATION)

* Sostituisci il passaggio Firma nei moduli adattivi con l’opzione Firma invio di un modulo adattivo, presente nella stessa finestra. Consente di continuare a fornire un&#39;esperienza di firma [nel browser](https://medium.com/adobetech/using-adobe-sign-to-e-sign-an-adaptive-form-heres-the-best-way-to-do-it-dc3e15f9b684). (SIGNATURE_STEP)

* Rimuovi il passaggio di verifica dai moduli adattivi esistenti prima di spostare tali moduli in un ambiente di Cloud Service. (VERIFY_STEP)

* Non vi sono alternative a **[!UICONTROL Forms Portal submit action]**. È possibile utilizzare questa azione di invio una volta che la funzionalità di Forms Portal è stata rilasciata per il Cloud Service. Controlla le note sulle versioni mensili per verificare la disponibilità delle funzioni. (FORMS_PORTAL_SUBMISSION, FORMS_PORTAL)

* Non esiste un&#39;azione di invio alternativa alle azioni di invio **[!UICONTROL Invia a flusso di lavoro Forms]**. È possibile sviluppare un’azione di invio personalizzata per inviare dati, allegati o documenti di record (DoR) a un processo di LiveCycle. (LC_WORKFLOW_SUBMISSION)

* Non eseguire la migrazione delle comunicazioni interattive, delle lettere e dei dizionari correlati in un ambiente di Cloud Service. (FP_PROFILE_INTERACTIVE_COMMUNICATIONS)

* Disattiva l&#39;opzione **[!UICONTROL Salva come bozza]** e **[!UICONTROL Abilita salvataggio automatico]** nei moduli adattivi prima di migrarli al Cloud Service. È possibile abilitare queste opzioni una volta rilasciata la funzione Forms Portal per il Cloud Service. Controlla le note sulle versioni mensili per verificare la disponibilità delle funzioni. (DRAFT_AUTO_SAVE, DRAFT_SAVE)

* Non viene effettuata alcuna sostituzione del pannello a soffietto metadati. Rimuovi dai moduli prima di migrarli al Cloud Service.(METADATA_ACCORDION_FORM_CONTAINER)

* Utilizza Google reCaptcha invece del servizio CAPTCHA fornito da Adobe Experience Manager. (FORMS_CAPTCHA)

Rivolgiti a [Adobe Support](https://helpx.adobe.com/enterprise/using/support-for-experience-cloud.html) per ottenere chiarimenti o per risolvere eventuali problemi.
