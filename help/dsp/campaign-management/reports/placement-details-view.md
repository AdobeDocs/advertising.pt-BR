---
title: Exibir os detalhes de sites, anúncios, frequência e inventário de uma disposição
description: Saiba como visualizar os sites direcionados, anúncios, frequência e dados de inventário para um posicionamento.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Exibir os detalhes de sites, anúncios, frequência e inventário de uma disposição

Para cada posicionamento, é possível [abrir uma (exibição detalhada [!UICONTROL Inspector])](placement-details-view.md), que lista todos os sites, anúncios e ofertas direcionados em uma disposição. Também inclui dados de frequência para o posicionamento. Opcionalmente, é possível exportar os dados de qualquer guia.

![inserção Inspetor](/help/dsp/assets/placement-inspector.png)

## Informações no posicionamento [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Todos os sites nos quais o posicionamento teve impressões.

  A variável [!UICONTROL Sites] inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e um [!UICONTROL Exclude] em cada linha, para excluir rapidamente um site do posicionamento.

* **[!UICONTROL Ads]:** Todos os anúncios no posicionamento.

  A variável [!UICONTROL Ads] A guia inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e botões de ação rápida em cada linha, como [!UICONTROL Pause] (para pausar rapidamente um anúncio).

* **[!UICONTROL Frequency]:** Dados para cada nível de frequência de anúncio para o posicionamento, incluindo:
   * o nível de frequência do anúncio (como &quot;1&quot; para todas as instâncias em que os usuários viram um anúncio uma vez)
   * o número exclusivo estimado de dispositivos/navegadores ou pessoas (dependendo da [!UICONTROL Cross Device Level] para a campanha) que receberam impressões no nível de frequência especificado
   * o número estimado de impressões no nível de frequência especificado
   * a frequência média estimada para o nível de frequência especificado. Esse valor é igual a (Impressões estimadas)/(Únicos estimados).

* **[!UICONTROL Inventory]:** Informações sobre todas as ofertas direcionadas pelo posicionamento.

  A variável [!UICONTROL Inventory] permite a solução rápida de problemas ao mostrar estatísticas de desempenho, como [!UICONTROL Auctions], [!UICONTROL Bids], e [!UICONTROL Win Rate]. A guia inclui recursos de pesquisa e filtro, as mesmas opções de exibição de coluna padrão e personalizada disponíveis na página principal e botões de ação rápida em cada linha, incluindo [!UICONTROL Edit], [!UICONTROL View Report], e [[!UICONTROL Auction Insights] para obter mais soluções de problemas](/help/dsp/inventory/private-deal-auction-insights.md).

## Abra o [!UICONTROL Placement Inspector]

1. Abra a exibição de disposições para a campanha ou o pacote principal:

   * Exibir todos os posicionamentos na campanha pai:

      1. No menu principal, clique em **[!UICONTROL Campaigns]**.

      1. Clique no nome da campanha.

      1. Clique em **[!UICONTROL Placements]** guia.

   * Exibir todos os posicionamentos no pacote pai:

      1. No menu principal, clique em **[!UICONTROL Campaigns]**.

      1. Clique no nome da campanha.

      1. Clique em **[!UICONTROL Packages]** guia.

      1. Clique no nome do pacote pai.

1. Mantenha o cursor sobre a linha de posicionamento e clique em **[!UICONTROL More]** e clique em uma opção:

   * Para exibir todos os sites que o posicionamento direciona, clique em **[!UICONTROL Sites]**.

   * Para exibir todos os anúncios no posicionamento, clique em **[!UICONTROL Ads]**.

   * Para exibir os dados de frequência do posicionamento, clique em **[!UICONTROL Frequency]**.

   * Para exibir todas as ofertas que o posicionamento direciona, clique em **[!UICONTROL Inventory]**.

1. (Opcional) [Alterar a exibição de coluna](campaign-data-views-manage.md#column-view-change) conforme necessário para exibir as métricas necessárias.

1. (Opcional) Para exportar os dados em qualquer guia, clique em ![Mais](/help/search-social-commerce/assets/more.png "Mais") no canto superior direito e clique em **[!UICONTROL Export]**.

   Os dados são salvos na pasta de download padrão do navegador como um relatório no formato XLSM.

## Solução de problemas de inventário

| Problema | Causa possível | Ações a serem executadas |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | O editor não começou a enviar solicitações de oferta. | Entre em contato com o editor para ativar o negócio. |
| | O negócio foi configurado incorretamente, por exemplo, inserindo uma ID de negócio externa incorreta. | Confirme os detalhes da negociação e edite-a. |
| [!UICONTROL Auctions but no Bids] | O direcionamento de posicionamento não corresponde às solicitações de oferta recebidas para a oferta. <br><br> Por exemplo, uma inserção pode ter como alvo uma região geográfica que não é elegível para o negócio. | Edite os destinos de posicionamento conforme necessário para evitar incompatibilidades de direcionamento. |
| | O posicionamento não tem um anúncio ativo com o tipo de mídia necessário para o negócio. | Crie e anexe um anúncio com o tipo de mídia correto ao posicionamento. |
| | O posicionamento não tem orçamento adequado. | Aumentar o orçamento de posicionamento para permitir lances em solicitações recebidas. |
| | As datas de voo de posicionamento não se sobrepõem às datas de entrega de impressão da negociação. | Edite as datas de voo da disposição conforme necessário. |
| [!UICONTROL Low Win Rate] | O lance máximo da disposição (piso ou fixo) está abaixo do mínimo exigido pela negociação. | Aumentar a posição [!UICONTROL Max Bid] conforme necessário. |
| | O posicionamento usa filtros pré-oferta que limitam a oferta. | Diminua os limites dos filtros pré-oferta para permitir mais lances. |
| | O direcionamento de público-alvo para o posicionamento é muito restritivo. | Verifique se os públicos-alvo especificados têm usuários ativos suficientes e expanda o público-alvo, se possível. |

>[!MORELIKETHIS]
>
>* [Tipos de relatórios de desempenho em visualizações do Campaign Management](campaign-reports-about.md)
>* [Gerenciar As Visualizações De Dados Do Campaign](campaign-data-views-manage.md)
