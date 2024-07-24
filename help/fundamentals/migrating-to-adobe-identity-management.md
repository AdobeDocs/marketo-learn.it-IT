---
title: Migrazione ad Adobe Identity Management
description: Descrizione in arrivo.
role: User
level: Beginner
hide: true
hidefromtoc: true
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: 8c9705b79083fd7b143b88800046180c94d377da
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Migrazione ad Adobe Identity Management

Adobe migliora il modo in cui gestisci gli abbonamenti e gli utenti Adobe Marketo Engage. Stiamo aumentando la produttività della tua organizzazione effettuando la migrazione degli abbonamenti di Marketo Engage e degli utenti a Adobe Admin Console.

Questo tutorial ti aiuterà a navigare nella migrazione in modo da poter iniziare a gestire Adobe Marketo Engage insieme ad altri account e prodotti di Adobe per i tuoi utenti in una posizione centrale. La migrazione è necessaria e non influirà sul flusso di lavoro di marketing, sui contenuti, sulle integrazioni o sulle risorse.

## Elenco di controllo pre-migrazione per amministratori di Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Per garantire che la tua organizzazione possa migrare Adobe Marketo Engage a Adobe Admin Console, ti consigliamo di seguire l’elenco di controllo seguente per gestire le modifiche imminenti.

### 1. Identifica l&#39;amministratore di sistema e discute le azioni da intraprendere {#identify-your-system-administrators}

* Se non sai chi siano gli amministratori di sistema all&#39;interno della tua organizzazione, contatta il team dell&#39;account Adobe o contatta il supporto Adobe `marketocares@marketo.com`.

* Conferma Adobe Admin Console (o l’organizzazione di Adobe) in cui verrà effettuata la migrazione delle sottoscrizioni di Marketo Engage.  Le sottoscrizioni di Marketo Engage devono essere distribuite nella stessa organizzazione del Dynamic Chat, uno strumento nativo di automazione delle conversazioni integrato con il Marketo Engage. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"}

* Scopri cosa comunicare con gli amministratori di sistema nella [sezione E-mail di esempio](#announce-the-migration-timeline).

### 2. Acquisisci familiarità con i cambiamenti e gli impatti della migrazione all’identità Adobe {#familiarize-yourself-with-the-changes}

Nel video seguente, il team di Marketo Engage per la gestione dei prodotti illustra il percorso di migrazione e le aspettative.

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?quality=12&learn=on){transcript=true}

Ulteriori informazioni su questo argomento per gli amministratori di Marketo Engage sono disponibili nei seguenti articoli della guida:

* [Elenco di controllo installazione utente](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Panoramica di Adobe Identity Management](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Informazioni su abbonamento Marketo e migrazione utente a Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migrazione a Adobe Identity con la console di migrazione](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Informazioni sull&#39;utilizzo di Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html){target="_blank"}

### 3. Annuncerai ai tuoi team interni i tempi e la preparazione necessari per la migrazione {#announce-the-migration-timeline}

* Contrassegna la data di migrazione sui calendari degli amministratori di Marketo Engage e degli utenti una volta pianificata.

Puoi modificare la data di migrazione in **Amministratore** > **Console di migrazione** > **Pre-migrazione** per adattarla meglio alla tua sequenza temporale interna. Ulteriori informazioni sulla riprogrammazione e sui limiti di [modifica della data di migrazione](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* Inviare un messaggio e-mail agli amministratori di sistema.

Di seguito è riportato un esempio di e-mail da inviare agli amministratori di sistema. In genere, il reparto IT gestisce tutte le licenze Adobe.

`---------------------------------------------------`

**Oggetto: Supporto richiesto: migrazione degli abbonamenti di Marketo Engage a Adobe Admin Console**

Gentile `[IT Administrator/NAME]`,

La sottoscrizione al Marketo Engage verrà presto migrata al sistema Adobe Identity Management. `[Marketing Operation team]` necessita del tuo aiuto per completare alcuni passaggi necessari prima che inizi la migrazione degli utenti, al fine di ridurre al minimo l&#39;impatto sugli utenti del Marketo Engage.

`1.` Conferma se l&#39;organizzazione gestisce già altri prodotti Adobe in Adobe Admin Console e se il Marketo Engage verrà migrato alla stessa console.

* Gli abbonamenti al Marketo Engage devono trovarsi nella stessa organizzazione del Dynamic Chat, uno strumento nativo di automazione delle conversazioni integrato con il Marketo Engage.

* In caso di domande o dubbi sull&#39;Admin Console a cui verrà aggiunto il Marketo Engage, contatta il supporto Adobe all&#39;indirizzo `marketocares@marketo.com` e usa il CC.

`2.` Cerca un&#39;e-mail dall&#39;Adobe con l&#39;oggetto &quot;Azione richiesta per gestire l&#39;accesso utente a Adobe Marketo Engage `[Package Tier]`&quot;. Questa e-mail è stata inviata dopo il provisioning delle licenze di Marketo Engage nel nostro Admin Console. Solo gli amministratori di sistema riceveranno questa e-mail. Vi preghiamo di informarci immediatamente quando lo ricevete.

* L’Adobe può richiedere il consenso dell’utente, dell’amministratore di sistema dell’Admin Console, per eseguire automaticamente la migrazione degli utenti alla console esistente della nostra organizzazione. Nell&#39;e-mail con oggetto &quot;Azione richiesta per gestire l&#39;accesso degli utenti a Adobe Marketo Engage `[Package Tier]`&quot;, fare clic sul pulsante &quot;Inizia&quot; per passare alla pagina del consenso.

`3.` **Facoltativo:** Configurazione SSO (Single Sign-On) in Adobe Admin Console.

* Per migliorare ulteriormente l’accesso degli utenti con SSO sulla propria identità di Adobe, ti chiediamo di fornire assistenza per la configurazione SSO su Adobe Admin Console prima che si verifichi la migrazione degli utenti.

Apprezziamo la vostra collaborazione durante questa transizione. Fatemi sapere quando avete completato questi passaggi in modo da poter procedere con la migrazione.

Cordiali saluti

`[Your Name]`

`---------------------------------------------------`

* Invia un messaggio e-mail agli utenti del Marketo Engage.

Di seguito è riportato un esempio di e-mail che puoi utilizzare per annunciare la prossima migrazione agli utenti del tuo Marketo Engage che non dispongono di privilegi di amministratore.

`---------------------------------------------------`

**Oggetto: Aggiornamento importante - Migrazione degli abbonamenti di Marketo Engage a Adobe Admin Console**

Gentili utenti del Marketo Engage,

Abbiamo un annuncio importante riguardante la nostra istanza di Marketo Engage e le modalità di accesso. Adobe sta trasferendo gli abbonamenti e gli utenti del Marketo Engage al Adobe Admin Console per consentirci di centralizzare tutte le attività di amministrazione dei prodotti in un’unica posizione. Questo non influirà sui flussi di lavoro di marketing, sui contenuti, sulle integrazioni o sulle risorse.

**Dettagli chiave:**

* **Data migrazione**: `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Tempistica**: la migrazione inizia verso mezzanotte, ora locale, del nostro abbonamento.

* **Impatto**: durante la migrazione degli utenti non si verificherà alcuna perdita di accesso al prodotto. Se hai effettuato l’accesso durante la migrazione dell’account, ti verrà richiesto di eseguire nuovamente l’accesso in pochi minuti utilizzando Adobe Identity dopo la migrazione.

* **Vantaggi**: autentica il Marketo Engage e altri prodotti di Adobe utilizzando un&#39;unica identità di Adobe, un Adobe ID o un Federated ID di Adobe (SSO).

**Operazioni da eseguire:**

`1.` **Prepara**: per eseguire la migrazione a un&#39;identità Adobe è necessaria la verifica e-mail.

i. Hai ricevuto un&#39;e-mail di richiesta di verifica via e-mail con un collegamento (rimane valido per 3 giorni). Se il collegamento è scaduto, puoi inviare di nuovo l&#39;e-mail di verifica dal Marketo Engage accedendo a **Amministratore** > **Il mio account** > **Impostazioni account** e facendo clic su **Invia di nuovo verifica**.

ii. Per il completamento della verifica e-mail è necessaria una sessione utente attiva. Accedi al tuo abbonamento di Marketo Engage utilizzando prima l’URL del provider di identità (IdP).

`2.` **Onboard**: dopo la migrazione dell&#39;account utente, riceverai un&#39;e-mail da un Adobe riguardante le modifiche al metodo di accesso.

i. Accettare il nuovo invito facendo clic sul pulsante &quot;Accetta invito&quot; ed effettuare l&#39;accesso con Adobe Identity.

ii. Nella pagina di accesso di Adobe, accedi con un Adobe ID esistente.

`3.` **Contatto**: se hai domande o hai bisogno di assistenza dopo la migrazione del tuo account, o se la migrazione del tuo account non è avvenuta e hai perso l&#39;accesso al Marketo Engage, contatta il team di migrazione del Marketo Engage all&#39;indirizzo `[your internal contact email/phone]`.

Apprezziamo la vostra collaborazione durante questa transizione. Grazie per la comprensione e l&#39;impegno nel garantire la sicurezza dei nostri sistemi.

Cordiali saluti

`[Your Name]`

`---------------------------------------------------`
