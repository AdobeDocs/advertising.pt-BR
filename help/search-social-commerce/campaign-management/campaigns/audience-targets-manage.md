---
title: Gerenciar metas de público-alvo para campanhas e grupos de anúncios
description: Saiba como configurar e gerenciar metas de público-alvo para suas [!DNL Google Ads] e [!DNL Microsoft Advertising] campanhas e grupos de anúncios.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Gerencie metas de público para suas campanhas e grupos de anúncios do [!DNL Google Ads] e do [!DNL Microsoft Advertising]

*[!DNL Google Ads]e [!DNL Microsoft Advertising] somente*

[!DNL Google Ads] campanhas e grupos de anúncios, e [!DNL Microsoft Advertising] grupos de anúncios, podem direcionar públicos-alvo específicos da mesma rede de anúncios. A rede de anúncios determina o tamanho que um público-alvo deve ter para ser direcionado.

>[!NOTE]
>
>As exclusões sempre substituem as inclusões/metas.

Você pode configurar direcionamentos de público-alvo, editar os modificadores de lances para públicos-alvo e alterar o status dos direcionamentos de público-alvo.

## Configurar públicos-alvo

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Na barra de ferramentas acima da tabela de dados, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").

1. Selecione a rede de publicidade e o nome da conta e clique em **[!UICONTROL Continue]**.

1. Configure as metas de público-alvo para campanhas e grupos de anúncios específicos:

   1. Selecione os públicos-alvo aplicáveis à rede de anúncios especificada.

      Como opção, você pode pesquisar públicos-alvo que contenham uma sequência de texto específica com no mínimo três caracteres. Para qualquer público correspondente, clique em **[!UICONTROL Include]** para selecioná-lo.

      [!DNL Google Ads] públicos-alvo de correspondência do cliente estão disponíveis somente para campanhas de pesquisa e compras.

   1. Especifique os destinos:

      1. (Opcional) Para expandir uma campanha para seus grupos de anúncios secundários, clique no nome da campanha.

      1. (Opcional) Para filtrar uma lista de campanhas ou lista de grupos de anúncios por uma sequência de caracteres de texto incluída no nome, clique em ![Filtro](/help/search-social-commerce/assets/filter.png "Filtro") , insira ou cole a sequência de caracteres de texto no campo de entrada e pressione a tecla **[!UICONTROL Enter]**.

      1. Especifique cada campanha e público alvo do grupo de anúncios da rede de anúncios especificada clicando no círculo vazio adjacente para que uma marca de seleção azul (![Selecionar](/help/search-social-commerce/assets/include.png "Selecionar")) seja exibida.

      Você não pode configurar um público-alvo para uma campanha principal e para um grupo de anúncios secundário (que usa o público-alvo automaticamente).

1. Clique em **[!UICONTROL Post]**.

1. (Opcional) Defina um ajuste de oferta para o público alvo de uma das seguintes maneiras a partir da exibição [!UICONTROL Targets]:

   * Clique na coluna **[!UICONTROL Bid Adjustment]** e insira um valor.

   * Marque a caixa de seleção ao lado da linha de destino. Na barra de ferramentas, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar"), insira o modificador de oferta e clique em **[!UICONTROL Post]**.

   Os valores podem incluir:

   * *0%:* Para não ajustar ofertas para anúncios para este público-alvo.

   * /[*Outros valores de -90% a 900%*/]: para aumentar ou diminuir a oferta de anúncios para este público-alvo. Por exemplo, se o lance no nível da palavra-chave for 1 USD e o ajuste de lance para uma meta de público-alvo específica for 50%, o lance para esse público-alvo aumentará para 1,50 USD.

## Editar o modificador de oferta para públicos alvo

Você pode alterar o modificador de oferta e o status das metas de público-alvo para todos os tipos de público-alvo, exceto para públicos-alvo no mercado.

>[!NOTE]
>
>O Search, Social e Commerce otimiza automaticamente o modificador de oferta quando a campanha principal usa a estratégia de oferta CPC e está em um portfólio configurado para otimizar automaticamente os valores de ajuste de oferta para metas de público-alvo.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Siga um destes procedimentos:

   * Para editar um modificador de oferta para um público alvo, clique na coluna **[!UICONTROL Bid Adjustment]** e edite o ajuste de oferta.

   * Para editar um modificador de lance para um ou mais targets, faça o seguinte:

      1. Marque a caixa de seleção ao lado de cada target a ser editado.

         Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Na barra de ferramentas acima da tabela, clique em ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

      1. Edite os campos **[!UICONTROL Bid Modifier]** e/ou **[!UICONTROL Status]**.

         Para o campo [!UICONTROL Bid Modifier], você tem opções para alterar valores existentes para um valor especificado ou para aumentar ou diminuir o valor por uma porcentagem especificada ou valor monetário, com um limite.

         Para um valor definido, o valor pode incluir:

         * *0%:* Para não ajustar ofertas para anúncios para este público-alvo.

         * /[*Outros valores de -90% a 900%*/]: para aumentar ou diminuir a oferta de anúncios para este público-alvo. Por exemplo, se o lance no nível da palavra-chave for 1 USD e o ajuste de lance para uma meta de público-alvo específica for 50%, o lance para esse público-alvo aumentará para 1,50 USD.

         Para vários alvos, as alterações são aplicadas a todos os alvos selecionados.

      1. (Opcional) Clique em **[!UICONTROL Additional Details]** e, opcionalmente, insira um nome e uma descrição para o projeto.

      1. Clique em **[!UICONTROL Post]**.

## Alterar o status dos públicos-alvo

Você pode pausar um público-alvo ativo para desativar a licitação. Posteriormente, é possível retomar o lance alterando o status para ativo.

Você também pode excluir um público-alvo de pesquisa ativo ou pausado.

1. No menu principal, clique em **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Nos submenus, clique em **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Opcional) Filtre a lista para incluir públicos-alvo específicos.

1. Marque a caixa de seleção ao lado de cada target de público-alvo cujo status você deseja alterar.

   Para obter dicas sobre como selecionar várias linhas, consulte &quot;[Selecionar várias linhas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Na barra de ferramentas, clique no botão de status:

   * Para ativar as linhas, clique em ![Ativar](/help/search-social-commerce/assets/activate.png "Ativar").

   * Para pausar as linhas, clique em ![Pausar](/help/search-social-commerce/assets/pause.png "Pausar").

   * Para excluir as linhas, clique em ![Mais ações](/help/search-social-commerce/assets/more.png "Mais ações") e selecione **[!UICONTROL Delete]**. Na mensagem de confirmação, clique em **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Sobre públicos-alvo](audience-about.md)
>* [Gerenciar exclusões de público alvo para campanhas e grupos de anúncios](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
