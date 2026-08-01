---
title: Configurações de anúncios responsivos do [!DNL Microsoft Advertising]
description: Referencie as configurações de  [!DNL Microsoft Advertising] anúncios responsivos.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 243
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configurações de anúncios responsivos (público-alvo)

O formato de anúncio responsivo está disponível para anúncios de público-alvo com base em imagem, vídeo e TV conectada com base em vídeo no [!DNL Microsoft Audience Network]. A rede de publicidade monta dinamicamente anúncios responsivos usando as combinações mais eficazes de elementos de publicidade.

## [!UICONTROL Basic Settings]

*Somente novos anúncios*

**[!UICONTROL Network]:** A rede de anúncios.

**[!UICONTROL Account]:** A conta da rede de publicidade.

**[!UICONTROL Campaign]:** A campanha.

**[!UICONTROL Ad Group]:** O grupo de anúncios.

## [!UICONTROL Audience CTV Video Ad Details]

<!-- I can't find a video ad -- this same header is used for image ads. Need to verify the video ad settings and when you'll get them -->

### Anúncios de vídeo

**[!UICONTROL Videos]:** A URL de um anúncio de vídeo.

**[!UICONTROL Status]:** O status do anúncio: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

### Anúncios de imagem)

>[!NOTE]
>
>A rede de publicidade cria automaticamente anúncios para campanhas de público vinculadas a uma loja do centro de comércio usando as informações do produto da loja e o direcionamento do usuário no nível do grupo de anúncios. Não é necessário criar anúncios manualmente.

**[!UICONTROL Images]:** Até 15 imagens JPEG ou PNG para o anúncio. Inclua pelo menos uma imagem com uma proporção de 1,91:1. Consulte as proporções e dimensões permitidas para [imagens de anúncios de público-alvo](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Para anúncios de público-alvo, o [!DNL Microsoft Advertising] recorta automaticamente essa imagem para todas as taxas de proporções possíveis.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres. Ela pode ser usada em formatos de anúncios somente para chamadas.

**[!UICONTROL Short Headlines]:** No mínimo três e no máximo 15 manchetes curtas com pelo menos uma palavra e no máximo 30 caracteres cada.

**[!UICONTROL Long Headlines]:** No mínimo três e no máximo cinco manchetes longas com no máximo 90 caracteres cada.

**[!UICONTROL Ad Text]:** Pelo menos duas e até quatro descrições com pelo menos uma palavra e no máximo 90 caracteres cada.

**[!UICONTROL Status]:** O status do anúncio: *[!UICONTROL Active]* ou *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Gerenciar anúncios](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
