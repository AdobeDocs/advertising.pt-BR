---
title: Exibir o relatório de posicionamento [!UICONTROL Diagnostics]
description: Saiba como diagnosticar problemas com a configuração e o ritmo da inserção.
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: db8e4bd75063216c27a7e14c8d7699e2f4e09ba4
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Exibir o relatório de posicionamento [!UICONTROL Diagnostics]

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

Relatórios de diagnóstico podem ajudar a diagnosticar problemas com a configuração e o ritmo da inserção assim que a campanha estiver ativa.

## Informações no relatório de posicionamento [!UICONTROL Diagnostics]

* **[!UICONTROL Change Log]:** Mostra as alterações nas configurações de posicionamento de chaves, como nome, status e lance máximo. Cada entrada inclui a data e o nome de usuário da pessoa que fez a alteração.

* **[!UICONTROL Ad Approvals]:** Mostra se os anúncios foram aprovados ou rejeitados pelos provedores de estoque. Como opção, é possível alterar o status de qualquer anúncio (por exemplo, pausar um anúncio rejeitado) ou abrir as configurações do anúncio.

* **[!UICONTROL Non Bids]:** Mostra por que a DSP não ofereceu o posicionamento.

## Abrir o relatório de posicionamento [!UICONTROL Diagnostics]

1. Abra o relatório [!UICONTROL Diagnostics]:

   1. Abra as configurações de posicionamento:

      1. No menu principal, clique em **[!UICONTROL Campaigns]**.

      1. Clique no nome da campanha e em **[!UICONTROL Placements]**.

      1. Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   1. No canto superior direito, clique em ![Diagnóstico de posicionamento](/help/dsp/assets/placement-diagnostics.png).

1. Siga um destes procedimentos:

   * Para exibir o log de alterações:

      1. Clique em **[!UICONTROL Change Log]**.

      1. (Opcional) Filtre os resultados do relatório:

         * No menu de data, altere o período padrão do relatório Últimos 14 Dias para outro período (*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],* ou *[!UICONTROL Last 1 year]*).

         * No menu esquerdo, filtre o relatório por um nome de usuário específico.

         * No menu direito, filtre o relatório por uma configuração de disposição específica.

   * Para exibir o status das aprovações de anúncios:

      1. No canto superior direito, clique em **[!UICONTROL Ad Approvals]**.

      1. (Opcional) Para pausar ou ativar o anúncio, clique na opção de status (![Opção de status](/help/dsp/assets/status-switch.png)) na coluna Anúncio).

      1. (Opcional) Para abrir as configurações de um anúncio, clique em **[!UICONTROL View Ad]** ao lado do anúncio.

   * Para ver por que a DSP não ofereceu a inserção:

      1. No canto superior direito, clique em **[!UICONTROL Non Bids]**.

      1. (Opcional) Para filtrar o posicionamento por um target de negociação privada específico, selecione a negociação. <!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. (Opcional) Para alterar o intervalo de datas, clique no campo de data e selecione uma data ou intervalo de datas diferente.

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Tipos de Relatórios de Desempenho em Exibições de Gerenciamento de Campanha](campaign-reports-about.md)
>* [Exibir o Relatório de Previsão de Posicionamento](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
