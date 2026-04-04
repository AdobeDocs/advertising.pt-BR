---
title: 'Editar uma regra de valor de conversão  [!DNL Google Ads] '
description: Saiba como editar  [!DNL Google Ads] as regras de valor de conversão.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Editar uma regra de valor de conversão de [!DNL Google Ads]

É possível editar uma regra de valor de conversão em contas/campanhas para as quais as conversões são rastreadas no nível de conta individual ou inferior. Não é possível editar uma regra para uma conta com conversões entre contas que são rastreadas no nível da conta principal.

1. No menu principal, clique em **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Por padrão, a guia **[!UICONTROL Campaign]** é selecionada para mostrar todas as regras no nível da campanha.

1. (Opcional) Para exibir todas as regras no nível da conta, clique na guia **[!UICONTROL Account]**.

1. Marque a caixa de seleção ao lado da regra.

1. Na barra de ferramentas de ações em massa,

   * Para ativar (habilitar) as regras pausadas, clique em (/help/search-social-commerce/assets/edit-new.png &quot;Editar).

1. Edite as [configurações da regra de conversão](google-conversion-value-rule-settings.md).

   Não é possível editar os tipos de condição de uma regra existente, mas você pode editar as condições e os ajustes de valor.

   Você deve configurar uma condição primária e um ajuste de valor. Como opção, você pode configurar uma condição secundária.

   **Observação:** se você adicionar uma condição secundária, ela deverá ser do mesmo tipo de condição que as outras regras da conta. Por exemplo, se a Regra 1, outras regras na conta tiverem a condição secundária &quot;Local&quot;, quando outras regras incluírem uma condição secundária, a condição secundária deverá ser &quot;Local&quot;. Quando você inclui uma condição secundária, a condição secundária é unida à condição primária usando o operador booleano ALL, para que ambas as condições sejam atendidas para iniciar um ajuste de valor.

1. Clique em **[!UICONTROL Review and Save]** para examinar as configurações.

1. Clique em **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Sobre [!DNL Google Ads] regras de valor de conversão](about-google-conversion-value-rules.md)
>* [Criar uma [!DNL Google Ads] regra de valor de conversão](create-google-conversion-value-rule.md)
>* [Alterar o status de uma [!DNL Google Ads] regra de valor de conversão](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configurações da regra do valor de conversão](google-conversion-value-rule-settings.md)

