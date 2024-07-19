---
title: Criar e implementar um segmento personalizado
description: Saiba como criar e implementar um segmento personalizado para rastrear usuários expostos a anúncios ou usuários que visitam suas páginas da Web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 2fe54fbcd9711e714246f074ede086910b538b80
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Criar e implementar um segmento personalizado

Você pode coletar seus próprios dados de público-alvo primários criando e implementando um segmento DSP personalizado. Você pode usar o segmento para rastrear a) usuários expostos a anúncios de dispositivos móveis e de desktop e b) usuários que visitam páginas da Web específicas. Posteriormente, você pode redirecionar os usuários no segmento com anúncios adicionais ou impedir que eles recebam anúncios adicionais.

>[!NOTE]
>
>Para rastrear as IDs de usuários a partir de solicitações de cancelamento de venda em seu site, de acordo com a California Consumer Privacy Act (CCPA), crie um [segmento de cancelamento de venda da CCPA](ccpa-opt-out-segment-create.md).

## Pré-requisitos para que os segmentos rastreiem IDs ID5

*recurso do Beta*

* Antes de gerar um segmento para rastrear usuários associados a IDs ID5, assine um contrato com [!DNL ID5] e obtenha a ID de parceiro da sua organização. Entre em contato com a equipe de conta do Adobe para obter instruções.

* Para a medição no Adobe Analytics, você deve:

   1. Conclua todos os [pré-requisitos para implementação [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) e verifique se a [ID do AMO e a EF ID](/help/integrations/analytics/ids.md) estão sendo populadas nas URLs de rastreamento.

   1. Adicione o seguinte parâmetro às suas páginas da Web antes ou dentro do [código JavaScript necessário para o  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — em qualquer lugar antes da inicialização do último serviço de evento.

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

   1. Use qualquer ferramenta de depuração de navegador para verificar se cada chamada foi iniciada para o domínio `lasteventf-tm.everesttech.net` e contém o parâmetro `_les_id5` com uma ID5 criptografada como seu valor.

## Criar e implementar um segmento personalizado

1. Crie o segmento:

   1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Digite um **[!UICONTROL Segment Name]** exclusivo.

   1. Para o **[!UICONTROL Segment Type]**, selecione *[!UICONTROL Custom]*.

   1. Digite o **[!UICONTROL Lookback Window]**, que é o número de dias que um cookie de usuário permanece no segmento.

      A janela padrão é de 45 dias. Insira um valor de um (1) a 365.

   1. Clique em **[!UICONTROL Advanced]** para expandir as configurações avançadas e selecione os tipos de identificadores de usuário que a marca de segmento rastreia:

      * *[!UICONTROL Cookies]:* (o padrão) A marca de segmento rastreia cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* A marca de segmento rastreia [!DNL ID5] IDs. Nenhuma taxa é incorrida para impressões entregues a IDs universais.

        **[!UICONTROL Terms of Service]:** Os termos do contrato de serviço para usar IDs universais. Você ou outro usuário na conta do DSP deve aceitar os termos uma vez antes que você possa usar IDs universais para um novo tipo de ID. Para clientes com contratos de serviço gerenciado, a equipe de conta do Adobe obterá seu consentimento e aceitará os termos em nome da organização. Para ler os termos, clique em **>**. Para aceitar os termos, navegue até a parte inferior dos termos e clique em **[!UICONTROL Accept]**.

   1. Clique em **[!UICONTROL Save]**.

1. Copie e implemente tags para rastrear o segmento, conforme necessário:

   1. Retornar a **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Mantenha o cursor sobre a linha de segmento e clique em **[!UICONTROL Get Pixel]**.

      * Para rastrear visitantes móveis e da área de trabalho em uma página da Web:

         1. Copie a marca de rastreamento de exibição de página, chamada &quot;[!UICONTROL Desktop or mobile websites]&quot;.

         1. (Marcas para segmentos que rastreiam [!DNL ID5] IDs) Na marca copiada, substitua `ID5_PARTNER_ID` pela ID de parceiro que [!DNL ID5] atribuiu à sua organização.

            Por exemplo, se a ID do parceiro ID5 for `abcde` e a tag de segmento gerada for

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            em seguida, substitua `ID5_PARTNER_ID` por `abcde` na tag para obter o seguinte:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Sua organização recebeu a ID de parceiro quando assinou um contrato com [!DNL ID5]. Caso não saiba a ID do parceiro, entre em contato com a equipe de conta do Adobe.

            Esta etapa não é necessária para que as marcas rastreiem [!DNL ID5] IDs para usuários expostos a uma unidade de publicidade em dispositivos móveis ou desktop.

         1. Forneça a tag ao anunciante ou contato do site para implantação.

            O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

      * Para rastrear usuários expostos a uma unidade de publicidade em dispositivos móveis ou desktop:

         1. Copie a marca de rastreamento de impressão, chamada &quot;[!UICONTROL Desktop or mobile ads]&quot;.

         1. Adicione a marca à guia [!UICONTROL Pixel] para cada anúncio relevante ou à seção [!UICONTROL Event Pixels] das configurações [[!UICONTROL Tracking] para cada posicionamento relevante](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Depois que uma tag de rastreamento é implementada, você pode usar o segmento nos destinos ou exclusões de público-alvo para qualquer posicionamento.

>[!TIP]
>
>Controle o tamanho do segmento à medida que os usuários são rastreados.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Público-Alvo](audience-about.md)
>* [Editar informações do segmento](segment-edit.md)
>* [Excluir um segmento](segment-delete.md)
>* [Exibir Pixels de Rastreamento de um Segmento](segment-view-pixels.md)
>* [Compartilhar ou Parar de Compartilhar um Segmento](segment-share.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
