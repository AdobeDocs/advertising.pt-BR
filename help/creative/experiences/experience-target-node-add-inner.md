---
title: Adicionar um nó de direcionamento entre nós em uma experiência
description: Saiba como adicionar um nó de direcionamento entre os corpos de direcionamento em uma experiência de anúncio.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
source-wordcount: '1117'
ht-degree: 0%
---
# Adicionar um nó de direcionamento entre nós em uma experiência

*Experiências somente com direcionamento de árvore de decisão*

Ao inserir um nó de destino entre níveis existentes, o novo nó de destino retém todos os destinos e criações secundários existentes, e o novo nó é chamado inicialmente de &quot;Todos&quot;. Como opção, você pode manter o novo nó sem adicionar destinos mais específicos.

Para definir um destino específico, adicione outro nó de destino irmão no mesmo nível, especifique o novo destino e atribua criações somente a esse destino. Adicionar um nó de destino irmão cria o novo nó de destino e move todos os destinos e criações filhos anteriormente atribuídos a &quot;Todos&quot; para um novo nó &quot;Tudo mais&quot; no mesmo nível. Dessa forma, a adição do novo destino não afeta as ramificações secundárias existentes, pois somente o novo nó irmão inclui as novas informações de direcionamento.

>[!NOTE]
>
>Para adicionar um nó de destino ao nível inferior de uma árvore de decisão, consulte &quot;[Adicionar um nó de destino ao nível final em uma experiência](experience-target-node-add-final.md).&quot;

## Uso do editor orientado por IA (Beta) {#ai-editor}

Enquanto você [cria](experience-create-targeting.md#ai-editor) ou [edita](experience-edit-targeting.md#ai-editor) a experiência, poderá solicitar que o agente de IA insira um nível de destino. Identifique onde inseri-lo e quais ramificações e criações existentes devem ser mantidas e revise o resultado. Para inserir o nível diretamente na tela:

1. No limite onde você deseja inserir o nível, clique em **[!UICONTROL Add targeting level]**.

   Na exibição horizontal, esse controle é um ícone com o mesmo rótulo.

1. Em **[!UICONTROL New targeting level]**, selecione a categoria de destino e clique em **[!UICONTROL Add targeting level]**.

   * Para públicos-alvo, selecione **[!UICONTROL Audience]**.

   * Para destinos geográficos, selecione uma única categoria geográfica (como **[!UICONTROL Geo: Country]**).

   * Para destinos de transmissão de dados, selecione **[!UICONTROL Data Pass]**.

   * Para redirecionar destinos de pixels, selecione **[!UICONTROL RT Pixel]**.

   * Para destinos de dispositivo, selecione uma única categoria de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   Inserir um nível não solicita valores de destino. O novo nível usa inicialmente &quot;Todos&quot; e retém os públicos-alvo e criativos secundários existentes.

1. (Opcional) Para definir um destino específico no novo nível, [adicione um nó de destino irmão](experience-target-node-add-sibling.md#ai-editor). Caso contrário, mantenha o novo nó &quot;All&quot; sem adicionar targets específicos.

1. (Opcional) Para renomear um nó de destino definido pelo usuário, clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, insira o **[!UICONTROL Node Name]** e clique em **[!UICONTROL Save]**.

   Não é possível renomear um nó &quot;Todos&quot; ou &quot;Todos os outros&quot;.

1. Revise as ramificações retidas e [atribua pacotes criativos](experience-assign-creative-bundles.md#ai-editor) a qualquer nó final novo.

1. [Salve a experiência](#save).

## Usar o editor manual {#manual-editor}

[Abra o editor manual](experience-edit-targeting.md#experience-open) antes de seguir essas etapas.

1. No nó em que você deseja inserir o destino, clique em ![Adicionar](/help/creative/assets/add.png "Adicionar") e selecione **[!UICONTROL Insert New Target]**.

1. Siga um destes procedimentos:

   * Se os nós irmãos ainda não existirem, faça o seguinte:

     1. Selecione o tipo de destino e clique em **[!UICONTROL Apply]**:

        * Para públicos-alvo, selecione **[!UICONTROL Audience]**.

        * Para destinos geográficos, selecione uma única categoria geográfica (como **[!UICONTROL Geo: Country]**).

        * Para destinos de transmissão de dados, selecione **[!UICONTROL Data Pass]**.

        * Para redirecionar destinos de pixels, selecione **[!UICONTROL RT Pixel]**.

        * Para destinos de dispositivo, selecione uma única categoria de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   * Se os nós irmãos já existirem, faça o seguinte:

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

     * Para um destino de passagem de dados, como opção, personalize a chave de passagem de dados, insira um único valor de passagem de dados e clique em **[!UICONTROL Apply]**.

       A chave de passagem de dados padrão está configurada no campo **[!UICONTROL Data Pass]**, na seção **[!UICONTROL Advanced]** das [configurações gerais de experiência](experience-settings-targeting.md). Personalize a chave do target, se necessário.

     * Para um destino de pixel de redirecionamento, selecione um único pixel de redirecionamento a ser usado e os valores de qualquer atributo de pixel necessário para mostrar as criações e clique em **[!UICONTROL Apply]**.

       Os atributos disponíveis estão configurados nas [configurações de pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

     * Para destinos de dispositivos, faça o seguinte:

       1. Selecione os alvos.

       1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

          Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados (uma instrução [!DNL Boolean] `AND`).

       1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

       1. Clique em **[!UICONTROL Apply]**.

1. (Opcional) Especifique um nome de ramificação personalizado para uma ramificação definida pelo usuário.

   Por padrão, as ramificações definidas pelo usuário são rotuladas com os destinos aplicados.

   Não é possível criar um nome de ramificação personalizado para uma ramificação &quot;Todos&quot; ou &quot;Todos os outros&quot;.

   1. Mantenha o cursor sobre o nó de destino e clique em **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Insira o **[!UICONTROL Node Name]** e clique em **[!UICONTROL Save]**.

1. (Opcional) [Atribuir pacotes criativos](experience-assign-creative-bundles.md#manual-editor) ao novo nó de destino e ao nó &quot;Todo Resto&quot;.

1. (Opcional) [Adicione um nó de destino irmão](experience-target-node-add-sibling.md#manual-editor) do tipo de destino especificado.

## Salve a experiência {#save}

As etapas a seguir se aplicam a ambos os editores.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Adicionar um nó de destino ao nível final](experience-target-node-add-final.md)
>* [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Atribuir criações a um nó final](experience-assign-creative-bundles.md)
>* [Excluir um nó de destino ou nó de folha de criação](/help/creative/experiences/experience-target-node-delete.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
