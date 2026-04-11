---
title: '[!DNL Google Ads] configurações da regra de valor de conversão'
description: Referencie as configurações de  [!DNL Google Ads] regras de valor de conversão.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# [!DNL Google Ads] configurações da regra de valor de conversão

<!-- Go through all -->

| Seção | Parâmetro | Descrição |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | A rede de publicidade. |
| | [!UICONTROL Account] | A conta da rede de publicidade. |
| | [!UICONTROL Campaign] | A campanha publicitária. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Tipo de condição\] | (Somente leitura para regras existentes) O tipo de condição que deve ser atendida para acionar um ajuste de valor:<ul><li>**Dispositivo:** Para direcionar todos os tipos de dispositivos ou tipos específicos.</li><li>**Local:** Para direcionar todos os países e territórios ou direcionar e excluir locais específicos.</li><li>**Públicos-alvo:** Para direcionar todos os públicos-alvo ou públicos-alvo específicos</li></ul>**Observação:** todas as regras em uma conta devem usar o mesmo tipo de condições primárias e secundárias (opcionais). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;. |
| | Tipo de condição > Dispositivo | (Somente condições do dispositivo) Qual dispositivo deve ser direcionado:<ul><li>**Todos os dispositivos** — Para direcionar todos os tipos de dispositivos.</li><li>**Selecionar dispositivos** — Para especificar um ou mais tipos de dispositivos a serem direcionados: **Área de Trabalho**, **Celular** e **Tablet**.</li></ul>Em uma condição, vários destinos são unidos usando o operador booleano OR, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: se \[O dispositivo é móvel OU tablet\], Adicionar 1.5. |
| | Tipo de condição > Local | (Somente condições de localização) Os públicos-alvos e exclusões de localização:<ul><li>**Todos os países e territórios** — Para direcionar todos os países e locais ou direcionar e excluir locais específicos.</li><li>**Insira um local** — Para direcionar e excluir locais específicos.</li></ul><ul><li>Para expandir um local ou sublocal, clique em > depois do nome.</li><li>Para adicionar um destino, selecione-o uma vez para mostrar uma marca de seleção verde.</li><li>Para excluir um destino, selecione o destino uma segunda vez para mostrar um **[!UICONTROL X]** vermelho.</li><li>Para remover um target ou uma exclusão, siga um destes procedimentos:<ul><li>Clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado do item na coluna [!UICONTROL Selections].</li><li>Selecione o destino até que nenhuma marca de seleção ou [!UICONTROL X] seja exibida.</li></ul></li></ul>Dentro de uma condição, vários targets ou exclusões são unidos usando o operador booleano OR, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: Se \[O local é Argélia OU Tunísia\], então Adicione 1,5. |
| | Tipo de condição > Público | (Somente condições do público-alvo) O público-alvo direciona:<ul><li>**Todos os segmentos de público-alvo** — Para direcionar todos os [!DNL Google Ads] segmentos de público-alvo.</li><li>**Insira os segmentos de público-alvo** — Para segmentar segmentos de público-alvo [!DNL Google Ads] específicos.</li></ul><ul><li>Para expandir uma categoria ou subcategoria em seus segmentos, clique em > depois do nome.</li><li>Para adicionar um target, selecione o target.</li><li>Para remover um destino, desmarque-o ou clique em ![Excluir](/help/search-social-commerce/assets/delete.png "Excluir") ao lado do item na coluna Seleção.</li></ul>Dentro de uma condição, vários targets ou exclusões são unidos usando o operador booleano OR, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Exemplo: Se \[O público-alvo é de viagens de negócios OU de férias em família\], Adicionar 1.5.<br><br>**Observação:** depois de salvar um público-alvo, você poderá adicionar outros públicos-alvo, mas não poderá removê-los fora do editor [!DNL Google Ads]. Se você precisar remover um público-alvo, faça logon diretamente no [!DNL Google Ads] e use o editor [!DNL Google Ads]. |
| Condições > Condição Secundária | | (Opcional; somente leitura para regras existentes) O tipo de condição que deve ser atendida para acionar um ajuste de valor. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador booleano ALL, para que ambas as condições sejam atendidas para iniciar um ajuste de valor. Exemplo: Se \[O local é Argélia OU Tunísia\] AND \[O dispositivo é móvel OU tablet\], então Adicione 1.5.<br><br>Consulte as entradas de Condição primária para obter descrições.<br><br>**Observação:** todas as regras em uma conta devem usar o mesmo tipo de condições primárias e secundárias (opcionais). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;. |
| Ajuste de Valor | Valor | Especifique o tipo de ajuste e insira um valor positivo:<ul><li>**Adicionar** — Adiciona o valor especificado ao valor de conversão passado. O valor deve ser maior que zero (0).</li><li>**Multiplicar** — Multiplica o valor de conversão passado pelo valor especificado. O valor deve ser de 0,5 a 10.</li></ul> |

>[!MORELIKETHIS]
>
>* [Sobre [!DNL Google Ads] regras de valor de conversão](about-google-conversion-value-rules.md)
>* [Criar uma [!DNL Google Ads] regra de valor de conversão](create-google-conversion-value-rule.md)
>* [Editar uma [!DNL Google Ads] regra de valor de conversão](edit-google-conversion-value-rule.md)
>* [Alterar o status de uma [!DNL Google Ads] regra de valor de conversão](change-the-status-of-google-conversion-value-rule.md)

