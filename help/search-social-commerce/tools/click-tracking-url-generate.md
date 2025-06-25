---
title: Gerar um URL de rastreamento de cliques
description: Saiba como gerar manualmente um URL de rastreamento de cliques do Search, Social e Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Gerar um URL de rastreamento de cliques do Search, Social e Commerce usando a ferramenta URLs de rastreamento

*Somente anunciantes com rastreamento de conversão do Adobe Advertising*

Para obter informações sobre quando você deve gerar e implementar manualmente uma URL de rastreamento de cliques, consulte &quot;[Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Esse recurso não implementa o modelo de rastreamento ou a URL de destino na conta de anúncio relevante.

1. No menu principal, clique em **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Selecione a conta da rede de publicidade na lista.

   ([!DNL Google Ads] palavras-chave; texto, instalação de aplicativo móvel e anúncios de pesquisa dinâmica; inserções; sitelinks e grupos de produtos) As tags de rastreamento para o campo de modelo de rastreamento são exibidas. Eles não incluem parâmetros de acréscimo no nível da conta. Pule para a Etapa 4.

   Para todos os outros tipos de tags, insira informações para gerar uma tag.

1. (Se necessário) Gere uma tag:

   1. Especifique as páginas de aterrissagem, com sitelinks ou nomes de produtos, quando solicitado, de uma das seguintes maneiras:

      * Especifique um arquivo contendo as informações inserindo o caminho completo e o nome do arquivo ou clicando em **[!UICONTROL Browse]** para localizar o arquivo no dispositivo ou na rede. O arquivo deve ser um arquivo de texto delimitado por tabulação com um item por linha no seguinte formato:

         * (Criações, Anúncios padrão) `**landing_page**`

           onde `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           onde `sitelink` é o nome do sitelink e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           O arquivo pode incluir até 10.000 linhas.

         * ([!DNL Google Merchant Center] grupos de produtos e [!DNL Microsoft Advertising] anúncios de produtos) `product name <tab> ** <tab> landing_page`

           onde `product name` é o nome do produto e `landing_page` é uma URL de página de aterrissagem ou URL de base válida.

           Exemplo: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           O arquivo pode incluir até 10.000 linhas.

      * No campo de entrada, insira um item por linha no seguinte formato:

         * (Criações, Anúncios padrão) `landing_page`

           onde `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink**landing_page`

           onde `sitelink` é o nome do sitelink e `landing_page` é um URL de página de aterrissagem ou URL de base válido.

           Exemplo: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] grupos de produtos e [!DNL Microsoft Advertising] anúncios de produtos) `product name**landing_page`

           onde `product name` é o nome do produto e `landing_page` é uma URL de página de aterrissagem ou URL de base válida.

           Exemplo: Acme PR208**http://www.example.com/travel.html

   1. Clique em **[!UICONTROL Generate Tracking URLs]**.

1. (Opcional) Copie os URLs (começando com &quot;http&quot; ou &quot;https&quot;) da tela ou página de saída e implemente-os na conta de pesquisa ou social.

Para contas com URLs de destino, insira os valores nos campos [!UICONTROL Base URL] apropriados.

Para contas com URLs finais, insira o valor na tela no campo [!UICONTROL Tracking Template] apropriado. Você deve adicionar um parâmetro para a URL final após o parâmetro `&url=` (como `{lpurl}`). Para contas do [!DNL Yahoo! Japan Ads], use o parâmetro `{lpurl}`. Para obter uma lista de parâmetros [!DNL Google Ads] e [!DNL Microsoft Advertising] para indicar as URLs finais em modelos de rastreamento, consulte a [[!DNL Google Ads] documentação](https://support.google.com/google-ads/answer/6305348) (consulte os parâmetros &quot;Somente modelo de rastreamento&quot; na seção sobre &quot;Parâmetros [!DNL ValueTrack] Disponíveis&quot;) e a [[!DNL Microsoft Advertising] documentação](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Sobre as ferramentas para criar e decodificar marcas de rastreamento](tracking-tools-about.md)
>* [Quando e como gerar URLs de rastreamento de cliques](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Decodificar uma URL de rastreamento de cliques de Search, Social e Commerce](click-tracking-url-decode.md)
