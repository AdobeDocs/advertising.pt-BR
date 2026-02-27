---
title: Campos disponíveis para arquivos de feed de anúncios dinâmicos
description: Saiba mais sobre os campos que podem ser incluídos nos arquivos de feed usados para criar anúncios dinâmicos.
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
source-git-commit: 5bf0474f49160775d31dff0d434ba1e069f27959
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Apêndice: Campos disponíveis para arquivos de feed de anúncios dinâmicos

Os seguintes campos de feed estão disponíveis no back-end do Advertising Creative. Você pode carregar um [arquivo de feed](/help/creative/feeds/asset-manage.md) que usa nomes de campo específicos da sua organização. No entanto, antes de criar um [catálogo](/help/creative/feeds/catalog-manage.md) a partir do seu arquivo de feed, você deve mapear cada campo do arquivo de feed para um dos seguintes campos do [modelo de feed](/help/creative/feeds/feed-template-manage.md) que você usará para criar o catálogo.

O único campo que deve ter um equivalente em seu arquivo de feed é `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Nome do campo | Tipo de dados | Obrigatório? |
|------------|-----------|-----------|
| AD_SIZE | varchar(32) | NÃO |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NÃO |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NÃO |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NÃO |
| AREA_CODE | texto | NÃO |
| AUDIENCE_SEGMENT | texto | NÃO |
| AUDIO_1 | varchar(1024) | NÃO |
| AUDIO_2 | varchar(1024) | NÃO |
| AUDIO_3 | varchar(1024) | NÃO |
| AUDIO_4 | varchar(1024) | NÃO |
| AUDIO_5 | varchar(1024) | NÃO |
| CIDADE | texto | NÃO |
| PAÍS | texto | NÃO |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NÃO |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NÃO |
| DATAPASS_FILTER_1 | texto | NÃO |
| DATAPASS_FILTER_2 | texto | NÃO |
| DATAPASS_FILTER_3 | texto | NÃO |
| DATAPASS_FILTER_4 | texto | NÃO |
| DATAPASS_FILTER_5 | texto | NÃO |
| DISCOUNT_PRICE | decimal(10,2) | NÃO |
| DMA | texto | NÃO |
| IMAGEM | varchar(1024) | NÃO |
| IMAGE_1 | varchar(1024) | NÃO |
| IMAGE_2 | varchar(1024) | NÃO |
| IMAGE_3 | varchar(1024) | NÃO |
| IMAGE_4 | varchar(1024) | NÃO |
| IMAGE_5 | varchar(1024) | NÃO |
| IMAGE_6 | varchar(1024) | NÃO |
| IMAGE_7 | varchar(1024) | NÃO |
| IMAGE_8 | varchar(1024) | NÃO |
| IMAGE_9 | varchar(1024) | NÃO |
| IMAGE_10 | varchar(1024) | NÃO |
| IMAGE_HEIGHT | int | NÃO |
| IMAGE_WIDTH | int | NÃO |
| IS_DEFAULT | enum | NÃO |
| IDIOMA | texto | NÃO |
| PART_NUM | varchar(64) | SIM |
| PREÇO | decimal(10,2) | NÃO |
| PRODUCT_NAME | texto | NÃO |
| URL_DO_PRODUTO | texto | NÃO |
| PROFILE_FILTER_1 | texto | NÃO |
| PROFILE_FILTER_2 | texto | NÃO |
| PROFILE_FILTER_3 | texto | NÃO |
| PROFILE_FILTER_4 | texto | NÃO |
| PROFILE_FILTER_5 | texto | NÃO |
| CLASSIFICAÇÃO | int | NÃO |
| ESTADO | texto | NÃO |
| TEXTO_1 | texto | NÃO |
| TEXTO_2 | texto | NÃO |
| TEXTO_3 | texto | NÃO |
| TEXTO_4 | texto | NÃO |
| TEXTO_5 | texto | NÃO |
| TEXTO_6 | texto | NÃO |
| TEXTO_7 | texto | NÃO |
| TEXTO_8 | texto | NÃO |
| TEXTO_9 | texto | NÃO |
| TEXTO_10 | texto | NÃO |
| TEXTO_11 | texto | NÃO |
| TEXTO_12 | texto | NÃO |
| TEXTO_13 | texto | NÃO |
| TEXTO_14 | texto | NÃO |
| TEXTO_15 | texto | NÃO |
| VIDEO_1 | varchar(1024) | NÃO |
| VIDEO_2 | varchar(1024) | NÃO |
| VIDEO_3 | varchar(1024) | NÃO |
| VIDEO_4 | varchar(1024) | NÃO |
| VIDEO_5 | varchar(1024) | NÃO |
| ZIP | texto | NÃO |

>[!MORELIKETHIS]
>
>* [Fluxos de trabalho para anúncios dinâmicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gerenciar arquivos de ativos](/help/creative/feeds/asset-manage.md)
>* [Gerenciar modelos de feed](/help/creative/feeds/feed-template-manage.md)
>* [Gerenciar catálogos](/help/creative/feeds/catalog-manage.md)
