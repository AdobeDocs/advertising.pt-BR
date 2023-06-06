---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---
# Campo Títulos de anúncio nas configurações de anúncio RSA

**[!UICONTROL Ad Titles]:** Pelo menos três e até quinze títulos de anúncios (manchetes), com marcadores de posição opcionais. A rede de publicidade exibe anúncios com até três títulos; insira pelo menos três. O tamanho máximo de cada título é de 30 caracteres, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Para fixar um título a uma posição específica, selecione a opção de fixação (como &quot;[!UICONTROL Pinned at position 1]&quot;). Pelo menos um título deve estar disponível para cada posição. Se você fixar vários títulos na mesma posição, o anúncio final sempre incluirá um desses títulos na posição especificada. Os títulos fixados na posição 3 podem não ser mostrados com o anúncio.

Para adicionar um título adicional, clique em **[!UICONTROL + Add]**.
