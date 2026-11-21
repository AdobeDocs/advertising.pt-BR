---
title: Configurações do grupo de anúncios [!DNL ChatGPT]
description: Referencie as configurações para [!DNL ChatGPT] grupos de anúncios.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 487af67f7215bf4a070af5e813649288141b0ed4
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# Configurações do grupo de anúncios [!DNL ChatGPT]

*Anúncios em [!DNL ChatGPT] são um recurso piloto de[!DNL OpenAI]*

## Guia [!UICONTROL Basic Settings]

*Somente novos grupos de anúncios*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha. Não é possível alterar a campanha após criar o grupo de publicidade.

## Guia [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group name]:** Um nome de grupo de anúncios que é exclusivo na campanha e inclui pelo menos três caracteres.

**[!UICONTROL Status]:** O status de exibição do grupo de anúncios: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. O padrão para novos grupos de anúncios é *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (Campanhas com o objetivo [!UICONTROL Clicks] ou [!UICONTROL Conversions]) Como dar lances para anúncios no grupo de publicidade:

* *[!UICONTROL Autobid]:* (O padrão para novos grupos de anúncios) [!DNL OpenAI] ajusta automaticamente as ofertas para obter o máximo de cliques ou conversões do seu orçamento, dependendo do objetivo da campanha. Você não insere um valor de lance. Essa opção está disponível para orçamentos de campanha diários e vitalícios.

* *[!UICONTROL Target CPC]:* (Campanhas com o objetivo [!UICONTROL Clicks]) Oferece ofertas para uma meta de custo por clique médio. Insira a meta no campo [!UICONTROL Target CPC].

* *[!UICONTROL Target CPA]:* (Campanhas com o objetivo [!UICONTROL Conversions]) Oferece ofertas para uma meta de custo médio por conversão. Insira a meta no campo [!UICONTROL Target CPA].

* *[!UICONTROL Manual: Max bid]:* (Somente grupos de anúncios de oferta existentes manualmente) Mantém a oferta máxima existente como um valor somente leitura. Você pode manter essa estratégia ou alternar para [!UICONTROL Autobid] ou a estratégia de destino do objetivo da campanha. Essa opção não está disponível para novos grupos de anúncios ou ao editar grupos de anúncios que já usam lances automáticos ou de público alvo.

Os grupos de anúncios de oferta manual existentes não são alterados automaticamente para outra estratégia. Editar apenas um valor de meta ou uma configuração não relacionada não altera uma estratégia de ofertas de meta existente.

**[!UICONTROL Target CPC]:** (Grupos de anúncios com a estratégia de oferta [!UICONTROL Target CPC]; obrigatório) O custo médio por clique que você deseja atingir, na moeda da conta. Insira um valor positivo. Essa é uma meta de custo médio, não uma oferta máxima.

**[!UICONTROL Target CPA]:** (Grupos de anúncios com a estratégia de oferta [!UICONTROL Target CPA]; obrigatório) O custo médio por conversão que você deseja realizar, na moeda da conta. Insira um valor positivo. Essa é uma meta de custo médio, não uma oferta máxima.

**[!UICONTROL Maximum CPC bid]:** (Campanhas com o objetivo [!UICONTROL Clicks]; somente grupos de anúncios de oferta manual existentes; somente leitura) O valor máximo existente que você pagará por cada clique.

**[!UICONTROL Conversion-optimized bid cap]:** (Campanhas com o objetivo [!UICONTROL Conversions]; apenas grupos de anúncios de oferta manual existentes; somente leitura) O valor máximo existente que você está disposto a oferecer para uma conversão. [!DNL OpenAI] usa a taxa de conversão prevista para converter este valor em uma oferta de leilão por impressão.

**[!UICONTROL Maximum CPM bid]:** (Campanhas com o objetivo [!UICONTROL Reach]) O valor máximo que você pagará por mil impressões, na moeda da conta. Insira um valor de 0,01-5000. Campanhas de alcance não têm as opções [!UICONTROL Bid strategy].

**[!UICONTROL Context hints (optional)]:** Descrição das conversas, tópicos ou palavras-chave para os quais seus produtos ou serviços podem ser relevantes. Separe as dicas com vírgulas ou quebras de linha. Suas dicas podem ser usadas para orientar a correspondência, mas não são regras de direcionamento de correspondência exata. Consulte [[!DNL ChatGPT Ads] ajuda sobre como gravar dicas de contexto eficazes](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (Opcional) Quaisquer parâmetros a serem anexados ao final das URLs de página de aterrissagem para rastrear informações. Exemplo: `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Gerenciar grupos de anúncios](ad-group-manage.md)
