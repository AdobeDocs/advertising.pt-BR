---
title: Criar uma meta personalizada
description: Criar uma meta personalizada
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Criar uma meta personalizada

Você pode criar metas personalizadas como *objetivos* no prazo de [!DNL Advertising Search, Social, & Commerce].

Para criar uma meta personalizada, a conta do DSP deve estar vinculada a um [!DNL Search, Social, & Commerce] com a mesma ID de organização da Adobe Experience Cloud, de dentro do [!DNL Search, Social, & Commerce] configurações do cliente. Se sua conta do DSP não estiver vinculada a um [!DNL Search, Social, & Commerce] , entre em contato com a equipe da sua conta Adobe.

>[!TIP]
>
>Consulte a [práticas recomendadas para criar metas personalizadas](custom-goal-best-practices.md) para obter dicas sobre como configurar suas metas personalizadas.

1. Efetue logon no [!DNL Advertising Search, Social, & Commerce] at (usuários na América do Norte) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (todos os outros usuários) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Verifique se as métricas que você deseja incluir em sua meta foram rastreadas, estão disponíveis no produto e incluem um nome de exibição:
   1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. Localize a métrica e verifique se **[!UICONTROL Show in UI and Reports]** está ativado para a métrica.
   1. Se a métrica não tiver um valor no campo **[!UICONTROL Display Name]** , clique na célula, digite o nome de exibição e clique em **[!UICONTROL Apply].**
1. Criar a meta personalizada como um *objetivo*:
   1. No menu principal, clique em **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Na barra de ferramentas, clique em **[!UICONTROL Create objective].**
   1. Insira as configurações de objetivo:
      1. No **[!UICONTROL Change Objective Name]** insira o nome do objetivo.

         O nome do objetivo será mostrado no campo [!UICONTROL Custom Goals] nas configurações do pacote DSP.

      1. Associar propriedades ao objetivo:

         >[!NOTE]
         >
         > Todas as métricas de conversão rastreadas para o anunciante são listadas por padrão no [!UICONTROL Available Properties] lista.

         * Para importar um arquivo CSV com métricas de conversão e seus pesos, clique em **[!UICONTROL Import]** e localize o arquivo a ser importado.

           As métricas de conversão importadas já devem existir para o anunciante; os nomes não diferenciam maiúsculas de minúsculas.

           As métricas de conversão importadas substituem todas as propriedades existentes especificadas.

         * Para especificar manualmente a primeira métrica de conversão com o peso padrão (1), selecione em uma lista de todas as métricas de conversão rastreadas para o anunciante.

         * Para adicionar outra métrica de conversão manualmente com o peso padrão (1), clique em **[!UICONTROL +]** .

           >[!TIP]
           >
           > Para procurar uma métrica na lista, insira uma string de qualquer lugar dentro do nome da métrica.

         * Para adicionar manualmente várias métricas de conversão, clique em **[!UICONTROL Add Multiple Properties].** Para cada métrica de conversão que deseja adicionar, clique no nome da métrica no [!UICONTROL Available Properties] e arraste-a para a [!UICONTROL Added Properties] coluna. Quando terminar de adicionar métricas, clique em **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Para procurar uma métrica na lista, insira uma string de qualquer lugar dentro do nome da métrica no campo de entrada.
           >* Para filtrar a lista para excluir métricas que são excluídas em relatórios, selecione a opção **[!UICONTROL Hide properties excluded from reports].**

         * (Quando o objetivo contiver várias métricas de conversão) Para alterar o peso de uma métrica em relação às outras métricas do objetivo, insira valores na variável **[!UICONTROL Weight]** campo(s)

      1. Na parte inferior das configurações, clique em **[!UICONTROL Save]**.

Depois de criar um objetivo, você pode atribuí-lo a um pacote DSP como uma meta personalizada quando a meta de otimização terminar com &quot;[!UICONTROL - Custom Goal]&quot; (como &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;).

>[!TIP]
>
>Para obter o desempenho ideal, as métricas combinadas na meta personalizada (objetivo) devem totalizar pelo menos dez conversões por dia. Caso contrário, a prática recomendada é adicionar outras métricas de conversão de suporte, como páginas de produtos ou inícios de aplicativos, ao objetivo. Consulte [Práticas recomendadas para a criação de uma meta personalizada](custom-goal-best-practices.md) para obter diretrizes.

>[!MORELIKETHIS]
>
>* [Sobre metas personalizadas](custom-goal-about.md)
>* [Práticas recomendadas para a criação de uma meta personalizada](custom-goal-best-practices.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
> * [Como o DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
