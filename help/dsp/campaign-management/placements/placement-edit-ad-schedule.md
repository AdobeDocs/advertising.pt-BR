---
title: Editar cronogramas de publicidade para inserções
description: Saiba como alterar os agendamentos de anúncios para os anúncios anexados a inserções.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Editar cronogramas de publicidade para inserções

## Editar os cronogramas de publicidade para uma ou mais disposições

Você pode alterar as datas de veiculação programadas e a rotação de anúncios para os anúncios anexados a vários posicionamentos usando uma planilha do [!DNL Microsoft Excel]. Cada anúncio pode estar ativo durante vários voos.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Marque a caixa de seleção ao lado de cada posicionamento cujos dados de anúncio você deseja baixar.

1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Quando o arquivo estiver disponível, clique em **[!UICONTROL Download]** na notificação na parte superior da página do navegador para baixar um arquivo de planilha (no formato XLSX) de acordo com o procedimento normal do navegador.

   ![Notificação de Pronto para Download](/help/dsp/assets/download-ready.png "Notificação de Pronto para Download")

1. Abra o arquivo baixado, edite os campos de informações de voo de cada linha de anúncio a ser incluída no voo e salve o arquivo atualizado:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (como [!UICONTROL Flight 1 Start Date] e [!UICONTROL Flight 1 End Date]): a primeira e a última data do voo. Use o formato AAAA-MM-DD para cada data. Quaisquer anúncios com campos vazios de data de veiculação são tratados como anúncios não participantes.

   * **[!UICONTROL Flight N Weight]** (como [!UICONTROL Flight 1 Weight]): como girar os anúncios para um voo. Insira um valor:

      * Para girar os anúncios de um voo uniformemente, digite `[!UICONTROL Even]`.

      * Para girar os anúncios de um voo de forma desigual, insira o peso relativo pelo qual girar cada anúncio, como uma porcentagem (como `40` para 40%). O peso total do voo deve ser igual a 100.

1. Faça upload do modelo de programação de anúncios editado:

   1. Marque a caixa de seleção ao lado de cada posicionamento aplicável.

   1. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]** e especifique o arquivo a ser carregado.

## Editar a programação de anúncios para um único posicionamento

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

É possível alterar as datas de veiculação programadas e a rotação dos anúncios anexados a uma disposição. Cada anúncio pode estar ativo durante vários voos.

1. No menu principal, clique em **[!UICONTROL Campaigns]**.

1. Clique no nome da campanha.

1. No submenu, clique em **[!UICONTROL Placements]**.

1. Ao lado do nome do posicionamento, clique em **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Siga um destes procedimentos:

   * Para adicionar um voo, clique em **[!UICONTROL Add Flight]** e especifique a data de início e a data de término.

   * Para adicionar um voo existente a um anúncio, clique em **[!UICONTROL +]** na linha de anúncio da coluna de voo.

   * Para remover um voo existente de um anúncio, clique em **[!UICONTROL x]** na linha de anúncio da coluna de voo.

      * (Quando vários anúncios tiverem o mesmo andamento) Para girar os anúncios de forma desigual, clique em **[!UICONTROL Even Rotation]** nas informações do andamento e insira o peso relativo pelo qual girar cada anúncio, como uma porcentagem.

        Os pesos totais devem ser iguais a 100.

1. No canto superior direito, clique em **[!UICONTROL Continue]**.

1. Revise os detalhes do voo e clique em **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Posicionamento](placement-about.md)
>* [Editar posicionamentos](placement-edit.md)
>* [Exibir o Log de Alterações para um Posicionamento](placement-change-log.md)
>* [Configurações de posicionamento](placement-settings.md)
