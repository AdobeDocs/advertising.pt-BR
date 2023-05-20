---
title: Editar um público-alvo reutilizável
description: Saiba como editar um público-alvo reutilizável.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Editar um público-alvo reutilizável

Ao editar um público usado em qualquer disposição ou outro público reutilizável, as alterações são aplicadas imediatamente a esses posicionamentos e públicos.<!-- verify -->

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Mantenha o cursor sobre a linha de público-alvo e clique **[!UICONTROL Edit]**.

1. Edite as configurações do público-alvo de qualquer uma das seguintes maneiras:

   >[!NOTE]
   >
   >Se você editar a lógica do segmento de público-alvo, [dados de tamanho do público](audience-about.md) é atualizado no painel direito.

   * (Opcional) Para editar a variável **[!UICONTROL Audience Name]** click ![Editar](/help/dsp/assets/edit.png) ao lado do nome do público-alvo, insira um nome de público-alvo exclusivo e clique em **[!UICONTROL Apply]**.

   * (Opcional) Para editar manualmente a lógica do segmento, usando segmentos disponíveis na [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments], e [!UICONTROL Saved Audiences] guias](audience-settings.md), faça o seguinte.

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





1. Clique em **[!UICONTROL Save]**.

1. Na mensagem de confirmação, clique em **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de público-alvo](audience-about.md)
>* [Criar um público-alvo reutilizável](reusable-audience-create.md)
>* [Duplicar um público-alvo reutilizável](reusable-audience-duplicate.md)
>* [Exibir detalhes sobre um público-alvo reutilizável](reusable-audience-view-details.md)
>* [Compartilhar um público-alvo reutilizável](reusable-audience-share.md)
>* [Exportar um público-alvo reutilizável](reusable-audience-export.md)
>* [Copiar a chave de segmento de um público-alvo reutilizável para a área de transferência](reusable-audience-clipboard.md)
>* [Excluir um público-alvo reutilizável](reusable-audience-delete.md)
>* [Configurações de público](audience-settings.md)
>* [Sintaxe da lógica do segmento de público-alvo](audience-segment-logic-syntax.md)
>* [Provedores de dados de terceiros disponíveis](third-party-data-providers.md)

