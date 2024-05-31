---
title: Criar e implementar um segmento personalizado
description: Saiba como criar e implementar um segmento personalizado para rastrear usuários expostos a anúncios ou usuários que visitam suas páginas da Web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: b90e831d0fdd5f4f4f47381a2603a3adaea765b2
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Criar e implementar um segmento personalizado

Você pode coletar seus próprios dados de público-alvo primários criando e implementando um segmento DSP personalizado. Você pode usar o segmento para rastrear a) usuários expostos a anúncios de dispositivos móveis e de desktop e b) usuários que visitam páginas da Web específicas. Posteriormente, você pode redirecionar os usuários no segmento com anúncios adicionais ou impedir que eles recebam anúncios adicionais.

>[!NOTE]
>
>Para rastrear IDs de usuários a partir de solicitações de cancelamento de venda em seu site, de acordo com a California Consumer Privacy Act (CCPA), crie um [Segmento de cancelamento de venda do CCPA](ccpa-opt-out-segment-create.md).

## Pré-requisitos para que os segmentos rastreiem IDs ID5

*Recurso beta*

* Antes de gerar um segmento para rastrear usuários associados a IDs ID5, você deve assinar um contrato com a [!DNL ID5] e obtenha a ID de parceiro da organização. Entre em contato com a equipe de conta do Adobe para obter instruções.

* Para a medição no Adobe Analytics, você deve:

   1. Concluir tudo [pré-requisitos para implementar o [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)e certifique-se de que o [ID AMO e ID EF](/help/integrations/analytics/ids.md) estão sendo preenchidos nos URLs de rastreamento.

   1. Adicione o seguinte parâmetro às suas páginas da Web antes ou dentro do [Código JavaScript necessário para [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — em qualquer lugar antes da inicialização do último serviço de evento.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Exemplo:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

## Criar e implementar um segmento personalizado

1. Crie o segmento:

   1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Insira um único **[!UICONTROL Segment Name]**.

   1. Para o **[!UICONTROL Segment Type]**, selecione *[!UICONTROL Custom]*.

   1. Insira o **[!UICONTROL Lookback Window]**, que é o número de dias que um cookie do usuário permanece no segmento.

      A janela padrão é de 45 dias. Insira um valor de um (1) a 365.

   1. Clique em **[!UICONTROL Advanced]** para expandir as configurações avançadas e selecionar os tipos de identificadores de usuário que a tag de segmento rastreia:

      * *[!UICONTROL Cookies]:* (O padrão) A tag de segmento rastreia cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* A tag de segmento rastreia [!DNL ID5] IDs. Nenhuma taxa é incorrida para impressões entregues a IDs universais.

        **[!UICONTROL Terms of Service]:** Os termos do contrato de serviço para usar IDs universais. Você ou outro usuário na conta do DSP deve aceitar os termos uma vez antes que você possa usar IDs universais para um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta do Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **>**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

   1. Clique em **[!UICONTROL Save]**.

1. Copie e implemente tags para rastrear o segmento, conforme necessário:

   1. Retornar para **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Mantenha o cursor sobre a linha de segmento e clique em **[!UICONTROL Get Pixel]**.

      * Para rastrear visitantes móveis e da área de trabalho em uma página da Web:

         1. Copie a tag de rastreamento de exibição de página, chamada de &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Forneça a tag ao anunciante ou contato do site para implantação.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

      * Para rastrear usuários expostos a uma unidade de publicidade em dispositivos móveis ou desktop:

         1. Copie a tag de rastreamento de impressão, chamada de &quot;[!UICONTROL Desktop or mobile ads].&quot;

   1. (Tags para segmentos que rastream [!DNL ID5] IDs para visitantes móveis e de desktop a uma página da Web) Na tag copiada, substitua `ID5_PARTNER_ID` com a ID do parceiro que [!DNL ID5] atribuído à sua organização.

   Por exemplo, se a ID do parceiro ID5 for `abcde` e a tag de segmento gerada for

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   depois substituir `ID5_PARTNER_ID` com `abcde` na tag para obter o seguinte:

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   Sua organização recebeu a ID do parceiro quando assinou um contrato com a [!DNL ID5]. Caso não saiba a ID do parceiro, entre em contato com a equipe de conta do Adobe.

   Essa etapa não é necessária para que as tags rastreiem [!DNL ID5] IDs para usuários expostos a uma unidade de publicidade em dispositivos móveis ou desktop.

1. Adicione a tag ao [!UICONTROL Pixel] para cada anúncio relevante ou para o [!UICONTROL Event Pixels] seção do [[!UICONTROL Tracking] configurações para cada posicionamento relevante](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Depois que uma tag de rastreamento é implementada, você pode usar o segmento nos destinos ou exclusões de público-alvo para qualquer posicionamento.

>[!TIP]
>
>Controle o tamanho do segmento à medida que os usuários são rastreados.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Editar informações do segmento](segment-edit.md)
>* [Excluir um segmento](segment-delete.md)
>* [Exibir pixels de rastreamento para um segmento](segment-view-pixels.md)
>* [Compartilhar ou parar de compartilhar um segmento](segment-share.md)
>* [Criar e implementar uma [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
