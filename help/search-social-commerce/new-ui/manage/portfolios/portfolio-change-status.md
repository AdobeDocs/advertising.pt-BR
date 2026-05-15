---
title: (Nova interface) Alterar o status de um portfólio
description: Saiba como alterar o status de um portfólio ou excluir um portfólio inativo.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# (Nova interface) Alterar o status de um portfólio

*recurso do Beta*

O status de um portfólio pode ser um dos seguintes:

* **Inativo:** o recurso de otimização está coletando dados de custo/clique/impressão para as campanhas relevantes para fins de relatório, mas não está modelando os dados nem otimizando orçamentos e ofertas de campanha.

* **Ativo:** o recurso de otimização está coletando dados de custo/clique/impressão e dados de receita para as campanhas relevantes e está modelando os dados, mas não está otimizando orçamentos de campanha ou lances. Ative um portfólio inativo para começar a modelar dados ou faça downgrade de um portfólio otimizado para o estado ativo para interromper a otimização.

* **Otimizado:** o recurso de otimização está coletando dados de custo/clique/impressão e dados de receita para as campanhas relevantes, modelando os dados e otimizando orçamentos e ofertas de campanha (quando relevante) na data de início do portfólio designada. Alterar o status para otimizado também é chamado de lançamento do portfólio.

Para interromper a coleta de dados de custo/clique/impressão e dados de receita para as campanhas relevantes, exclua o portfólio. A exclusão de um portfólio o torna indisponível no Search, Social e Commerce.

Todas as alterações no status do portfólio são registradas no histórico de alterações do portfólio.

## Otimizar, ativar ou desativar um portfólio

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenha o cursor sobre a linha do portfólio e clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar") ao lado de [!UICONTROL Portfolio Status].

1. Alterar o status:

   * Para ativar um portfólio inativo ou otimizado, selecione **[!UICONTROL Active]**.

   * Para desativar um portfólio ativo, selecione **[!UICONTROL Inactive]**.

   * Para otimizar (iniciar) um portfólio ativo, selecione **[!UICONTROL Optimized]**.

     >[!NOTE]
     >
     >* Você só poderá iniciar um portfólio se ele já estiver ativo e contiver pelo menos uma campanha ativa com pelo menos um anúncio ativo e palavra-chave/posicionamento.
     >* Antes de iniciar um portfólio, você deve implementar as tags de rastreamento de conversão nas páginas da Web do anunciante.
     >* Antes de iniciar um portfólio, a prática recomendada é executar uma análise de linha de base.
     >* Se você estiver lançando um novo portfólio, verifique se a data de início é hoje ou posterior.>* Evite alterar o portfólio na primeira semana após o lançamento, mesmo que o desempenho seja volátil.
     >* Depois que a Pesquisa, o Social e o Commerce começarem a otimizar um portfólio, você deverá permitir que ele gerencie todas as alterações de oferta futuras (quando aplicável). Search, Social e Commerce substituirão todas as alterações feitas na rede de anúncios.
     >* Depois de iniciar um portfólio, você pode definir lances manuais temporariamente para qualquer campanha CPC no portfólio, criando e publicando bulksheets de campanha. Quaisquer alterações de lance resultantes dos dados publicados são aplicáveis por um dia. Depois disso, o Search, Social e Commerce retoma a definição de ofertas de acordo com sua própria estratégia de otimização.

## Excluir um portfólio inativo

Você pode excluir apenas portfólios inativos. Se o portfólio estiver otimizado ou ativo, altere primeiro seu status para inativo antes de ter a opção de excluí-lo.

1. No menu principal, clique em **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Siga um destes procedimentos:

   * Mantenha o cursor sobre a linha do portfólio e clique em **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Marque a caixa de seleção ao lado do portfólio. Na barra de ferramentas de ações em massa, clique em ![Excluir](/help/search-social-commerce/assets/delete-new.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Criar um portfólio](portfolio-create.md)
>* [(Nova interface do usuário) Editar um portfólio](portfolio-edit.md)
>* [Sobre portfólios](portfolio-about.md)
