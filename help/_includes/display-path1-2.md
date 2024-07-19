---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Exibir os campos Caminho 1 e Caminho 2 em algumas configurações de anúncio

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Opcional) Texto que é adicionado à URL de exibição que é extraída automaticamente da URL final. Cada caminho é precedido na URL por uma barra (`/`). Um caminho não pode conter caracteres de barra (`/`) ou nova linha (`\n`). O comprimento máximo de cada caminho é de 15 caracteres ou 7 caracteres de byte duplo.

Para inserir um personalizador de anúncios, use os seguintes formatos, onde `Default text` é um valor opcional a ser inserido quando o arquivo de feed não incluir um valor válido:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Por exemplo, se [!UICONTROL Display Path 1] for &quot;ofertas&quot; e [!UICONTROL Display Path 2] for &quot;local&quot;, a URL de exibição será `<display URL>/deals/local`, como www.example.com/deals/local.
