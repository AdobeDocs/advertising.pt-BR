---
title: Criar um contrato de [!UICONTROL Simple Ad Serving]
description: Saiba como criar um pixel de rastreamento para uma oferta do [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Criar um contrato de [!UICONTROL Simple Ad Serving]

1. No menu principal, clique em **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Acima da tabela de dados, clique em **[!UICONTROL Create]** e selecione **[!UICONTROL Simple Ad Serving]**.

1. Insira as [configurações de negócios](simple-deal-settings.md):

   1. Na seção [!UICONTROL Select Ad Source], especifique as informações sobre o editor, anunciante e campanha, o tipo de anúncio e clique em **[!UICONTROL Next]**.

   1. Na seção [!UICONTROL Select Ad(s)], especifique um anúncio para usar como proxy no DSP:

      1. Siga um destes procedimentos:

         * Para anúncios existentes, selecione os anúncios a serem usados.

         * Para novos anúncios, crie um proxy [anúncio de terceiros](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > O DSP não veicula os anúncios que você especifica. O editor serve o anúncio.

      1. Clique em **[!UICONTROL Next]**.

   1. Em Detalhes do Feed, edite os detalhes do feed e clique em **[!UICONTROL Next]**.

      O DSP gera automaticamente um posicionamento chamado &quot;Posicionamento SAS - &lt;*nome do negócio*>&quot; para o anúncio. No posicionamento, a oferta é direcionada automaticamente na seção [!UICONTROL Inventory Targets]. Todas as outras opções de direcionamento são inaplicáveis.

1. Envie os pixels de rastreamento de eventos ao editor para implementação de uma das seguintes maneiras:

   * (Opcional) Na tela [!UICONTROL Activate Tag with Publisher], envie a tag de negócios para o editor.

     Quando você conclui as etapas anteriores, o DSP gera uma mensagem de email que pode ser enviada ao editor. A mensagem inclui os detalhes do contrato, um link a partir do qual a tag de contrato será recuperada e um código de autorização para o link.

      1. Analise os detalhes do negócio e siga um destes procedimentos:

         * Para colar as informações em uma mensagem de email em um aplicativo de email no seu dispositivo, clique em **[!UICONTROL Email & Done]** e selecione o aplicativo de email. O campo [!UICONTROL CC:] é pré-preenchido com um endereço de suporte [!DNL Adobe]. Em seguida, você pode enviar a mensagem para o contato apropriado do editor.

         * Para copiar as informações para a área de transferência, clique em **[!UICONTROL Copy Email].** Em seguida, você pode colar manualmente o conteúdo em uma mensagem de email e enviá-lo ao contato apropriado do editor. Você deve incluir uma cópia (CC:) para `publisher-support-global@adobe.com`. Quando terminar de copiar a mensagem, clique em **[!UICONTROL Email & Done]**.

      1. (Se necessário) Acompanhe o editor para ver se a tag inclui as macros apropriadas para que a tag funcione com o servidor de anúncios do editor.

   * (Opcional) Envie manualmente os pixels de rastreamento de eventos para o editor:

      1. Na linha de negócios na exibição [!UICONTROL Deals], clique em ![Menu de opções](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Os pixels do evento incluem um [!UICONTROL Clickthrough] pixel e um [!UICONTROL Impression] pixel. Anúncios de vídeo e áudio também incluem pixels de evento por quartil concluídos (de [!UICONTROL 25% Complete] a [!UICONTROL 100% Complete]).

      1. Copie os pixels de rastreamento de eventos e forneça-os ao editor.

>[!MORELIKETHIS]
>
>* [Sobre [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Configurações](simple-deal-settings.md)
>* [Exibir um Relatório Detalhado de um Acordo](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
