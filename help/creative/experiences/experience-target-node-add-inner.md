---
title: Adicionar um nó de direcionamento entre nós em uma experiência
description: Saiba como adicionar um nó de direcionamento entre os corpos de direcionamento em uma experiência de anúncio.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
source-git-commit: dac7252e118e467fbc924cf162756d7ecd69892f
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Adicionar um nó de direcionamento entre nós em uma experiência

*Experiências somente com direcionamento de árvore de decisão*
*Beta fechado*

Ao inserir um nó de destino entre níveis existentes, o novo nó de destino retém todos os destinos e criações secundários existentes, e o novo nó é chamado inicialmente de &quot;Todos&quot;. Como opção, você pode manter o novo nó sem adicionar destinos mais específicos.

Para definir um destino específico, adicione outro nó de destino irmão no mesmo nível, especifique o novo destino e atribua criações somente a esse destino. Adicionar um nó de destino irmão cria o novo nó de destino e move todos os destinos e criações filhos anteriormente atribuídos a &quot;Todos&quot; para um novo nó &quot;Tudo mais&quot; no mesmo nível. Dessa forma, a adição do novo destino não afeta as ramificações secundárias existentes, pois somente o novo nó irmão inclui as novas informações de direcionamento.

>[!NOTE]
>
>Para adicionar um nó de destino ao nível inferior de uma árvore de decisão, consulte &quot;[Adicionar um nó de destino ao nível final em uma experiência](experience-target-node-add-final.md).&quot;

<!-- 1. [ways to get to the decision tree] -->

1. No nó em que você deseja inserir o destino, clique em ![Adicionar](/help/creative/assets/add.png "Adicionar") e selecione **[!UICONTROL Insert New Target]**.

1. Siga um destes procedimentos:

   * Se os nós irmãos ainda não existirem, faça o seguinte:

      1. Selecione o tipo de destino e clique em **[!UICONTROL Apply]**:

         * Para Públicos-alvo da Adobe, selecione **[!UICONTROL Adobe Audience]**.

         * Para destinos geográficos, selecione uma única categoria geográfica (como [!UICONTROL Geo: Country]).

         * Para destinos de transmissão de dados, selecione **[!UICONTROL Data Pass]**.

         * Para destinos de pixel de redirecionamento, selecione **[!UICONTROL RT Pixel].

         * Para destinos de dispositivo, selecione uma única categoria de destino (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** ou **[!UICONTROL Device: Browser]**).

   * Se os nós irmãos já existirem, faça o seguinte:

      * Para Públicos-alvo da Adobe, faça o seguinte:

         1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções do [!UICONTROL Audience Targeting], abra a guia **[!UICONTROL Adobe Segments]**, especifique um ou mais dos destinos de público-alvo [!DNL Adobe] do anunciante e clique em **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.

         1. (Opcional) Para criar vários nós de destino quando vários públicos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

            Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada público-alvo especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os públicos especificados.

         1. Clique em **[!UICONTROL Apply]**.

      * Para públicos-alvo geográficos, faça o seguinte:

         1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções de [!UICONTROL Geo Targeting], especifique um ou mais dos destinos geográficos e clique em **[!UICONTROL Save]**.

            Os destinos de CEP têm opções de edição em massa. Para colar vários códigos postais, clique na guia **[!UICONTROL Paste postal codes]**, selecione o país, cole ou insira códigos postais separados por vírgulas ou em linhas separadas e clique em **[!UICONTROL Include All]**. Para remover um destino de código postal incluído, mantenha o cursor sobre o destino e clique em ![Remover](/help/creative/assets/delete.png "Remover") **[!UICONTROL Remove]**.

         1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

            Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados.

         1. Clique em **[!UICONTROL Apply]**.

      * Para um destino de passagem de dados, como opção, personalize a chave de passagem de dados, insira um único valor de passagem de dados e clique em **[!UICONTROL Apply]**.

        Um valor padrão para a chave no par chave-valor já está definido no campo **[!UICONTROL Data Pass]** na seção [!UICONTROL Advanced] das [configurações de experiência](experience-settings-targeting.md). Opcionalmente, é possível personalizar a chave.

      * Para um destino de pixel de redirecionamento, selecione um único pixel de redirecionamento a ser usado e os valores de qualquer atributo de pixel necessário para mostrar as criações e clique em **[!UICONTROL Apply]**.

        Os atributos do pixel de redirecionamento estão configurados nas [configurações do pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

      * Para destinos de dispositivos, faça o seguinte:

         1. Selecione os alvos.

         1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

            Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados.

         1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         1. Clique em **[!UICONTROL Apply]**.

1. Siga um destes procedimentos:

   * (Opcional) [Atribuir criativos](experience-assign-creative-bundles.md) ao novo nó de destino e ao nó &quot;Todo Resto&quot;.

   * (Opcional) [Adicione um nó de destino irmão](experience-target-node-add-sibling.md) do tipo de destino especificado.

   * (Opcional) Para salvar a experiência:

      1. Clique em **[!UICONTROL Save]** e depois em **[!UICONTROL OK]**.

      1. (Se cada nó no nível mais inferior não incluir pelo menos um criativo): Siga um destes procedimentos:

         * Para salvar a experiência sem todos os pacotes criativos necessários, clique em **[!UICONTROL Save as Draft]**.

           Não é possível criar uma tag de anúncio para uma experiência de rascunho.

         * Para atribuir o criativo padrão a cada destino que ainda não recebeu um pacote criativo, clique em **[!UICONTROL Assign Default Creatives]**. Depois de revisar a árvore atualizada com os criativos padrão atribuídos, clique em **[!UICONTROL Save]** e **[!UICONTROL OK]**.

         * Para continuar editando a árvore decisória, clique em **[!UICONTROL Continue Edit]**.

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
