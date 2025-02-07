---
title: Configurações para experiências não direcionadas
description: Consulte descrições de todas as configurações para experiências de anúncio sem direcionamento de árvore decisória.
feature: Creative Experiences
source-git-commit: fbf663b38282f48facab57efaf5533892642a252
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 0%

---

# Configurações para experiências não direcionadas

*Beta fechado*

## seção [!UICONTROL Experience basics]

**[!UICONTROL Advertiser]:** (Somente leitura para experiências existentes) O anunciante que oferecerá os elementos de criação incluídos na experiência. Depois de salvar a experiência, você não poderá alterar o anunciante.

**[!UICONTROL Experience Name]:** Um nome exclusivo para a experiência. **Dica:** use um nome fácil de encontrar quando você usar a experiência como um anúncio no Advertising DSP ou em outro DSP.

**[!UICONTROL Creative Library]:** (Somente leitura para experiências existentes) Uma única biblioteca criativa para usar na experiência. Depois de salvar a experiência, você não poderá alterar a biblioteca.

## seção [!UICONTROL Default creatives]

**\[Criações padrão especificadas\]:** As criações de imagem padrão a serem usadas quando um navegador não pode exibir criações atribuídas à experiência, como quando o navegador não está habilitado para JavaScript ou o servidor de anúncios não pode personalizar o anúncio devido a atrasos. Inclua um criativo de imagem por tamanho de anúncio ao qual a experiência se aplica. Suas opções determinam os tamanhos criativos que podem ser usados para a experiência. <!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

Para experiências sem direcionamento de árvore de decisão, você pode substituir os criativos padrão por criativos do mesmo tamanho em [!UICONTROL Tag Manager].<!-- verify -->

* Para adicionar um criativo padrão com dimensões diferentes, clique em **[!UICONTROL + Add Sizes]**, marque a caixa de seleção ao lado de cada criativo a ser adicionado do painel direito e clique em **[!UICONTROL Add Creatives]**.

* Para excluir um criativo padrão, mantenha o cursor sobre a miniatura criativa e clique em ![Excluir](/help/creative/assets/delete.png "Excluir").

* Para excluir todas as criações padrão, clique em ![Excluir](/help/creative/assets/delete.png "Excluir") **[!UICONTROL Delete all]**.

* Para mostrar ou ocultar o painel Criativos à direita, clique em ![Mostrar/Ocultar](/help/creative/assets/hide-show-creatives.png "Mostrar/Ocultar") no canto superior direito do painel.

## seção [!UICONTROL Targeting]

**[!UICONTROL Targeting]:** (Somente leitura para experiências existentes) Não aplicável quando você não deseja habilitar o direcionamento usando uma árvore de decisão; mantenha essa opção desabilitada.

**[!UICONTROL Dynamic ads]:** (Somente leitura para experiências existentes) Indica que a experiência inclui anúncios dinâmicos. **Observação:** uma experiência pode incluir todos os anúncios padrão ou todos os anúncios dinâmicos.

**[!UICONTROL Language Targeting]:** (Experiências somente com anúncios padrão; opcional; somente leitura para experiências existentes) Verifica as configurações de idioma do navegador do usuário e exibe um criativo no idioma especificado quando um criativo nesse idioma estiver disponível. Quando um criativo no idioma especificado pelo navegador não está disponível, a configuração [!UICONTROL Preferred language] é usada. Depois de salvar a experiência, você não poderá alterar essa configuração.

**[!UICONTROL Preferred language]:** (Experiências somente com anúncios padrão; somente leitura para experiências existentes) O idioma para todos os anúncios criados a partir da experiência, exceto quando [!UICONTROL Language Targeting] está habilitado. Depois de salvar a experiência, você não poderá alterar essa configuração.

## seção [!UICONTROL Advanced]

**Data Pass:** (Experiências somente com anúncios dinâmicos; opcional) Para direcionar usuários com base em pares de valores-chave específicos que o DSP, o editor ou o parceiro transmite em tempo real na impressão. Você pode especificar até cinco chaves de passagem de dados (parâmetros).<!-- May move this to just within the decision tree. -->

Posteriormente, ao criar uma tag de experiência de anúncio para um tamanho criativo específico, cada chave especificada nesse campo é anexada como uma macro na tag. Você deve inserir o valor de cada par de valor-chave na tag antes de implementar a tag como um anúncio no DSP.

**Raio:** (somente experiências com anúncios dinâmicos; opcional) Um raio de usuário para direcionamento. Selecione um raio de 0 a 200 milhas.<!-- Does this end up in the ad tag parameters? -->

**Pixel de RT:** (Experiências somente com anúncios dinâmicos; opcional) Um pixel de redirecionamento [!UICONTROL Creative] para direcionamento potencial. Ao configurar o direcionamento na árvore de decisão, você pode incluir um nível de nós de destino de pixel de RT e especificar o pixel a ser direcionado para cada nó, bem como os valores necessários para os atributos de pixel que devem estar presentes para mostrar as criações nos pacotes criativos atribuídos. Se você não especificar um pixel nesse campo, ainda será possível especificar um na árvore de decisão.&lt;!— De R: &quot;o pixel de RT deve ser por meio da seleção de conteúdo na configuração do anúncio dinâmico&quot; — esclarecer. Eu vejo &quot;Datapass&quot; (uma palavra) nas configurações de anúncios dinâmicos, mas não tenho certeza de como essa configuração e este nível de experiência funcionam juntos. —>

**[!UICONTROL Label]:** <!-- should be "Labels" --> (Opcional) Quaisquer rótulos específicos de [!DNL Creative] para aplicar à experiência. Você pode filtrar experiências por rótulo na exibição Experiências<!-- sic -->.

* Para selecionar rótulos existentes, clique em ![Abaixo](/help/creative/assets/chevron-down.png "Abaixo") e marque a caixa de seleção ao lado de cada rótulo a ser aplicado.

* Para pesquisar rótulos existentes, comece inserindo uma cadeia de texto no nome do rótulo.

* Para criar um novo rótulo para aplicar, abra a lista, clique em **+ Adicionar Rótulo**, digite um novo nome de rótulo no campo [!UICONTROL Label] e clique em **Criar**.

* Para remover um rótulo, desmarque a caixa de seleção ao lado do nome do rótulo.

**[!UICONTROL Impression Tracking URL]:** (opcional) uma URL de rastreamento de impressão de terceiros a ser anexada à URL da página de aterrissagem para qualquer anúncio criado a partir da experiência. É possível incluir até cinco URLs. Para adicionar uma URL adicional, clique em ![ícone](/help/creative/assets/create.png) **[!UICONTROL Add More] e insira a URL.

Depois de inserir um URL, todas as macros disponíveis e os dados com os quais elas são substituídas são listados mais abaixo na página. Para inserir uma das macros na URL, mantenha o cursor sobre a descrição da macro e clique em ![Copiar para a área de transferência](/help/creative/assets/copy-to-clipboard.png "Copiar para a área de transferência") e cole a macro sempre que desejar no campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefixa automaticamente suas próprias marcas de rastreamento de impressão à URL da página de aterrissagem.
>* Você pode substituir esse URL por qualquer criativo na experiência.
>* Você também pode inserir um código de rastreamento de impressão de terceiros no JavaScript no campo [!UICONTROL Client JS]

**[!UICONTROL Click Tracking URL]:** (Opcional) (Opcional) Uma URL de rastreamento de cliques de terceiros a ser anexada à URL da página de aterrissagem. É possível incluir até cinco URLs. Para adicionar uma URL adicional, clique no ![ícone](/help/creative/assets/create.png) **[!UICONTROL Add More]** e insira a URL.

Depois de inserir um URL, todas as macros disponíveis e os dados com os quais elas são substituídas são listados mais abaixo na página. Para inserir uma das macros na URL, mantenha o cursor sobre a descrição da macro e clique em ![Copiar para a área de transferência](/help/creative/assets/copy-to-clipboard.png "Copiar para a área de transferência") e cole a macro sempre que desejar no campo URL.

>[!NOTE]
>
>* [!DNL Creative] prefixa automaticamente suas próprias marcas de rastreamento de impressão à URL da página de aterrissagem.
>* Você pode substituir esta URL para qualquer <!-- creative bundle for targeted experiences --> criativo na experiência.

**[!UICONTROL Client JS]:** (Opcional) Qualquer um dos seguintes:

* (Quando o anunciante usa um fornecedor de conformidade OBA para os anúncios) Código JavaScript apontando para a sobreposição de anúncio que permite que os usuários recusem o direcionamento comportamental online (OBA).

* Qualquer código de rastreamento de impressão de terceiros do JavaScript que será anexado à página de aterrissagem. **Observação:** também é possível inserir uma URL de rastreamento de impressão de terceiros no campo [!UICONTROL Impression Tracking URL].

>[!MORELIKETHIS]
>
>* [Criar uma experiência sem definição de metas da árvore de decisão](experience-create-no-targeting.md)
>* [Editar uma experiência sem definição de metas da árvore de decisão](experience-edit-no-targeting.md)
>* [Crie manualmente uma marca de anúncio para um tamanho criativo aplicável](experience-tag-create-manually.md)
>* [Atribuir criações a uma marca de anúncio para experiências sem direcionamento](experience-tag-assign-creatives.md)
>* [Personalizar as URLs de rastreamento para uma experiência sem direcionamento](experience-tracking-urls-no-targeting.md)
>* [Personalize a otimização criativa e o agendamento de uma experiência sem direcionamento](experience-optimization-scheduling-no-targeting.md)
