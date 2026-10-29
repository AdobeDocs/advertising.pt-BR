---
title: Gerenciar campanhas de anúncios conversacionais de [!DNL ChatGPT Ads]
description: Saiba como criar e gerenciar campanhas, grupos de anúncios e anúncios de cartão de chat do [!DNL ChatGPT Ads], um recurso beta que coloca anúncios dentro de conversas do assistente de IA.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# Gerenciar campanhas publicitárias conversacionais, grupos de anúncios e anúncios de [!DNL ChatGPT Ads]

*recurso do Beta*

Gerencie campanhas, grupos de anúncios e anúncios de cartão de chat do [!DNL ChatGPT Ads] em uma [conta de anúncios conversacionais](account-manage.md).

Você será cobrado pelo uso de [!DNL ChatGPT Ads] no final do mês com suas outras faturas. Em caso de dúvidas sobre cobrança, entre em contato com a equipe de conta da Adobe.

## A visualização [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] {#campaign-views-about}

A exibição [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] inclui três guias: [!UICONTROL Campaigns], [!UICONTROL Ad Groups] e [!UICONTROL Ads]. Cada guia lista as campanhas, grupos de anúncios ou anúncios da conta selecionada, juntamente com os dados de desempenho do intervalo de datas selecionado. Os dados de desempenho nos níveis de campanha, grupo de anúncios e anúncio incluem [!UICONTROL Impressions], [!UICONTROL Clicks], [!UICONTROL Spend], [!UICONTROL CTR], [!UICONTROL Avg CPC] e [!UICONTROL Avg CPM].

>[!NOTE]
>
>* As organizações configuradas para exibir valores de imposto em exibições de relatórios não os verão para [!DNL ChatGPT Ads]. Calcule os valores de imposto manualmente.

### Ações disponíveis

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [Criar](#campaign-create) ou [editar](#campaign-edit) uma campanha

* [Criar](#ad-group-create) ou [editar](#ad-group-edit) um grupo de anúncios para uma campanha existente

* [Crie](#ad-create) ou [edite](#ad-edit) um anúncio para um grupo de anúncios existente

* [Ativar ou pausar uma campanha, grupo de publicidade ou anúncio](#pause-activate)

* [Arquivar uma campanha, grupo de anúncios ou anúncio](#archive)

* [Detalhar de campanhas a grupos de anúncios e anúncios](#drill-down)

* [Atualizar a campanha, o grupo de publicidade ou a lista de publicidade](#refresh)

## Campanhas

### Criar uma campanha publicitária conversacional [!DNL ChatGPT Ads] {#campaign-create}

Ao criar uma campanha, você pode, opcionalmente, criar seu primeiro grupo de anúncios e anúncio. Cada etapa cria essa entidade assim que você clica em **[!UICONTROL Next]**, de modo que não é possível voltar para uma etapa anterior. Se precisar alterar algo depois, edite-a depois que o assistente for fechado.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu, clique na guia **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. No canto superior direito, clique em **[!UICONTROL Create]>[!UICONTROL Campaign]**.

1. Especifique as [configurações da campanha](#campaign-settings).

1. Clique em **[!UICONTROL Next]** para salvar as configurações da campanha.

1. Siga um destes procedimentos:

   * Se não quiser criar um grupo de anúncios para a campanha, clique em **[!UICONTROL Close]**.

     >[!TIP]
     >
     >Para criar um grupo de anúncios ou um anúncio mais tarde, consulte &quot;[Criar um grupo de anúncios](#ad-group-create)&quot; ou &quot;[Criar um anúncio](#ad-create).&quot;

   * (Opcional) Crie um grupo de anúncios:

     1. Especifique as [configurações do grupo de anúncios](#ad-group-settings).

     1. Clique em **[!UICONTROL Next]** para salvar as configurações do grupo de anúncios.

     1. (Opcional) Se não quiser criar um anúncio para a campanha, clique em **[!UICONTROL Close]**.

   * (Opcional após criar um grupo de anúncios) Crie um anúncio:

     1. Especifique as [configurações de anúncio](#ad-settings).

     1. Clique em **[!UICONTROL Create ad]**.

### Editar configurações de campanha publicitária conversacional de [!DNL ChatGPT Ads] {#campaign-edit}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu à esquerda, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. (Se necessário) Acima da tabela de dados, clique na guia **[!UICONTROL Campaigns]**.

1. Mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Edite qualquer uma das [configurações da campanha](#campaign-settings), [configurações do grupo de anúncios](#ad-group-settings) e [configurações de anúncios](#ad-settings).

1. Clique em **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] configurações de campanha publicitária conversacional {#campaign-settings}

**[!UICONTROL Campaign name]:** Um nome exclusivo para a campanha. O nome deve incluir pelo menos três caracteres.

**[!UICONTROL Campaign type]:** (Somente leitura) *Standard* é o único tipo disponível.

**[!UICONTROL Objective]:** A métrica na qual focalizar a campanha: *Alcance* ou *Cliques*. O objetivo determina o tipo de oferta para os grupos de publicidade da campanha.

**[!UICONTROL Locations]:** (Opcional) Um ou mais locais específicos para direcionamento. Para direcionar todos os locais, deixe essa configuração vazia. Para especificar um local específico, insira pelo menos duas letras que apareçam em qualquer lugar dentro do nome e clique no nome nos resultados da pesquisa.

**[!UICONTROL Budget type]:** *Orçamento diário* ou *Orçamento vitalício*.

**[!UICONTROL Budget]:** O orçamento para o tipo de orçamento especificado. O valor deve ser maior que zero (0).

**[!UICONTROL Start date]:** A data de início da campanha, no fuso horário da conta.

**[!UICONTROL Set an end date]:** (opcional) permite que você especifique uma data de término para a campanha. Ao selecionar esta opção, especifique o **[!UICONTROL End date]**.

## Grupos de anúncios

### Criar um grupo de anúncios [!DNL ChatGPT Ads] para uma campanha existente {#ad-group-create}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu, clique na guia **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. No canto superior direito, clique em **[!UICONTROL Create]>[!UICONTROL Ad Group]**.

1. Especifique as [configurações do grupo de anúncios](#ad-group-settings), incluindo a campanha pai.

1. Clique em **[!UICONTROL Create ad group]**.

## Editar um grupo de anúncios [!DNL ChatGPT Ads] {#ad-group-edit}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu à esquerda, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. Acima da tabela de dados, clique na guia **[!UICONTROL Ad Groups]**.

1. Mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Edite as configurações de [grupo de anúncios](#ad-group-settings).

1. Clique em **[!UICONTROL Save]**.

### Configurações do grupo de anúncios [!DNL ChatGPT Ads] {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Grupos de anúncios somente para campanhas existentes) A campanha à qual o grupo de anúncios pertence.

**[!UICONTROL Ad group name]:** Um nome exclusivo para o grupo de anúncios. O nome deve incluir pelo menos três caracteres.

**[!UICONTROL Maximum CPC bid]** ou **[!UICONTROL Maximum CPM bid]:** O valor máximo que você pagará por cada clique ou por 1.000 impressões. O valor deve ser maior que zero (0). O objetivo da campanha determina o campo de oferta: *Cliques* campanhas mostram **[!UICONTROL Maximum CPC bid]** e *Alcance* campanhas mostram **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Lances mais altos podem ganhar mais leilões.

**[!UICONTROL Context hints]:** (Opcional) Uma descrição das conversas, tópicos ou palavras-chave para os quais seus produtos ou serviços são relevantes. Essas dicas orientam a correspondência, mas não são regras de direcionamento de correspondência exata.

## Anúncios

### Crie um anúncio de cartão de chat [!DNL ChatGPT Ads] para um grupo de anúncios existente {#ad-create}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu, clique na guia **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. No canto superior direito, clique em **[!UICONTROL Create]>[!UICONTROL Ad]**.

1. Especifique as [configurações de anúncios](#ad-settings), incluindo a campanha pai e o grupo de anúncios.

1. Clique em **[!UICONTROL Create ad]**.

## Editar um anúncio de cartão de chat do [!DNL ChatGPT Ads] {#ad-edit}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu à esquerda, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. Acima da tabela de dados, clique na guia **[!UICONTROL Ads]**.

1. Mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Edite as configurações de [ad](#ad-settings).

1. Clique em **[!UICONTROL Save]**.

### Configurações de anúncio de cartão de chat do [!DNL ChatGPT Ads] {#ad-settings}

**[!UICONTROL Parent campaign]** e **[!UICONTROL Parent ad group]:** (Anúncios somente em grupos de anúncios existentes) A campanha e o grupo de anúncios aos quais o anúncio pertence.

**[!UICONTROL Ad name]:** Um nome exclusivo para o anúncio. O nome deve incluir pelo menos três caracteres.

**[!UICONTROL Ad URL (Link)]:** A URL da página de aterrissagem, iniciando com `http://` ou `https://`.

**[!UICONTROL Title (headline)]:** O título do anúncio. O título deve ter entre 3 e 50 caracteres. **Observação:** o título pode estar truncado em alguns tipos de posicionamento.

**[!UICONTROL Description]:** O texto do corpo do anúncio. A descrição deve ter entre 3 e 100 caracteres.

**[!UICONTROL Ad image]:** Uma imagem JPG ou PNG para incluir no anúncio. Para carregar uma imagem, clique em (novos anúncios) **[!UICONTROL Upload image (PNG/JPG)]** ou **[!UICONTROL Change image]** e localize e selecione um arquivo em seu dispositivo ou rede.

**[!UICONTROL Preview]:** Uma visualização do anúncio, com base nas configurações do anúncio.

## Ativar ou pausar uma campanha, grupo de publicidade ou anúncio [!DNL ChatGPT Ads] {#pause-activate}

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu à esquerda, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. Na guia **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, localize a linha.

1. Na coluna **[!UICONTROL Active]**, siga um destes procedimentos:

   * Para ativar um item pausado, ative o alternador (à direita).

   * Para pausar um item ativo, desative o botão de alternância (à esquerda).

## Arquivar uma campanha, grupo de anúncios ou anúncio de [!DNL ChatGPT Ads] {#archive}

O arquivamento remove permanentemente a campanha, grupo de anúncios ou anúncio das exibições [!UICONTROL Conversational Ads].

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. No submenu à esquerda, clique em **[!UICONTROL Campaigns]**.

1. No canto superior direito, selecione um anunciante e uma conta [!DNL ChatGPT Ads].

1. Na guia **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, mantenha o cursor sobre a linha e clique em **[!UICONTROL ...]>[!UICONTROL Archive]**.

## Detalhar campanhas de [!DNL ChatGPT Ads] para grupos de anúncios e anúncios {#drill-down}

* Clique em uma linha de campanha para exibir apenas seus grupos de anúncios na guia **[!UICONTROL Ad Groups]** ou clique em uma linha de grupo de anúncios para exibir apenas seus anúncios na guia **[!UICONTROL Ads]**.

Para remover o filtro e ver todas as linhas no modo de exibição, clique em **X** no filtro acima da tabela de dados.

## Atualizar a campanha, o grupo de publicidade ou a lista de publicidade {#refresh}

Exibe novamente a lista de campanhas, grupos de anúncios ou anúncios quando outros usuários podem ter feito alterações ou adições.

1. No menu principal, clique em **[!UICONTROL Conversational Ads Beta]**.

1. Na exibição **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, clique em **[!UICONTROL Refresh]** acima da tabela de dados.

>[!MORELIKETHIS]
>
>* [Gerenciar contas de anúncios conversacionais](account-manage.md)
