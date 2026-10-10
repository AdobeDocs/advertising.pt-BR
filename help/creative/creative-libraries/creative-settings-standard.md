---
title: Configurações de criação padrão
description: Referencie as configurações para criações padrão.
feature: Creative Standard Creatives
exl-id: 8eb66310-4860-4ca0-9678-a9e33639c529
TQID: 'https://experienceleague.adobe.com/WO5ViZMhKZBWTHbxgSIxTC79tydB5P765ueJ9EvyEUQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '3351'
ht-degree: 0%
---
# Configurações de criação padrão

As configurações variam por tipo de criação.

Ao editar várias criações ao mesmo tempo:

* É possível editar as configurações de cada criativo ao mesmo tempo ou individualmente. Por padrão, todas as criações escolhidas são selecionadas, e todas as configurações especificadas são aplicadas a todas as criações selecionadas. Para editar configurações de criações específicas, desmarque cada criação inaplicável antes de editar os campos; repita para criações adicionais, se necessário.

* Algumas configurações são aplicadas a todas as criações selecionadas.

## Configurações criativas flexíveis do HTML5 {#creative-settings-flexible-html5}

### Guia Detalhes

#### Nova interface

**Nome do Creative:** O nome do criativo. O nome do modelo ou do arquivo carregado é usado por padrão, mas você pode alterar o nome. Para vários criadores, é possível editar os nomes criativos individuais. **Dica:** inclua o tamanho do anúncio no nome criativo e Use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. Ao fazer upload ou editar várias criações, o mesmo valor é aplicado a cada criação selecionada.

**Formato:** (Somente leitura; somente criações existentes) O formato criativo (*[!UICONTROL Flexible]*).

**Tamanho do Creative:** (Somente leitura para criativos existentes) As dimensões do criativo. Se qualquer imagem incluída no criativo for maior que o tamanho especificado, ela será redimensionada de acordo.

**[!UICONTROL Click Tags]:** As variáveis que permitem redirecionamentos de rastreamento de cliques dos anúncios de banner incluídos. Os nomes das variáveis e os URLs da página de aterrissagem correspondentes são preenchidos na unidade de criação carregada, mas é possível alterar os URLs padrão. Para várias criações, é possível editar as tags de clique individuais.

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar um rótulo existente, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e clique no rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece a inserir uma cadeia de texto no campo **[!UICONTROL Label]**.

* Para criar um novo rótulo para aplicar às criações, insira um nome de rótulo exclusivo no campo **[!UICONTROL Label]** e clique em **Adicionar Marca**

* Para remover um rótulo aplicado, clique em **X** ao lado do nome do rótulo.

#### Interface herdada

**Nome do Creative:** O nome do criativo. O nome do modelo ou do arquivo carregado é usado por padrão, mas você pode alterar o nome. Para vários criadores, é possível editar os nomes criativos individuais. **Dica:** inclua o tamanho do anúncio no nome criativo e Use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. Ao fazer upload ou editar várias criações, o mesmo valor é aplicado a cada criação selecionada.

**Tamanho do Creative:** (Somente leitura para criativos existentes) As dimensões do criativo. Se qualquer imagem incluída no criativo for maior que o tamanho especificado, ela será redimensionada de acordo.

**[!UICONTROL Click Tags]:** As variáveis que permitem redirecionamentos de rastreamento de cliques dos anúncios de banner incluídos. Os nomes das variáveis e os URLs da página de aterrissagem correspondentes são preenchidos na unidade de criação carregada, mas é possível alterar os URLs padrão. Para várias criações, é possível editar as tags de clique individuais.

<!--
 I don't see this as of 1/30. I do see the option to create one custom LP per creative (for any creative type), not one per click tag for flexible HTML5 creatives.
>[!NOTE]
>
>When you include the creative in an experience, you can replace the default value for any of the click tags with a custom landing page URL to generate a derivation of the base creative.
-->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative] e incluir a dimensão [!UICONTROL Creative Label] em [!UICONTROL Custom Creative Report].

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar às criações, abra a lista, clique em **+ Adicionar Rótulo**, insira um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

### Guia Atributos

**\[Todos os atributos de conteúdo padrão aplicáveis ao criativo\]:** Os nomes e valores de atributos padrão são preenchidos a partir da unidade criativa flexível, mas você pode alterar os valores opcionalmente.

>[!NOTE]
>
>Também é possível substituir o valor padrão de qualquer um dos atributos criativos por um valor personalizado ao incluir o criativo em uma experiência. Editar os atributos em uma experiência cria uma variação do criativo principal.

Para obter informações sobre atributos disponíveis em modelos predefinidos, consulte &quot;[Modelos de criação flexíveis disponíveis](#flexible-creative-templates-available).&quot;

### Guia Modelo

*Somente criações existentes*

O arquivo de modelo flexível do HTML5 para o criativo.

Opcionalmente, é possível substituir o modelo existente por um novo que tenha um layout diferente, mas tenha o mesmo conjunto de nomes de atributo que o modelo original. O novo modelo deve estar em formato ZIP com no máximo 2 MB. Quando o criativo está em um pacote, todas as experiências que usam o pacote usam subsequentemente o layout do novo modelo.

Ao atualizar o modelo de um criativo principal com variações secundárias, as variações são atualizadas com todas as alterações no layout do modelo, mas os valores de atributo da variação não são alterados.

Para substituir o modelo de publicidade existente:

1. Clique em **Atualizar Modelo**.

1. (Somente interface herdada) Clique em **Continuar**.

1. Especifique um arquivo ZIP:

   * (Nova interface do usuário) Siga um destes procedimentos:

     * Arraste e solte um arquivo em seu dispositivo ou rede na caixa.

     * Clique em **[!UICONTROL Browse files]** para localizar o arquivo no dispositivo ou na rede.

   * (Interface herdada) Selecione um arquivo no seu dispositivo ou rede na caixa.

   Consulte as [especificações flexíveis do anúncio](#flexible-ad-spec).

1. Edite as novas [configurações flexíveis de anúncios do HTML](#flexible-ad-settings), conforme necessário.

1. Clique em (nova interface) **[!UICONTROL Update Creative]** ou (interface herdada) **[!UICONTROL Save]**

## configurações de criação do HTML5 {#creative-settings-html5}

### Guia Detalhes

Para novas criações, as configurações a seguir não estão em uma guia nomeada.

#### Nova interface

**Nome do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. Para vários criadores, é possível editar os nomes criativos individuais. **Dica:** inclua o tamanho do anúncio no nome criativo e Use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Formato:** (Somente leitura; somente criações existentes) O formato criativo (*[!UICONTROL HTML5]*).

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. Ao fazer upload ou editar várias criações, o mesmo valor é aplicado a cada criação selecionada.

**Tamanho do Creative:** (Somente leitura para criativos existentes) As dimensões do criativo. Se qualquer imagem incluída no criativo for maior que o tamanho especificado, ela será redimensionada de acordo.

**[!UICONTROL Click Tags]:** (somente criações estáticas do HTML5) As variáveis que permitem redirecionamentos de rastreamento de cliques dos anúncios de banner incluídos. Os nomes das variáveis e os URLs da página de aterrissagem correspondentes são preenchidos na unidade de criação carregada, mas é possível alterar os URLs padrão. Para várias criações, é possível editar as tags de clique individuais.

>[!NOTE]
>
>Ao incluir a criação em uma experiência, é possível substituir o valor padrão de qualquer uma das tags de clique por um URL de página de aterrissagem personalizado para gerar uma derivação da criação básica.

**URL da página de aterrissagem:** (criações simples do HTML5 com apenas uma página de aterrissagem) A URL da página de aterrissagem padrão para cada anúncio ao qual você associa as criações. Deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso.

Ao incluir um criativo em um pacote e atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar um rótulo existente, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e clique no rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece a inserir uma cadeia de texto no campo **[!UICONTROL Label]**.

* Para criar um novo rótulo para aplicar às criações, insira um nome de rótulo exclusivo no campo **[!UICONTROL Label]** e clique em **Adicionar Marca**

* Para remover um rótulo aplicado, clique em **X** ao lado do nome do rótulo.

#### Interface herdada

**Nome do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. Para vários criadores, é possível editar os nomes criativos individuais. **Dica:** inclua o tamanho do anúncio no nome criativo e Use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. Ao fazer upload ou editar várias criações, o mesmo valor é aplicado a cada criação selecionada.

**Tamanho do Creative:** (Somente leitura para criativos existentes) As dimensões do criativo. Se qualquer imagem incluída no criativo for maior que o tamanho especificado, ela será redimensionada de acordo.

**[!UICONTROL Click Tags]:** (somente criações estáticas do HTML5) As variáveis que permitem redirecionamentos de rastreamento de cliques dos anúncios de banner incluídos. Os nomes das variáveis e os URLs da página de aterrissagem correspondentes são preenchidos na unidade de criação carregada, mas é possível alterar os URLs padrão. Para várias criações, é possível editar as tags de clique individuais.

>[!NOTE]
>
>Ao incluir a criação em uma experiência, é possível substituir o valor padrão de qualquer uma das tags de clique por um URL de página de aterrissagem personalizado para gerar uma derivação da criação básica.

**URL da página de aterrissagem:** (criações simples do HTML5 com apenas uma página de aterrissagem) A URL da página de aterrissagem padrão para cada anúncio ao qual você associa as criações. Deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso.

Ao incluir um criativo em um pacote e atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar às criações, abra a lista, clique em **+ Adicionar Rótulo**, insira um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

### Guia Modelo

*Somente criações estáticas HTML5 existentes*

O arquivo de modelo HTML5 para o criativo.

Opcionalmente, é possível substituir o modelo existente por um novo que tenha um layout diferente, mas tenha o mesmo conjunto de nomes de atributo que o modelo original. O novo modelo deve estar em formato ZIP com no máximo 2 MB. Quando o criativo está em um pacote, todas as experiências que usam o pacote usam subsequentemente o layout do novo modelo.

Ao atualizar o modelo de um criativo principal com variações secundárias, as variações são atualizadas com todas as alterações no layout do modelo, mas os valores de atributo da variação não são alterados.

Para substituir o modelo de publicidade existente:

1. Clique em **Atualizar Modelo**.

1. Clique em **Continuar**.

1. Especifique um arquivo ZIP de uma das seguintes maneiras:

   * Arraste e solte um arquivo em seu dispositivo ou rede na caixa.

   * Clique em **[!UICONTROL select a file]** para localizar o arquivo no dispositivo ou na rede.

   Consulte as [especificações de anúncios do HTML](html5-creative-specification.md).

1. Edite as novas [configurações de anúncio do HTML5](#creative-settings-html5), conforme necessário.

1. Clique em **[!UICONTROL Edit]**

## Configurações de criação da imagem {#creative-settings-image}

### Nova interface

**Nome do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. Para várias imagens, é possível editar os nomes criativos individuais. **Dica:** use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Formato:** (Somente leitura; somente criações existentes) O formato criativo (*[!UICONTROL Image]*).

**Tamanho do Creative:** (Somente leitura) As dimensões das imagens carregadas.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. O mesmo valor se aplica a todas as imagens selecionadas. Ao incluir os elementos de criação em uma experiência, é possível personalizar as preferências de idioma da experiência.

**URL da página de aterrissagem:** a URL da página de aterrissagem padrão para cada anúncio ao qual você associa as criações. O URL da página de aterrissagem deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso. O mesmo valor se aplica a todas as imagens selecionadas.

Ao incluir um criativo em um pacote e, em seguida, atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar um rótulo existente, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e clique no rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece a inserir uma cadeia de texto no campo **[!UICONTROL Label]**.

* Para criar um novo rótulo para aplicar às criações, insira um nome de rótulo exclusivo no campo **[!UICONTROL Label]** e clique em **Adicionar Marca**

* Para remover um rótulo aplicado, clique em **X** ao lado do nome do rótulo.

### Interface herdada

**Nome do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. Para várias imagens, é possível editar os nomes criativos individuais. **Dica:** use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. O mesmo valor se aplica a todas as imagens selecionadas. Ao incluir os elementos de criação em uma experiência, é possível personalizar as preferências de idioma da experiência.

**Tamanho do Creative:** (Somente leitura) As dimensões das imagens carregadas.

**URL da página de aterrissagem:** a URL da página de aterrissagem padrão para cada anúncio ao qual você associa as criações. O URL da página de aterrissagem deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso. O mesmo valor se aplica a todas as imagens selecionadas.

Ao incluir um criativo em um pacote e, em seguida, atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar às criações, abra a lista, clique em **+ Adicionar Rótulo**, insira um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

## Configurações de criação de terceiros {#creative-settings-third-party}

**JavaScriptCode:** uma marca JavaScript (e, opcionalmente, uma marca alternativa para navegadores sem suporte a JavaScript) que aponta para o criativo no servidor de anúncios de terceiros. O script pode variar por servidor de publicidade. Ao editar várias criações, o mesmo valor é aplicado a cada criação selecionada.

Todas as [macros disponíveis](/help/creative/creative-macros.md) e os dados com os quais elas foram substituídas estão listados abaixo do campo de entrada. Para inserir uma das macros na marca, mantenha o cursor sobre a descrição da macro e clique em ![Copiar para a área de transferência](/help/creative/assets/copy-to-clipboard.png "Copiar para a área de transferência") e cole a imagem no local desejado dentro da marca.

Ao incluir esse criativo em uma experiência que você implementa como um anúncio de uma DSP, a DSP usa as informações nessa tag para exibir o anúncio e rastrear impressões e cliques nele. A DSP envia a tag para a troca de anúncios. Quando o anúncio é exibido e clicado, o servidor de anúncios, o DSP e [!DNL Creative] rastreiam os eventos.

**[!UICONTROL Advertiser]:** (Somente leitura) O anunciante para o qual a biblioteca está disponível.

**Nome do Creative:** O nome do criativo. **Dica:** use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Tamanho do Creative:** (Somente leitura para anúncios existentes) As dimensões do criativo. Para novas criações, selecione em uma lista de tamanhos de anúncio padrão.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações.

**URL da página de aterrissagem:** a URL da página de aterrissagem usada para validar cada anúncio ao qual você associa as criações. O servidor de anúncios de terceiros determina a página de aterrissagem real de cada anúncio.

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar às criações, abra a lista, clique em **+ Adicionar Rótulo**, insira um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

## Configurações de criação de vídeo {#creative-settings-video}

### Nova interface

**Nome do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. **Dica:** use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Formato:** (Somente leitura; somente criações existentes) O formato criativo (*[!UICONTROL Standard Video]*).

**Tamanho:** (Somente leitura) as dimensões do vídeo, que é preenchido automaticamente.

**Duração:** (Somente leitura) A duração do vídeo, que é preenchido automaticamente.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa o criativo. Ao incluir o criativo em uma experiência, você pode personalizar as preferências de idioma da experiência.

**URL da página de aterrissagem:** a URL da página de aterrissagem padrão para cada anúncio ao qual você associa o criativo. O URL da página de aterrissagem deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso.

Ao incluir um criativo em um pacote e, em seguida, atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote.

**Rótulo:** (opcional) Quaisquer rótulos a serem aplicados ao criativo. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar um rótulo existente, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e clique no rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece a inserir uma cadeia de texto no campo **[!UICONTROL Label]**.

* Para criar um novo rótulo para aplicar às criações, insira um nome de rótulo exclusivo no campo **[!UICONTROL Label]** e clique em **Adicionar Marca**

* Para remover um rótulo aplicado, clique em **X** ao lado do nome do rótulo.

### Interface herdada

**Nome do ativo do Creative:** O nome do criativo. Para um novo criativo, o nome do arquivo é usado por padrão, mas você pode alterar o nome. Para vários arquivos, é possível editar os nomes criativos individuais. **Dica:** use um nome que possa ser facilmente encontrado ao incluir o criativo em uma experiência.

**Duração:** (Somente leitura) A duração do vídeo, que é preenchido automaticamente.

**Idioma:** o idioma padrão para cada anúncio ao qual você associa as criações. O mesmo valor se aplica a todas as criações selecionadas. Ao incluir os elementos de criação em uma experiência, é possível personalizar as preferências de idioma da experiência.

**URL da página de aterrissagem:** a URL da página de aterrissagem padrão para cada anúncio ao qual você associa as criações. O URL da página de aterrissagem deve ser um URL válido começando com http:// ou https://. Ele pode incluir parâmetros de rastreamento de terceiros ou [[!DNL Creative] macros](/help/creative/creative-macros.md) para seu próprio uso. O mesmo valor se aplica a todas as imagens selecionadas.

Ao incluir um criativo em um pacote e, em seguida, atribuir o pacote a uma experiência, é possível alterar o URL da página inicial, bem como adicionar URLs de rastreamento de impressões e cliques e JavaScript para cada criativo no pacote. <!-- NOT SURE APPLICABLE ANYMORE: to generate a variation of the base creative. -->

**Rótulo:** (opcional) quaisquer rótulos a serem aplicados a todas as criações selecionadas. Você pode filtrar criações por rótulo em várias exibições dentro de [!DNL Creative].

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar às criações, abra a lista, clique em **+ Adicionar Rótulo**, insira um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

>[!MORELIKETHIS]
>
>* [Adicionar criações padrão a uma biblioteca criativa](/help/creative/creative-libraries/creative-add-standard.md)
>* [Editar criações padrão](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Macros disponíveis para rastrear URLs](/help/creative/creative-macros.md)
