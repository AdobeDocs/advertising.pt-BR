---
title: 'Criar uma regra de valor de conversão  [!DNL Google Ads] '
description: Saiba como criar  [!DNL Google Ads] regras de valor de conversão.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Criar uma regra de valor de conversão [!DNL Google Ads]

Você pode criar regras de valor de conversão no nível da conta e do nível da campanha em contas do [!DNL Google Ads] para as quais as conversões são rastreadas no nível da conta individual ou inferior. Não é possível criar regras para contas com conversões entre contas que são rastreadas no nível da conta principal.

Cada regra inclui até duas condições, bem como o ajuste do valor de conversão a ser aplicado quando as condições forem atendidas. Todas as regras em uma conta devem usar o mesmo tipo de condições principais e secundárias (opcional). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;.

É possível criar várias regras no nível de cada campanha. No entanto, o [!DNL Google Ads] ainda não oferece a capacidade de criar novas regras no nível da conta fora do editor [!DNL Google Ads] quando uma regra no nível da conta já existe. Para criar regras adicionais a nível de conta, faça logon diretamente no [!DNL Google Ads] e use o editor [!DNL Google Ads].

**Observação:** as regras de valor de conversão no nível da campanha substituem as regras no nível da conta e somente uma regra pode ser aplicada a uma conversão. Para obter mais informações, consulte [como [!DNL Google Ads] determina qual regra é aplicada a uma conversão quando a conversão atende às condições para várias regras](https://support.google.com/google-ads/answer/10520348).

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Por padrão, a guia **[!UICONTROL Campaign]** é selecionada para mostrar todas as regras no nível da campanha.

1. (Opcional) Para criar uma regra no nível da conta, clique na guia **[!UICONTROL Account]**.

1. Na barra de ferramentas, clique em ![Criar](/help/search-social-commerce/assets/add.png "Criar").<!-- Upload newer icon -->

1. Selecione a rede de publicidade e a conta. Para regras no nível da campanha, selecione também a campanha. Depois clique em **[!UICONTROL Next]**.

1. Defina as [configurações da regra de conversão](google-conversion-value-rule-settings.md).

   Você deve configurar uma condição primária e um ajuste de valor. Como opção, você pode configurar uma condição secundária.

   Dentro de uma condição, vários targets ou exclusões são unidos usando o operador booleano OR, para que qualquer opção possa ser atendida para iniciar um ajuste de valor. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador booleano ALL, para que ambas as condições sejam atendidas para iniciar um ajuste de valor. Exemplo: se \[O local é Argélia OU Tunísia\] E \[O dispositivo é móvel OU tablet\], adicione 1.5.

   **Observação:** todas as regras em uma conta devem usar o mesmo tipo de condições primárias e secundárias (opcionais). Por exemplo, se a Regra 1 incluir a condição principal &quot;Público-alvo&quot; e a condição secundária &quot;Localização&quot;, todas as outras regras na conta deverão ter a condição principal &quot;Público-alvo&quot;. Quando as outras regras incluírem uma condição secundária, ela deverá ser &quot;Localização&quot;.

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre [!DNL Google Ads] regras de valor de conversão](about-google-conversion-value-rules.md)
>* [Editar uma [!DNL Google Ads] regra de valor de conversão](edit-google-conversion-value-rule.md)
>* [Alterar o status de uma [!DNL Google Ads] regra de valor de conversão](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configurações da regra do valor de conversão](google-conversion-value-rule-settings.md)

