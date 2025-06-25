---
title: Habilitar carregamento de objetivos para redes de anúncios
description: Saiba como carregar objetivos para seus portfólios híbridos do  [!DNL Google Ads] and [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Habilitar carregamento de objetivos para redes de anúncios

*Anunciantes somente com contas [!DNL Google Ads] e [!DNL Microsoft Advertising]*

*Anunciantes habilitados somente para otimização híbrida*

Search, Social e Commerce podem fazer upload dos objetivos dos portfólios de uma conta de anunciante para [!DNL Google Ads] e [!DNL Microsoft Advertising], para que você possa usá-los para otimização híbrida. Os objetivos carregados estão disponíveis como ações de conversão para metas de conversão personalizadas no nível da conta e da campanha.

Habilitar essa opção aciona automaticamente um upload para objetivos em portfólios que contêm campanhas com estratégias de oferta inteligente. O Search, Social e Commerce cria uma conversão na rede de anúncios para cada objetivo aplicável. A conversão representa todas as métricas de conversão ponderadas no objetivo no nível da ID de EF (clique na ID). Para [!DNL Google Ads] cliques, a ID EF é o [!DNL Google Ads] `gclid`; para [!DNL Microsoft Advertising] cliques, a ID EF é o [!DNL Microsoft Advertising] `msclkid`. Devido a essa ID de clique, os dados de conversão podem ser mapeados para a palavra-chave específica e para o tempo de clique.

Cada conversão carregada tem o seguinte nome:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

onde `<network_ID>` é a ID numérica que o Search, Social e Commerce usa para a rede de publicidade, `<objective_id>` é a ID de objetivo numérica e `<network_account_ID>` é a ID numérica da conta da rede de publicidade ou da conta do gerente.

Os carregamentos para [!DNL Google Ads] ocorrem diariamente às 06:00 no fuso horário do anunciante. Os carregamentos para [!DNL Microsoft Advertising] ocorrem diariamente às 09:00 no fuso horário do anunciante.

>[!IMPORTANT]
>
>As conversões rastreadas pelo Google Ads e pela tag de rastreamento universal de eventos (UET) do Microsoft Advertising não são recarregadas nas redes de anúncios. Se você incluí-los em um objetivo, é necessário adicioná-los às metas da campanha no editor da rede de publicidade.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Marque a caixa de seleção ao lado de **[!UICONTROL Enable Objective Upload]**.

1. (Anunciantes com contas do [!DNL Google Ads] que fazem negócios no Espaço Econômico Europeu (EEE) ou Reino Unido (Reino Unido); opcional) Se você coletou o consentimento de usuários do EEE e Reino Unido para carregar seus dados para fins de publicidade, marque a caixa de seleção ao lado de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Clique em **[!UICONTROL Save]**.

1. (Se suas conversões forem rastreadas no nível de uma conta de gerente) [Adicionar credenciais para sua conta de gerente](/help/search-social-commerce/admin/manager-accounts.md) em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Verifique se cada objetivo — denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — aparece dentro de dois dias na rede de publicidade.

   No editor [!DNL Google Ads], procure suas [ações de conversão](https://support.google.com/google-ads/answer/11461796). No editor [!DNL Microsoft Advertising], procure suas [metas de conversão](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Se necessário, atualize o intervalo de datas para incluir a data do upload.

## Como o objetivo ponderado é calculado

O objetivo ponderado passado para a rede de publicidade é a soma de todos os valores de métrica coletados, com exceção das conversões rastreadas por [!DNL Google Ads] ou pela tag de rastreamento universal de eventos (UET) [!DNL Microsoft Advertising]. O valor é calculado usando o método de atribuição configurado para a conta Search, Social e Commerce do anunciante.

Por exemplo, digamos que a métrica de objetivo seja Adições ao carrinho com um peso de 25, e suas métricas de assistência incluem GL_Lead e Receita com pesos de 1 e Downloads com um peso de 0,5.

![Exemplo de um objetivo ponderado](/help/search-social-commerce/assets/objective-example.png "Exemplo de um objetivo ponderado")

Suponha que uma palavra-chave tenha resultado nas seguintes ações para o portfólio:

* 10 adições ao carrinho
* US$ 500 em receita
* 50 Downloads
* 5 GL_Lead

GL_Lead não está incluído no cálculo/upload porque é uma métrica rastreada pelo Google Ads. Portanto, o valor objetivo ponderado é calculado como ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>Você pode exibir dados para a receita ponderada do Adobe Advertising nos relatórios da rede de publicidade. Como prática recomendada, compare a receita ponderada com a [!DNL Google Ads] &quot;Todas as conversões. (por conv. tempo)&quot; ou a métrica [!DNL Microsoft Advertising] &quot;Todas as conv. receita&quot;, segmentada para a métrica O_ACS_OBJ*.<!--clarify -->

## Solução de problemas de objetivos ausentes

Se o objetivo — denominado `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — de um de seus portfólios não aparecer na rede de anúncios, verifique o seguinte:

* ([!DNL Google Ads]) Verifique se as conversões devem ser carregadas no nível de conta ou de gerente. Caso seja necessário fazer upload deles no nível do gerente:

   * Verifique se as credenciais da conta de gerente [!DNL Google Ads] são fornecidas em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Se necessário, [adicione as credenciais para a conta de gerente](/help/search-social-commerce/admin/manager-accounts.md).

   * Verifique se a conta da rede de publicidade já inclui o mesmo nome de métrica. Em caso afirmativo, renomeie a métrica para que a propriedade correta em nível de gerente possa ser criada.

* Verifique se a opção &quot;híbrida&quot; do portfólio está selecionada e se o objetivo tem receita válida.

>[!MORELIKETHIS]
>
>* [Sobre o gerenciamento das métricas de conversão de um anunciante](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Carregar métricas de conversão rastreadas por Pesquisa, Social e Commerce para [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
