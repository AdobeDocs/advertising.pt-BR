---
title: Configurações de anúncios responsivos do [!DNL Microsoft Advertising]
description: Referencie as configurações de  [!DNL Microsoft Advertising] anúncios responsivos.
exl-id: 29404500-d929-4683-be71-150ea8ab805d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/K4R8gmgxfaMP0JdZiz4RkZkfC6-0T2BsyxpcwK-X3bQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# [!DNL Microsoft Advertising] configurações de anúncios responsivos (público-alvo)

O formato de anúncio responsivo está disponível para anúncios de público-alvo com base em imagem, vídeo e TV conectada com base em vídeo no [!DNL Microsoft Audience Network]. A rede de publicidade monta dinamicamente anúncios responsivos usando as combinações mais eficazes de elementos de publicidade.

## [!UICONTROL Ad Settings] (para anúncios de vídeo) e [!UICONTROL Audience CTV Video Ad Details]

**[!UICONTROL Videos]:** A URL de um anúncio de vídeo.

**[!UICONTROL Status]:** O status do anúncio.

## [!UICONTROL Responsive Ad Details] (para anúncios de imagem)

>[!NOTE]
>
>A rede de publicidade cria automaticamente anúncios para campanhas de público vinculadas a uma loja do centro de comércio usando as informações do produto da loja e o direcionamento do usuário no nível do grupo de anúncios. Não é necessário criar anúncios manualmente.

**[!UICONTROL Images]:** Até 15 imagens JPEG ou PNG para o anúncio. Inclua pelo menos uma imagem com uma taxa de proporção de 1,91:1. Consulte as proporções e dimensões permitidas para [imagens de anúncios de público-alvo](https://help.ads.microsoft.com/#apex/ads/en/56912/0).

Para anúncios de público-alvo, o [!DNL Microsoft Advertising] recorta automaticamente essa imagem para todas as taxas de proporções possíveis.

<!-- Instructions -->

{{$include /help/_includes/images-ms-multimedia-responsive-ad.md}}

**[!UICONTROL Business Name]:** O nome da empresa, com no máximo 25 caracteres. Ela pode ser usada em formatos de anúncios somente para chamadas.

**[!UICONTROL Short Headlines]:** No mínimo três e no máximo 15 manchetes curtas com pelo menos uma palavra e no máximo 30 caracteres cada.

**[!UICONTROL Long Headlines]:** No mínimo três e no máximo cinco manchetes longas com no máximo 90 caracteres cada.

**[!UICONTROL Ad Text]:** Pelo menos duas e até quatro descrições com pelo menos uma palavra e no máximo 90 caracteres cada.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Sobre anúncios](ad-about.md)
>* [Gerenciar anúncios](ad-manage.md)
>* [[!DNL Microsoft Advertising] configurações expandidas de anúncios de pesquisa dinâmica](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] configurações de anúncios multimídia](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] configurações de anúncio de produto](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] configurações responsivas de pesquisa e publicidade](ad-settings-microsoft-rsa.md)
