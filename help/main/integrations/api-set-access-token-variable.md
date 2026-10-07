---
title: 'Marketo Video sull’API: come impostare il token di accesso in una variabile'
description: Scopri come configurare l’applicazione Postman e come sfruttare le variabili per salvare i dati nella variabile a scopo di riutilizzabilità.
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00.000Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: dca84292-69e9-4116-a575-667d31fa060d
    internal-label: APIs
subfeature_v2:
  - id: cf1396d8-ab85-4e93-b35d-d9b573024abf
    internal-label: REST APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 4768ecb20d4d9c70452ae084256928261f3a80eb
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 27%
---
# Guida API - Impostare il token di accesso in una variabile

Scopri come configurare l’applicazione Postman e utilizzare le variabili per salvare i dati nella variabile per riutilizzarli. Scopri anche come effettuare la prima chiamata API REST di Marketo Engage per ottenere il token di accesso.

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

* [Documentazione per sviluppatori Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3453991/?captions=ita&learn=on)
