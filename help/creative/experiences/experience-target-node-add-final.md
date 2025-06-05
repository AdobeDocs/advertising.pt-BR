---
title: Adicionar um nó de direcionamento ao nível final em uma experiência
description: Saiba como adicionar um nó de direcionamento ao nível de destino final de uma experiência de anúncio.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: 9f93990bcd6b3c8f7d6fb29186da620ac6d4ecf5
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Adicionar um nó de direcionamento ao nível final em uma experiência

*Experiências somente com direcionamento de árvore de decisão*
*Beta fechado*

Ao adicionar um nó de destino ao nível mais baixo da experiência, seja o nó &quot;All&quot; raiz, um nó específico do destino ou um nó &quot;Everything Else&quot;, você define o destino diretamente e não precisa criar um nó irmão. Adicionar um nó de nível inferior cria o nó de destino e um nó &quot;Everything Else&quot; adicional no mesmo nível.

>[!NOTE]
>
>Para inserir um nó de destino entre níveis existentes de uma árvore decisória, consulte &quot;[Inserir um nó de destino entre nós em uma experiência](experience-target-node-add-inner.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. No nó em que você deseja inserir o destino, clique em ![Adicionar](/help/creative/assets/add.png "Adicionar") e selecione **[!UICONTROL Insert New Target]**.

1. Especifique os destinos:

   * Para públicos-alvo da Adobe, selecione **[!UICONTROL Adobe Audience]** e faça o seguinte:

      1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções do [!UICONTROL Audience Targeting], abra a guia **[!UICONTROL Adobe Segments]**, especifique um ou mais dos destinos de público-alvo [!DNL Adobe] do anunciante e clique em **[!UICONTROL Create]**.

      1. (Opcional) Para criar vários nós de destino quando vários públicos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada público-alvo especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os públicos especificados.

      1. Clique em **[!UICONTROL Apply]**.

   * Para destinos geográficos, selecione uma única categoria geográfica (como [!UICONTROL Geo: Country]) e faça o seguinte:

      1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções de [!UICONTROL Geo Targeting], especifique um ou mais dos destinos geográficos e clique em **[!UICONTROL Save]**.

         Os destinos de CEP têm opções de edição em massa. Para colar vários códigos postais, clique na guia **[!UICONTROL Paste postal codes]**, selecione o país, cole ou insira códigos postais separados por vírgulas ou em linhas separadas e clique em **[!UICONTROL Include All]**. Para remover um destino de código postal incluído, mantenha o cursor sobre o destino e clique em ![Remover](/help/creative/assets/delete.png "Remover") **[!UICONTROL Remove]**.

      1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados.

      1. Clique em **[!UICONTROL Apply]**.

   * Para um destino de passagem de dados, selecione **[!UICONTROL Data Pass]**, como opção, personalize a chave de passagem de dados, insira um único valor de passagem de dados e clique em **[!UICONTROL Apply]**.

   Um valor padrão para a chave no par chave-valor já está definido no campo **[!UICONTROL Data Pass]** na seção [!UICONTROL Advanced] das [configurações de experiência](experience-settings-targeting.md). Opcionalmente, é possível personalizar a chave.

   * Para um destino de pixel de redirecionamento, selecione **[!UICONTROL RT Pixel]**, selecione um único pixel de redirecionamento a ser usado e os valores de qualquer atributo de pixel necessário para mostrar as criações e clique em **[!UICONTROL Apply]**.

     Os atributos do pixel de redirecionamento estão configurados nas [configurações do pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

   * Para destinos de dispositivos, faça o seguinte:

      1. Selecione uma única categoria de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**) e selecione os destinos.

      1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados.

      1. Clique em **[!UICONTROL Apply]**.

1. Siga um destes procedimentos:

   * (Opcional) [Atribuir criativos](experience-assign-creative-bundles.md) ao novo nó de destino e ao nó &quot;Todo Resto&quot;.

   * (Opcional) Para salvar a experiência:

      1. Clique em **[!UICONTROL Save]** e depois em **[!UICONTROL OK]**.

      1. (Se cada nó no nível mais inferior não incluir pelo menos um criativo): Siga um destes procedimentos:

         * Para salvar a experiência sem todos os pacotes criativos necessários, clique em **[!UICONTROL Save as Draft]**.

           Não é possível criar uma tag de anúncio para uma experiência de rascunho.

         * Para atribuir o criativo padrão a cada destino que ainda não recebeu um pacote criativo, clique em **[!UICONTROL Assign Default Creatives]**. Depois de revisar a árvore atualizada com os criativos padrão atribuídos, clique em **[!UICONTROL Save]** e **[!UICONTROL OK]**.

         * Para continuar editando a árvore decisória, clique em **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Inserir um nó de destino entre nós](experience-target-node-add-inner.md)
>* [Adicionar um nó de destino irmão entre nós](experience-target-node-add-sibling.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Atribuir criações a um nó final](experience-assign-creative-bundles.md)
>* [Excluir um nó de destino ou nó de folha de criação](/help/creative/experiences/experience-target-node-delete.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
