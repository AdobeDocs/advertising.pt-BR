---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Exibir os campos Caminho 1 e Caminho 2 em algumas configurações de anúncio

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Opcional) Texto adicionado ao URL de exibição que é extraído automaticamente do URL final. Cada caminho é precedido no URL por uma barra (`/`). Um caminho não pode conter barra (`/`) ou nova linha (`\n`) caracteres. O comprimento máximo de cada caminho é de 15 caracteres ou 7 caracteres de byte duplo.

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Por exemplo, se o Caminho de exibição 1 for &quot;ofertas&quot; e o Caminho de exibição 2 for &quot;local&quot;, o URL de exibição será `<display URL>/deals/local`, como www.example.com/deals/local.
