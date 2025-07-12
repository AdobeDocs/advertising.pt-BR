---
title: Personalizar opções de transcodificação para uma tag de experiência de vídeo e anúncios
description: Saiba como personalizar as opções de transcodificação para uma tag de anúncio de vídeo.
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
source-git-commit: 3d0d42d19c11276f13a4e003c382a2d2410ab037
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Personalizar opções de transcodificação para uma tag de experiência de vídeo e anúncios

*Beta fechado*

É possível personalizar as opções de transcodificação para uma experiência de anúncio de vídeo para garantir uma reprodução rápida e controle de qualidade entre editores.

1. No menu principal, clique em **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Siga um destes procedimentos:

* No modo de exibição de cartão, clique em **[!UICONTROL ...]** ao lado do nome da experiência e, em seguida, clique em **[!UICONTROL Tag Manager]**.

* Na exibição de tabela, mantenha o cursor sobre a linha, clique em **[!UICONTROL More]** e em **[!UICONTROL Tag Manager]**.

1. Mantenha o cursor sobre a linha da marca de anúncio aplicável, clique em **[!UICONTROL More]** e em **[!UICONTROL Video Settings]**.

1. Na lista de **[!UICONTROL Publisher specific transcodes]**, selecione o tipo de transcodificação.

1. Clique em **[!UICONTROL Save Settings]**.

## Especificação de transcodificação padrão ([!DNL Adobe] DSP)

| Tipo de arquivo | Dimensões | Taxa de bits do vídeo | Taxa de quadros do vídeo | Taxa de áudio | Taxa de amostragem de áudio | Nível de áudio |
|---|---|---|---|---|---|---|
| mp4 | 640x360 | 1000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 400x300 | 1000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 1024x768 | 500 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 640x480 | 1000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 960x540 | 2000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 960x720 | 2000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 1280x720 | 2000 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 1920x1080 | 3500 kbps | 23,98 qps | 128 kbps | 44,100 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 640x360 | 800 kbps | 23,98 qps | 96 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 640x360 | 400 kbps | 23,98 qps | 128 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |
| mp4 | 1920x1080 | 16000 kbps | 23,98 qps | 256 kbps | 48.000 kHz | 24 LKFS (+/- 2,0 dB) |

>[!MORELIKETHIS]
>
>* [Sobre suas bibliotecas criativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Criar uma experiência com direcionamento](/help/creative/experiences/experience-create-targeting.md)
>* [Crie manualmente uma marca de anúncio para um tamanho criativo aplicável](experience-tag-create-manually.md)
>* [Exportar e implementar uma marca de experiência de anúncio para uma experiência ao vivo](experience-tag-export.md)
