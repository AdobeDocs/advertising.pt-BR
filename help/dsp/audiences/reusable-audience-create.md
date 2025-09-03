---
title: Criar um público-alvo reutilizável
description: Saiba como criar públicos-alvo reutilizáveis que consistem em segmentos de público-alvo e outros públicos-alvo salvos.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Criar um público-alvo reutilizável

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

É possível salvar e gerenciar públicos reutilizáveis, que são grupos de segmentos de público-alvo e até mesmo outros públicos salvos, que você pode usar como destinos ou exclusões para vários posicionamentos.

>[!NOTE]
>
>(Anunciantes para os quais o DSP converte IDs de email com hash em segmentos LiveRamp RampID) Os segmentos primários RampID que não são anexados a uma inserção ativa, programada ou pausada são pausados. O segmento é descrito na lista de segmentos como &quot;Pausado automaticamente&quot;.

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Digite um **[!UICONTROL Audience Name]** exclusivo.

1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

   Quando você compartilha um público-alvo, o público-alvo se torna disponível como um alvo ou exclusão para todos os anunciantes na conta. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para usuários aos quais os segmentos são compartilhados. Por exemplo, se você compartilhar um público contendo segmentos do Adobe Analytics com um anunciante que não está mapeado para a mesma conta [!DNL Analytics], o segmento não será visualizado nesse público para esse anunciante. Somente os segmentos disponíveis para esse anunciante são visualizados no público-alvo.

1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   >[!NOTE]
   >
   >À medida que você cria o público-alvo, os [dados detalhados sobre o tamanho do público-alvo](audience-about.md) são atualizados no painel direito

   * Para criar manualmente a lógica do segmento, usando segmentos disponíveis nas guias [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] e [!UICONTROL Saved Audiences]](audience-settings.md), faça o seguinte.

      * Para adicionar o primeiro segmento, localize o segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

      * Para adicionar um segmento a um grupo de segmentos existente:

         1. Clique no grupo de segmentos no painel direito.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

            *[!UICONTROL Exclude All]* não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, crie esse público-alvo como *[!UICONTROL Include Any]* e, em seguida, em um posicionamento, selecione esse público-alvo no menu Públicos-alvo excluídos.

         1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

            O grupo de segmentos é atualizado automaticamente com o novo segmento.

      * Para adicionar um novo grupo de segmentos:

         1. Clique em **[!UICONTROL + New Group]** no painel direito.

         1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para *[!UICONTROL And]* ou *[!UICONTROL Or]*, conforme necessário.

         1. Localize os segmentos para o novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

         1. (Opcional) Altere a lógica do grupo para *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, conforme necessário.

   * Para usar a lógica de segmento de um público-alvo existente:

      1. Copie a lógica do segmento do público-alvo existente de qualquer uma das seguintes maneiras:

         * Na exibição Todos os Públicos-alvo, mantenha o cursor sobre a linha de público-alvo e clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Nas configurações para o público existente, na parte superior do painel lógico do segmento, clique em **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Em um editor de texto, crie manualmente a lógica do segmento usando IDs de segmento alfanuméricos e [sintaxe booleana](audience-segment-logic-syntax.md), e copie-a para a área de transferência.

      1. Clique em **[!UICONTROL paste in an audience rule to begin building]**, cole a lógica de segmento existente no campo de entrada e clique em **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Se o público-alvo já incluir qualquer lógica de segmento, colar em uma nova lógica de segmento substituirá a lógica existente.

1. Clique em **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Público-Alvo](audience-about.md)
>* [Configurações de público-alvo](audience-settings.md)
>* [Sintaxe da lógica do segmento de público-alvo](audience-segment-logic-syntax.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)
>* [Criar e implementar um segmento personalizado](custom-segment-create.md)
>* [Criar e implementar um [!UICONTROL CCPA Opt-Out-of-Sale] segmento](ccpa-opt-out-segment-create.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
