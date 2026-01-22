---
title: Migrazione ad Adobe Identity Management
description: Questo tutorial ti aiuterà a gestire la migrazione degli utenti e degli abbonamenti di Marketo Engage in Adobe Admin Console.
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: ht
source-wordcount: '1250'
ht-degree: 100%

---

# Migrazione ad Adobe Identity Management

Adobe sta migliorando la gestione degli abbonamenti e degli utenti di Adobe Marketo Engage. Attraverso la migrazione degli abbonamenti e degli utenti Marketo Engage in Adobe Admin Console, viene offerta una maggiore produttività alle organizzazioni.

Questo tutorial ti aiuterà ad orientarti nella migrazione, permettendoti di gestire Adobe Marketo Engage insieme agli account e prodotti Adobe in un’unica posizione centralizzata per tutti i tuoi utenti. La migrazione è necessaria e non interesserà i flussi di lavoro di marketing, i contenuti, le integrazioni o le risorse.

## Elenco di controllo pre-migrazione per gli amministratori di Marketo Engage {#pre-migration-checklist-for-marketo-engage-administrators}

Per assicurarti che la tua organizzazione possa effettuare la migrazione di Adobe Marketo Engage in Adobe Admin Console, ti consigliamo di seguire l’elenco di controllo seguente per gestire le modifiche in arrivo.

### &#x200B;1. Identifica l’amministratore di sistema e il team IT e discuti le azioni che potrebbero dover intraprendere {#identify-your-system-administrators}

* Se non sai chi siano gli amministratori di sistema nella tua organizzazione, contatta il team del tuo account Adobe o rivolgiti al supporto Adobe `marketocares@marketo.com`.

* Conferma quale Adobe Admin Console (o organizzazione Adobe) su cui verrà effettuata la migrazione degli abbonamenti Marketo Engage. È probabile che tu disponga di Adobe Admin Console per [Dynamic Chat](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}, uno strumento nativo di automazione delle conversazioni in Marketo Engage. Gli abbonamenti a Marketo Engage devono essere distribuiti nella stessa organizzazione di Dynamic Chat.

* Dopo aver eseguito la migrazione ad Adobe Identity, collabora con il tuo team IT per aggiungere all’elenco Consentiti tutti i domini Adobe elencati [nella parte superiore di questo articolo](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} per evitare interruzioni dell’accesso a Marketo Engage.

* **Facoltativo:** [implementa il Single Sign On (SSO)](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} prima della migrazione degli utenti.

  >[!NOTE]
  >
  >Esistono differenza tra l’accesso SSO supportato da Marketo Engage e quello di Adobe Admin Console. Pertanto, potrebbe essere necessario implementare modifiche alla configurazione.

* **Facoltativo:** personalizza la [durata massima della sessione desiderata](https://helpx.adobe.com/it/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} prima della migrazione degli utenti affinché gli utenti di Marketo Engage rimangano autenticati.

* Scopri cosa comunicare ai tuoi amministratori di sistema nella [sezione E-mail di esempio](#announce-the-migration-timeline).

### &#x200B;2. Acquisisci familiarità con le modifiche e gli effetti derivanti dalla migrazione ad Adobe Identity {#familiarize-yourself-with-the-changes}

Nel video seguente, il team di Gestione prodotto di Marketo Engage ti guida attraverso il percorso di migrazione e ti spiegherà che cosa aspettarti.

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?t=170/?quality=12&learn=on){transcript=true}

Ulteriore assistenza su questo argomento per gli amministratori di Marketo Engage è disponibile nei seguenti articoli della guida:

* [Elenco di controllo per la configurazione utente](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Panoramica di Adobe Identity Management](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Informazioni sull’abbonamento a Marketo e sulla migrazione degli utenti ad Adobe Admin Console](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migrazione ad Adobe Identity con la console di migrazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Informazioni sull’utilizzo di Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html){target="_blank"}

### &#x200B;3. Comunica la timeline della migrazione e la preparazione necessaria ai tuoi team interni {#announce-the-migration-timeline}

* Una volta pianificata, segna la data di migrazione sui calendari degli amministratori e degli utenti di Marketo Engage.

   * Puoi modificare tale data in **Amministrazione** > **Console di migrazione** > **Pre-migrazione** per adattarla meglio alla tua timeline interna. Ulteriori informazioni sulla riprogrammazione e sulle limitazioni relative alla [modifica della data di migrazione](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}.

* **Inviare un’e-mail agli amministratori di sistema**

Di seguito è riportata un’e-mail di esempio da inviare agli amministratori. In genere, è il tuo reparto IT a gestire tutte le licenze Adobe.

+++ E-mail di esempio da inviare agli amministratori di sistema

**Oggetto: Supporto richiesto - Migrazione degli abbonamenti di Marketo Engage ad Adobe Admin Console**

Gentile `[IT Administrator/NAME]`,

Presto verrà eseguita la migrazione del nostro abbonamento a Marketo Engage ad Adobe Identity Management System. Il `[Marketing Operation team]` ha bisogno del tuo aiuto per completare alcuni passaggi obbligatori prima di iniziare la migrazione degli utenti, in modo da ridurre al minimo l’impatto sugli utenti di Marketo Engage.

`1.` Conferma se l’organizzazione gestisce già altri prodotti Adobe in Adobe Admin Console e se la migrazione di Marketo Engage verrà eseguita sulla stessa console.

* Gli abbonamenti Marketo Engage devono trovarsi nella stessa organizzazione di Dynamic Chat, uno strumento nativo di automazione delle conversazioni integrato con Marketo Engage.

* In caso di domande o dubbi relativi ad Admin Console, contatta il supporto Adobe all’indirizzo `marketocares@marketo.com` e metterci in copia CC.

`2.` Verifica la ricezione di un’e-mail da parte di Adobe con oggetto “Azione richiesta per gestire l’accesso degli utenti ad Adobe Marketo Engage `[Package Tier]`”. Tale e-mail è stata inviata dopo il provisioning delle licenze di Marketo Engage in Admin Console. Solo gli amministratori di sistema la riceveranno. Rivolgiti a noi non appena la ricevi.

* In qualità di amministratore di sistema, Adobe potrebbe richiederti il consenso per eseguire automaticamente la migrazione degli utenti alla console esistente della nostra organizzazione. Nell’e-mail con oggetto “Azione richiesta per gestire l’accesso degli utenti ad Adobe Marketo Engage `[Package Tier]`”, fai clic sul pulsante “Inizia” per accedere alla pagina del consenso.

`3.` Dopo la migrazione, Marketo Engage non sarà più ospitato su experience.adobe.com ma su Adobe Experience Cloud. Per evitare interruzioni all’accesso a Marketo Engage, inserisci nell’elenco Consentiti tutti i domini Adobe elencati [nella parte superiore di questo articolo](https://experienceleague.adobe.com/it/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}.

`4.` **Facoltativo:** configura l’accesso SSO (Single Sign-On) in Adobe Admin Console.

* Per agevolare gli utenti che in futuro effettueranno l’accesso ad Adobe Identity tramite SSO, è necessario fornirci assistenza durante la relativa configurazione in Adobe Admin Console, prima che venga eseguita la migrazione degli utenti.

`5.` **Facoltativo:** imposta una [durata massima di sessione](https://helpx.adobe.com/it/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"} più lunga in Adobe Admin Console.

* Per evitare che gli utenti debbano effettuare l’accesso frequentemente, puoi personalizzare la durata della sessione in Impostazioni avanzate impostando un intervallo di tempo più lungo.

La tua collaborazione in questa fase di transizione è molto apprezzata. Facci sapere quando avrai completato questi passaggi, in modo da poter procedere con la migrazione.

Cordiali saluti,

`[Your Name]`

+++

* **Inviare un’e-mail agli utenti di Marketo Engage**

Di seguito è riportata un’e-mail di esempio per gli utenti di Marketo Engage che **non** dispongono di privilegi di amministratore.

+++ E-mail di esempio per comunicare la migrazione imminente 

**Oggetto: Aggiornamento importante - Migrazione degli abbonamenti di Marketo Engage ad Adobe Admin Console**

Gentili utenti di Marketo Engage,

Abbiamo una comunicazione importante riguardo alla nostra istanza di Marketo Engage e alle future modalità di accesso. Adobe sta trasferendo gli abbonamenti e gli utenti di Marketo Engage in Adobe Admin Console per consentirci di centralizzare l’amministrazione di tutti i prodotti in un’unica posizione. Questo trasferimento non interesserà i flussi di lavoro di marketing, i contenuti, le integrazioni o le risorse.

**Dettagli chiave:**

* **Data della migrazione**: `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **Tempistiche**: la migrazione inizierà intorno alla mezzanotte, ora locale per il nostro abbonamento.

* **Impatto**: durante la migrazione degli utenti, non si verificherà alcuna interruzione dell’accesso al prodotto. Se avrai effettuato l’accesso durante la migrazione del tuo account, la sessione verrà terminata e, dopo pochi minuti, ti verrà richiesto accedere di nuovo tramite Adobe Identity.

* **Vantaggi**: autenticazione di Marketo Engage e altri prodotti Adobe utilizzando un’unica identità Adobe, un Adobe ID o un Adobe Federated ID (SSO).

**Azioni richieste:**

`1.` **Preparazione**: per poter eseguire la migrazione a un’Adobe Identity è necessaria la verifica e-mail.

i. Hai ricevuto un’e-mail di richiesta di verifica con un collegamento (valido per 3 giorni). Se il collegamento è scaduto, puoi inviare nuovamente l’e-mail di verifica dall’interno di Marketo Engage facendo clic sull’icona “Il mio profilo”, quindi passando a **Il mio account** > **Impostazioni account** > **Invia di nuovo la verifica**.

ii. Per il corretto completamento della verifica e-mail è necessaria una sessione utente attiva. Effettua prima l’accesso al tuo abbonamento a Marketo Engage utilizzando l’URL del tuo provider di identità (IdP).

`2.` **Onboarding**: una volta eseguita la migrazione del tuo account utente, riceverai un’e-mail da Adobe relativa alle modifiche apportate alla modalità di accesso.

i. Accetta il nuovo invito facendo clic sul pulsante “Accetta invito” ed effettuando l’accesso tramite Adobe Identity.

ii. Nella pagina di accesso di Adobe, effettua l’accesso utilizzando un Adobe ID esistente.

iii. È necessario prima effettuare l’accesso all’istanza di Marketo Engage per qualsiasi URL precedentemente contrassegnato con segnalibro sul dominio engage-xx.marketo a cui desideri accedere.

`3.` **Contatto**: se hai domande o necessiti di assistenza dopo la migrazione del tuo account, oppure se la migrazione del tuo account non è stata effettuata e hai perso l’accesso a Marketo Engage, contatta il team responsabile della migrazione di Marketo Engage tramite `[your internal contact email/phone]`.

La tua collaborazione in questa fase di transizione è molto apprezzata. Grazie per la collaborazione e per l’impegno nel garantire la sicurezza dei nostri sistemi.

Cordiali saluti,

`[Your Name]`

+++
