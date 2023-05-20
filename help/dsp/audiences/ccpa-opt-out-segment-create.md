---
title: Criar e implementar um segmento de cancelamento de venda da CCPA
description: Saiba como criar e implementar um segmento para rastrear IDs de usuários a partir de solicitações de cancelamento de venda do consumidor.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Criar e implementar um segmento de cancelamento de venda da CCPA

Você pode criar um segmento para rastrear IDs de usuários a partir de solicitações de cancelamento de venda do consumidor em seu site, de acordo com a California Consumer Privacy Act (CCPA). Os usuários permanecem em segmentos de cancelamento de venda do CCPA indefinidamente.

Depois que a tag de pixel de segmento for implementada, a Adobe Advertising começará a coletar um pool de IDs em nome do anunciante.

>[!NOTE]
>
>* Para obter informações sobre como comunicar solicitações de cancelamento de venda do CCPA à Adobe Advertising usando a API do Adobe Experience Platform Privacy Service, consulte [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Para rastrear usuários que visitam páginas da Web para finalidades não relacionadas ao rastreamento de eventos de cancelamento de venda do CCPA, bem como usuários expostos a anúncios de dispositivos de desktop, móveis e CTV, crie um [segmento personalizado](/help/dsp/audiences/custom-segment-create.md).


1. Crie o segmento:

   1. No menu principal, clique em **Públicos > Segmentos**.

   1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

   1. Insira um único **[!UICONTROL Segment Name]**.

      Nome de segmento recomendado: &quot;&lt;*Nome do anunciante*> - Cancelamento de venda do CCPA&quot; (como &quot;Acme - Cancelamento de venda do CCPA&quot;)

   1. Para o [!UICONTROL Segment Type], selecione **[!UICONTROL CCPA Opt-out of sale]**.

   1. Clique em **[!UICONTROL Save]**.

1. Copie e implemente uma tag de pixel para rastrear o segmento:

   1. Retornar para **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Na linha de segmento, mantenha o cursor sobre o novo segmento e clique em **[!UICONTROL Get pixel]**.

   1. Copiar o pixel da imagem (começando com `<img src="https://rtd-tm.everesttech.net"`) para coletar IDs de usuário de visitantes móveis e de desktop para uma página da Web.

   1. Forneça a tag ao anunciante ou contato do site para implantação usando o mecanismo que a empresa usa para rastrear solicitações de cancelamento de venda do CCPA (como o uso de uma Plataforma de gerenciamento de consentimento).

      O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

      Depois que o pixel for implementado, a Adobe Advertising começará a coletar um pool de IDs em nome do anunciante.

      Embora a escolha e a lógica da implementação sejam da responsabilidade do anunciante, este é um exemplo de como um anunciante pode acionar o pixel:

      1. Um consumidor acessa a página inicial do anunciante.
      1. O consumidor encontra e clica no botão &quot;Recusa de venda do CCPA&quot; do anunciante.
      1. O consumidor é apresentado a uma lista de provedores de serviços com os quais o anunciante trabalha.
      1. O consumidor marca a caixa para recusar a venda de dados à Adobe Advertising.

         Essa ação aciona o pixel para ser acionado e coletar a ID do cookie do consumidor dentro da &quot;[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Suporte de publicidade Adobe para a California Consumer Privacy Act: suporte de recusa do consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Sobre [!UICONTROL CCPA Opt-out-of-Sale] Segmentos e relatórios](ccpa-opt-out-about.md)
>* [Recuperar relatórios de cancelamento de venda do consumidor](ccpa-opt-out-segment-report-retrieve.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)

