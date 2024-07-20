---
title: Sviluppare una guida alla governance delle istanze con la relativa documentazione
description: Scopri come stabilire una solida procedura per la creazione e la manutenzione della documentazione e del registro modifiche per l’istanza di Marketo Engage. In questo modo non solo si risparmia tempo per la condivisione delle conoscenze del team, ma si migliora anche lo stato e l’efficienza dell’istanza.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: 4313b54a-1848-4684-b037-7a7795dd01ec
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 0%

---

# Sviluppare una guida alla governance delle istanze con la relativa documentazione

Quando entri in un&#39;istanza legacy di [!DNL Marketo Engage], spesso si verifica la mancanza di documentazione tecnica e funzionale aggiornata. In qualità di amministratore, stabilire linee guida per garantire una corretta governance delle istanze è una responsabilità fondamentale che non puoi ignorare. Si tratta di una delle strategie critiche per [aumentare l&#39;efficienza mentre si lavora in un&#39;istanza di Marketo Engage stabilita](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

Questo tutorial dettagliato, creato da [!DNL Adobe Marketo Champion] (2018), Nick Hajdin, ti guiderà attraverso questo processo per delineare la configurazione della tua istanza, documentare i programmi operativi principali e gestire [!DNL changelog] per applicare criteri di governance rigidi.

## Perché sviluppare una guida alla governance delle istanze e una documentazione per l’istanza ereditata?

La documentazione dettagliata e un [!DNL changelog] sono fondamentali per una gestione efficiente e per il trasferimento delle conoscenze all&#39;interno dell&#39;istanza [!DNL Marketo Engage]. Tenere traccia delle modifiche e delle decisioni apportate durante la configurazione dell’istanza può aiutarti a:

1. Formare gli utenti interni più facilmente e in modo scalabile.
2. Generare in modo più efficiente in [!DNL Marketo Engage] a lungo termine.
3. Mantenere lo stato di salute e l&#39;igiene dell&#39;istanza per evitare di trascorrere ore a cercare e-mail, [audit trail](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html) e [registro attività](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) per ottenere il contesto.
4. Risparmia tempo con il trasferimento delle conoscenze di [!DNL Marketo Engage] a un nuovo amministratore di [!DNL Marketo Engage] se il tuo team subisce un ricambio.

## Guida alla governance di [!DNL Marketo Engage] 101

Una guida alla governance funge da fonte di verità per la configurazione dell’istanza e i requisiti di progettazione del sistema. Le informazioni chiave che si consiglia di includere in questo documento sono:

* Strutture di programmi/cartelle
* Autorizzazione utente e ruolo
* Limiti di comunicazione
* Standard di governance
* Formazione interna degli utenti prima di concedere loro l’accesso alla piattaforma

## Come sviluppare e gestire una guida alla governance per l&#39;istanza [!DNL Marketo Engage]

### Passaggio 1: identifica la guida e la documentazione sullo stato attuale della governance

* **Impossibile individuare la documentazione per l&#39;istanza ereditata:** Se di recente è stato avviato un nuovo ruolo e non è possibile individuare la documentazione per l&#39;istanza ereditata, **passare al passaggio 2** e iniziare con un modello scaricabile fornito.
* **Ho la documentazione sul file:** Congratulazioni, questo è un buon segno! Assicurati di rivederne la rilevanza per vedere quando viene apportata l’ultima modifica. Se non viene gestito attivamente dai membri del gruppo, si consiglia di aggiornarlo e di istruire gli utenti interni su come mantenerlo aggiornato.

### Passaggio 2: identificare gli elementi da includere nella documentazione di [!DNL Marketo Engage] e [!DNL Changelogs]

Il formato varia da una piattaforma basata su cloud a un documento condiviso. Puoi progettare il formato che soddisfi le esigenze della tua organizzazione. [Di seguito è riportata una semplice documentazione e un modello di excel changelog](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) che descrive gli elementi importanti con cui è possibile iniziare. Tra questi:

* Documentazione
   * Nome modello programma
   * Canale
   * Data di creazione
   * Creato da
   * Scopo del programma
   * Stato
   * Collega al modello del programma
   * Nota
* Changelog
   * Nome modello programma
   * Data della modifica
   * Aggiornato da
   * Scopo dell’aggiornamento
   * Esperienza prima del cambiamento (includi collegamenti/schermate)
   * Esperienza dopo la modifica (includi collegamenti/schermate)
   * URL del programma

### Fase 3: Identificare e documentare lo stato attuale dei programmi operativi principali

Inizia identificando i principali programmi operativi con un impatto a livello di abbonamento. Alcuni esempi includono campagne di gestione dati, ciclo di vita dei lead, punteggio lead, sincronizzazione [!DNL CRM] e recapito messaggi.

Per ciascun programma operativo individuato, documentarne lo stato attuale. Ciò include dettagli sullo scopo del programma, sulla configurazione, sulle campagne intelligenti associate e sull’integrazione con altri strumenti (se applicabile).

### Passaggio 4: Applica manutenzione di [!DNL Changelog]

Il passaggio successivo consiste nel definire criteri di governance rigidi per l&#39;istanza [!DNL Marketo Engage] che richiede la manutenzione di &quot;[!DNL Changelog]&quot;. Questo criterio garantisce che tutti gli aggiornamenti apportati ai programmi operativi nell’istanza siano documentati in modo esauriente.

Informa il tuo team sull’importanza di questi documenti e su come accedervi e aggiornarli correttamente. Potrebbe essere utile assegnare responsabilità per la gestione del changelog, in modo che alcuni membri o amministratori del team dell’operazione di marketing designati registrino le modifiche in modo coerente e forniscano conclusioni.

### Passaggio 5: Centralizzazione della documentazione

Stabilire una posizione centrale o un repository per l&#39;archiviazione di tutta la documentazione relativa all&#39;istanza [!DNL Marketo Engage]. Potrebbe trattarsi di un&#39;unità condivisa, di una cartella dedicata o di un sistema basato su cloud.

### Passaggio 6: rivedere e aggiornare regolarmente

Pianifica revisioni regolari della documentazione per assicurarti che rimanga accurata e aggiornata. Può essere facilmente sottovalutato durante i periodi di grande affluenza. Imposta proattivamente i promemoria sul calendario per garantire che il team esegua regolarmente aggiornamenti per riflettere eventuali modifiche o ottimizzazioni nei programmi operativi.

## Quali sono le prossime novità?

Per iniziare, scarica questo [modello semplice](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

Segui i passaggi precedenti per sviluppare la guida alla governance e la documentazione. Durante il processo, tieni presenti queste regole generali:

**Aggiorna la documentazione esistente:**
È fondamentale mantenere aggiornata la documentazione. Se non è stata modificata negli ultimi 3 anni, conferma il tempo necessario per rivedere la documentazione durante l’audit dell’istanza.

**Condividi e tieni traccia di:**
Condividi la tua documentazione e [!DNL changelog] con i membri del gruppo pertinenti e istruiscili su come aggiornare questi record.

**Revisione periodica:** prepianificare il tempo necessario per esaminarle e gestirle nel corso dell&#39;anno in modo da includere eventuali nuove modifiche, ottimizzazioni o adeguamenti nel momento in cui si verificano.

La gestione di una documentazione completa e aggiornata per l’istanza di Marketo Engage consente di risparmiare tempo e lavoro a lungo termine e facilita un’efficace gestione delle istanze.

### Autori

**Nick Hajdin**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![Nick Hajdin](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**Amy Chiu**
*Responsabile marketing per l&#39;adozione e il mantenimento, Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
