---
title: Criar um público-alvo reutilizável
description: Saiba como criar públicos-alvo reutilizáveis que consistem em segmentos de público-alvo e outros públicos-alvo salvos.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Criar um público-alvo reutilizável

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

É possível salvar e gerenciar públicos reutilizáveis, que são grupos de segmentos de público-alvo e até mesmo outros públicos salvos, que você pode usar como destinos ou exclusões para vários posicionamentos.

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Insira um único [!UICONTROL Audience Name].

1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

   Quando você compartilha um público-alvo, o público-alvo se torna disponível como um alvo ou exclusão para todos os anunciantes na conta. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para usuários aos quais os segmentos são compartilhados. Por exemplo, se você compartilhar um público-alvo contendo segmentos do Adobe Analytics com um anunciante que não está mapeado para o mesmo [!DNL Analytics] conta, o segmento não será visualizado nesse público-alvo para esse anunciante. Somente os segmentos disponíveis para esse anunciante serão visualizados no público-alvo.

1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   >[!NOTE]
   >
   >À medida que você cria o público-alvo, [dados de tamanho do público](audience-about.md) é atualizado no painel direito

   * Para criar manualmente a lógica de segmento, usando segmentos disponíveis na [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], e [!UICONTROL Saved Audiences] guias](audience-settings.md), faça o seguinte.

      * Para adicionar o primeiro segmento, localize o segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

      * Para adicionar um segmento a um grupo de segmentos existente:

         1. Clique no grupo de segmentos no painel direito.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

            *[!UICONTROL Exclude All]* não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, crie esse público-alvo como *[!UICONTROL Include Any]* e, em seguida, em uma disposição, selecione esse público no menu Públicos-alvo excluídos.

         1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

            O grupo de segmentos é atualizado automaticamente com o novo segmento.
      * Para adicionar um novo grupo de segmentos:

         1. Clique em **[!UICONTROL + New Group]** no painel direito.

         1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para *[!UICONTROL And]* ou *[!UICONTROL Or]*, conforme necessário.

         1. Localize os segmentos para o novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.
   * Para usar a lógica de segmento de um público-alvo existente:

      1. Copie a lógica do segmento do público-alvo existente de qualquer uma das seguintes maneiras:

         * Na exibição Todos os públicos-alvo, mantenha o cursor sobre a linha de público-alvo e clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Nas configurações do público-alvo existente, na parte superior do painel lógico de segmentos, clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Em um editor de texto, crie manualmente a lógica do segmento usando IDs de segmento alfanuméricos e [Sintaxe booleana](audience-segment-logic-syntax.md), e copie-o para a área de transferência.
      1. Clique em **[!UICONTROL paste in an audience rule to begin building]**, cole a lógica do segmento existente no campo de entrada e clique em **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se o público-alvo já incluir qualquer lógica de segmento, colar em uma nova lógica de segmento substituirá a lógica existente.




1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Configurações de público](audience-settings.md)
>* [Sintaxe da lógica do segmento de público-alvo](audience-segment-logic-syntax.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar uma [!UICONTROL CCPA Opt-Out-of-Sale] Segmento](ccpa-opt-out-segment-create.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)

