---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---
# Exibir os campos Caminho 1 e Caminho 2 em algumas configurações de anúncio

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Opcional) Texto adicionado ao URL de exibição que é extraído automaticamente do URL final. Cada caminho é precedido no URL por uma barra (`/`). Um caminho não pode conter barra (`/`) ou nova linha (`\n`) caracteres. O comprimento máximo de cada caminho é de 15 caracteres ou 7 caracteres de byte duplo.

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não inclui um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Por exemplo, se [!UICONTROL Display Path 1] é &quot;ofertas&quot; e [!UICONTROL Display Path 2] for &quot;local&quot;, o URL de exibição será `<display URL>/deals/local`, como www.example.com/deals/local.
