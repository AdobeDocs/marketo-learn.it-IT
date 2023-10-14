---
title: Registra gli errori di sincronizzazione CRM per una facile risoluzione dei problemi
description: Scopri come utilizzare un registro di errori di sincronizzazione CRM per analizzare i problemi di sincronizzazione CRM e mantenerli in esecuzione senza problemi.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-12T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: true
source-git-commit: e7fe8da128a1c46620484d9b92823ba51791a671
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---


# Registra gli errori di sincronizzazione CRM per una facile risoluzione dei problemi

In qualità di amministratore di Marketo Engage, verificare se l’istanza è sincronizzata con il tuo sistema CRM deve essere una parte chiave del tuo [routine giornaliera](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. While the [Notifications section](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} (puoi trovarlo nell’angolo in alto a destra dell’interfaccia del Marketo Engage) è il punto in cui inizierai a trovare e analizzare i frequenti problemi di sincronizzazione. esiste un suggerimento pro che potrebbe aiutarti a gestire lo stato dell’istanza in modo organizzato.  Adobe Marketo Champion(2022), Amy Goldfine consiglia agli utenti amministratori di tenere un registro degli errori di sincronizzazione CRM per semplificare la risoluzione dei problemi.

![Schermata della scheda Errori di sincronizzazione](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Perché tenere traccia degli errori di sincronizzazione CRM?

Registrando gli errori di sincronizzazione CRM, gli amministratori di Marketo Engage possono esaminare i problemi e le tendenze con gli amministratori di CRM per correggere la causa principale. Segui i passaggi seguenti per documentare i problemi di sincronizzazione CRM per la tua istanza.

## Come mantenere un registro degli errori di sincronizzazione CRM

Prima di iniziare, scarica [Modello registro errori di sincronizzazione CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Passaggio 1:** Vai a *[!UICONTROL Amministratore] sezione* nel Marketo Engage. Sotto *[!UICONTROL Integrazione]*, fai clic su *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]*, o *[!DNL Veeva]*, a seconda di quale [!DNL CRM] utilizzi, quindi il *[!UICONTROL Errori di sincronizzazione]* scheda.

**Passaggio 2:** Puoi scegliere di [esporta i record di errori come [!DNL CSV] file tramite [!UICONTROL Filtro] pannello](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}. Se hai solo poche ore, copia e incolla direttamente dal *[!UICONTROL Errori di sincronizzazione]* La scheda sarebbe la strada da percorrere.

**Passaggio 3:** Prendi nota della data in cui si è verificato l’errore.

**Passaggio 4:** Immettere il numero di record persona interessati dall&#39;errore. (A volte il CRM genera un errore solo per una persona. A volte ci saranno molte persone con lo stesso errore contemporaneamente.)

**Passaggio 5:** Prendi nota dell’indirizzo e-mail di una persona interessata dall’errore. In questo modo è facile fare riferimento e discutere gli errori con l’amministratore di CRM.

**Passaggio 6:** Incolla i collegamenti al record persona in [!DNL Marketo Engage] e [!UICONTROL Contatto/lead CRM] della persona.

**Passaggio 7:** Nell’ultima colonna, incolla il testo effettivo dell’errore.

## Quali sono le prossime novità?

**Identificare i codici di errore:** Per comprendere i codici di errore, consulta le descrizioni nella documentazione per gli sviluppatori. [Tabella Codici di errore a livello di risposta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} e trovare i passaggi successivi tipici per risolvere gli errori.

## Autori

**Amy Goldfine**\
Adobe Marketo Champion (2022)
*Senior Manager, Operazioni di marketing, Iterable*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Responsabile dell’adozione e del mantenimento all’Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}

