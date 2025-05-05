---
title: 'Marketo Video sull’API: come impostare il token di accesso in una variabile'
description: Scopri come configurare l’applicazione Postman e come sfruttare le variabili per salvare i dati nella variabile a scopo di riutilizzabilità.
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
source-git-commit: 3243c3047efa1bcb92581a58aafe17689ff945fd
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 24%

---

# Guida API: come impostare il token di accesso in una variabile

Scopri come configurare l’applicazione Postman e utilizzare le variabili per salvare i dati nella variabile per riutilizzarli. Scoprirai anche come effettuare la prima chiamata API REST di Marketo Engage per ottenere il token di accesso.

>[!PREREQUISITES]
>
>Prima di iniziare questo video, crea un nome utente Solo API con un ruolo AOI e crea un servizio Launchpad. Segui i passaggi descritti negli articoli seguenti:
>
>* [Crea un ruolo utente solo API](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [Crea un utente solo API](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [Crea un servizio personalizzato da utilizzare con API REST](https://experienceleague.adobe.com/it/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**Riferimenti utilizzati in questo video:**

* Endpoint di autenticazione Marketo: `{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* Script JS per acquisire access_token dal corpo della risposta (posizioni sotto la scheda Script: ):

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Documentazione per sviluppatori di Marketi Engage](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
