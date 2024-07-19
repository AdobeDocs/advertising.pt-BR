---
title: Criar manualmente detalhes da ID do contrato
description: Saiba como inserir detalhes manualmente para uma ID de acordo.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Criar manualmente detalhes da ID do contrato

1. No menu principal, clique em **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Acima da tabela de dados, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Deal ID]**.

1. Insira as [configurações de negócios](deal-id-settings.md):

   1. Na seção [!UICONTROL Deal ID basics], especifique os detalhes do negócio e os anunciantes que podem acessá-lo. Para ofertas garantidas, você também deve especificar as datas de voo planejadas e o número estimado de impressões, somente para fins de rastreamento.

      Você pode rastrear o ritmo das ofertas garantidas incluindo a coluna &quot;Ritmo de impressão PG&quot; nos gastos em Inventário > Exibição de ofertas.

   1. (Somente usuários administradores; opcional) Na seção [!UICONTROL Technical], edite as configurações padrão conforme necessário.

   1. Clique em **[!UICONTROL Save]**.

1. (Somente ofertas garantidas) Selecione os anúncios a serem usados para a oferta (ou o pixel 1x1 para anúncios gerenciados pelo editor) e crie uma inserção programática garantida (PG) padrão.

   Os posicionamentos de PG padrão garantem que sua oferta sempre retorne um lance para cada solicitação de oferta. Se você não criar uma disposição padrão de PG, quaisquer disposições direcionadas para o negócio não darão lances, a menos que estejam configuradas corretamente. Você sempre deve criar um posicionamento de PG padrão. Na exibição [!UICONTROL Placements], os posicionamentos de PG padrão têm um valor de coluna [!UICONTROL Sub-type] de &quot;[!UICONTROL PG Default]&quot;.

   Opcionalmente, você pode usar a negociação como um destino de inventário em disposições adicionais, mas deve configurá-las corretamente para fazer ofertas.

   1. Nas configurações de [!UICONTROL Ad & Campaign Selection], selecione os anúncios a serem usados para a oferta:

      1. Selecione o anunciante, a campanha e o tipo de anúncio. Opcionalmente, selecione um status de anúncio pelo qual filtrar os anúncios.

      1. Na lista de anúncios disponíveis, marque a caixa de seleção ao lado de cada anúncio a ser usado para a negociação.

         Para cada anúncio gerenciado pelo editor, um pixel de rastreamento 1x1 é aplicado automaticamente depois que um anunciante e uma campanha são selecionados.

      1. Clique em **[!UICONTROL Apply]**.

   1. Na tela de configurações de posicionamento:

      1. Insira o nome da disposição.

      1. (Opcional) Edite as [configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md), incluindo a substituição da oferta padrão, que é preenchida automaticamente com o valor CPM da oferta; a alteração do intervalo de datas; ou a anexação de mais anúncios.

      A negociação é direcionada automaticamente na seção Metas de Inventário. Todas as outras opções de direcionamento são inaplicáveis.

      1. Clique em **[!UICONTROL Create placement]**.

Depois de criar a negociação, você pode usá-la como uma meta de inventário para várias disposições.

>[!NOTE]
>
> Você não precisa enviar a tag de negócios ao editor para verificação.

>[!TIP]
>
>* Na exibição [!UICONTROL Inventory] > [!UICONTROL Deals], a coluna [!UICONTROL Pacing & Budget] mostra como a transação está se aproximando da data de voo especificada e da meta de impressão.
>
>* Se o delivery estiver aquém ou acima do ritmo, entre em contato com seu editor para ajustar quanto volume ele está enviando através do negócio.

>[!MORELIKETHIS]
>
>* [Configurações manuais de ID do contrato](deal-id-settings.md)
>* [Configurar um contrato programático garantido](programmatic-guaranteed-set-up.md)
>* [Enviar um anúncio para uma oferta programática garantida com o  [!DNL FreeWheel]](freewheel-submit.md)
>* [Sobre Ofertas Programáticas Garantidas](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
