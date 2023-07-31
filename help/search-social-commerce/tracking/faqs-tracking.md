---
title: Perguntas frequentes sobre rastreamento
description: Saiba mais sobre respostas a perguntas comuns sobre rastreamento, incluindo a solução de problemas.
exl-id: f559b977-dd44-4d29-b49e-c41c6fb783d1
feature: Search Tracking
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Perguntas frequentes sobre rastreamento

## Recursos de rastreamento

+++É possível rastrear campanhas que o Adobe Advertising não gerencia?

Sim. Se o Search, Social e Commerce estiver sincronizando uma de suas contas de rede de anúncios, ele rastreará os dados de cliques da rede de anúncios para todos [tipos de campanha compatíveis](/help/search-social-commerce/introduction/supported-inventory.md) nessa conta. Ele também rastreia dados de conversão se você tiver adicionado o redirecionamento de Pesquisa, Social e Comércio aos URLs de destino do seu anúncio e/ou palavra-chave ou modelos de rastreamento e implementado o rastreamento de conversão em suas páginas de conversão. Esclareça com sua equipe de conta do Adobe quais campanhas você deseja que o Search, Social e Commerce simplesmente rastreiem e quais você deseja que eles gerenciem.
+++

+++Como faço para obter a atribuição de vários eventos?

Para anunciantes que usam tags de rastreamento de conversão de Pesquisa, Social e Comércio ou Adobe Analytics, o Adobe Advertising fornece várias opções para atribuir dados de conversão em uma série de eventos que levam a uma conversão. Uma configuração no nível do anunciante determina como atribuir dados de conversão em eventos, mesmo quando eles ocorrem em vários canais de anúncio, desde que os canais permitam o rastreamento de impressões no nível do evento. Por padrão, as conversões são atribuídas ao último evento (mais recente), mas a configuração pode ser definida de forma diferente; por exemplo, para atribuir conversões ao primeiro evento ou para pesar todos os eventos uniformemente. A alteração da regra de atribuição afeta como as ofertas futuras são calculadas.

Os anunciantes que fornecem todos os dados de conversão em um arquivo de feed devem atribuir a conversão aos próprios eventos de transação relacionados.

>[!NOTE]
>
>Em exibições, relatórios e simulações personalizadas de gerenciamento de campanhas e gerenciamento de portfólio (disponíveis para alguns usuários), é possível alterar a regra usada para atribuir dados de conversão nas exibições e resultados do relatório, sem afetar como as ofertas futuras são calculadas.

+++

+++Como o Adobe Advertising identifica transações duplicadas?

Transações duplicadas podem ocorrer quando um usuário atualiza a página de confirmação após concluir uma transação. O Adobe Advertising usa o `ev_transid` para eliminar transações duplicadas com a mesma ID de transação e valor de propriedade.

O seguinte é uma lógica de desduplicação de Adobe Advertising:

* **Quando um cliente envia um valor para o `ev_transid` atributo:** As solicitações de pixel subsequentes são consideradas duplicatas da anterior se as seguintes forem todas iguais: o `ev_transid`; a ID de rastreamento para a mesma palavra-chave, anúncio ou posicionamento; e o valor de uma métrica de conversão específica.

  Por exemplo, se vários aplicativos de empréstimo tiverem a mesma ID de aplicativo e valor de empréstimo para a mesma palavra-chave em uma rede de anúncios específica, eles serão considerados duplicados e somente o primeiro aplicativo de empréstimo será contado.

* **Quando um cliente não envia um valor para o `ev_transid` atributo:** As transações subsequentes são consideradas duplicatas da anterior se compartilharem uma ID de rastreamento para a mesma palavra-chave, anúncio ou posicionamento e o mesmo valor para uma métrica de conversão específica.

  Por exemplo, se vários aplicativos de empréstimo tiverem a mesma ID de palavra-chave e valor de empréstimo, eles serão considerados duplicados e somente o primeiro aplicativo de empréstimo será contado.
+++

## Tipos de implementação de rastreamento

+++Desejo parar de usar o serviço de rastreamento de conversão do Adobe Advertising para uma ou mais campanhas ou contas. Como posso remover rapidamente o código de rastreamento dos URLs de rastreamento?

Primeiro, consulte a Equipe de conta do Adobe para entender as implicações da remoção de URLs de rastreamento.

Na conta ou campanha, altere o método de rastreamento para &quot;[!UICONTROL No EF Redirect].&quot; Em seguida, crie uma bulksheet usando o &quot;[!UICONTROL Generate Tracking URLs]&quot; e publique-a na rede de publicidade. Todos os URLs de rastreamento ou de destino existentes são substituídos.
+++

## Perguntas sobre dados

+++Como sei qual métrica de conversão é de um feed de dados ou é rastreada pela tag de rastreamento de conversão do Adobe Advertising?

Em um [!UICONTROL Transaction Report], é possível saber se uma métrica de conversão incluída foi rastreada pelo pixel de rastreamento de conversão do Adobe Advertising, caso inclua a coluna personalizada &quot;[!UICONTROL Tracking URL].&quot; Os URLs de rastreamento com o pixel de rastreamento de Adobe Advertising começam com `http://pixel.everesttech.net`.
+++

+++O que são transações órfãs?

As transações órfãs são eventos de transação que não podem ser associados a uma palavra-chave ou anúncio específico. O Adobe Advertising atribui transação/receita a uma palavra-chave ou anúncio ao corresponder as IDs de rastreamento recebidas com o evento de receita à ID de rastreamento exclusiva no URL de rastreamento da palavra-chave ou do anúncio.

Quando uma equipe de conta do Adobe suspeita que as transações órfãs são responsáveis por uma queda na receita, a equipe de Atendimento ao cliente verifica os órfãos e, se encontrar algum, investiga o problema.

Órfãos ocorrem nas seguintes situações.

**Implementações do Pixel**

As transações órfãs quase nunca ocorrem para implementações de pixel. No entanto, os órfãos de pixels ocorreram quando:

* Os dados de clique não estão disponíveis para a data de clique da conversão. Nesse caso, os dados são mapeados de volta quando Search, Social e Commerce obtém os dados de cliques da rede de anúncios.

* Os logs de clique não são processados antes dos logs de conversão.

**Implementações do feed**

* A ID de rastreamento enviada no feed é de uma conta que o Search, Social e &amp; Commerce não conhecem.

* A conta não está sincronizada ou ocorreram erros durante o processo de sincronização.

* A ID de rastreamento foi adicionada e removida da rede de publicidade enquanto a Search, Social e Commerce estava fora de sincronia com a rede de publicidade. Portanto, a Search, Social e Commerce não tem informações sobre a ID. Esse problema continuará a causar receita órfã se houver um atraso no recebimento da receita.

* O cliente enviou uma ID de rastreamento formatada incorretamente no feed e não corresponde à ID de rastreamento no URL. Isso geralmente ocorre devido a um problema de formatação ou quando as IDs de rastreamento são abreviadas no feed.

* No arquivo de configuração, a expressão regular usada para extrair a ID de rastreamento dos URLs está incorreta ou desatualizada. Às vezes, o anunciante altera a ID de rastreamento no URL ou adota um sistema de rastreamento totalmente novo, o que requer que a equipe de implementação de Pesquisa, Social e Comércio atualize a expressão regular. Nesses casos, uma grande parte da receita é órfã.

**Implementações de feed usando uma ID de transação**

Nenhuma transação online está disponível antes das datas para as quais os dados estão disponíveis no feed offline.

**Implementações de feed usando um token (ef_id)**

O Search, Social e Commerce não encontrou um clique correspondente em seu servidor ou na rede de anúncios. Isso pode ocorrer porque os dados de clique não estão disponíveis para a data de clique da conversão ou (raramente) porque os logs de clique não foram processados antes dos logs de conversão. Quando Search, Social e Commerce recebe os dados de clique da rede de anúncios ou os logs de clique são processados, os dados são mapeados para a conversão.
+++

## Problemas de rastreamento de receita

+++Como corrijo dados antigos/incorretos de um arquivo de feed?

Entre em contato com o Atendimento ao cliente com o arquivo de dados corrigido.
+++

+++Várias palavras-chave têm os mesmos URLs de rastreamento.

**Implicações**

Para implementações de feed com várias IDs de rastreamento, os dados são relatados em relação a várias palavras-chave. Para outras implementações, as conversões podem ser atribuídas à palavra-chave errada porque o sistema atribui uma conversão arbitrariamente a uma das palavras-chave.

**Causa possível**

O URL de uma nova palavra-chave ou anúncio foi copiado de outra palavra-chave ou anúncio.

Isso não deve acontecer com anúncios de exibição ou sociais.

**Possível solução ou solução alternativa**

* Se você gerencia suas próprias palavras-chave e anúncios, crie um arquivo de bulksheet com os URLs corretos para os URLs duplicados e publique-o na conta apropriada usando o **[!UICONTROL Generate Tracking URLs]** que gera URLs para todas as palavras-chave e anúncios.

* Se uma Equipe da conta do Adobe gerenciar suas palavras-chave, peça que criem novos URLs para os URLs duplicados.
+++
