---
title: Migrazione ad Adobe Identity Management
description: Questo tutorial ti aiuterà a gestire la migrazione degli abbonamenti Marketo Engage e degli utenti a Adobe Admin Console.
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: tm+mt
source-wordcount: '1250'
ht-degree: 0%

---

# Migrazione ad Adobe Identity Management

Adobe sta migliorando il modo in cui gestisci gli abbonamenti e gli utenti Adobe Marketo Engage. Stiamo aumentando la produttività della tua organizzazione effettuando la migrazione degli abbonamenti Marketo Engage e degli utenti a Adobe Admin Console.

Questo tutorial ti aiuterà a navigare nella migrazione in modo da poter iniziare a gestire Adobe Marketo Engage insieme ad altri account e prodotti Adobe per i tuoi utenti da una posizione centrale. La migrazione è necessaria e non influirà sul flusso di lavoro di marketing, sui contenuti, sulle integrazioni o sulle risorse.

## Elenco di controllo pre-migrazione per amministratori di Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Per garantire che la tua organizzazione possa migrare Adobe Marketo Engage a Adobe Admin Console, ti consigliamo di seguire l’elenco di controllo seguente per gestire le modifiche imminenti.

### 1. Identificare l&#39;amministratore di sistema e il team IT e discutere le azioni da intraprendere {#identify-your-system-administrators}

* Se non sai chi siano gli amministratori di sistema nella tua organizzazione, contatta il team del tuo account Adobe o contatta il supporto Adobe `marketocares@marketo.com`.

* Conferma Adobe Admin Console (o l’organizzazione Adobe) in cui verrà effettuata la migrazione delle sottoscrizioni Marketo Engage. Probabilmente hai un Adobe Admin Console per [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}, uno strumento nativo di automazione delle conversazioni in Marketo Engage. Le sottoscrizioni Marketo Engage devono essere distribuite nella stessa organizzazione di Dynamic Chat.

* Collabora con il tuo team IT per inserire nell&#39;elenco Consentiti tutti i domini Adobe elencati [nella parte superiore di questo articolo](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} in modo da evitare interruzioni nell&#39;accesso a Marketo Engage dopo la migrazione ad Adobe Identity.

* **Facoltativo:** [Implementare Single Sign On (SSO)](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} prima della migrazione utente.

  >[!NOTE]
  >
  >Esistono differenze tra l&#39;SSO supportato da Marketo Engage e l&#39;SSO Adobe Admin Console. Di conseguenza, potrebbe essere necessario implementare le modifiche alla configurazione.

* **Facoltativo:** personalizza la [durata massima di sessione desiderata](https://helpx.adobe.com/it/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} prima della migrazione utente affinché gli utenti di Marketo Engage rimangano autenticati.

* Scopri cosa comunicare con gli amministratori di sistema nella [sezione E-mail di esempio](#announce-the-migration-timeline).

### 2. Acquisisci familiarità con le modifiche e gli impatti della migrazione ad Adobe Identity {#familiarize-yourself-with-the-changes}

Nel video seguente, il team di Product Management di Marketo Engage illustra il percorso di migrazione e le aspettative.

>[!VIDEO](https://video.tv.adobe.com/v/3432364/?t=170/?quality=12&learn=on&captions=ita){transcript=true}

Ulteriori informazioni su questo argomento per gli amministratori di Marketo Engage sono disponibili nei seguenti articoli della guida:

* [Elenco di controllo per l&#39;installazione utente](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Panoramica di Adobe Identity Management](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Informazioni su abbonamento Marketo e migrazione utente a Adobe Admin Console](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migrazione ad Adobe Identity con la console di migrazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Informazioni sull&#39;utilizzo di Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html){target="_blank"}

### 3. Annuncerai ai tuoi team interni i tempi e la preparazione necessari per la migrazione {#announce-the-migration-timeline}

* Una volta pianificata, contrassegna la data di migrazione nei calendari degli amministratori e degli utenti di Marketo Engage.

   * Puoi modificare la data di migrazione in **Amministratore** > **Console di migrazione** > **Pre-migrazione** per adattarla meglio alla tua sequenza temporale interna. Ulteriori informazioni sulla riprogrammazione e sui limiti di [modifica della data di migrazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* **Invia un&#39;e-mail agli amministratori di sistema**

Di seguito è riportato un esempio di e-mail da inviare agli amministratori. In genere, il reparto IT gestisce tutte le licenze Adobe.

+++ Esempio di e-mail da inviare agli amministratori di sistema

**Oggetto: Supporto richiesto: migrazione di abbonamenti Marketo Engage a Adobe Admin Console**

Gentile `[IT Administrator/NAME]`,

La sottoscrizione a Marketo Engage verrà presto migrata ad Adobe Identity Management System. `[Marketing Operation team]` necessita del tuo aiuto per completare alcuni passaggi necessari prima che inizi la migrazione degli utenti, al fine di ridurre al minimo l&#39;impatto sugli utenti di Marketo Engage.

`1.` Conferma se l&#39;organizzazione gestisce già altri prodotti Adobe in Adobe Admin Console e se Marketo Engage verrà migrato alla stessa console.

* Gli abbonamenti Marketo Engage devono trovarsi nella stessa organizzazione di Dynamic Chat, uno strumento nativo di automazione delle conversazioni integrato con Marketo Engage.

* In caso di domande o dubbi relativi ad Admin Console, contatta il supporto Adobe all&#39;indirizzo `marketocares@marketo.com` e usa il CC.

`2.` Cerca un&#39;e-mail da Adobe con oggetto &quot;Azione richiesta per gestire l&#39;accesso degli utenti a Adobe Marketo Engage `[Package Tier]`&quot;. Questa e-mail è stata inviata dopo il provisioning delle licenze Marketo Engage sul nostro Admin Console. Solo gli amministratori di sistema riceveranno questa e-mail. Vi preghiamo di informarci immediatamente quando lo ricevete.

* Adobe può richiedere il consenso dell’amministratore di sistema di Admin Console per eseguire automaticamente la migrazione degli utenti alla console esistente della nostra organizzazione. Nell&#39;e-mail con oggetto &quot;Azione richiesta per gestire l&#39;accesso degli utenti a Adobe Marketo Engage `[Package Tier]`&quot;, fare clic sul pulsante &quot;Inizia&quot; per passare alla pagina del consenso.

`3.` Dopo la migrazione, Marketo Engage passerà da experience.adobe.com a Adobe Experience Cloud. Inserire nell&#39;elenco Consentiti Per evitare interruzioni nell&#39;accesso a Marketo Engage, ti preghiamo di tutti i domini Adobe elencati [nella parte superiore di questo articolo](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}.

`4.` **Facoltativo:** configurare SSO (Single Sign-On) in Adobe Admin Console.

* A beneficio degli utenti che accedono con SSO sulla loro identità Adobe in futuro, consigliamo di configurare il SSO in Adobe Admin Console prima che si verifichi la migrazione degli utenti.

`5.` **Facoltativo:** Imposta una durata di [sessione massima](https://helpx.adobe.com/it/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} più lunga in Adobe Admin Console.

* Per evitare che gli utenti debbano accedere frequentemente, personalizza la durata della sessione in Impostazioni avanzate con una durata maggiore.

Apprezziamo la vostra collaborazione durante questa transizione. Fatemi sapere quando avete completato questi passaggi in modo da poter procedere con la migrazione.

Cordiali saluti

`[Your Name]`

+++

* **Invia un&#39;e-mail agli utenti di Marketo Engage**

Di seguito è riportato un esempio di messaggio e-mail per gli utenti di Marketo Engage che **non** dispongono di privilegi di amministratore.

+++ E-mail di esempio che annuncia la prossima migrazione

**Oggetto: Aggiornamento importante - Migrazione degli abbonamenti Marketo Engage a Adobe Admin Console**

Gentili utenti di Marketo Engage,

Abbiamo un annuncio importante riguardante la nostra istanza di Marketo Engage e le modalità di accesso. Adobe trasferisce gli abbonamenti e gli utenti Marketo Engage a Adobe Admin Console per consentirci di centralizzare l’amministrazione di tutti i prodotti in un’unica posizione. Questo non influirà sui flussi di lavoro di marketing, sui contenuti, sulle integrazioni o sulle risorse.

**Dettagli chiave:**

* **Data migrazione**: `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Tempistica**: la migrazione inizia verso mezzanotte, ora locale, del nostro abbonamento.

* **Impatto**: durante la migrazione degli utenti non si verificherà alcuna perdita di accesso al prodotto. Se hai effettuato l’accesso durante la migrazione dell’account, ti verrà richiesto di eseguire nuovamente l’accesso in pochi minuti con Adobe Identity dopo la migrazione.

* **Vantaggi**: autentica Marketo Engage e altri prodotti Adobe utilizzando un&#39;unica identità Adobe, un Adobe ID o un Federated ID (SSO) Adobe.

**Operazioni da eseguire:**

`1.` **Prepara**: è necessaria la verifica e-mail per eseguire la migrazione a un&#39;identità Adobe.

i. Hai ricevuto un&#39;e-mail di richiesta di verifica via e-mail con un collegamento (rimane valido per 3 giorni). Se il tuo collegamento è scaduto, puoi inviare nuovamente l&#39;e-mail di verifica da Marketo Engage facendo clic sull&#39;icona &quot;Il mio profilo&quot;, quindi vai a **Il mio account** > **Impostazioni account** > **Invia di nuovo la verifica**.

ii. Per il completamento della verifica e-mail è necessaria una sessione utente attiva. Accedi al tuo abbonamento a Marketo Engage utilizzando prima l’URL del provider di identità (IdP).

`2.` **Onboard**: dopo la migrazione dell&#39;account utente, Adobe ti invierà un&#39;e-mail relativa alle modifiche apportate al metodo di accesso.

i. Accetta il nuovo invito facendo clic sul pulsante &quot;Accetta invito&quot; ed effettuando l’accesso con Adobe Identity.

ii. Nella pagina di accesso di Adobe, accedi con un Adobe ID esistente.

iii. Devi prima accedere all’istanza di Marketo Engage per qualsiasi URL precedentemente segnalibro sul dominio engage-xx.marketo.com a cui stai navigando.

`3.` **Contatto**: se hai domande o hai bisogno di assistenza dopo la migrazione del tuo account, o se la migrazione del tuo account non è avvenuta e hai perso l&#39;accesso a Marketo Engage, contatta il team di migrazione di Marketo Engage all&#39;indirizzo `[your internal contact email/phone]`.

Apprezziamo la vostra collaborazione durante questa transizione. Grazie per la comprensione e l&#39;impegno nel garantire la sicurezza dei nostri sistemi.

Cordiali saluti

`[Your Name]`

+++
