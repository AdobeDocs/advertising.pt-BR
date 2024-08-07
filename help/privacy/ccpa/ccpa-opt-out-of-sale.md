---
title: Suporte Adobe Advertising para a California Consumer Privacy Act &#58; Suporte ao cliente que recusou a venda
description: Saiba mais sobre o suporte para capturar solicitações de cancelamento de venda do consumidor.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Suporte Adobe Advertising para a California Consumer Privacy Act: suporte ao cancelamento de venda do consumidor

*Para Demand Side Platform Adobe Advertising (DSP)*

>[!IMPORTANT]
>
>O conteúdo deste documento não é um aconselhamento jurídico e não se destina a substituir tal aconselhamento. Consulte seu advogado para obter recomendações sobre a California Consumer Privacy Act.

A California Consumer Privacy Act (CCPA) é a nova lei de privacidade da Califórnia, que entrou em vigor em 1º de janeiro de 2020. A CCPA fornece aos residentes da Califórnia novos direitos sobre suas informações pessoais e impõe responsabilidades de proteção de dados a determinadas entidades que realizam negócios na Califórnia. A CCPA dá aos consumidores o direito de acessar e apagar seus dados, bem como o direito de recusar certas atividades qualificadas como &quot;venda&quot; de informações pessoais a terceiros.

Como empresa, você determinará os dados pessoais que a Adobe Experience Cloud processa e armazena em seu nome.

Como seu provedor de serviços, o Adobe Advertising fornece suporte para que sua empresa cumpra as obrigações da CCPA aplicáveis ao uso de produtos e serviços Adobe Advertising, incluindo o gerenciamento de solicitações do cliente para acessar e excluir informações pessoais e o gerenciamento de solicitações do cliente para recusar a venda de informações pessoais.

Este documento descreve como o Adobe Advertising Demand Side Platform (DSP), como provedor de serviços, apoia o direito do consumidor de recusar a &quot;venda&quot; de &quot;informações pessoais&quot;, já que cada termo é definido pela CCPA. Ele inclui informações sobre como comunicar solicitações de recusa de venda ao Adobe Advertising e como recuperar relatórios de solicitações de recusa de venda de sua organização.

Para obter informações sobre como o [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; e [!DNL Advertising DCO] oferecem suporte aos direitos de acesso e exclusão de informações pessoais dos consumidores, consulte [Suporte Adobe Advertising para a California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ccpa/ccpa-access-delete.md).

Para obter mais informações sobre os serviços de privacidade de Adobe para CCPA, consulte o [Centro de Privacidade de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicando solicitações de cancelamento de venda do consumidor ao Adobe Advertising

Você pode comunicar solicitações de cancelamento de venda do cliente usando:

* um segmento de cancelamento de venda do CCPA criado no Advertising DSP
* a API do Adobe Experience Platform Privacy Service

### Método 1: comunicar solicitações de cancelamento de venda do CCPA usando um segmento [!UICONTROL CCPA Opt-Out-of-Sale] no Advertising DSP

>[!NOTE]
>
>Os usuários permanecem em segmentos de cancelamento de venda do CCPA indefinidamente.

1. Faça logon na conta do anunciante no Advertising DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Crie um segmento de cancelamento de venda do CCPA e implemente o pixel do segmento para capturar as solicitações de cancelamento](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Método 2: comunicar solicitações de cancelamento de venda do CCPA usando a API do Adobe Experience Platform Privacy Service

*Somente ID de organização da Adobe Experience Cloud atribuída aos anunciantes*

1. Implante uma biblioteca do JavaScript para recuperar os cookies do cliente. A mesma biblioteca, `AdobePrivacy.js`, é usada para todas as soluções da Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >As solicitações para algumas soluções da Adobe Experience Cloud não exigem a biblioteca JavaScript, mas as solicitações para Adobe Advertising exigem.

   Você deve implantar a biblioteca na página da Web a partir da qual seus clientes podem enviar solicitações de cancelamento de venda, como o portal de privacidade da sua empresa. A biblioteca ajuda a recuperar cookies Adobe (ID de namespace: `gsurferID`) para que você possa enviar essas identidades como parte de solicitações de recusa de venda por meio da API do Adobe Experience Platform Privacy Service.

1. Identifique a ID da organização do Experience Cloud e verifique se ela está vinculada às suas contas do Adobe Advertising.

   Uma ID de organização Experience Cloud é uma sequência de 24 caracteres alfanuméricos anexada com &quot;@AdobeOrg&quot;. Uma ID de organização foi atribuída à maioria dos clientes do Experience Cloud. Se a sua equipe de marketing ou o administrador interno do sistema Adobe não souber a ID da organização ou não tiver certeza se ela foi provisionada, entre em contato com a equipe de conta da Adobe. Você precisará da ID da organização para enviar solicitações à API de privacidade usando o namespace `imsOrgID`.

   >[!IMPORTANT]
   >
   >Entre em contato com o representante de Adobe Advertising da sua empresa para confirmar se todas as contas Adobe Advertising da sua organização — incluindo contas do [!DNL DSP] ou anunciantes, contas do [!DNL Search, Social, & Commerce] e contas do [!DNL Creative] ou [!DNL DCO] — estão vinculadas à ID da sua organização Experience Cloud.

1. Use a API do Adobe Experience Platform Privacy Service para [enviar solicitações de não participação na venda](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) para o Adobe Advertising em nome dos consumidores e para verificar o status das solicitações existentes.

   Consulte o Apêndice abaixo para obter um exemplo de solicitação de recusa de venda.

   >[!NOTE]
   >
   >Se sua empresa tiver várias IDs de organização de Experience Cloud, você deverá enviar solicitações de API separadas para cada uma. No entanto, você pode fazer uma solicitação de API para várias subsoluções de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] e [!DNL DCO]), com uma conta por subsolução.

Todas essas etapas são necessárias para receber suporte do Adobe Advertising. Para obter mais informações sobre essas e outras tarefas relacionadas que você precisa executar usando a Adobe Experience Platform Privacy Service e onde encontrar os itens necessários, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recuperação de relatórios de consumidores que enviaram solicitações de recusa de venda

O Adobe Advertising gera relatórios mensais de IDs que os clientes enviaram para solicitações de recusa de venda para a conta. Cada relatório está disponível como um arquivo de texto separado por tabulação e compactado no formato GZIP. Os dados consolidam solicitações capturadas usando segmentos de não participação na venda do CCPA que foram criados no Advertising DSP e quaisquer envios feitos por meio da API Privacy Service. As IDs de usuário capturadas nos segmentos de cancelamento de venda do CCPA são identificadas por segmento e pelo anunciante. Os relatórios são gerados no primeiro dia de cada mês do mês anterior. Por exemplo, a lista mensal de usuários de junho está disponível em 1º de julho.

Você pode recuperar links para os relatórios mensais criados nos três meses anteriores, no Advertising DSP ou usando o Advertising DSP [!DNL Trafficking API]. Cada link é válido por sete dias, mas é atualizado sempre que um cliente tenta recuperar um.

### Método 1: Recuperar relatórios de cancelamento de venda do consumidor no Advertising DSP

1. Faça logon na conta do anunciante no Advertising DSP em [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recupere os relatórios](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Método 2: Recuperar Relatórios de Cancelamento de Venda do Consumidor Usando o Advertising DSP [!DNL Trafficking API]

Este recurso está disponível para organizações que usam o [!DNL Trafficking API]. Consulte a documentação de [!DNL Trafficking API] para obter mais informações.<!-- Add link to API doc once it's published. -->

Se a sua organização não usa o [!DNL Trafficking API], mas está interessada em obter mais informações, contate a equipe de conta do Adobe.

## Apêndice: Exemplo de solicitação [!UICONTROL CCPA Opt-Out-of-Sale] para usuários da API Privacy Service

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
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

em que:

* `"namespace": "adCloud"` indica o espaço de cookies `adCloud`, e o valor correspondente é a ID do cookie do cliente conforme recuperada de `AdobePrivacy.js`
* `"include": ["adCloud"]` indica que a solicitação se aplica ao Adobe Advertising
