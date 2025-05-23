---
title: Adicionar criações padrão a uma biblioteca criativa
description: Saiba como adicionar criações padrão (não dinâmicas) a uma biblioteca criativa.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 38ba8473eae3df204f618eac1f20e605e57ece5a
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Adicionar criações padrão a uma biblioteca criativa

*Beta fechado*

Adicione criativos às suas [bibliotecas criativas](creative-library-manage.md) para usar com [experiências de anúncio](/help/creative/experiences/experience-about.md).

>[!NOTE]
>
> Você pode incluir criações individuais diretamente em experiências de anúncio que não têm metas de usuário definidas. Você também pode agrupar seus criadores em [pacotes](bundle-manage.md), que podem ser incluídos em experiências de anúncios direcionados.

## Adicionar anúncios flexíveis do HTML a uma biblioteca criativa {#flexible-creative-add}

Você pode executar um dos seguintes procedimentos:

* Fazer upload de seus próprios criativos flexíveis em arquivos ZIP.

* Use qualquer um dos modelos de criação flexíveis predefinidos carregados em sua conta como ponto de partida para sua própria criação flexível.

### Fazer upload de suas próprias criações flexíveis {#flexible-creative-upload}

Você pode fazer upload de várias unidades criativas flexíveis. As criações flexíveis devem estar no formato ZIP e podem ter até 2 MB. Para conhecer os requisitos do arquivo, consulte a [especificação criativa do HTML5](html5-creative-specification.md).

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]**, clique na subguia **[!UICONTROL Standard Ads]**.

1. Clique em **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Clique em **[!UICONTROL Upload New]**.

1. Especifique arquivos ZIP de uma das seguintes maneiras:

   * Arraste e solte arquivos no seu dispositivo ou rede na caixa.

   * Clique em **[!UICONTROL select a file]** para localizar os arquivos no dispositivo ou na rede.

   Consulte as [especificações flexíveis do anúncio](#flexible-ad-spec).

1. Adicionar ou remover arquivos criativos flexíveis:

   * Para adicionar um arquivo, clique em ![Adicionar](/help/creative/assets/create.png "Adicionar") no canto superior esquerdo e localize o arquivo em seu dispositivo ou rede.

   * Para remover um arquivo, desmarque a caixa de seleção ao lado dele.

1. Especifique as [configurações flexíveis de anúncios HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5).

   Por padrão, todas as criações que você acabou de fazer upload são selecionadas. Todas as configurações com apenas um valor se aplicam a todas as criações selecionadas; para algumas configurações, é possível especificar valores individuais. Para inserir configurações para criações específicas, desmarque a caixa de seleção ao lado de cada criação inaplicável.

1. Clique em **[!UICONTROL Create]**

### Adicionar criações flexíveis usando um modelo {#flexible-creative-use-template}

Você pode usar qualquer um dos modelos criativos flexíveis carregados em sua conta para criar anúncios de um tamanho predefinido. Após selecionar um modelo a ser usado, você editará as tags e os atributos de clique.&lt;!— Substitua a última frase por esta se adicionarmos o recurso de download do modelo de volta: Você pode a\) selecionar um modelo para usar e editar as tags e os atributos de clique; ou b\) [baixar um modelo como um arquivo ZIP](#download-flexible-creative-template), editar o conteúdo offline para criar seu próprio criativo e [carregar o arquivo editado como um novo criativo] (flexible-creative-upload).>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]**, clique na subguia **[!UICONTROL Standard Ads]**.

1. Clique em **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Clique em **[!UICONTROL Browse System Flexible Templates]**.

<!-- Not options as of 5/22/25:

1. In the left panel, select the creative size to see all available templates for that size.

1. Select the template:

   * In card view, click **[!UICONTROL ...]** next to the template name, and then click **[!UICONTROL Use Selected]**.
     
   * In table view, hold the cursor over the row and click **[!UICONTROL Use Selected]**.
-->

1. (Opcional) Para visualizar o modelo, clique em **[!UICONTROL ...]** ao lado do nome do modelo e em **[!UICONTROL Preview]**.

   Opcionalmente, é possível baixar o modelo

1. Ao lado do nome do modelo, clique em **[!UICONTROL ...]** e depois em **[!UICONTROL Use Selected]**.

1. Edite as [configurações flexíveis de criação do HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) para especificar o idioma e incluir suas próprias tags de clique, imagens e outros atributos.

   O tamanho máximo do criativo, uma vez compactado, é de 2 MB.<!-- Still true? -->

1. Clique em **[!UICONTROL Create]**.

## Adicionar um criativo do HTML5 a uma biblioteca criativa

É possível adicionar várias criações HTML5 de um único tipo (simples ou estático) de cada vez.

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>Você também pode [adicionar criações flexíveis do HTML5](#flexible-creative-add), que são criativas do HTML5 com todos os seus atributos como tags padrão do HTML que você pode editar diretamente no [!DNL Creative].

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]**, clique na subguia **[!UICONTROL Standard Ads]**.

1. Clique em **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Especifique os arquivos de uma das seguintes maneiras:

   * Arraste e solte arquivos no seu dispositivo ou rede na caixa.

   * Clique em **[!UICONTROL select a file]** para localizar o arquivo no dispositivo ou na rede.

   Consulte a [especificação de anúncio do HTML5](/help/creative/creative-libraries/html5-creative-specification.md).

1. Especifique as [configurações de anúncios do HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Por padrão, todas as criações que você acabou de fazer upload são selecionadas. Todas as configurações com apenas um valor se aplicam a todas as criações selecionadas; para algumas configurações, é possível especificar valores individuais. Para inserir configurações para criações específicas, desmarque a caixa de seleção ao lado de cada criação inaplicável.

1. Clique em **[!UICONTROL Create]**

## Adicionar um criativo de imagem a uma biblioteca criativa

As criações de imagem podem estar no formato GIF, JPEG, JPG ou PNG. O tamanho máximo do arquivo é de 2 (dois) MB. Consulte os [tamanhos de criação suportados](/help/creative/creative-libraries/creative-sizes.md).

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]**, clique na subguia **[!UICONTROL Standard Ads]**.

1. Clique em **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**.

1. Especifique as imagens:

   * Para ativos de imagem local, siga um destes procedimentos:

      * Arraste e solte arquivos no seu dispositivo ou rede na caixa.

      * Clique em **[!UICONTROL select a file]** para localizar arquivos no dispositivo ou na rede.

   * Para imagens na biblioteca do Adobe Experience Manager, faça o seguinte:

      1. Clique em **[!UICONTROL AEM Asset Library]**.

      1. Faça logon em sua conta da Experience Manager.

      1. Localize e selecione os arquivos nas visualizações [!UICONTROL Assets] ou [!UICONTROL Collections] e clique em **[!UICONTROL Select]** no canto superior direito.

1. Adicionar ou remover imagens:

   * Para adicionar uma imagem, clique em ![Adicionar](/help/creative/assets/create.png "Adicionar") no canto superior esquerdo e localize o arquivo em seu dispositivo ou rede.

   * Para remover uma imagem, desmarque a caixa de seleção ao lado dela.

1. Especifique as [configurações de criação da imagem](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image).

   Por padrão, todas as criações que você acabou de fazer upload são selecionadas, e todas as configurações especificadas são aplicadas a todas as criações selecionadas. Todas as configurações com apenas um valor se aplicam a todas as criações selecionadas. Para inserir configurações para criações específicas, desmarque cada criação inaplicável.

1. Clique em **[!UICONTROL Create]**

## Adicionar um criativo de terceiros a uma biblioteca criativa {#creative-add-third-party}

O [!DNL Creative] oferece suporte às marcas de rastreamento da JavaScript para criações hospedadas na maioria dos servidores de anúncios de terceiros.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Clique no nome da biblioteca.

1. Na guia **[!UICONTROL Creatives]**, clique na subguia **[!UICONTROL Standard Ads]**.

1. Clique em **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**.

1. Especifique a marca JavaScript e outras configurações para o criativo nas [configurações de criativo de terceiros](#creative-settings-third-party).

   Você pode copiar e colar qualquer uma das [macros disponíveis](/help/creative/creative-macros.md) na tag do JavaScript.

1. Clique em **[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [Editar criações padrão](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Configurações de criação padrão](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Macros disponíveis para rastrear URLs](/help/creative/creative-macros.md)
>* [Tamanhos de criativo com suporte](/help/creative/creative-libraries/creative-sizes.md)
>* [Visualizar um criativo](/help/creative/creative-libraries/creative-preview.md)
>* [Anexar e desanexar criações de conjuntos](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [Sobre suas bibliotecas criativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Gerenciar bibliotecas criativas](/help/creative/creative-libraries/creative-library-manage.md)
