---
title: 'Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento de venda do consumidor'
description: Saiba mais sobre o suporte para capturar solicitações de cancelamento de venda do consumidor.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento de venda do consumidor

*Para Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter recomendações sobre a California Consumer Privacy Act.

A California Consumer Privacy Act (CCPA) é a nova lei de privacidade da Califórnia, que entrou em vigor em 1º de janeiro de 2020. A CCPA fornece aos residentes da Califórnia novos direitos sobre suas informações pessoais e impõe responsabilidades de proteção de dados a determinadas entidades que realizam negócios na Califórnia. A CCPA dá aos consumidores o direito de acessar e apagar seus dados, bem como o direito de recusar certas atividades qualificadas como &quot;venda&quot; de informações pessoais a terceiros.

Como empresa, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Como seu provedor de serviços, o Adobe Advertising fornece suporte para que sua empresa cumpra as obrigações da CCPA aplicáveis ao uso de produtos e serviços Adobe Advertising, incluindo o gerenciamento de solicitações do cliente para acessar e excluir informações pessoais e o gerenciamento de solicitações do cliente para recusar a venda de informações pessoais.

Este documento descreve como o Adobe Advertising Demand Side Platform (DSP), como provedor de serviços, apoia o direito do consumidor de recusar a &quot;venda&quot; de &quot;informações pessoais&quot;, já que cada termo é definido pela CCPA. Ele inclui informações sobre como comunicar solicitações de recusa de venda ao Adobe Advertising e como recuperar relatórios de solicitações de recusa de venda de sua organização.

Para obter informações sobre como [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; e [!DNL Advertising DCO] suporte aos direitos de acesso e exclusão de informações pessoais dos consumidores, consulte [Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao acesso e exclusão de dados do consumidor](/help/privacy/ccpa/ccpa-access-delete.md).

Para obter mais informações sobre os serviços de privacidade do Adobe para CCPA, consulte o [Centro de privacidade do Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicando solicitações de cancelamento de venda do consumidor ao Adobe Advertising

Você pode comunicar solicitações de cancelamento de venda do cliente usando:

* um segmento de cancelamento de venda do CCPA criado na Advertising DSP
* a API do Adobe Experience Platform Privacy Service

### Método 1: comunicar solicitações de cancelamento de venda do CCPA usando um [!UICONTROL CCPA Opt-Out-of-Sale] Segmento no DSP publicitário

>[!NOTE]
>
>Os usuários permanecem em segmentos de cancelamento de venda do CCPA indefinidamente.

1. Faça logon na conta do anunciante em Advertising DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Crie um segmento de cancelamento de venda do CCPA e implemente o pixel do segmento para capturar as solicitações de cancelamento](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Método 2: comunicar solicitações de cancelamento de venda do CCPA usando a API do Adobe Experience Platform Privacy Service

*Somente anunciantes com uma ID de organização da Adobe Experience Cloud atribuída*

1. Implante uma biblioteca do JavaScript para recuperar os cookies do cliente. A mesma biblioteca, `AdobePrivacy.js`, é usado para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Adobe Experience Cloud não exigem a biblioteca JavaScript do, mas as solicitações para o Adobe Advertising exigem.

   Você deve implantar a biblioteca na página da Web a partir da qual seus clientes podem enviar solicitações de cancelamento de venda, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies de Adobe (ID do namespace: `gsurferID`) para que você possa enviar essas identidades como parte de solicitações de cancelamento de venda por meio da API do Adobe Experience Platform Privacy Service.

1. Identifique a ID da organização Experience Cloud e verifique se ela está vinculada às contas Adobe Advertising.

   Uma ID de organização Experience Cloud é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. Uma ID de organização foi atribuída à maioria dos clientes do Experience Cloud. Se a equipe de marketing ou o administrador interno do sistema Adobe não souber a ID da organização ou não tiver certeza se ela foi provisionada, entre em contato com o Atendimento ao cliente da Adobe em gdprsupport@adobe.com. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante da Adobe Advertising da empresa para confirmar se todas as contas Adobe Advertising da organização, incluindo [!DNL DSP] contas ou anunciantes, [!DNL Search, Social, & Commerce] contas e [!DNL Creative] ou [!DNL DCO] contas do — são vinculadas à sua ID da organização Experience Cloud.

1. Use a API do Adobe Experience Platform Privacy Service para [enviar solicitações de cancelamento de venda](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) Adobe Advertising em nome dos consumidores e para verificar o status das solicitações existentes.

   Consulte o Apêndice abaixo para obter um exemplo de solicitação de recusa de venda.

   >[!NOTE]
   >
   Se sua empresa tiver várias IDs de organização de Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para receber suporte do Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando o Adobe Experience Platform Privacy Service e onde encontrar os itens necessários, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recuperação de relatórios de consumidores que enviaram solicitações de recusa de venda

O Adobe Advertising gera relatórios mensais de IDs que os clientes enviaram para solicitações de recusa de venda para a conta. Cada relatório está disponível como um arquivo de texto separado por tabulação e compactado no formato GZIP. Os dados consolidam solicitações capturadas usando segmentos de cancelamento de venda do CCPA que foram criados no DSP de publicidade e quaisquer envios feitos por meio da API Privacy Service. As IDs de usuário capturadas nos segmentos de cancelamento de venda do CCPA são identificadas por segmento e pelo anunciante. Os relatórios são gerados no primeiro dia de cada mês do mês anterior. Por exemplo, a lista mensal de usuários de junho está disponível em 1º de julho.

É possível recuperar links para os relatórios mensais criados nos três meses anteriores, no DSP do Advertising ou usando o DSP do Advertising [!DNL Trafficking API]. Cada link é válido por sete dias, mas é atualizado sempre que um cliente tenta recuperar um.

### Método 1: Recuperar relatórios de cancelamento de venda do consumidor dentro do DSP do anúncio

1. Faça logon na conta do anunciante em Advertising DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recuperar os relatórios](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Método 2: recuperar relatórios de cancelamento de venda do consumidor usando o DSP do anúncio [!DNL Trafficking API]

Esse recurso está disponível para organizações que usam o [!DNL Trafficking API]. Consulte a documentação do [!DNL Trafficking API] para obter mais informações.

Se sua organização não usar o [!DNL Trafficking API] mas tiver interesse em mais informações, entre em contato com a equipe de conta da Adobe.

## Apêndice: Exemplo [!UICONTROL CCPA Opt-Out-of-Sale] Solicitação para usuários da API Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

em que:

* `"namespace": "AdCloud"` indica o `AdCloud` espaço de cookie, e o valor correspondente é a ID do cookie do cliente, conforme recuperada do `AdobePrivacy.js`
* `"include": ["AdCloud"]` indica que a solicitação se aplica ao Adobe Advertising
