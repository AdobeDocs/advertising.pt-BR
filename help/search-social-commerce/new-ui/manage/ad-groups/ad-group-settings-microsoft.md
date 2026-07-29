---
title: Configurações do grupo de anúncios [!DNL Microsoft Advertising]
description: Referencie as configurações de  [!DNL Microsoft Advertising] grupos de anúncios.
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 75e264e213f60ae45c4f51f0a21352f690d6d699
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# Configurações do grupo de anúncios [!DNL Microsoft Advertising]

## \[Início da página]

**[!UICONTROL Ad Group Name]:** Um nome de grupo de anúncios que é exclusivo dentro da campanha.

**[!UICONTROL Status]:** O status de exibição da campanha: *Ativa* ou *Pausada*. O padrão para novas campanhas de publicidade é *Ativo*.

## Guia [!UICONTROL Basic Settings]

*Somente novas campanhas*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

## Guia [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Language]:** (Campanhas de pesquisa) O idioma de destino dos anúncios.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## Guia [!UICONTROL Networks]

**[!UICONTROL Networks]:** (Pesquisar anúncios) Como e onde colocar anúncios no grupo de anúncios:

* *[!UICONTROL Only Bing and Yahoo websites]* (o padrão): Para fazer lances para anúncios na rede de pesquisa.

* *[!UICONTROL Only Bing and Yahoo syndicated search partners]:* Para fazer ofertas de anúncios em sites de parceiros sindicalizados.

* *[!UICONTROL Content Network]:* obsoleto

## Guia [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** obsoleto

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Grupos de anúncios de público-alvo) Se deseja:

* *[!UICONTROL Bid Only]:* Para mostrar anúncios até mesmo para pessoas que não estão associadas a públicos-alvo de direcionamento, desde que atendam a outros alvos de nível de grupo de anúncios. Você pode aumentar as chances de os anúncios serem exibidos para públicos-alvo específicos, no entanto, definindo lances mais altos para esses públicos-alvo.

* *[!UICONTROL Target and Bid]:* Para mostrar anúncios somente para usuários associados a públicos-alvo que também atendam a quaisquer outros alvos para o grupo de anúncios.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

Para [!DNL Microsoft Advertising] grupos de anúncios na rede de público-alvo, os modificadores de oferta para destinos de localização não são otimizados em portfólios padrão com a configuração &quot;[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;.

**[!UICONTROL Genre]:** (Grupos de anúncios em [!UICONTROL Audience CTV Video] campanhas; disponível nos EUA, CA, BR, MX, Reino Unido, DE, ES, FR, IT, AU, MY e TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->) Os gêneros alvo, que determinam os programas e canais nos quais seus anúncios aparecem:

* *[!UICONTROL All genres]:* (padrão) Direciona todos os gêneros.

* *[!UICONTROL Select From Below List]:* Destinos de gêneros selecionados. Selecione na lista de todos os gêneros disponíveis.

O posicionamento do anúncio de TV conectada (CTV) depende da qualidade do vídeo e do valor da oferta. Consulte os [requisitos técnicos para anúncios de CTV](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#Requisitos técnicos).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Opcional) Sexo específico a ser incluído ou excluído como destino: *[!UICONTROL Male]*, *[!UICONTROL Female]* e *[!UICONTROL Unknown]*. Por padrão, todos os gêneros são direcionados. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) apareça. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada gênero direcionado.

* Para excluir um valor, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

**[!UICONTROL Age]:** (Opcional) Categorias de idade específicas a serem incluídas ou excluídas como destinos: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]* e *[!UICONTROL Unknown]*. Por padrão, todas as idades são direcionadas. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) apareça. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada faixa etária de destino.

* Para excluir um valor, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

**[!UICONTROL Company targets]:** (Opcional) Empresas específicas de perfis do usuário [!DNL LinkedIn] a serem incluídas ou excluídas como destinos. Por padrão, todas as empresas são direcionadas. Para restringir o direcionamento, procure e selecione empresas individuais e empresas de organizações de nível médio. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) apareça. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada empresa-alvo.

* Para excluir um valor, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

**[!UICONTROL Industry]:** (Opcional) Setores específicos dos perfis do usuário [!DNL LinkedIn] a serem incluídos ou excluídos como destinos. Por padrão, todos os setores são direcionados. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) apareça. Opcionalmente, você pode aumentar ou diminuir ofertas em uma porcentagem especificada para cada setor direcionado.

* Para excluir um valor, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

**[!UICONTROL Job Function Targets]:** (Opcional) Funções de trabalho específicas dos perfis do usuário [!DNL LinkedIn] a serem incluídas ou excluídas como destinos. Por padrão, todas as funções de trabalho são direcionadas. As exclusões sempre substituem as inclusões.

* Para direcionar todos os valores, não selecione nenhum valor.

* Para incluir um valor, clique no círculo adjacente uma vez para que uma marca de seleção azul (![Incluir](/help/search-social-commerce/assets/include.png "Incluir")) apareça. Opcionalmente, você pode aumentar ou diminuir lances em uma porcentagem especificada para cada função da ordem de produção pretendida.

* Para excluir um valor, clique no círculo adjacente duas vezes para que uma marca de seleção vermelha (![Excluir](/help/search-social-commerce/assets/exclude.png "Excluir")) seja exibida.

## Guia [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## Guia [!UICONTROL Additional Ad Group Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

### [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campanhas somente na exibição/rede nativa; opcional) Sites na rede de exibição na qual você não deseja que seus anúncios sejam exibidos. Insira um URL válido, como www.example.com. Para especificar várias cadeias de caracteres, separe-as com vírgulas ou insira-as em linhas separadas.

Para obter informações sobre disponibilidade, consulte a ajuda do [!DNL Microsoft Advertising] para &quot;[Impedir a exibição de anúncios em sites específicos](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

### [!UICONTROL Ad Group Frequency Cap Settings]

(Opcional) O número de vezes que um cliente pode receber anúncios do grupo de anúncios. Insira um valor e selecione a unidade de tempo (*[!UICONTROL Hour]*, *[!UICONTROL Day]*, *[!UICONTROL Week]*) ou *[!UICONTROL Month]*).

>[!MORELIKETHIS]
>
>* [Gerenciar grupos de anúncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)
