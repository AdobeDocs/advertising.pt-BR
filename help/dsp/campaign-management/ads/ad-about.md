---
title: Sobre o gerenciamento de anúncios no DSP publicitário
description: Saiba mais sobre o gerenciamento de anúncios.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 9073400eb26957c63378bee90929009fcc82f78f
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Sobre o gerenciamento de anúncios no DSP publicitário

<!-- add "The Ads View (Dashboard?)" section -->

O DSP oferece suporte à entrega de anúncios por meio de tags de veiculação de anúncios de terceiros (como Google, Flashtalk ou Sizmek) para vários tipos de anúncios e ao upload direto de ativos para anúncios de exibição nativos. É possível fazer upload de tags de terceiros individualmente ou em massa. Os uploads em massa usam folhas de tags de parceiros ou um modelo de tag em massa.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Depois que seus anúncios forem configurados, anexe cada anúncio a um posicionamento, que inclui os parâmetros de direcionamento (como geografia, público-alvo, dispositivo e direcionamento de inventário) que controlam como sua campanha é veiculada. Você pode anexar um único anúncio a um ou vários posicionamentos.

## Tipos de anúncios disponíveis {#ad-types}

Todos os tipos de anúncios a seguir estão disponíveis no DSP. Para obter as especificações completas para cada tipo de anúncio, consulte [Especificações de publicidade](ad-specs.md).

* **Anúncios de áudio (somente de terceiros)**: os anúncios de áudio são reproduzidos entre o conteúdo em sites de editores digitais e podem ser executados de forma independente como arquivos de áudio ou junto com banners complementares. O áudio é mais adequado para impulsionar a percepção da marca e o engajamento com o público em movimento. Os principais indicadores de desempenho para áudio incluem [!UICONTROL Completion Rate] e [!UICONTROL Cost per Completion].

* **Exibir anúncios (somente terceiros)**: Anúncios de exibição são imagens animadas ou estáticas exibidas em navegadores da Web ou em aplicativos. Clicar na unidade de anúncio leva o usuário a um site de marca ou microsite. A exibição é melhor usada para impulsionar CPMs eficientes, aumentar a associação de mensagens, adicionar pontos de contato de marca ou produto adicionais e impulsionar os usuários pelo funil de compra. Os principais indicadores de desempenho para exibição incluem [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions], e [!UICONTROL Cost per Conversion]. O DSP é compatível com uma grande variedade de tamanhos de banners de exibição.

* **Anúncios em dispositivos móveis (somente de terceiros)**: os anúncios móveis podem estar em vídeo antes da exibição (VAST, MRAID) ou formato de exibição padrão. O vídeo móvel antes da exibição pode ser reproduzido automaticamente ou com clique para reproduzir, sendo mais adequado para alcançar visualizadores em várias telas. A exibição padrão móvel é uma imagem estática exibida em navegadores da Web móveis ou em aplicativos e é mais adequada para complementar compras de vídeo digital, associação de mensagens de unidade e adicionar pontos de contato de marca ou produto adicionais. Os anúncios móveis também podem funcionar como aquisições em tela cheia ou como intersticiais móveis, que são anúncios móveis em tela cheia e de alto impacto, usados com mais eficiência para desenvolver a percepção da marca para públicos móveis e gerar conversões.

* **Anúncios de exibição nativos (somente originais)**: os anúncios nativos são suportados no formato de exibição padrão. Os anúncios nativos incluem um título e/ou título, descrição, logotipo e imagem. Os elementos do anúncio são combinados e renderizados para corresponder ao estilo de página do editor, de modo que o anúncio se misture com o conteúdo orgânico do editor e conduza a um maior engajamento. O modelo nativo é mais adequado para reconhecer a marca e impulsionar a visualização do público-alvo e as taxas de engajamento com publicidade direcionada ao visualizador. Os principais indicadores de desempenho incluem [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions], e [!UICONTROL Cost Per Conversion].

* **Anúncios precedentes (somente de terceiros)**: anúncios precedentes (VAST e VPAID) são exibidos antes do conteúdo de vídeo premium e fornecem uma experiência do visualizador imersiva e envolvente. O vídeo antes da exibição pode ser interativo, conter recursos de mídia avançada e incluir sobreposições, sobreposições e planos de ação. Os principais indicadores de desempenho para anúncios de vídeo antes da exibição incluem [!UICONTROL Video Completion Rate] e [!UICONTROL Viewability Rate].

* **Anúncios de TV conectados (somente terceiros)**: Anúncios de TV conectados são exibidos antes e durante o conteúdo premium de vídeo de TV. Todo o inventário de TV conectado é executado em dispositivos de TV, o que significa que o vídeo é reproduzido automaticamente em um ambiente de tela cheia simplificado que os visualizadores não podem ignorar. A TV Conectada é o formato de vídeo digital mais próximo dos comerciais de TV. Os principais indicadores de desempenho para TV conectada incluem [!UICONTROL Completion Rate].

* **Anúncios de vídeo universal (somente de terceiros)**: anúncios de vídeo universais permitem direcionar o inventário de vídeo de ambientes de desktop, móveis e TV conectada para inventário VPAID e VAST usando uma única inserção de vídeo. Eles combinam todos os recursos de TV conectada, anúncios precedentes e anúncios precedentes móveis e são exibidos antes e durante o conteúdo de vídeo. Os principais indicadores de desempenho para vídeo universal incluem [!UICONTROL Completion Rate] e [!UICONTROL Viewability Rate].

   Anúncios de vídeo universais podem ser anexados somente a inserções de vídeo universais.

   Consulte &quot;[Perguntas frequentes sobre o Universal Video](/help/dsp/campaign-management/faq-universal-video.md)&quot; para obter mais informações sobre anúncios de vídeo universais.

## Aprovações de anúncios DSP

Ao criar um anúncio, o DSP o revisa em busca de categorias confidenciais, clique na funcionalidade de URL e na renderização de visualização.

Inicialmente, você verá um ponto vermelho no [!UICONTROL Status] coluna. O processo de revisão normalmente leva de 24 a 48 horas. Entretanto, um anúncio interrompido pode ter um status pendente por mais de 48 horas, portanto, você tem tempo para corrigir erros antes que o anúncio seja rejeitado. Os anúncios rejeitados incluem um motivo para a rejeição.

Quando o DSP aprovar um anúncio, você verá um ponto verde na coluna Status.

![indicador de aprovação no [!UICONTROL Status] coluna](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Seu anúncio só será veiculado se o DSP e o SSP tiverem aprovado o criativo. Cada SSP tem suas próprias exigências e processos de aprovação.

>[!MORELIKETHIS]
>
>* [Crie um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Especificações de publicidade](ad-specs.md)

