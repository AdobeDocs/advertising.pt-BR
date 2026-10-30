---
title: Adicionar um nó de destino irmão entre nós em uma experiência
description: Saiba como adicionar um nó irmão a qualquer nó que tenha um destino ou esteja no mesmo nível que um nó com um destino.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: 'https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%
---
# Adicionar um nó de destino irmão entre nós em uma experiência

*Experiências somente com direcionamento de árvore de decisão*

Você pode adicionar um nó irmão a qualquer nó que tenha um destino ou esteja no mesmo nível que um nó com um destino.

## Uso do editor orientado por IA (Beta) {#ai-editor}

Ao [criar](experience-create-targeting.md#ai-editor) ou [editar](experience-edit-targeting.md#ai-editor) a experiência, você pode descrever o novo destino irmão para o agente de IA. Identifique a ramificação principal e os valores de destino e revise o resultado. Para adicionar o irmão diretamente na tela:

1. Mantenha o cursor sobre o pai dos nós no nível em que deseja outro irmão e clique em **[!UICONTROL +]**.

   A categoria de destino é determinada pelo nível existente e o seletor de valor é aberto para essa categoria.

1. Especifique os valores de destino para a categoria:

   * Para públicos-alvo:

     * Para adicionar o primeiro segmento, localize e selecione o segmento de público-alvo.

     * Para adicionar segmentos a um grupo de segmentos existente:

       1. Selecione o grupo de segmentos.

       1. (Opcional) Altere a lógica do grupo para **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, conforme necessário.

          **[!UICONTROL Include Any]** corresponde usuários em pelo menos um segmento selecionado; **[!UICONTROL Include All]** requer associação em todos os segmentos selecionados.

          **[!UICONTROL Exclude All]** não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, compile o público-alvo usando o **[!UICONTROL Include Any]** e, em seguida, exclua esse público-alvo quando adicioná-lo a um posicionamento no DSP.

       1. Localize e selecione os segmentos adicionais.

     * Para adicionar um novo grupo de segmentos:

       1. Adicione um grupo.

       1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para **[!UICONTROL And]** ou **[!UICONTROL Or]**, conforme necessário.

          **[!UICONTROL And]** exige que os usuários atendam às condições de ambos os grupos; **[!UICONTROL Or]** exige que eles atendam às condições de pelo menos um grupo.

       1. Localize e selecione os segmentos para o novo grupo.

       1. (Opcional) Altere a lógica do grupo para **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, conforme necessário.

   * Para públicos-alvo geográficos:

     * Selecione os locais dentro da categoria geográfica no nível existente, como países, regiões ou cidades.

     * Para alvos de código postal, selecione o país e informe os códigos postais a serem incluídos. Para inserir vários códigos postais em massa, separe-os com vírgulas ou coloque cada código em uma linha separada.

   * Para públicos-alvo de transmissão de dados, insira a chave e o valor a serem correspondidos.

     A chave de passagem de dados padrão está configurada no campo **[!UICONTROL Data Pass]**, na seção **[!UICONTROL Advanced]** das [configurações gerais de experiência](experience-settings-targeting.md). Personalize a chave do target, se necessário.

   * Para destinos de pixel de redirecionamento, selecione o pixel de redirecionamento e especifique os valores para os atributos de pixel necessários para mostrar as criações.

     Os atributos disponíveis estão configurados nas [configurações de pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para destinos de dispositivos, selecione os valores na categoria de dispositivos no nível existente: tipos de dispositivos, sistemas operacionais ou navegadores.

1. (Se disponível; opcional) Selecione **[!UICONTROL Split Nodes]** para criar um nó de destino separado para cada valor selecionado, com suas próprias atribuições de conjunto criativo. Caso contrário, os valores selecionados serão agrupados em um nó de destino.

1. Clique em **[!UICONTROL Add Node]**.

1. (Opcional) Para renomear o novo nó, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, insira o **[!UICONTROL Node Name]** e clique em **[!UICONTROL Save]**.

1. [Atribuir pacotes criativos](experience-assign-creative-bundles.md#ai-editor) se o novo nó for um nó final, e [salvar a experiência](#save).

## Usar o editor manual {#manual-editor}

[Abra o editor manual](experience-edit-targeting.md#experience-open) antes de seguir essas etapas.

1. Acima do nó ao qual você deseja adicionar o nó irmão, clique em ![Adicionar](/help/creative/assets/add.png "Adicionar") e selecione **[!UICONTROL Insert Sibling Target]**.

1. Especifique os valores de destino para a categoria:

   * Para públicos-alvo:

     1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções de **[!UICONTROL Audience Targeting]**.

     1. Configure os segmentos e grupos de público-alvo:

        * Para adicionar o primeiro segmento, localize o segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento.

        * Para adicionar segmentos a um grupo de segmentos existente:

          1. Clique no grupo de segmentos no painel direito.

          1. (Opcional) Altere a lógica do grupo para **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, conforme necessário.

             **[!UICONTROL Include Any]** corresponde usuários em pelo menos um segmento selecionado; **[!UICONTROL Include All]** requer associação em todos os segmentos selecionados.

             **[!UICONTROL Exclude All]** não está disponível para o primeiro grupo de segmentos. Para um público-alvo que inclua apenas exclusões, compile o público-alvo usando o **[!UICONTROL Include Any]** e, em seguida, exclua esse público-alvo quando adicioná-lo a um posicionamento no DSP.

          1. Localize o novo segmento no painel esquerdo e marque a caixa de seleção ao lado do nome do segmento. Repita o procedimento para cada segmento adicional.

             O grupo de segmentos é atualizado automaticamente com os novos segmentos.

        * Para adicionar um novo grupo de segmentos:

          1. Clique em **[!UICONTROL + New Group]** no painel direito.

          1. (Opcional) Altere a lógica entre o grupo anterior e o novo grupo para **[!UICONTROL And]** ou **[!UICONTROL Or]**, conforme necessário.

             **[!UICONTROL And]** exige que os usuários atendam às condições de ambos os grupos; **[!UICONTROL Or]** exige que eles atendam às condições de pelo menos um grupo.

          1. Localize os segmentos para o novo grupo no painel esquerdo e marque as caixas de seleção ao lado dos nomes dos segmentos.

          1. (Opcional) Altere a lógica do grupo para **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**, conforme necessário.

     1. Clique em **[!UICONTROL Create]**.

     1. Clique em **[!UICONTROL Apply]**.

   * Para públicos-alvo geográficos, faça o seguinte:

     1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções de [!UICONTROL Geo Targeting], especifique um ou mais dos destinos geográficos e clique em **[!UICONTROL Save]**.

        Os destinos de CEP têm opções de edição em massa. Para colar vários códigos postais, clique na guia **[!UICONTROL Paste postal codes]**, selecione o país, cole ou insira códigos postais separados por vírgulas ou em linhas separadas e clique em **[!UICONTROL Include All]**. Para remover um destino de código postal incluído, mantenha o cursor sobre o destino e clique em ![Remover](/help/creative/assets/delete.png "Remover") **[!UICONTROL Remove]**.

     1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

        Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados (uma instrução [!DNL Boolean] `AND`).

     1. Clique em **[!UICONTROL Apply]**.

   * Para destinos de passagem de dados, como opção, personalize a chave de passagem de dados, insira um único valor de passagem de dados e clique em **[!UICONTROL Apply]**.

     A chave de passagem de dados padrão está configurada no campo **[!UICONTROL Data Pass]**, na seção **[!UICONTROL Advanced]** das [configurações gerais de experiência](experience-settings-targeting.md). Personalize a chave do target, se necessário.

   * Para destinos de pixel de redirecionamento, selecione o pixel de redirecionamento a ser usado e os valores necessários para qualquer atributo de pixel que deve estar presente para mostrar as criações. Depois clique em **[!UICONTROL Apply]**.

     Os atributos disponíveis estão configurados nas [configurações de pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para destinos de dispositivos, faça o seguinte:

     1. Selecione os alvos.

     1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

        Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados (uma instrução [!DNL Boolean] `AND`).

     1. Clique em **[!UICONTROL Apply]**.

1. (Opcional) Especifique um nome de ramificação personalizado para uma ramificação definida pelo usuário.

   Por padrão, as ramificações definidas pelo usuário são rotuladas com os destinos aplicados.

   Não é possível criar um nome de ramificação personalizado para uma ramificação &quot;Todos&quot; ou &quot;Todos os outros&quot;.

   1. Mantenha o cursor sobre o nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Insira o **[!UICONTROL Node Name]** e clique em **[!UICONTROL Save]**.

1. (Opcional) [Atribuir pacotes criativos](experience-assign-creative-bundles.md#manual-editor) ao novo nó de destino.

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Adicionar um nó de destino ao nível final](experience-target-node-add-final.md)
>* [Inserir um nó de destino entre nós](experience-target-node-add-inner.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Atribuir criações a um nó final](experience-assign-creative-bundles.md)
>* [Excluir um nó de destino ou nó de folha de criação](/help/creative/experiences/experience-target-node-delete.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
