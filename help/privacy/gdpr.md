---
title: Adobe Advertising support for the General Data Protection Regulation
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
TQID: https://experienceleague.adobe.com/qR5H-xgBKdtWcMYfrdGdk1y5s9PEA0-hNGZADbR6TuM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1046
ht-degree: 0%

---

# Adobe Advertising support for the General Data Protection Regulation

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consult with your legal counsel for advice concerning the General Data Protection Regulation.

The General Data Protection Regulation (GDPR), a law in effect May 25, 2018, gives all individuals (data subjects) within the borders of the European Union (EU) control of their personal data and simplifies the regulatory environment for international business. This law applies to all businesses (data controllers) that offer goods or services to, monitor the behavior of, or collect personal data from individuals within the borders of the EU at the time their personal data is processed, regardless of the data controller&#39;s business location.

Adobe CX Enterprise acts as a data processor for any personal data it receives and stores on behalf of its customers. As a data controller, you determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] support your data subjects&#39; GDPR data access and deletion rights using the Adobe Experience Platform Privacy Service API and Privacy Service UI.

For more information about what GDPR means for your business, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitação de dados compatíveis com o Adobe Advertising

O Adobe Experience Platform permite que as empresas concluam as seguintes tarefas:

* Access a data subject&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for data subjects using a browser; or delete ID-level data stored within [!DNL DSP] for data subjects using apps on mobile devices.
* Verifique o status de uma ou de todas as solicitações existentes.

## Configuração necessária para enviar solicitações para o Adobe Advertising

To make requests to access and delete data for Adobe Advertising, you must:

1. Deploy a JavaScript library to retrieve and remove your data subject cookies. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe CX Enterprise.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da CX Enterprise não exigem a biblioteca da JavaScript, mas as solicitações para a Adobe Advertising exigem.

   You should deploy the library on the webpage from which your data subjects can submit access and delete requests, such as your company&#39;s privacy portal. The library helps you retrieve [!DNL Adobe] cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of access and delete requests via the Adobe Experience Platform Privacy Service API.

   When the data subject asks to delete personal data, the library also deletes the data subject&#39;s cookie from the data subject&#39;s browser.

   >[!NOTE]
   >
   >Deleting personal data is different than Opt-Out, which stops the targeting of an end user with audience segments. However, when a data subject asks to delete personal data from [!DNL Creative], [!DNL DSP], or [!DNL DCO], the library also sends a request to Adobe Advertising to opt out the data subject from segment targeting. For advertisers with [!DNL Search, Social, & Commerce], we recommend that you provide the data subjects a link to [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), which explains how to opt out of audience segment targeting.

1. Identify your CX Enterprise organization ID and make sure it&#39;s linked to your Adobe Advertising accounts.

   Uma ID de organização da CX Enterprise é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. A maioria dos clientes do CX Enterprise recebeu uma ID de organização. If your marketing team or internal [!DNL Adobe] system administrator doesn&#39;t know your organization ID, or isn&#39;t sure if it&#39;s been provisioned, then contact Adobe Customer Care at gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o namespace `imsOrgID`.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Adobe Advertising de sua empresa para confirmar se todas as contas da Adobe Advertising de sua organização — incluindo contas do [!DNL DSP] ou anunciantes, contas do [!DNL Search, Social, & Commerce] e contas do [!DNL Creative] ou do [!DNL DCO] — estão vinculadas à sua ID da organização da CX Enterprise.

1. Use either the [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (for automated requests) or the [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR) (for ad-hoc requests) to submit access and delete requests to Adobe Advertising on behalf of the data subjects, and to check the status of existing requests.

   For advertisers who have a mobile app to interact with data subjects and launch campaigns with DSP, you must download the Privacy-ready Mobile SDKs for CX Enterprise. The Mobile SDKs allow data controllers to set opt-out status flags, retrieve the data subject&#39;s device ID (namespace ID: `deviceID`), and submit requests to the Privacy Service API. Seu aplicativo móvel exigirá um SDK versão 4.15.0 ou superior.

   When you submit a data subject&#39;s access request, the Privacy Service API returns a data subject&#39;s information based on the specified cookie or device ID, which you then must return to the data subject.

   When you submit a data subject&#39;s delete request, the cookie ID or device ID and all cost, click, and revenue data associated with the cookie are deleted from the server.

   >[!NOTE]
   >
   >If your company has multiple CX Enterprise organization IDs, then you must send separate API requests for each. No entanto, você pode fazer uma solicitação de API para várias subsoluções da Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), com uma conta por subsolução.

All steps are necessary for Adobe Advertising. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the necessary items, see &quot;[Privacy Service overview](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).&quot;

## Valores de campo obrigatórios em solicitações JSON do Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*sua ID da organização da CX Enterprise*>

`"users":`

* `"key":` &lt;*geralmente o nome do titular dos dados*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica o espaço de cookies [!DNL adcloud])

   * `"value":` &lt;*o valor real da ID do cookie do titular dos dados conforme recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o produto [!DNL Adobe] que se aplica à solicitação)

* `"regulation": **gdpr**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de solicitação enviada pelo titular dos dados usando uma ID de usuário do Adobe Advertising recuperada de `AdobePrivacy.js`

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
```

## Campos de dados retornados para solicitações de acesso

Este é um exemplo de uma resposta de acesso para o Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
