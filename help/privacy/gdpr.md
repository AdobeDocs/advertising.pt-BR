---
title: Suporte de publicidade Adobe para o Regulamento Geral sobre a Proteção de Dados
description: Saiba mais sobre os tipos de solicitação de dados compatíveis, a configuração necessária e os valores de campo, além de exemplos de solicitações de acesso à API usando IDs de produto herdadas e campos de dados retornados
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: df19f47971e97727c85bce99ce80b677fbdb1a49
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 0%

---

# Suporte de Adobe Advertising para o Regulamento Geral sobre a Proteção de Dados

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter recomendações sobre o Regulamento Geral sobre a Proteção de Dados.

O Regulamento Geral sobre a Proteção de Dados (GDPR), uma lei em vigor desde 25 de maio de 2018 concede a todos os indivíduos (titulares de dados) dentro das fronteiras da União Europeia (UE) o controle de seus dados pessoais e simplifica o ambiente regulamentar para as empresas internacionais. Esta lei se aplica a todas as empresas (controladores de dados) que oferecem bens ou serviços para monitorar o comportamento ou coletar dados pessoais de indivíduos dentro das fronteiras da UE no momento em que seus dados pessoais são processados, independentemente da localização comercial do controlador de dados.

A Adobe Experience Cloud atua como um processador de dados para todos os dados pessoais que recebe e armazena em nome de seus clientes. Como controlador de dados, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Este documento descreve como [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); e [!DNL Advertising DCO] Ofereça suporte aos direitos de acesso e exclusão de dados do GDPR de seus titulares de dados usando a API do Adobe Experience Platform Privacy Service e a interface do Privacy Service.

Para obter mais informações sobre o que o GDPR significa para sua empresa, consulte [GDPR e sua empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitação de dados suportados para publicidade de Adobe

O Adobe Experience Platform permite que as empresas concluam as seguintes tarefas:

* Acesse os dados de nível de cookie de um titular de dados ou os dados de nível de ID do dispositivo (para anúncios em aplicativos móveis) no [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]ou [!DNL DCO].
* Excluir dados em nível de cookie armazenados no [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]ou [!DNL DCO] para titulares de dados usando um navegador ou excluir dados de nível de ID armazenados no [!DNL DSP] para titulares de dados que usam aplicativos em dispositivos móveis.
* Verifique o status de uma ou de todas as solicitações existentes.

## Configuração necessária para enviar solicitações de publicidade de Adobe

Para fazer solicitações de acesso e exclusão de dados para o Adobe Advertising, é necessário:

1. Implante uma biblioteca JavaScript para recuperar e remover os cookies do titular dos dados. A mesma biblioteca, `AdobePrivacy.js`, é usado para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Adobe Experience Cloud não exigem a biblioteca JavaScript, mas as solicitações para a Adobe Advertising exigem.

   Você deve implantar a biblioteca na página da Web a partir da qual os titulares de dados podem enviar solicitações de acesso e exclusão, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies de Adobe (ID do namespace: `gsurferID`) para poder enviar essas identidades como parte das solicitações de acesso e exclusão por meio da API do Adobe Experience Platform Privacy Service.

   Quando o titular dos dados solicita a exclusão de dados pessoais, a biblioteca também exclui o cookie do titular dos dados do navegador do titular dos dados.

   >[!NOTE]
   >
   >A exclusão de dados pessoais é diferente da opção de não participação, que interrompe o direcionamento de um usuário final com segmentos de público-alvo. No entanto, quando um titular de dados solicita a [!DNL Creative], [!DNL DSP]ou [!DNL DCO], a biblioteca também envia uma solicitação ao Adobe Advertising para recusar o titular dos dados no direcionamento de segmentos. Para anunciantes com [!DNL Search, Social, & Commerce], recomendamos que você forneça aos titulares dos dados um link para [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), que explica como recusar o direcionamento de segmentos de público-alvo.

1. Identifique a ID da organização Experience Cloud e verifique se ela está vinculada às suas contas Adobe Advertising.

   Uma ID de organização Experience Cloud é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. Uma ID de organização foi atribuída à maioria dos clientes do Experience Cloud. Se a equipe de marketing ou o administrador interno do sistema Adobe não souber a ID da organização ou não tiver certeza se ela foi provisionada, entre em contato com o Atendimento ao cliente da Adobe em gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Adobe Advertising da sua empresa para confirmar se todas as contas da Adobe Advertising da sua organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search, Social, & Commerce] contas e [!DNL Creative] ou [!DNL DCO] contas do — são vinculadas à sua ID da organização Experience Cloud.

1. Use o [API do Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitações automatizadas) ou o [IU DO PRIVACY SERVICE](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR) (para solicitações ad-hoc) enviar solicitações de acesso e exclusão ao Adobe Advertising em nome dos titulares de dados e verificar o status das solicitações existentes.

   Para anunciantes que têm um aplicativo móvel para interagir com titulares de dados e iniciar campanhas com DSP, será necessário baixar os SDKs móveis prontos para privacidade para o Experience Cloud. Os SDKs móveis permitem que os controladores de dados definam sinalizadores de status de recusa, recuperem a ID de dispositivo do titular dos dados (ID de namespace: deviceID) e enviem solicitações para a API Privacy Service. Seu aplicativo móvel exigirá um SDK versão 4.15.0 ou superior.

   Ao enviar uma solicitação de acesso do titular de dados, a API do Privacy Service retorna as informações de um titular de dados com base no cookie ou na ID do dispositivo especificada, que você deve retornar ao titular dos dados.

   Ao enviar uma solicitação de exclusão de um titular de dados, a ID do cookie ou a ID do dispositivo e todos os dados de custo, clique e receita associados ao cookie são excluídos do servidor.

   >[!NOTE]
   >
   Se sua empresa tiver várias IDs de organização de Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias sub-soluções da Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para o Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando o Adobe Experience Platform Privacy Service e onde encontrar os itens necessários, consulte [Privacidade e o RGPD](https://developer.adobe.com/client-sdks/documentation/privacy-and-gdpr/).

## Valores de campo obrigatórios em solicitações JSON do Adobe Advertising

&quot;&quot;company context&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*seu valor de ID de organização IMS*>

`"users":`

* `"key":` &lt;*geralmente, o nome do titular dos dados*>

* `"action":` ou `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica a [!DNL adcloud] espaço do cookie)

   * `"value":` &lt;*o valor real da ID do cookie do titular dos dados conforme recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o produto Adobe que se aplica à solicitação)

* `"regulation": **gdpr**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de solicitação enviada por titular de dados usando uma ID de usuário Adobe Advertising recuperada de `AdobePrivacy.js`

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
}
```

## Campos de dados retornados para solicitações de acesso

Veja a seguir um exemplo de uma resposta de acesso para o Adobe Advertising.

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
