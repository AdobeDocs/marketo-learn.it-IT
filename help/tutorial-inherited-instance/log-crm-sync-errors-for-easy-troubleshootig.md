---
title: Registra gli errori di sincronizzazione CRM per una facile risoluzione dei problemi
description: Scopri come utilizzare un registro di errori di sincronizzazione CRM per analizzare i problemi di sincronizzazione CRM e mantenerli in esecuzione senza problemi.
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Registra gli errori di sincronizzazione CRM per una facile risoluzione dei problemi

In qualità di amministratore di Marketo Engage, verificare se l&#39;istanza è sincronizzata con il CRM deve essere una parte chiave della [routine giornaliera](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}. Mentre la [sezione Notifiche](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html?lang=it){target="_blank"} (trovala nell&#39;angolo in alto a destra dell&#39;interfaccia di Marketo Engage) è il luogo in cui inizierai a trovare e analizzare i frequenti problemi di sincronizzazione, esiste un suggerimento pro che potrebbe aiutarti a gestire lo stato dell&#39;istanza in modo organizzato. Adobe Marketo Champion (2019-2022), Amy Goldfine consiglia agli utenti amministratori di mantenere un registro degli errori di sincronizzazione CRM per semplificare la risoluzione dei problemi.

![Schermata della scheda Errori di sincronizzazione](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## Perché tenere traccia degli errori di sincronizzazione CRM?

Registrando gli errori di sincronizzazione CRM, gli amministratori di Marketo Engage possono esaminare i problemi e le tendenze con gli amministratori di CRM per correggere la causa principale. Segui i passaggi seguenti per documentare i problemi di sincronizzazione CRM per la tua istanza.

## Come mantenere un registro degli errori di sincronizzazione CRM

Prima di iniziare, scaricare il modello di registro degli errori di sincronizzazione di [CRM](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx).

**Passaggio 1:** Vai alla *[!UICONTROL sezione Amministratore]* nel Marketo Engage. In *[!UICONTROL Integrazione]*, fare clic su *[!DNL Salesforce]*, *[!DNL Microsoft Dynamics]* o *[!DNL Veeva]*, a seconda di quale [!DNL CRM] si utilizza, quindi sulla scheda *[!UICONTROL Errori di sincronizzazione]*.

**Passaggio 2:** Puoi scegliere di [esportare i record di errori come file [!DNL CSV] tramite il pannello [!UICONTROL Filtro]](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html?lang=it#filter-sync-errors){target="_blank"}. Se hai solo poche ore, è consigliabile copiare e incollare direttamente dalla scheda *[!UICONTROL Errori di sincronizzazione]*.

**Passaggio 3:** Prendere nota della data in cui si è verificato l&#39;errore.

**Passaggio 4:** Immettere il numero di record persona interessati dall&#39;errore. (A volte il CRM genera un errore solo per una persona. A volte ci saranno molte persone con lo stesso errore contemporaneamente.)

**Passaggio 5:** Prendere nota dell&#39;indirizzo di posta elettronica di una persona interessata dall&#39;errore. In questo modo è facile fare riferimento e discutere gli errori con l’amministratore di CRM.

**Passaggio 6:** Incolla i collegamenti al record persona in [!DNL Marketo Engage] e al [!UICONTROL record Contatto/lead CRM] di tale persona.

**Passaggio 7:** Nell&#39;ultima colonna incollare il testo effettivo dell&#39;errore.

## Quali sono le prossime novità?

**Identificare i codici di errore:** Per comprendere i codici di errore, cercare le descrizioni nella documentazione per gli sviluppatori [Tabella dei codici di errore a livello di risposta](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} e trovare i passaggi successivi tipici per risolvere gli errori.

## Autori

**Amy Goldfine**\
Adobe Marketo Champion (2019-2022)
*Fondatore, MarketingOpsAdvice.com*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Responsabile dell&#39;adozione e del mantenimento all&#39;Adobe*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
