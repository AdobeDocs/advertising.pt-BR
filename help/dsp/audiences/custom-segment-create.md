---
title: Criar e implementar um segmento personalizado
description: Saiba como criar e implementar um segmento personalizado para rastrear usuários expostos a anúncios ou usuários que visitam suas páginas da Web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 67b59f4f066d25f323620b83b5a0cb49beb3ee04
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# Criar e implementar um segmento personalizado

Você pode coletar seus próprios dados de público-alvo primários criando e implementando um segmento DSP personalizado. Você pode usar o segmento para rastrear a) usuários expostos a anúncios de dispositivos móveis e de desktop e b) usuários que visitam páginas da Web específicas. Posteriormente, você pode redirecionar os usuários no segmento com anúncios adicionais ou impedir que eles recebam anúncios adicionais.

>[!NOTE]
>
>Para rastrear IDs de usuários a partir de solicitações de cancelamento de venda em seu site, de acordo com a California Consumer Privacy Act (CCPA), crie um [Segmento de cancelamento de venda do CCPA](ccpa-opt-out-segment-create.md).

1. Crie o segmento:

   1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Insira um único **[!UICONTROL Segment Name]**.

   1. Para o **[!UICONTROL Segment Type]**, selecione *[!UICONTROL Custom]*.

   1. Insira o **[!UICONTROL Segment Window]**, que é o número de dias que um cookie do usuário permanece no segmento.

      A janela padrão é de 45 dias. Insira um valor de um (1) a 365.

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
