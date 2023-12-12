---
title: Criar uma disposição
description: Saiba como criar uma disposição.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: d1e1a8507b08a64bdc582c2967964b869c7d5bc7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Criar uma disposição

>[!TIP]
>
>Crie inserções com base em metas de campanha ou necessidades de relatórios específicas.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha na qual o posicionamento será incluído.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**. No [!UICONTROL Placement Types] do menu, clique no tipo de posicionamento.

   O tipo de posicionamento determina o tipo de anúncio que o posicionamento pode incluir.

1. Insira o [configurações de posicionamento](placement-settings.md):

   1. Especifique a [!UICONTROL Placement Basics] configurações.

   1. No [!UICONTROL Goals] especifique a [!UICONTROL Gross Budget] e, opcionalmente, especifique metas adicionais de posicionamento.

      Alguns campos têm valores padrão que podem ser substituídos.

      Se o pacote ao qual o posicionamento é atribuído tiver ritmo no nível do pacote, suas metas e configurações de ritmo refletirão as configurações do pacote.

   1. (Opcional) Na [!UICONTROL Geo-Targeting] , restrinja os locais incluídos ou excluídos.

      Se você não identificar locais específicos, todos os locais serão direcionados.

      >[!NOTE]
      >
      >Os locais de cidade e DMA não estão disponíveis para inserções do Roku.

   1. No [!UICONTROL Inventory Targeting] restringir as origens de inventário a serem incluídas ou excluídas.

      Para a maioria dos tipos de posicionamento, todos os tipos de inventário e todas as origens para cada tipo são incluídos por padrão. Para [!DNL Roku] posicionamentos, você deve especificar o tipo de inventário e as origens.

   1. (Opcional) Na [!UICONTROL Site Targeting] , restrinja os sites que deseja direcionar e especifique os sites que deseja excluir.

   1. (Opcional) Na [!UICONTROL Audience Targeting] seção:

      1. Restrinja o público. Isso inclui selecionar segmentos de público-alvo para direcionar na disposição.

         Para [!DNL Roku] posicionamentos, você pode aproveitar [O público-alvo exclusivo do DSP que corresponde a [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) incluindo um ou mais segmentos de público-alvo que podem ser comparados com o [!DNL Roku] (aceitação) conjunto de dados determinísticos.

      1. (Para campanhas com direcionamento entre dispositivos em nível de pessoas; opcional) Quando o posicionamento segmenta um ou mais públicos específicos, habilite o direcionamento entre dispositivos com base em pessoas para o posicionamento.

         O direcionamento entre dispositivos com base em pessoas é fornecido pela [!DNL LiveRamp] usando somente dados dos EUA. O serviço está disponível para todos os anunciantes a US$ 0,35 CPM para impressões fornecidas usando o [!DNL LiveRamp] gráfico de dispositivos (ou seja, para dispositivos não encontrados nos segmentos de público-alvo direcionados).

   1. (Opcional) Na [!DNL Brand Safety and Media Targeting] aplicar restrições de segurança da marca para suas inserções.

   1. (Opcional) Na [!DNL Tracking] insira pixels de evento de terceiros ou pixels de conversão para anúncios no posicionamento.

      >[!NOTE]
      >
      >([!DNL Roku] posicionamentos) Fornecedores de pixels de terceiros aprovados por [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], e [!DNL Research Now].

1. Clique em **[!UICONTROL Create Placement]**.

1. (Opcional) Anexar anúncios ao posicionamento:

   1. Clique em **[!UICONTROL Attach an ad]**.

   1. Siga um destes procedimentos:

      * Para criar um novo anúncio:

         1. Clique em **[!UICONTROL Create a New Ad].**

         1. Especifique as configurações de publicidade para [anúncios de áudio](/help/dsp/campaign-management/ads/ad-settings-audio.md), [TV conectada](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [exibir anúncios](/help/dsp/campaign-management/ads/ad-settings-display.md), [anúncios móveis](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [anúncios nativos](/help/dsp/campaign-management/ads/ad-settings-native.md), [anúncios antes da exibição](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)ou [anúncios de vídeo universais](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Inserções de vídeo universais podem conter somente anúncios de vídeo universais.

         1. Clique em **[!UICONTROL Save & Submit for Review]**.

         1. (Opcional) Para cada anúncio adicional que você deseja criar para o posicionamento, clique em **[!UICONTROL Attach Another Ad]** e, em seguida, repita as Etapas 1 a 3.

         1. Caso não anexe nenhum anúncio existente, clique em **[!UICONTROL I'm done for now]**.

      * Para anexar anúncios existentes na campanha:

      1. Clique em **[!UICONTROL Select an Ad]**.

      1. Siga um destes procedimentos:

         * Para adicionar um anúncio por vez:

            1. Ao lado do nome do anúncio, clique em **[!UICONTROL Select].**

            1. (Opcional) Para cada anúncio adicional que você deseja anexar, clique em **[!UICONTROL Attach Another Ad]** e, em seguida, repita o processo.

         * Para adicionar até 20 anúncios por vez:

            1. Marque a caixa de seleção acima da lista de anúncios.

            1. Marque a caixa de seleção ao lado de cada anúncio a ser adicionado.

            1. Clique em **[!UICONTROL Attach]**.

            1. Ao lado do nome do anúncio, clique em **[!UICONTROL Select]**.

      1. (Opcional) Para substituir o período de veiculação padrão e a rotação de anúncios para anúncios específicos no posicionamento:

         1. Clique em **[!UICONTROL Custom Schedule Ads]**.

         1. Siga um destes procedimentos:

            * Para adicionar um voo, clique em **[!UICONTROL Add Flight]** e especifique a data inicial e a data final.

            * Para adicionar um voo existente a um anúncio, clique em **[!UICONTROL +]** na linha de anúncio da coluna de voo.

            * Para remover um voo existente de um anúncio, clique em **[!UICONTROL x]** na linha de anúncio da coluna de voo.

            * (Quando vários anúncios tiverem o mesmo andamento) Para girar os anúncios de forma desigual, clique em **[!UICONTROL Even Rotation]** nas informações de voo e insira o peso relativo pelo qual girar cada anúncio, como uma porcentagem.

              Os pesos totais devem ser iguais a 100.

         1. No canto superior direito, clique em **[!UICONTROL Continue]**.

         1. Revise os detalhes do voo e clique em **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento de posicionamento](placement-about.md)
>* [Editar uma disposição](placement-edit.md)
>* [Editar os cronogramas de anúncios para disposições](placement-edit-ad-schedule.md)
>* [Pausar ou ativar um posicionamento](placement-pause-activate.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
>* [Exibir o Relatório de Previsão de Posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Perguntas frequentes sobre o Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Atalhos de teclado](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Solução de problemas de desempenho](/help/dsp/optimization/troubleshooting-performance.md)
>* [Vídeo: como criar uma disposição de exibição padrão](https://video.tv.adobe.com/v/340454)
