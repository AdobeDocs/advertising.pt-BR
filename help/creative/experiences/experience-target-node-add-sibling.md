---
title: Adicionar um nó de destino irmão entre nós em uma experiência
description: Saiba como adicionar um nó irmão a qualquer nó que tenha um destino ou esteja no mesmo nível que um nó com um destino.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: 8961833c854ed41e4cca69787a5dc70dce2f203c
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Adicionar um nó de destino irmão entre nós em uma experiência

*Experiências somente com direcionamento de árvore de decisão*
*Beta fechado*

Você pode adicionar um nó irmão a qualquer nó que tenha um destino ou esteja no mesmo nível que um nó com um destino.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Acima do nó ao qual você deseja adicionar o nó irmão, clique em ![Adicionar](/help/creative/assets/add.png "Adicionar") e selecione **[!UICONTROL Insert Sibling Target]**.

1. Especifique os destinos:

   * Para Públicos-alvo da Adobe, faça o seguinte:

      1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções do [!UICONTROL Audience Targeting], abra a guia **[!UICONTROL Adobe Segments]**, especifique um ou mais dos destinos de público-alvo [!DNL Adobe] do anunciante e clique em **[!UICONTROL Save]**.

      1. (Opcional) Para criar vários nós de destino quando vários públicos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada público-alvo especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os públicos especificados (uma instrução [!DNL Boolean] `AND`).

      1. Clique em **[!UICONTROL Apply]**.

   * Para públicos-alvo geográficos, faça o seguinte:

      1. Clique em **[!UICONTROL Click to Browse]** para abrir as opções de [!UICONTROL Geo Targeting], especifique um ou mais dos destinos geográficos e clique em **[!UICONTROL Save]**.

         Os destinos de CEP têm opções de edição em massa. Para colar vários códigos postais, clique na guia **[!UICONTROL Paste postal codes]**, selecione o país, cole ou insira códigos postais separados por vírgulas ou em linhas separadas e clique em **[!UICONTROL Include All]**. Para remover um destino de código postal incluído, mantenha o cursor sobre o destino e clique em ![Remover](/help/creative/assets/delete.png "Remover") **[!UICONTROL Remove]**.

      1. (Opcional) Para criar vários nós de destino quando vários destinos geográficos forem especificados, selecione **[!UICONTROL Split targets to create nodes]**.

         Esse recurso cria um nó de destino separado (com pacotes criativos separados) para cada destino geográfico especificado. Se você não dividir os destinos, o usuário deverá pertencer a todos os locais especificados (uma instrução [!DNL Boolean] `AND`).

      1. Clique em **[!UICONTROL Apply]**.

   * Para destinos de passagem de dados, como opção, personalize a chave de passagem de dados, insira um único valor de passagem de dados e clique em **[!UICONTROL Apply]**.

     Um valor padrão para a chave no par chave-valor já está definido no campo **[!UICONTROL Data Pass]** na seção [!UICONTROL Advanced] das [configurações de experiência](experience-settings-targeting.md). Opcionalmente, é possível personalizar a chave.

   * Para destinos de pixel de redirecionamento, selecione o pixel de redirecionamento a ser usado e os valores necessários para qualquer atributo de pixel que deve estar presente para mostrar as criações. Depois clique em **[!UICONTROL Apply]**.

     Os atributos do pixel de redirecionamento estão configurados nas [configurações do pixel de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md).

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

1. Siga um destes procedimentos:

   * (Opcional) [Atribuir criativos](experience-assign-creative-bundles.md) ao novo nó de destino.

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
>* [Inserir um nó de destino entre nós](experience-target-node-add-inner.md)
>* [Copiar nós filhos e criações para outro nó no mesmo nível](experience-target-node-copy.md)
>* [Atribuir criações a um nó final](experience-assign-creative-bundles.md)
>* [Excluir um nó de destino ou nó de folha de criação](/help/creative/experiences/experience-target-node-delete.md)
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Configurações de experiência direcionadas](experience-settings-targeting.md)
