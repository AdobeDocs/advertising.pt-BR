---
title: Gerenciar anúncios
description: Saiba mais sobre anúncios em Pesquisa, Social e Comércio, incluindo os tipos de anúncios disponíveis.
source-git-commit: eaf08dedb14bdf0c0be087e48c79bbf21b0990aa
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 0%

---

# Sobre anúncios

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads], e [!DNL Yandex] somente contas*

Um anúncio pode ser exibido em um site de destino (para campanhas de conteúdo ou direcionadas por posicionamento); quando um usuário pesquisa uma das palavras-chave no grupo de anúncios (para campanhas de pesquisa) ou para conteúdo em seu site (anúncios de pesquisa dinâmicos no [!DNL Google Ads] campanhas somente de pesquisa); ou quando um usuário realiza uma pesquisa relevante para um dos itens em sua [!DNL Google Merchant Center] ou [!DNL Microsoft® Merchant Center] feed de produto (anúncios de compras no [!DNL Google Ads] ou anúncios de produto no [!DNL Microsoft® Advertising] campanhas).

## Tipos de anúncios disponíveis

Você pode criar e gerenciar os tipos de anúncios suportados para grupos de anúncios em uma conta de rede de anúncios sincronizada:

* **Anúncios de texto ou anúncios de texto expandidos** para um grupo de publicidade em uma campanha direcionada à rede de pesquisa. Os anúncios de texto podem incluir parâmetros de rastreamento opcionais que substituem os parâmetros de nível de grupo ou campanha do anúncio. Dependendo da rede de anúncios, talvez seja possível criar anúncios de texto expandidos/estendidos ou anúncios de texto padrão.

* Entre dispositivos, nativo **anúncios de público-alvo** para [!DNL Microsoft® Advertising] campanhas no [!DNL Microsoft® Audience Network]. Você tem duas opções para anúncios de público-alvo, com base nas configurações da campanha:

   * Se a campanha estiver vinculada a uma loja central de comerciantes, permita que a rede de publicidade gere automaticamente anúncios baseados em feed de anúncios para a campanha, usando as informações de produto da loja. Não é necessário criar anúncios baseados em feed para a campanha, mas você deve criar grupos de anúncios com direcionamento do usuário.

   * Se a campanha não estiver vinculada a uma conta do centro do comerciante, crie anúncios de público-alvo baseados em imagem usando o formato de anúncio responsivo, que inclui vários ativos de texto e imagem. A rede de anúncios monta os anúncios usando as combinações mais eficazes de elementos de anúncios e os exibe em sites como [!DNL MSN], [!DNL Outlook.com], e [!DNL Microsoft® Edge].

* **Anúncios somente de chamada** para [!DNL Google Ads] campanhas na rede de pesquisa. Anúncios somente para chamada são anúncios de texto que incluem um número de telefone. Opcionalmente, você pode usar um [!DNL Google Ads]- número de encaminhamento atribuído para o relatório avançado de chamadas.

* **Anúncios de pesquisa dinâmica expandidos** (agora chamado apenas de &quot;anúncios de pesquisa dinâmica&quot; nas redes de anúncios) para [!DNL Google Ads] e [!DNL Microsoft® Advertising] grupos de anúncios de pesquisa dinâmica em campanhas de pesquisa. Os anúncios de pesquisa dinâmicos usam o conteúdo de seu site, em vez de palavras-chave, para decidir quando mostrar seus anúncios. A rede de publicidade gera dinamicamente o título, escolhe o URL da página de aterrissagem e o URL de exibição e gera automaticamente o URL final.

  É possível definir as páginas dos sites cujo conteúdo é usado para direcionar os anúncios de pesquisa dinâmica, configurando alvos de pesquisa dinâmica específicos para o grupo de anúncios. Para [!DNL Google Ads], você pode criar alvos de pesquisa dinâmica em Pesquisa, Social e &amp; Commerce; para [!DNL Microsoft® Advertising], você deve criá-los em [!DNL Microsoft® Advertising]. Entrada [!DNL Google Ads] , você pode especificar um domínio de site e idioma no campo &quot;[!DNL DSA Options]&quot; em vez de, ou além de, criar públicos-alvo de pesquisa dinâmica.

  Quando o termo de pesquisa de um usuário corresponde exatamente a uma palavra-chave em uma de suas campanhas baseadas em palavras-chave, um anúncio da campanha baseada em palavras-chave é exibido em vez de um anúncio de pesquisa dinâmica. A rede de anúncios mostra um anúncio de pesquisa dinâmica em vez de um anúncio direcionado por palavra-chave quando o termo de pesquisa do usuário é uma correspondência ampla ou correspondência de frase para uma de suas palavras-chave e seu anúncio de pesquisa dinâmica tem uma classificação de anúncio mais alta.

  Para obter mais informações sobre os anúncios de pesquisa dinâmica, consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/2471185) e [[!DNL Microsoft® Advertising] documentação](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Anúncios multimídia** para [!DNL Microsoft® Advertising] campanhas de pesquisa. Anúncios multimídia são anúncios de imagens grandes, exibidos em posições proeminentes da linha principal e da barra lateral, e apenas um anúncio multimídia é exibido por página. Eles podem incluir vários ativos de texto e imagem, como anúncios responsivos, e a rede de anúncios monta os anúncios usando as combinações mais eficazes de elementos de anúncios. Os anúncios multimídia não substituem os posicionamentos de anúncios de texto.

* Linhas de promoção para **[!DNL Microsoft® Advertising]anúncios de produto (compras)** na rede de compras. Os anúncios de compras usam produtos em seu existente [!DNL Microsoft® Merchant Center] feed do produto, em vez de palavras-chave, para decidir como e onde mostrar seus anúncios. Os URLs da cópia de anúncio e da página de aterrissagem são gerados automaticamente a partir das informações do produto no feed, mas você pode, opcionalmente, configurar linhas de promoção a serem incluídas no grupo de anúncios.

  Você pode controlar quais produtos são mostrados com o seu [!DNL Microsoft® Advertising] anúncios de compras configurando grupos de produtos separados para o grupo de anúncios, a partir da [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] exibição.

  Para obter mais informações sobre o fluxo de trabalho para anúncios de produtos/compras, consulte &quot;[Implementar [!DNL Microsoft® Advertising] campanhas de compras](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md).&quot;  Para obter informações adicionais sobre anúncios de produtos, consulte [Documentação de publicidade da Microsoft®](https://help.ads.microsoft.com/#apex/3/en/51082).

* Anúncios de pesquisa responsivos para [!DNL Google Ads] e [!DNL Microsoft® Advertising] campanhas na rede de pesquisa. A rede de publicidade monta dinamicamente anúncios de pesquisa responsivos baseados em texto a partir de um conjunto de títulos e descrições de anúncios, favorecendo combinações com bom desempenho juntas. O anúncio inclui até três títulos, duas descrições e um URL personalizável do URL base e campos opcionais de caminho 1 e caminho 2. Opcionalmente, é possível fixar títulos e descrições de anúncios em posições específicas.

>[!NOTE]
>
>[!DNL Google Ads] não forneça dados fora de seus editores nativos sobre as combinações de texto que foram exibidas como anúncios. Para obter mais informações sobre relatórios para cada combinação de texto, consulte [Documentação do Google Ads](https://support.google.com/google-ads/answer/7684791).

## A variável [!UICONTROL Ads] exibir

É possível criar, editar e alterar o status dos anúncios de [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] exibição.

## Dados de desempenho no nível do anúncio

Os dados no nível do anúncio estão disponíveis para a maioria dos tipos de anúncios.

No entanto, não está disponível para [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA), desempenho máximo, compras inteligentes e [!DNL YouTube] campanhas. Espere discrepâncias entre o total de dados de nível de anúncio de uma campanha e o total de dados da campanha.

| Rede de publicidade/Campanha/Tipo de anúncio | Disponibilidade de dados |
|---|---|
| [!DNL Google Ads] anúncio de pesquisa dinâmica (DSA) | Campanha, grupo de publicidade |
| [!DNL Google Ads] desempenho máximo | Campaign |
| [!DNL Google Ads] compras, compras inteligentes | Campanha, grupo de publicidade |
| [!DNL Google Ads] [!DNL YouTube] | Campanha, grupo de publicidade |

>[!MORELIKETHIS]
>
>* [Gerenciar anúncios](ad-manage.md)
