---
title: Suporte do Adobe Advertising para o Regulamento Geral sobre a Proteção de Dados
description: Saiba mais sobre os tipos de solicitação de dados compatíveis, a configuração necessária e os valores de campo, além de exemplos de solicitações de acesso à API usando IDs de produto herdadas e campos de dados retornados
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Suporte do Adobe Advertising para o Regulamento Geral sobre a Proteção de Dados

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; e Adobe Advertising DCO*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter recomendações sobre o Regulamento Geral sobre a Proteção de Dados.

O Regulamento Geral sobre a Proteção de Dados (GDPR), uma lei em vigor desde 25 de maio de 2018 concede a todos os indivíduos (titulares de dados) dentro das fronteiras da União Europeia (UE) o controle de seus dados pessoais e simplifica o ambiente regulamentar para as empresas internacionais. Esta lei se aplica a todas as empresas (controladores de dados) que oferecem bens ou serviços para monitorar o comportamento ou coletar dados pessoais de indivíduos dentro das fronteiras da UE no momento em que seus dados pessoais são processados, independentemente da localização comercial do controlador de dados.

A Adobe Experience Cloud atua como um processador de dados para todos os dados pessoais que recebe e armazena em nome de seus clientes. Como controlador de dados, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Este documento descreve como o [!DNL Advertising Search, Social, & Commerce], o Advertising Creative, o Advertising DSP (Demand Side Platform) e o [!DNL Advertising DCO] oferecem suporte aos direitos de acesso e exclusão de dados do GDPR de seus titulares de dados usando a API do Adobe Experience Platform Privacy Service e a interface do usuário do Privacy Service.

Para obter mais informações sobre o que o GDPR significa para sua empresa, consulte [GDPR e sua empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitação de dados compatíveis com o Adobe Advertising

O Adobe Experience Platform permite que as empresas concluam as seguintes tarefas:

* Acesse os dados no nível de cookie de um titular de dados ou os dados no nível de ID do dispositivo (para anúncios em aplicativos móveis) no [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO].
* Exclua dados a nível de cookie armazenados em [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] ou [!DNL DCO] para titulares de dados usando um navegador; ou exclua dados a nível de ID armazenados em [!DNL DSP] para titulares de dados usando aplicativos em dispositivos móveis.
* Verifique o status de uma ou de todas as solicitações existentes.

## Configuração necessária para enviar solicitações para o Adobe Advertising

Para fazer solicitações de acesso e exclusão de dados do Adobe Advertising, você deve:

1. Implante uma biblioteca do JavaScript para recuperar e remover os cookies do titular dos dados. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Experience Cloud não exigem a biblioteca da JavaScript, mas as solicitações para a Adobe Advertising exigem.

   Você deve implantar a biblioteca na página da Web a partir da qual seus titulares de dados podem enviar solicitações de acesso e exclusão, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar os cookies [!DNL Adobe] (ID do namespace: `gsurferID`) para que você possa enviar essas identidades como parte das solicitações de acesso e exclusão por meio da API do Adobe Experience Platform Privacy Service.

   Quando o titular dos dados solicita a exclusão de dados pessoais, a biblioteca também exclui o cookie do titular dos dados do navegador do titular dos dados.

   >[!NOTE]
   >
   >A exclusão de dados pessoais é diferente da opção de não participação, que interrompe o direcionamento de um usuário final com segmentos de público-alvo. No entanto, quando um titular de dados solicita a exclusão de dados pessoais de [!DNL Creative], [!DNL DSP] ou [!DNL DCO], a biblioteca também envia uma solicitação à Adobe Advertising para recusar a exclusão do titular de dados do direcionamento de segmento. Para anunciantes com [!DNL Search, Social, & Commerce], recomendamos que você forneça aos titulares de dados um link para [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), que explica como recusar o direcionamento de segmentos de público-alvo.

1. Identifique a ID da organização da Experience Cloud e verifique se ela está vinculada às suas contas da Adobe Advertising.

   Uma ID de organização da Experience Cloud é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. A maioria dos clientes do Experience Cloud recebeu uma ID de organização. Se a sua equipe de marketing ou o administrador interno do sistema [!DNL Adobe] não souber a ID da organização ou não tiver certeza se ela foi provisionada, entre em contato com o Atendimento ao cliente da Adobe em gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o namespace `imsOrgID`.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Adobe Advertising de sua empresa para confirmar se todas as contas da Adobe Advertising de sua organização — incluindo contas do [!DNL DSP] ou anunciantes, contas do [!DNL Search, Social, & Commerce] e contas do [!DNL Creative] ou do [!DNL DCO] — estão vinculadas à sua ID da organização da Experience Cloud.

1. Use a [API do Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitações automatizadas) ou a [Interface do usuário do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=pt-BR) (para solicitações ad-hoc) para enviar solicitações de acesso e de exclusão ao Adobe Advertising em nome dos titulares de dados e para verificar o status das solicitações existentes.

   Para anunciantes que têm um aplicativo móvel para interagir com titulares de dados e iniciar campanhas com o DSP, você deve baixar os SDKs móveis prontos para privacidade para o Experience Cloud. Os SDKs móveis permitem que controladores de dados definam sinalizadores de status de recusa, recuperem a ID de dispositivo do titular dos dados (ID de namespace: `deviceID`) e enviem solicitações para a API do Privacy Service. Seu aplicativo móvel exigirá um SDK versão 4.15.0 ou superior.

   Ao enviar uma solicitação de acesso do titular de dados, a API do Privacy Service retorna as informações de um titular de dados com base no cookie ou na ID do dispositivo especificada, que você deve retornar ao titular dos dados.

   Ao enviar uma solicitação de exclusão de um titular de dados, a ID do cookie ou a ID do dispositivo e todos os dados de custo, clique e receita associados ao cookie são excluídos do servidor.

   >[!NOTE]
   >
   >Se sua empresa tiver várias IDs de organização da Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções da Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), com uma conta por subsolução.

Todas as etapas são necessárias para o Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando a Adobe Experience Platform Privacy Service e onde encontrar os itens necessários, consulte &quot;[visão geral do Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).&quot;

## Valores de campo obrigatórios em solicitações JSON do Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*ID da organização da Experience Cloud*>

`"users":`

* `"key":` &lt;*normalmente é o nome do titular dos dados*>

* `"action":` `**access**` ou `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica o espaço de cookies [!DNL adcloud])

   * `"value":` &lt;*o valor real da ID do cookie do titular dos dados foi recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que é o produto [!DNL Adobe] que se aplica à solicitação)

* `"regulation": **gdpr**` (que é o regulamento de privacidade que se aplica à solicitação)

## Exemplo de Solicitação Enviada por Titular de Dados Usando uma ID de Usuário do Adobe Advertising Recuperada de `AdobePrivacy.js`

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
