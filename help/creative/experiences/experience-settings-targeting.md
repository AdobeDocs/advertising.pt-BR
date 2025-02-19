---
title: Configurações de experiência direcionada
description: Consulte descrições de todas as configurações para experiências de anúncios direcionados.
feature: Creative Experiences
exl-id: cb6fd855-6534-4eac-b34b-323073d186be
source-git-commit: 727860ba89ae98d50a33befa28ab1654650263e6
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 0%

---

# Configurações de experiência de anúncio direcionado

*Beta fechado*

## seção [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Somente leitura para experiências existentes) O anunciante que fará lances nas combinações criativa e de destino incluídas na experiência. Depois de salvar a experiência, você não poderá alterar o anunciante.

**[!UICONTROL Experience Name]:** Um nome exclusivo para a experiência. **Dica:** use um nome fácil de encontrar quando você usar a experiência como um anúncio no Advertising DSP ou em outra DSP.

**[!UICONTROL Creative Library]:** (Somente leitura para experiências existentes) Uma única biblioteca criativa para usar na experiência. Depois de salvar a experiência, você não poderá alterar a biblioteca.

## seção [!UICONTROL Default creatives]

**\[Criações padrão especificadas\]:** As criações de imagem padrão a serem usadas quando um navegador não pode exibir criações atribuídas à experiência, como quando o navegador não está habilitado para JavaScript ou o servidor de anúncios não pode personalizar o anúncio devido a atrasos. Inclua um criativo de imagem por tamanho de anúncio ao qual a experiência se aplica. Suas escolhas determinam os tamanhos criativos que podem ser usados para a experiência.<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. This feels a little wonky in that there isn't a distinct/obvious "Creative Sizes" setting to reference. -->

Para experiências com definição de metas da árvore de decisão, é possível substituir os criativos padrão por pacotes criativos que contenham criativos do mesmo tamanho de dentro da árvore de decisão.<!-- verify -->

* Para adicionar um criativo padrão com dimensões diferentes, clique em **[!UICONTROL + Add Sizes]**, marque a caixa de seleção ao lado de cada criativo a ser adicionado do painel direito e clique em **[!UICONTROL Add Creatives]**.

* Para excluir um criativo padrão, mantenha o cursor sobre a miniatura criativa e clique em ![Excluir](/help/creative/assets/delete.png "Excluir").

* Para excluir todas as criações padrão, clique em ![Excluir](/help/creative/assets/delete.png "Excluir") **[!UICONTROL Delete all]**.

* Para mostrar ou ocultar o painel Criativos à direita, clique em ![Mostrar/Ocultar](/help/creative/assets/hide-show-creatives.png "Mostrar/Ocultar") no canto superior direito do painel.

## seção [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Somente leitura para experiências existentes) Habilita o direcionamento criativo usando uma árvore de decisão e a criação automática de marca. Depois de salvar a experiência, você não poderá alterar essa configuração.

**[!UICONTROL Dynamic ads]:** (Somente leitura para experiências existentes) Indica que a experiência inclui anúncios dinâmicos. **Observação:** uma experiência pode incluir todos os anúncios padrão ou todos os anúncios dinâmicos. Depois de salvar a experiência, você não poderá alterar essa configuração.

**[!UICONTROL Language Targeting]:** (Experiências somente com anúncios padrão; opcional; somente leitura para experiências existentes) Verifica as configurações de idioma do navegador do usuário e exibe um criativo no idioma especificado quando um criativo nesse idioma estiver disponível. Quando um criativo no idioma especificado pelo navegador não está disponível, a configuração [!UICONTROL Preferred language] é usada.

Depois de salvar a experiência, você não poderá alterar essa configuração.

**[!UICONTROL Preferred language]:** (Experiências somente com anúncios padrão; somente leitura para experiências existentes) O idioma para todos os anúncios criados a partir da experiência, exceto quando [!UICONTROL Language Targeting] está habilitado. Depois de salvar a experiência, você não poderá alterar essa configuração.

## seção [!UICONTROL Advanced]

**Data Pass:** (Somente leitura para experiências existentes; opcional) Para direcionar usuários com base em pares de valores-chave específicos que o DSP, editor ou parceiro transmite em tempo real na impressão. É possível especificar até cinco chaves de passagem de dados (parâmetros). Ao configurar o direcionamento na árvore de decisão, você pode incluir um nível de dados para passar nós de destino e especificar os valores para direcionar para cada nó. Se você não especificar uma chave neste campo ao criar a experiência, ainda poderá especificar uma na árvore de decisão.<!-- May move this to just within the decision tree.  -->

Cada chave é anexada como uma macro na experiência de anúncio
tag, que pode ser gerada para implementar como um anúncio na DSP.

**Raio:** (somente experiências com anúncios dinâmicos; opcional) um raio de um código postal dos Estados Unidos especificado no arquivo de feed a ser direcionado; selecione um raio de 0 a 200 milhas. O arquivo de feed usado para criar os anúncios dinâmicos da experiência deve incluir uma [!UICONTROL ZIP] coluna<!-- or a user-named column mapped to a ZIP column --> com um valor para cada linha de produto no arquivo. Por exemplo, para um raio de 10 milhas, um anúncio de um produto disponível no 95110 pode ser exibido aos usuários dentro de 10 milhas de 95110.

**Pixel de RT:** (Somente leitura para experiências existentes; opcional) Um pixel de redirecionamento [!UICONTROL Creative] potencialmente direcionado. Ao configurar o direcionamento na árvore de decisão, você pode incluir um nível de nós de destino de pixel de RT e especificar o pixel a ser direcionado para cada nó, bem como os valores necessários para os atributos de pixel que devem estar presentes para mostrar as criações nos pacotes criativos atribuídos. Se você não especificar um pixel neste campo ao criar a experiência, ainda poderá especificar um na árvore de decisão.<!-- May move this to just within the decision tree. -->

**Rótulo:** <!-- should be "Labels" --> (Opcional) Quaisquer rótulos específicos de [!DNL Creative] para aplicar à experiência. Você pode filtrar experiências por rótulo na exibição Experiências<!-- sic -->.

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar, abra a lista, clique em **+ Adicionar Rótulo**, digite um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

**URL de rastreamento de impressão:** (opcional) uma URL de rastreamento de impressão de terceiros a ser anexada à URL da página de aterrissagem para qualquer anúncio criado a partir da experiência. É possível incluir até cinco URLs. Para adicionar uma URL adicional, clique em ![ícone](/help/creative/assets/create.png) **[!UICONTROL Add More] e insira a URL.

Depois de inserir uma URL, todas as [macros disponíveis](/help/creative/creative-macros.md) e os dados com os quais elas foram substituídas serão listados mais abaixo na página. Para inserir uma das macros na URL, mantenha o cursor sobre a descrição da macro e clique em ![Copiar para a área de transferência](/help/creative/assets/copy-to-clipboard.png "Copiar para a área de transferência") e cole a macro sempre que desejar no campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefixa automaticamente suas próprias marcas de rastreamento de impressão à URL da página de aterrissagem.
>* Você pode [substituir esta URL para qualquer criativo na experiência](experience-tracking-urls-targeting.md).
>* Você também pode inserir um código de rastreamento de impressão de terceiros no JavaScript no campo [!UICONTROL Client JS]

**URL de Rastreamento de Cliques:** (Opcional) (Opcional) Uma URL de rastreamento de cliques de terceiros a ser anexada à URL da página inicial. É possível incluir até cinco URLs. Para adicionar uma URL adicional, clique em ![ícone](/help/creative/assets/create.png) **[!UICONTROL Add More] e insira a URL.

Depois de inserir uma URL, todas as [macros disponíveis](/help/creative/creative-macros.md) e os dados com os quais elas foram substituídas serão listados mais abaixo na página. Para inserir uma das macros na URL, mantenha o cursor sobre a descrição da macro e clique em ![Copiar para a área de transferência](/help/creative/assets/copy-to-clipboard.png "Copiar para a área de transferência") e cole a macro sempre que desejar no campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefixa automaticamente suas próprias marcas de rastreamento de impressão à URL da página de aterrissagem.
>* Você pode [substituir esta URL para qualquer criativo na experiência](experience-tracking-urls-targeting.md).

**JS do Cliente:** (Opcional) Qualquer um dos seguintes:

* (Quando o anunciante usa um fornecedor de conformidade OBA para os anúncios) Código JavaScript apontando para a sobreposição de anúncio que permite que os usuários recusem o direcionamento comportamental online (OBA).

* Qualquer código de rastreamento de impressão de terceiros do JavaScript que será anexado à página de aterrissagem. **Observação:** também é possível inserir uma URL de rastreamento de impressão de terceiros no campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Editar uma experiência com direcionamento de árvore de decisão](experience-edit-targeting.md)
>* [Macros disponíveis para rastrear URLs](/help/creative/creative-macros.md)
