---
title: 'Tutorial: come attivare una campagna avanzata in Marketo Engage utilizzando l’API REST e i token'
description: Scopri come attivare una campagna avanzata in Marketo Engage utilizzando l’API REST e personalizzare l’e-mail utilizzando I miei token.
feature: REST API
role: Admin, Developer
level: Experienced
source-git-commit: dcfffa299cbcfef489f5b618fae29f745b878d26
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Come attivare una campagna avanzata in Marketo Engage utilizzando l’API REST e i token

Questo tutorial illustra come attivare una campagna avanzata in Marketo Engage utilizzando l’API REST e personalizzare l’e-mail utilizzando I miei token. Questo caso d’uso è ideale per le notifiche attivate dai clienti, ad esempio i promemoria dei webinar, i passaggi di onboarding o i follow-up successivi all’acquisto.

## Caso di utilizzo {#use-case}

Una persona si registra per un webinar tramite una piattaforma esterna (ad esempio, app personalizzata, Pendo, Eventbrite). Si desidera eseguire automaticamente le operazioni seguenti:

* Attivare un messaggio e-mail di promemoria da Marketo Engage
* Personalizzalo con:
   * Nome della persona
   * Titolo webinar
   * Un collegamento di unione univoco

Questa operazione può essere eseguita utilizzando l’API REST e I miei token.

## Passaggio 1: creare la campagna avanzata {#step-one}

1. Vai a **Attività di marketing** e crea nella cartella [Programmi](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/creating-programs/understanding-programs){target="_blank"} una nuova [Campagna avanzata](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/understanding-smart-campaigns){target="_blank"} denominata `Send Webinar Reminder`.

1. Nella scheda **Elenco avanzato**, [aggiungi un trigger](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/creating-a-smart-campaign/define-smart-list-for-smart-campaign-trigger){target="_blank"} per consentire la chiamata della campagna tramite l&#39;API:

   * Seleziona **La campagna è richiesta** come attivatore
   * Imposta **Source** su `Web Service API`

![Configurazione trigger elenco avanzato](assets/trigger-smart-campaign-rest-api-1.png)

## Passaggio 2: definire il contenuto dell’e-mail {#step-two}

Crea o modifica una [risorsa e-mail](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/assets/emails){target="_blank"} che fa riferimento sia a Persona che a [I miei token](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/programs/tokens/managing-my-tokens){target="_blank"}.

>[!NOTE]
>
>Assicurati di inserire i token direttamente nel contenuto dell’e-mail, come mostrato di seguito.

```html
Hi {{lead.First Name:default=Customer}}

You're registered for **{{my.WebinarTitle}}**.

Join here: {{my.JoinLink}}
```

>[!IMPORTANT]
>
>Se utilizzi un token per inserire dinamicamente un URL immagine (ad esempio, `{{my.WebinarImage}}`), devi racchiudere il token in un tag immagine HTML:
>
> ```html
> <img src="{{my.WebinarImage}}" alt="Webinar banner" />
> ```
>
>Marketo Enagage **non** eseguirà il rendering dell&#39;immagine a meno che il token non venga inserito all&#39;interno di un tag immagine valido.

![L&#39;editor di posta elettronica mostra l&#39;utilizzo del token](assets/trigger-smart-campaign-rest-api-2.png)

## Passaggio 3: aggiungere token al programma {#step-three}

Per trasmettere i valori in modo dinamico tramite API, i token devono già esistere in Marketo Engage. Devi crearli nella scheda **I miei token** del programma.

1. Vai alla scheda **I miei token** del programma principale.

2. Trascina un **Token di testo** dal pannello a destra per ogni valore dinamico.

* `{{my.WebinarTitle}}` - Token di testo
* `{{my.JoinLink}}` - Token di testo
* `{{my.WebinarImage}}` - Token di testo (verrà utilizzato come `src` in un tag `<img>`)

![Scheda I miei token nella campagna](assets/trigger-smart-campaign-rest-api-3.png)

## Passaggio 4: impostare le regole di qualificazione della campagna e attivare la campagna {#step-four}

1. Configura le [regole di qualificazione](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-campaigns/using-smart-campaigns/edit-qualification-rules-in-a-smart-campaign){target="_blank"} per controllare la frequenza con cui una persona può eseguire Smart Campaign.

1. Una volta configurata, fai clic su **Attiva** per abilitare Smart Campaign a ricevere richieste attivate da API.

![Regola di qualificazione per Smart Campaign](assets/trigger-smart-campaign-rest-api-4.png)

## Passaggio 5: attivare la campagna tramite API REST {#step-five}

### Trovare l’ID campagna {#find-the-campaign-id}

Per attivare una campagna avanzata tramite API, è necessario l&#39;**ID campagna**:

1. Trova e seleziona la campagna avanzata da attivare.

1. Osserva l’URL nel browser. Si presenterà così: `https://app-XXX.marketo.com/#/classic/SC`**1234**`A1ZN38`.

1. Le 4 cifre dopo `SC` sono l&#39;ID della tua campagna; nell&#39;esempio precedente l&#39;ID della campagna avanzata è &#39;1234&#39;

Utilizza il seguente endpoint:

```
POST /rest/v1/campaigns/{campaignId}/trigger.json
```

Esempio:

```
POST /rest/v1/campaigns/1234/trigger.json
```

### Esempio di corpo della richiesta {#example-request-body}

```json
{
  "input": {
    "leads": [
      {
        "id": 1002200
      }
    ],
    "tokens": [
      {
        "name": "{{my.WebinarTitle}}",
        "value": "Scaling Customer Engagement in 2025"
      },
      {
        "name": "{{my.JoinLink}}",
        "value": "https://webinars.company.com/join/abc123"
      },
      {
        "name": "{{my.WebinarImage}}",
        "value": "https://experienceleague.adobe.com/en/docs/marketo-learn/tutorials/events/media_1c6f338a518ada11550084c8ab3a6bbf554ff6eac.jpeg"
      }
    ]
  }
}
```

>[!IMPORTANT]
>
>Sostituisci `1002200` nell&#39;esempio di corpo di cui sopra con l&#39;ID persona corretto dalla tua istanza di Marketo Engage.

## Authorization {#authorization}

Tutte le richieste API REST di Marketo richiedono un token di accesso OAuth 2.0.

Per recuperare il token di accesso, utilizza il seguente endpoint:

```
GET /identity/oauth/token?grant_type=client_credentials&client_id=XXX&client_secret=YYY
```

Una volta ricevuto il token di accesso, includilo come _parametro query_ in tutte le richieste API:

```
Authorization: Bearer YOUR_ACCESS_TOKEN
```

## Best practice {#best-practices}

* Aggiungi valori di fallback/predefiniti ai token per il test e il controllo qualità
* Usa `{{lead.token}}` per i campi persona e `{{my.token}}` per i valori dinamici con ambito campagna
* Marketo Engage supporta fino a 100 persone per richiesta
* Le persone devono soddisfare i criteri dell’elenco avanzato, altrimenti vengono ignorate automaticamente

## Riepilogo {#summary}

Con questo approccio, puoi personalizzare le comunicazioni utilizzando campagne intelligenti attivate da piattaforme esterne tramite API. È utile per scenari come le conferme di registrazione ai webinar, le e-mail di onboarding e le notifiche transazionali, il tutto mentre si inseriscono dati in tempo reale utilizzando I miei token.
