---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# Campo Descrições do anúncio nas configurações de anúncio RSA

**[!UICONTROL Ad Descriptions]:** Pelo menos duas e até quatro descrições de anúncio, com pinos de posição opcionais. A rede de publicidade exibe anúncios com até duas descrições; insira pelo menos duas. O comprimento máximo de cada descrição é de 90 caracteres, incluindo qualquer texto dinâmico (como os valores de palavras-chave e personalizadores de anúncios).

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não incluir um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Para fixar uma descrição a uma posição específica, selecione a opção de fixação (como &quot;[!UICONTROL Pinned at position 1]&quot;). Pelo menos uma descrição deve estar disponível para cada posição. Se você fixar várias descrições na mesma posição, o anúncio final sempre incluirá uma dessas descrições na posição especificada. As descrições fixadas na posição 2 podem não ser mostradas com o anúncio.

Para adicionar uma descrição adicional, clique em **[!UICONTROL + Add]**.
