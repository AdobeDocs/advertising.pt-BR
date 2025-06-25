---
title: Perguntas frequentes sobre campanhas
description: Consulte respostas de perguntas sobre o gerenciamento de campanhas e visualizações de dados de campanha.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Perguntas frequentes sobre o gerenciamento de campanhas

## Informações gerais

+++É possível mover campanhas e componentes de uma conta para outra?

Não mova ou copie um componente de campanha ou de campanha, que tem uma ID exclusiva, para uma conta com uma ID de conta diferente. Isso resulta em erros de dados.
+++

+++Quando os dados de cliques são atualizados pelas redes de anúncios?

O processo de obtenção dos dados de cliques do dia anterior nos mecanismos de pesquisa começa às 06:00 no fuso horário do anunciante.

Além disso, as [!DNL Google Ads] métricas de desempenho em nível de campanha na rede de pesquisa do dia atual são extraídas às 08:00 e 16:00 no fuso horário do anunciante.
+++

+++Que ações fazem com que palavras-chave e anúncios percam seu histórico?

>[!NOTE]
>
>(Anunciantes com portfólios) Espere que o desempenho das novas combinações de palavras-chave e tipos de correspondência seja volátil, enquanto o Search, Social e Commerce reúne dados para criar modelos para elas.

**Ações nas exibições [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns], no processo de postagem de bulksheet e no próprio editor de rede de anúncios:**

A palavra-chave ou anúncio existente é excluído e outro é criado quando:

* ([!DNL Baidu], [!DNL Google Ads] e [!DNL Yandex]) Você edita um nome de palavra-chave.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] e [!DNL Yandex]) Você altera o tipo de correspondência de uma palavra-chave.

* Você move uma palavra-chave entre grupos de anúncios.

* ([!DNL Google Ads] anúncios de pesquisa dinâmica, [!DNL Microsoft Advertising] anúncios de texto expandidos e todos os tipos de anúncios em outras redes de anúncios com suporte) Você edita uma cópia de anúncio (título/título ou descrição) ou uma imagem de anúncio.

* Você move um anúncio entre grupos de anúncios.

**Eventos no processo de lançamento do feed de estoque do produto:**

Um anúncio ou palavra-chave existente é excluído e outro é criado quando:

* Um arquivo de feed contém um novo valor para uma coluna usada em uma variação de anúncio.

* As configurações do modelo para um anúncio foram alteradas desde a última propagação.

* Um novo arquivo de feed inclui uma linha para um anúncio ou palavra-chave que a) estava em um arquivo anterior, mas b) foi omitido desde então e foi pausado ou excluído de acordo com as configurações de dados do feed.

Dependendo das [configurações de dados do feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), um anúncio ou palavra-chave existente poderá ser excluído quando:

* Um novo arquivo de feed não inclui uma linha para um anúncio ou palavra-chave existente.

* A data de término agendada para os componentes de um arquivo de feed publicado ocorre.

* O nível de estoque de um item cai abaixo de um mínimo especificado nas configurações de dados de feed.
+++

+++([!DNL Google Ads] campanhas) As alterações nos nomes para exibição das minhas [!DNL Google] conversões rastreadas foram revertidas.

Se você alterar os nomes para exibição das métricas de conversão em Pesquisa, Social e Commerce, suas alterações serão substituídas pelos nomes configurados em [!DNL Google Ads]. Faça qualquer alteração de nome em [!DNL Google Ads].
+++

+++(Campanhas do Google Ads) É possível usar um orçamento compartilhado para campanhas em portfólios?

Para obter melhores resultados, não adicione campanhas do [!DNL Google Ads] a um orçamento compartilhado do [!DNL Google Ads] se elas estiverem em portfólios otimizados configurados como &quot;[!UICONTROL Auto adjust campaign budget limits].&quot; Se você fizer isso, [!DNL Google Ads] substituirá os orçamentos de campanha otimizados para Pesquisa, Social e Commerce, o que pode levar a ineficiências de oferta.
+++

+++([!DNL Google Ads] campanhas) Posso enviar usuários móveis e não móveis para diferentes páginas de aterrissagem?

Você pode usar os [!DNL Google Ads] [!DNL ValueTrack] parâmetros `{ifmobile}` e `{ifnotmobile}` para determinar o nome de domínio da página de aterrissagem de uma das duas formas a seguir, conforme aplicável aos seus sites:

* Inclua a designação móvel como o servidor host usando `{ifmobile:m}{ifnotmobile:www}`.

  Por exemplo, `http://{ifmobile:m}{ifnotmobile:www}.example.com` leva usuários móveis para m.example.com e usuários não móveis para www.example.com.

* Inclua a designação móvel como o domínio de nível superior usando `{ifmobile:mobi}{ifnotmobile:com}`.

  Por exemplo, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` leva usuários móveis para www.example.mobi e usuários não móveis para www.example.com.

Em ambos os casos, as URLs de base com rastreamento de Search, Social e Commerce incluem as tags `{}` não codificadas e quaisquer parâmetros adicionais anexados à URL de base.

>[!NOTE]
>
>Não use um URL completo como o valor para ifnotmobile e ifmobile; use apenas a parte variável do URL (como &quot;m&quot; versus &quot;www&quot;, ou &quot;mobi&quot; versus &quot;com&quot;).

+++

+++([!DNL Google Ads] campanhas na rede de pesquisa) Quais dados são mostrados para hoje?

[!DNL Google Ads] métricas de desempenho em nível de campanha na rede de pesquisa do dia atual são extraídas às 08:00 e 16:00 no fuso horário do anunciante.

Na guia [!UICONTROL Campaigns] da exibição [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] e na exibição [!UICONTROL Optimization] > [!UICONTROL Portfolios], quando você cria relatórios sobre [!UICONTROL Today] ou em um intervalo de datas personalizado que inclui o dia atual, os dados incluem os dados sincronizados mais recentemente.

>[!NOTE]
>
>Os dados de cliques, impressões e conversões são atrasados em três horas e não são concluídos até o próximo pull de dados.

+++

+++Qual é a diferença entre um modelo de rastreamento e um sufixo de página de destino?

Use um sufixo de página de aterrissagem somente para redes de anúncios que oferecem suporte ao rastreamento paralelo. Em Search, Social e Commerce, os modelos de rastreamento e os sufixos de página de aterrissagem devem incluir um identificador de clique na rede de anúncios, mas os modelos de rastreamento incluem parâmetros de rastreamento adicionais.

Consulte as próximas Perguntas frequentes sobre o [suporte ao rastreamento paralelo](#parallel-tracking) para obter mais informações sobre como os modelos de rastreamento e os sufixos de página de aterrissagem são carregados quando um usuário clica em um anúncio.

+++

+++([!DNL Google Ads] e [!DNL Microsoft Advertising]) O Search, Social e Commerce oferece suporte ao rastreamento paralelo de anúncios em [!DNL Google Ads] ou [!DNL Microsoft Advertising]? {#parallel-tracking}

O rastreamento paralelo envia clientes diretamente do seu anúncio para o URL final, que pode incluir parâmetros anexados de um sufixo de URL final ou &quot;sufixo de página inicial&quot;. O URL do modelo de rastreamento (com parâmetros adicionais para medição de cliques) é carregado separadamente em segundo plano; como resultado, a landing page é carregada mais rapidamente.

O Search, Social e &amp; Commerce oferece suporte ao rastreamento paralelo para campanhas de pesquisa e compras usando o identificador de cliques da rede de publicidade (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para [!DNL Google Ads]). Use um [nível de conta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) ou [nível de campanha](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (chamado &quot;[!DNL final URL suffix]&quot; nas redes de anúncios), que é anexado às URLs da página de aterrissagem para rastrear cliques em anúncios secundários de navegadores que oferecem suporte para rastreamento paralelo. Consulte os [formatos de sufixo obrigatórios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e [formatos de sufixo obrigatórios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Quando um usuário visualiza seu anúncio em um navegador que não oferece suporte ao rastreamento paralelo, a rede de anúncios usa o rastreamento sequencial: os clientes são enviados primeiro ao URL do modelo de rastreamento, que pode redirecionar os clientes para servidores de rastreamento intermediários antes de redirecioná-los para o URL final (que pode incluir parâmetros adicionais em um sufixo de página de aterrissagem). Todos os modelos de rastreamento de uma conta de rede de publicidade devem incluir o mesmo parâmetro de identificador de cliques usado em [!UICONTROL Landing Page Suffix]. Consulte os [formatos de modelo de rastreamento para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) e os [formatos de modelo de rastreamento para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Por que as URLs de rastreamento dos meus anúncios incluem &quot;`&EV_HASH={<hash>}`&quot;?

Ao carregar anúncios usando um [feed de inventário de produtos](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) para uma conta com o redirecionamento de pixels de Pesquisa, Social e Commerce e com rastreamento de nível de palavra-chave e criação, o Search, Social e Commerce adiciona o parâmetro de hash e o valor ao modelo de rastreamento do anúncio ou à URL de destino para identificar se ele foi criado usando o recurso de feed de inventário.
+++

## Feeds de inventário

+++(Feeds de inventário de produtos) Devo pausar ou excluir anúncios que estão obsoletos ou que são para um produto cujo nível de estoque está abaixo de um mínimo especificado?

Depende dos requisitos comerciais do anunciante.

Quando você pausa anúncios, eles são reativados se você reenviar o mesmo anúncio ou o nível de estoque ultrapassar o mínimo. Isso permite que você retenha o histórico do anúncio.

Quando você exclui anúncios e os reenvia, novos anúncios são criados e os dados históricos precisam ser acumulados para os novos anúncios. No entanto, se você não espera enviar novamente os anúncios excluídos, ter dados históricos não é importante.
+++

+++(Feeds de inventário de produtos) Se eu excluir um modelo de anúncio e criar um novo e idêntico, faltam itens no próximo arquivo de feed pausado (quando as configurações do arquivo de feed são definidas para isso)?

Se o próximo arquivo de feed não tiver itens de linha e você não tiver lançado esses itens de linha do novo modelo por meio de um arquivo de feed anterior, os itens de linha ausentes não serão reconhecidos como &quot;ausentes&quot;, portanto, não serão criados. Para evitar isso, propague o arquivo de feed anterior por meio do novo modelo e publique os dados antes de propagar e publicar dados de um novo arquivo.
+++

+++(Feeds de inventário de produtos) É possível atualizar preços para meus produtos sem afetar a pontuação de qualidade de um anúncio?

Para campanhas [!DNL Google Ads], sim: as variáveis [!DNL Google Ads] `{Param 1}` e `{Param 2}` permitem inserir dinamicamente valores numéricos em uma variação de anúncio sem excluir e recriar o anúncio e, portanto, sem afetar a pontuação de qualidade.

Para usar uma variável `{Param 1}` ou `{Param 2}` para seus dados de preço, mapeie a coluna de preço em seu arquivo de dados para essa variável nos modelos de feed apropriados e, em seguida, inclua a variável em seus modelos de variação de anúncios.

Por exemplo, se a coluna for chamada de &quot;Preço&quot;, abra o modelo de feed que cria os anúncios, clique no campo de entrada ao lado de **[!UICONTROL Param 1]** e clique na coluna **[!UICONTROL Price]** na lista [!UICONTROL Feeds/Available Columns], que insere `[Price]` como o valor de [!UICONTROL Param 1]. Em seguida, no modelo de variação de anúncios, na parte inferior do modelo de feed, insira `{param1:default text}`, onde &quot;texto padrão&quot; é o texto a ser usado se a coluna de parâmetro no arquivo de feed estiver vazia para uma linha de anúncio.

Ao enviar dados, os campos de dados das colunas [!UICONTROL Param1] e [!UICONTROL Param2] podem incluir até 25 caracteres, incluindo dados numéricos, símbolos de moeda e códigos de moeda, além dos seguintes caracteres não numéricos: `, . % + - /`
+++

+++Minhas campanhas geradas por feeds de inventário têm muitas transações órfãs.

Se as [configurações de dados de feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) estiverem definidas para excluir anúncios em várias situações, quaisquer conversões atrasadas que ocorrerem após os cliques no anúncio poderão causar [transações órfãs](/help/search-social-commerce/glossary.md#o-p). A prática recomendada é pausar os anúncios em vez de excluí-los. Se um anúncio ainda não tiver recebido nenhuma receita após um longo tempo, é possível excluí-lo por meio de uma bulksheet ou exibição de gerenciamento de anúncios.
+++

## Problemas de desempenho relacionados à conta e à campanha

+++Algumas de minhas campanhas estão gastando mais ou menos do que os orçamentos da campanha.

* Isso é normal em um portfólio otimizado configurado com a opção &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot;. Quando esta opção está habilitada, você pode gastar até *N* vezes o orçamento de cada campanha, onde *N* é o valor da configuração &quot;[!UICONTROL Multiple]&quot;. Essa opção permite que o recurso de otimização ajuste os gastos de campanhas individuais, conforme necessário, enquanto orienta todo o portfólio a atender à sua meta.
* Se as campanhas [!DNL Google Ads] usarem um orçamento compartilhado, o [!DNL Google Ads] ajustará os gastos de campanhas individuais conforme necessário para gastar todo o orçamento compartilhado.
+++
