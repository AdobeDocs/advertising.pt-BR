---
title: Sobre [!DNL Google Ads] as regras de valor de conversão
description: Saiba como visualizar e gerenciar  [!DNL Google Ads] as regras de valor de conversão do Search, Social e Commerce.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Cerca de [!DNL Google Ads] regras de valor de conversão

O Search, Social e Commerce sincroniza automaticamente as [regras de valor de conversão](https://support.google.com/google-ads/answer/10518330) das suas contas do [!DNL Google Ads]. As regras de valor de conversão permitem ajustar os valores dos eventos de conversão com base nas informações do usuário, incluindo o tipo de dispositivo, o local e o segmento de público-alvo. Você pode usar regras para ofertas baseadas em valor em campanhas máximas de pesquisa, exibição, compras e desempenho com o Google Smart Bidding. Para campanhas com estratégias de lances Maximizar conversões e Direcionar ROAS, [!DNL Google Ads] algoritmos começarão a preferir conversões com um valor maior.

As regras de valor de conversão no nível da campanha substituem as regras no nível da conta. Quando uma conversão satisfaz várias regras de valor de conversão, somente uma das regras é aplicada. Normalmente, a regra mais específica é aplicada, mas consulte a [[!DNL Google Ads] documentação sobre prioridades para os diferentes tipos de condição de regra](https://support.google.com/google-ads/answer/10520348).

## A exibição e a funcionalidade [!UICONTROL Conversion Value Rules]

Todas as regras criadas na interface [!DNL Google Ads] são sincronizadas em 24 horas e estão disponíveis na exibição [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]. Algumas contas podem gerenciar suas regras de valor de conversão:

* Em contas para as quais as conversões são rastreadas no nível de conta individual ou de campanha, é possível criar, editar e alterar o status das regras no nível de conta e de campanha.

  As contas podem ser vinculadas a [!DNL Google Ads] contas de gerente, mas elas não podem usar o rastreamento de conversões entre contas (para as quais as conversões são rastreadas em todas as contas na conta de gerente).

* Em contas que usam o rastreamento de conversão entre contas, suas regras de nível de conta e de nível de campanha são herdadas da conta do gerente e são somente leitura.

## Regras de valor de conversão com portfólios do Search, Social e Commerce

Quando a conta do anunciante está configurada para carregar objetivos do Search, Social e Commerce para [!DNL Google Ads], e você inclui uma campanha que usa uma regra de valor de conversão em um portfólio com um objetivo, então [!DNL Google Ads] aplica a regra de valor de conversão ao valor de conversão original especificado no objetivo. Como resultado, os dados de conversão do Search, Social e Commerce são diferentes dos dados de conversão do [!DNL Google Ads].

Por exemplo, suponha que o objetivo use uma única métrica de conversão &quot;Clientes potenciais&quot; e dê às conversões de dispositivos móveis um peso de 10 e às conversões de dispositivos não móveis um peso de 10. Search, Social e Commerce conta um evento de qualquer tipo de dispositivo como uma (1) conversão e credita o valor de conversão como 10. No entanto, suponha que uma campanha nesse portfólio use uma regra de valor de conversão &quot;Se o Dispositivo for Móvel, multiplique por 2&quot;. Quando um evento de cliente potencial móvel é rastreado para essa campanha, [!DNL Google Ads] também credita a contagem de conversão como um (1), mas o valor de conversão como (10 x 2) = 20.

Para ver mais informações sobre suas regras, incluindo os valores de conversão originais antes da aplicação das regras, consulte o [relatório de regras de valor de conversão em [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Criar uma [!DNL Google Ads] regra de valor de conversão](create-google-conversion-value-rule.md)
>* [Editar uma [!DNL Google Ads] regra de valor de conversão](edit-google-conversion-value-rule.md)
>* [Alterar o status de uma [!DNL Google Ads] regra de valor de conversão](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configurações da regra do valor de conversão](google-conversion-value-rule-settings.md)

