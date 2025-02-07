---
title: Editar criações padrão em uma biblioteca criativa
description: Saiba como alterar as configurações de criações padrão (não dinâmicas) em uma biblioteca criativa.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Editar criações padrão em uma biblioteca criativa

*Beta fechado*

É possível editar algumas configurações para cada tipo de criação padrão. Você pode editar vários <!-- or creative variations --> criativos do mesmo tipo criativo (HTML simples com apenas uma página de aterrissagem, HTML estático com várias páginas de aterrissagem, HTML flexível, imagem ou terceiros<!-- , or dynamic -->) somente.

Para criações de HTML5 flexível e HTML 5 estático, você pode fazer upload de um novo arquivo de modelo com um layout diferente, mas o mesmo conjunto de nomes de atributo. Para criações em HTML5 simples, é possível editar quaisquer atributos ou adicionar imagens fazendo upload de um novo modelo com os novos atributos ou imagens. Em todos os casos, o modelo deve ser um arquivo local em formato ZIP com no máximo 2 MB.

Ao editar um <!-- or creative variation --> criativo que está incluído em um pacote, suas alterações são automaticamente aplicadas em todas as experiências que incluem o pacote, exceto que qualquer página de aterrissagem personalizada e URLs de rastreamento especificadas no nível de experiência permanecem aplicáveis ao pacote anexado a essa experiência.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Opcional) [Personalize a exibição](/help/creative/introduction/customize-data-views.md) para incluir bibliotecas específicas.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]** > **[!UICONTROL Standard Ads]**, selecione as criações:

   * (Opcional) [Personalize o modo de exibição](/help/creative/introduction/customize-data-views.md) para incluir criações específicas.

   * Para editar um único criativo:

      * Na exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome criativo e, em seguida, clique em **[!UICONTROL Edit]**.

      * Na exibição de tabela, mantenha o cursor sobre a linha e clique em **[!UICONTROL Edit]**.

   * Para editar uma ou mais criações, marque a caixa de seleção de cada criação que deseja editar. Na barra de ferramentas de ações em massa, clique em **[!UICONTROL Edit]**.

     Para selecionar todas as linhas, marque a caixa de seleção global no canto superior esquerdo.

1. Edite as [configurações de criação de imagem](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image), [configurações de criação de HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5), [configurações flexíveis de criação de HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) ou [configurações de criação de terceiros](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party). <!-- , or [dynamic creative settings](/help/creative/creative-libraries/creative-settings-dynamic.md) -->

   Ao editar várias criações ao mesmo tempo:

   * É possível editar as configurações de cada criativo ao mesmo tempo ou individualmente. Por padrão, todas as criações escolhidas são selecionadas e todas as configurações especificadas são aplicadas a todas as criações selecionadas. Para editar configurações de criações específicas, desmarque cada criação inaplicável antes de editar os campos; repita para criações adicionais, se necessário.

   * Algumas configurações são aplicadas a todas as criações selecionadas.

   >[!NOTE]
   >
   >* (Somente criações de HTML5 flexíveis) É possível editar atributos somente para criações únicas.<!-- Also, when you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed. -->

<!-- Not there as of 1/16/25. If we do add it, verify the applicable ad types:   
1. (Flexible HTML5 [or third-party should be possible, but not so] creatives; optional) Once you've made your changes, click ![]() to preview the new creative. 
-->

1. Clique em **Salvar**.

<!-- Not there as of 1/16/25. If we do add it, add back in:
1. (Flexible HTML5 or third-party creatives; optional) Regenerate the thumbnail within the table view or cards view if the change isn't visible immediately.
-->

>[!MORELIKETHIS]
>
>* [Adicionar criações padrão a uma biblioteca criativa](creative-add-standard.md)
>* [Configurações de criação padrão](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Visualizar um criativo](/help/creative/creative-libraries/creative-preview.md)
>* [Criações duplicadas](/help/creative/creative-libraries/creative-duplicate.md)
>* [Excluir criações](/help/creative/creative-libraries/creative-delete.md)
