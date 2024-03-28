---
title: 'Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao acesso e exclusão de dados do consumidor'
description: Saiba mais sobre os tipos de solicitação de dados compatíveis, a configuração necessária e os valores de campo, além de exemplos de solicitações de acesso à API usando IDs de produto herdadas e campos de dados retornados.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 2e2d95ab2a6add695c3852a06e256b6db980779d
workflow-type: tm+mt
source-wordcount: '1042'
ht-degree: 0%

---

# Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao acesso e exclusão de dados do consumidor

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter recomendações sobre a California Consumer Privacy Act.

A California Consumer Privacy Act (CCPA) é a nova lei de privacidade da Califórnia, que entrou em vigor em 1º de janeiro de 2020. A CCPA fornece aos residentes da Califórnia novos direitos sobre suas informações pessoais e impõe responsabilidades de proteção de dados a determinadas entidades que realizam negócios na Califórnia. A CCPA dá aos consumidores o direito de acessar e apagar suas informações pessoais, bem como o direito de recusar certas atividades qualificadas como &quot;venda&quot; de informações pessoais a terceiros.

Como empresa, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Como seu provedor de serviços, o Adobe Advertising fornece suporte para que sua empresa cumpra as obrigações da CCPA aplicáveis ao uso de produtos e serviços do Adobe Advertising, incluindo o gerenciamento de solicitações para acessar e excluir informações pessoais e o gerenciamento de solicitações para recusar a venda de informações pessoais.

Este documento descreve como [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); e [!DNL Advertising DCO] — como provedores de serviços — oferecem suporte aos direitos dos consumidores de acessar e excluir informações pessoais usando o Adobe [!DNL Experience Platform Privacy Service API] e [!DNL Privacy Service UI].

Para obter informações sobre como a Advertising DSP apoia o direito do consumidor de recusar a venda de informações pessoais, consulte [Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento da participação do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Para obter mais informações sobre os serviços de privacidade do Adobe para CCPA, consulte o [Centro de privacidade do Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipos de solicitação de dados suportados para o Adobe Advertising

O Adobe Experience Platform permite que as empresas concluam as seguintes tarefas:

* Acesse dados de nível de cookie do consumidor ou dados de nível de ID do dispositivo (para anúncios em aplicativos móveis) no [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]ou [!DNL DCO].
* Excluir dados em nível de cookie armazenados no [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]ou [!DNL DCO] para consumidores que usam um navegador ou excluem dados de nível de ID armazenados no [!DNL DSP] para consumidores que usam aplicativos em dispositivos móveis.
* Verifique o status de uma ou de todas as solicitações existentes.

## Configuração necessária para enviar solicitações para o Adobe Advertising

Para fazer solicitações de acesso e exclusão de informações pessoais do consumidor do Adobe Advertising, é necessário:

1. Implante uma biblioteca do JavaScript para recuperar e remover os cookies do cliente. A mesma biblioteca, `AdobePrivacy.js`, é usado para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções de Experience Cloud não exigem a biblioteca de JavaScript do, mas as solicitações para o Adobe Advertising exigem.

   Você deve implantar a biblioteca na página da Web a partir da qual seus clientes podem enviar solicitações de acesso e exclusão, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies de Adobe (ID do namespace: `gsurferID`) para que você possa enviar essas identidades como parte das solicitações de acesso e exclusão por meio do [!DNL Adobe Experience Platform Privacy Service API].

   Quando o cliente solicita a exclusão de dados pessoais, a biblioteca também exclui o cookie do cliente do navegador do cliente.

   >[!NOTE]
   >
   >A exclusão de dados pessoais é diferente da recusa, o que interrompe o direcionamento de um usuário final com segmentos de público-alvo. No entanto, quando um consumidor solicita a exclusão de dados [!DNL Creative], [!DNL DSP]ou [!DNL DCO], a biblioteca também envia uma solicitação ao Adobe Advertising para recusar o cliente do direcionamento de segmentos. Para anunciantes com [!DNL Search, Social, & Commerce], recomendamos que você forneça aos clientes um link para [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), que explica como recusar o direcionamento de segmentos de público-alvo.

1. Identifique a ID da organização do Experience Cloud e verifique se ela está vinculada às suas contas do Adobe Advertising.

   Uma ID de organização Experience Cloud é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. Uma ID de organização foi atribuída à maioria dos clientes do Experience Cloud. Se sua equipe de marketing ou equipe interna [!DNL Adobe] O administrador do sistema não sabe sua ID da organização ou não tem certeza se ela foi provisionada, então entre em contato com a equipe de conta do Adobe. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Adobe Advertising da empresa para confirmar se todas as contas Adobe Advertising da organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search, Social, & Commerce] contas e [!DNL Creative] ou [!DNL DCO] contas do — são vinculadas à sua ID da organização Experience Cloud.

1. Use o [API do Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitações automatizadas) ou o [IU DO PRIVACY SERVICE](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR) (para solicitações ad-hoc) enviar solicitações para acessar e excluir informações pessoais ao Adobe Advertising em nome dos consumidores e verificar o status das solicitações existentes.

   Para anunciantes que têm um aplicativo móvel para interagir com clientes e iniciar campanhas com [!DNL DSP], será necessário baixar os SDKs móveis prontos para privacidade para o Experience Cloud. Os SDKs móveis permitem que as empresas definam sinalizadores de status de recusa e recuperem a ID do dispositivo do consumidor (ID de namespace: `deviceID`) e enviar solicitações à API Privacy Service. Seu aplicativo móvel exigirá um SDK versão 4.15.0 ou superior.

   Ao enviar uma solicitação de acesso do consumidor, a API Privacy Service retorna as informações do consumidor com base no cookie ou ID do dispositivo especificado, que você deve retornar ao consumidor.

   Ao enviar uma solicitação de exclusão do consumidor, a ID do cookie ou a ID do dispositivo e todos os dados de custo, clique e receita associados ao cookie são excluídos do servidor.

   >[!NOTE]
   >
   >Se sua empresa tiver várias IDs de organização de Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para receber suporte do Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando o Adobe Experience Platform Privacy Service e onde encontrar os itens necessários, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valores de campo obrigatórios em solicitações JSON do Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*sua ID da organização Experience Cloud*>

&quot;users&quot;:

* `"key":` &lt;*geralmente, o nome do cliente*>

* `"action":` ou `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica a [!DNL adCloud] espaço do cookie)

   * `"value":` &lt;*o valor real da ID do cookie do cliente conforme recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o [!DNL Adobe] produto que se aplica à solicitação)

* `"regulation": **ccpa**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de solicitação enviada por um consumidor usando uma ID de usuário do Adobe Advertising recuperada de AdobePrivacy.js

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
    "regulation":"ccpa"
}
```

## Campos de dados retornados para solicitações de acesso

Veja a seguir um exemplo de uma resposta de acesso a informações pessoais para o Adobe Advertising.

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
