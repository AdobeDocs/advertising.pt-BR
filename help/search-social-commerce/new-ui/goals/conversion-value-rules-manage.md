---
title: (Nova interface do usuário) Gerenciar [!DNL Google Ads] regras de valor de conversão
description: Saiba como visualizar e gerenciar  [!DNL Google Ads] as regras de valor de conversão do Search, Social e Commerce.
feature: Conversions
source-git-commit: 1113c9f6ff8446d075dc9b90441f4119eb657598
workflow-type: tm+mt
source-wordcount: '1844'
ht-degree: 0%

---

# (Nova interface do usuário) Gerenciar [!DNL Google Ads] regras de valor de conversão

*recurso do Beta*

[!DNL Google Ads] [as regras de valor de conversão](https://support.google.com/google-ads/answer/10518330) permitem que você ajuste os valores dos eventos de conversão com base nas informações do usuário, incluindo o tipo de dispositivo, o local e o segmento do público-alvo. Você pode usar regras para ofertas baseadas em valor em campanhas máximas de pesquisa, exibição, compras e desempenho com o Google Smart Bidding. Para campanhas com estratégias de lances Maximizar conversões e Direcionar ROAS, [!DNL Google Ads] algoritmos começarão a preferir conversões com um valor maior.

As regras de valor de conversão no nível da campanha substituem as regras no nível da conta. Quando uma conversão satisfaz várias regras de valor de conversão, somente uma das regras é aplicada. Normalmente, a regra mais específica é aplicada, mas consulte a [[!DNL Google Ads] documentação sobre prioridades para os diferentes tipos de condição de regra](https://support.google.com/google-ads/answer/10520348).

## A exibição e a funcionalidade [!UICONTROL Conversion Value Rules]

O Search, Social e Commerce sincroniza automaticamente as regras de valor de conversão de suas contas do [!DNL Google Ads]. Todas as regras criadas na interface [!DNL Google Ads] são sincronizadas em 24 horas e estão disponíveis na exibição [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules].

Algumas contas podem gerenciar suas regras de valor de conversão:

* Em contas para as quais as conversões são rastreadas no nível de conta individual ou de campanha, você pode [criar](#google-conversion-value-rule-create), [editar](#google-conversion-value-rule-edit) e [alterar o status](#google-conversion-value-rule-change-status) das suas regras no nível de conta e de campanha.

  As contas podem ser vinculadas a [!DNL Google Ads] contas de gerente, mas elas não podem usar o rastreamento de conversões entre contas (para as quais as conversões são rastreadas em todas as contas na conta de gerente).

* Em contas que usam o rastreamento de conversão entre contas, suas regras de nível de conta e de nível de campanha são herdadas da conta do gerente e são somente leitura.

## Regras de valor de conversão com portfólios do Search, Social e Commerce

Quando a conta do anunciante está configurada para carregar objetivos do Search, Social e Commerce para [!DNL Google Ads], e você inclui uma campanha que usa uma regra de valor de conversão em um portfólio com um objetivo, então [!DNL Google Ads] aplica a regra de valor de conversão ao valor de conversão original especificado no objetivo. Como resultado, os dados de conversão do Search, Social e Commerce são diferentes dos dados de conversão do [!DNL Google Ads].

Por exemplo, suponha que o objetivo use uma única métrica de conversão &quot;Clientes potenciais&quot; e dê às conversões de dispositivos móveis um peso de 10 e às conversões de dispositivos não móveis um peso de 10. Search, Social e Commerce conta um evento de qualquer tipo de dispositivo como uma (1) conversão e credita o valor de conversão como 10. No entanto, suponha que uma campanha nesse portfólio use uma regra de valor de conversão &quot;Se o Dispositivo for Móvel, multiplique por 2&quot;. Quando um evento de cliente potencial móvel é rastreado para essa campanha, [!DNL Google Ads] também credita a contagem de conversão como um (1), mas o valor de conversão como (10 x 2) = 20.

Para ver mais informações sobre suas regras, incluindo os valores de conversão originais antes da aplicação das regras, consulte o [relatório de regras de valor de conversão em [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Criar uma regra de valor de conversão [!DNL Google Ads] {#google-conversion-value-rule-create}

Você pode criar regras de valor de conversão no nível da conta e do nível da campanha em contas do [!DNL Google Ads] para as quais as conversões são rastreadas no nível da conta individual ou inferior. Não é possível criar regras para contas com conversões entre contas que são rastreadas no nível da conta principal.

Cada regra inclui até duas condições, bem como o ajuste do valor de conversão a ser aplicado quando as condições forem atendidas. Todas as regras em uma conta devem usar o mesmo tipo de condições principais e secundárias (opcional). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;.

É possível criar várias regras no nível de cada campanha. No entanto, o [!DNL Google Ads] ainda não oferece a capacidade de criar novas regras no nível da conta fora do editor [!DNL Google Ads] quando uma regra no nível da conta já existe. Para criar regras adicionais a nível de conta, faça logon diretamente no [!DNL Google Ads] e use o editor [!DNL Google Ads].

**Observação:** as regras de valor de conversão no nível da campanha substituem as regras no nível da conta e somente uma regra pode ser aplicada a uma conversão. Para obter mais informações, consulte [como [!DNL Google Ads] determina qual regra é aplicada a uma conversão quando a conversão atende às condições para várias regras](https://support.google.com/google-ads/answer/10520348).

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Por padrão, a guia **[!UICONTROL Campaign]** é selecionada para mostrar todas as regras no nível da campanha.

1. (Opcional) Para criar uma regra no nível da conta, clique na guia **[!UICONTROL Account]**.

1. Na barra de ferramentas, clique em **[!UICONTROL Create Campaign Rule]** (na guia [!UICONTROL Campaign]) ou **[!UICONTROL Create Account Rule]** (na guia [!UICONTROL Account]).

1. Selecione a rede de publicidade e a conta. Para regras no nível da campanha, selecione também a campanha. Depois clique em **[!UICONTROL Next]**.

1. Defina as [configurações da regra de conversão](#google-ads-conversion-value-rule-settings).

   Você deve configurar uma condição primária e um ajuste de valor. Como opção, você pode configurar uma condição secundária.

   Em uma condição, vários destinos ou exclusões são unidos usando o operador Booleano `OR`, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador Booleano `ALL`, de modo que ambas as condições devem ser atendidas para iniciar um ajuste de valor. Exemplo: se \[O local é Argélia OU Tunísia\] E \[O dispositivo é móvel OU tablet\], adicione 1.5.

   **Observação:** todas as regras em uma conta devem usar o mesmo tipo de condições primárias e secundárias (opcionais). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;.

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

## Editar uma regra de valor de conversão de [!DNL Google Ads] {#google-conversion-value-rule-edit}

É possível editar uma regra de valor de conversão em contas/campanhas para as quais as conversões são rastreadas no nível de conta individual ou inferior. Não é possível editar uma regra para uma conta com conversões entre contas que são rastreadas no nível da conta principal.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Por padrão, a guia **[!UICONTROL Campaign]** é selecionada para mostrar todas as regras no nível da campanha.

1. (Opcional) Para exibir todas as regras no nível da conta, clique na guia **[!UICONTROL Account]**.

1. Marque a caixa de seleção ao lado da regra.

1. Na barra de ferramentas de ações em massa, clique em (/help/search-social-commerce/assets/edit-new.png &quot;Editar).

1. Edite as [configurações da regra de conversão](#google-ads-conversion-value-rule-settings).

   Não é possível editar os tipos de condição de uma regra existente, mas você pode editar as condições e os ajustes de valor.

   Você deve configurar uma condição primária e um ajuste de valor. Como opção, você pode configurar uma condição secundária.

   **Observação:** se você adicionar uma condição secundária, ela deverá ser do mesmo tipo de condição que as outras regras da conta. Por exemplo, se a Regra 1, outras regras na conta tiverem a condição secundária &quot;Local&quot;, quando outras regras incluírem uma condição secundária, a condição secundária deverá ser &quot;Local&quot;. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador Booleano `ALL`, de modo que ambas as condições devem ser atendidas para iniciar um ajuste de valor.

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

## Alterar o status de uma regra de valor de conversão [!DNL Google Ads] {#google-conversion-value-rule-change-status}

É possível pausar, ativar ou excluir uma regra de valor de conversão em contas e campanhas para as quais as conversões são rastreadas no nível de conta individual.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Por padrão, a guia **[!UICONTROL Campaign]** é selecionada para mostrar todas as regras no nível da campanha.

1. (Opcional) Para exibir todas as regras no nível da conta, clique na guia **[!UICONTROL Account]**.

1. Marque a caixa de seleção ao lado de cada linha a ser alterada.

1. Na barra de ferramentas de ações em massa,

   * Para ativar (habilitar) as regras pausadas, clique em **[!UICONTROL ...]>[!UICONTROL Activate]**.

   * Para pausar as regras ativas, clique em **[!UICONTROL ...]>[!UICONTROL Pause]**.

   * Para excluir regras ativas ou pausadas, clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir").

1. Na mensagem de confirmação, clique em **[!UICONTROL Confirm]**.

## [!DNL Google Ads] configurações da regra de valor de conversão {#google-conversion-value-rule-settings}

| Seção | Parâmetro | Descrição |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | A rede de publicidade. |
| | [!UICONTROL Account] | A conta da rede de publicidade. |
| | [!UICONTROL Campaign] | (Somente regras de valor de conversão no nível da campanha) A campanha publicitária. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Tipo de condição\] | (Somente leitura para regras existentes) O tipo de condição que deve ser atendida para acionar um ajuste de valor:<ul><li>*[!UICONTROL Device]:* Para direcionar todos os tipos de dispositivos ou tipos específicos.</li><li>*[!UICONTROL Location]:* Direcionar todos os países e territórios ou direcionar e excluir locais específicos.</li><li>*[!UICONTROL Audiences]:* Para direcionar todos os públicos ou públicos específicos</li></ul>**Observação:** todas as regras em uma conta devem usar o mesmo tipo de condições primárias e secundárias (opcionais). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;. |
| | \[Tipo de condição\] > [!UICONTROL Device] e [!UICONTROL Device Level] | (Somente condições do dispositivo) Qual dispositivo deve ser direcionado:<ul><li>*[!UICONTROL All devices]:** Para direcionar todos os tipos de dispositivo.</li><li>*[!UICONTROL Select devices]:* Para especificar um ou mais tipos de dispositivo para destino: *[!UICONTROL Desktop]:*, *[!UICONTROL Mobile]* e *[!UICONTROL Tablet]:*.</li></ul>Em uma condição, vários destinos são unidos usando o operador booleano `OR`, de modo que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: se \[O dispositivo é móvel OU tablet\], Adicionar 1.5. |
| | \[Tipo de condição\] > [!UICONTROL Location] e [!UICONTROL Location Level] | (Somente condições de localização) Os públicos-alvos e exclusões de localização:<ul><li>*[!UICONTROL All countries and territories]:* Para direcionar todos os países e locais ou direcionar e excluir locais específicos.</li><li>*[!UICONTROL Enter a location]:* Para direcionar e excluir locais específicos.</li></ul><ul><li>Para expandir um local ou sublocal, clique em `>` depois do nome.</li><li>Para adicionar um destino, selecione-o uma vez para mostrar uma marca de seleção verde.</li><li>Para excluir um destino, selecione o destino uma segunda vez para mostrar um **[!UICONTROL X]** vermelho.</li><li>Para remover um target ou uma exclusão, siga um destes procedimentos:<ul><li>Clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado do item na coluna [!UICONTROL Selections].</li><li>Selecione o destino até que nenhuma marca de seleção ou [!UICONTROL X] seja exibida.</li></ul></li></ul>Em uma condição, vários destinos ou exclusões são unidos usando o operador Booleano `OR`, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: Se \[O local é Argélia OU Tunísia\], então Adicione 1,5. |
| | \[Tipo de condição\] > [!UICONTROL Audience] e [!UICONTROL Audience Level] | (Somente condições do público-alvo) O público-alvo direciona:<ul><li>*[!UICONTROL All audience segments]:* Para direcionar todos os [!DNL Google Ads] segmentos de público-alvo.</li><li>*[!UICONTROL Enter audience segments]:* Para segmentar segmentos de público-alvo específicos de [!DNL Google Ads].</li></ul><ul><li>Para expandir uma categoria ou subcategoria em seus segmentos, clique em `>` depois do nome.</li><li>Para adicionar um target, selecione o target.</li><li>Para remover um destino, desmarque-o ou clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado do item na coluna [!UICONTROL Selection].</li></ul>Dentro de uma condição, vários targets ou exclusões são unidos usando o operador booleano OR, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: Se \[O público-alvo é de viagens de negócios OU de férias em família\], Adicionar 1.5.<br><br>**Observação:** depois de salvar um público-alvo, você poderá adicionar outros públicos-alvo, mas não poderá removê-los fora do editor [!DNL Google Ads]. Se você precisar remover um público-alvo, faça logon diretamente no [!DNL Google Ads] e use o editor [!DNL Google Ads]. |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[Tipo de condição\] | (Opcional; somente leitura para regras existentes) O tipo de condição que deve ser atendida para acionar um ajuste de valor. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador Booleano `ALL`, de modo que ambas as condições devem ser atendidas para iniciar um ajuste de valor. Exemplo: Se \[O local é Argélia OU Tunísia\] E \[O dispositivo é móvel OU tablet\], então Adicione 1.5.<br><br>Consulte as entradas das condições primárias para obter descrições.<br><br>**Observação:** todas as regras de uma conta devem usar o mesmo tipo de condições primárias e (opcionais) secundárias. Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;. |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation] e [!UICONTROL Adjustment Value] | Especifique o tipo de ajuste e insira um valor positivo:<ul><li>*[!UICONTROL Add]:* Adiciona o valor especificado ao valor de conversão passado. O valor deve ser maior que zero (0).</li><li>*[!UICONTROL Multiply]:* Multiplica o valor de conversão passado pelo valor especificado. O valor deve ser de 0,5 a 10.</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
