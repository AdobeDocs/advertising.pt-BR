---
title: Especificações de publicidade
description: Consulte as especificações gerais e específicas do editor.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 10e85f9ec0b7b867828cc9ac154af6f4982c44d2
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Especificações para os tipos de anúncios suportados

## Anúncios de vídeo (pré-lançamento, CTV e vídeo universal)

### Screens compatível

Por padrão, os anúncios são entregues em dispositivos de desktop, móveis e TV conectada. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Servidores de anúncios de terceiros compatíveis

Você pode usar folhas de marcas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Para obter uma lista completa de fornecedores suportados, consulte &quot;[Parceiros de Veiculação de Anúncios Certificados](certified-ad-servers.md)&quot;.

### Requisitos para Assets de vídeo de alta definição

**Tipo de Marca de Vídeo:** VPAID 2.0 JavaScript ou VAST (CTV). Todas as unidades de anúncios VPAID devem seguir a [especificação VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf), conforme definido pelo Interative Advertising Bureau (IAB).

**Codec de Vídeo:** MP4/H.264

**Resolução:** 1280x720 para 720p, 1920x1080 para 1080p

**Taxa de bits:** 1500-2500 kbps para 720p, 2500-3500 kbps para 1080p

**H.264 Perfil/Nível:** Alto perfil, nível 3.1 para 720p; Alto perfil, nível 4.0 para 1080p

**Taxa de Quadros do Vídeo:** 29,970 quadros/s (comumente conhecidos como 30 quadros/s) para países NTSC, 25 quadros/s para países PAL, 23,976 quadros/s (comumente conhecidos como 24 quadros/s) para conteúdo de aparência de filme

**Espaço de Cor do Vídeo:** 4:2:0 Subamostragem YUV Chroma

**Entrelaçamento de Vídeo:** Verificação progressiva, ou seja, não entrelaçada. Sem movimento intracampo (quadros de mistura) ou entrelaçamento.

**Líderes (Tablet):** Não permitido

**Codec de áudio:** AAC-LC ou HE-AACv1

**Taxa de áudio:** 128-192 kbps para AAC-LC, 64-128 kbps para HE-AACv1

**Canal de áudio:** mixagem estéreo de 2 canais

**Taxa de Amostragem de Áudio:** 44,1 kHz ou 48 kHz, conforme o material de origem

**Níveis de Áudio:** 24 LKFS (+/- 2,0 dB) nos EUA conforme ATSC A/85; 23 LUFS (+/- 1,0) na UE conforme EBU R128

#### Requisitos adicionais do editor para anúncios de TV conectada

* **Rede A+E:** Consulte as [especificações de anúncios](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf) da Rede A+E

* **Descoberta:** Consulte as [especificações de anúncios](/help/dsp/assets/discovery-networks-ad-specs.pdf) da Descoberta.

* **Disney (incluindo Hulu):** Consulte as [especificações de anúncios](https://hulu.disneyadsales.com/ad-products/video-commercial/) da Disney.

* **Máx HBO:** Consulte as [especificações de anúncios](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx) do máx HBO.

* **NBCUniversal:**

   * [Vídeo digital](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pavão](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Consulte as [especificações de anúncios](https://www.paramount.com/digital-ads) da Paramount.

## Exibir anúncios

### Screens compatível

Os anúncios são entregues por padrão em dispositivos móveis e desktop. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Tipos de arquivo suportados

**Imagem:** GIF, JPG/JPEG, PNG

**HTML5:** Tipos de arquivo de imagem: GIF, JPG/JPEG, PNG, SVG

### Requisitos para o Image Assets

O Universal Display é compatível.

**Tamanhos de anúncios recomendados:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480 x 60, 640 x 480, 88 x 31, 728 x 90, 970 x 250, 970 x 90

**Servidores de Publicidade de Terceiros com Suporte:** Você pode usar folhas de marcas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Para obter uma lista completa de fornecedores suportados, consulte &quot;[Parceiros de Veiculação de Anúncios Certificados](certified-ad-servers.md)&quot;.

## Anúncios de áudio

### Screens compatível

Desktop, Mobile, Tablet, Alto-falantes inteligentes e TV conectada

### Servidores de anúncios de terceiros compatíveis

Você pode usar folhas de marcas de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] e [!DNL Sizmek]. Para obter uma lista completa de fornecedores suportados, consulte &quot;[Parceiros de Veiculação de Anúncios Certificados](certified-ad-servers.md)&quot;.

### Requisitos para Assets de áudio

**Tipo de arquivo:** MP3, OGG, AAC

**Líderes (tabulação):** Não permitido

**Tamanho máximo do arquivo:** 2 MB

**Taxa de bits:** 128

**Comprimento do Arquivo:** 0-60s

#### Requisitos adicionais do editor

* **[!DNL iHeartRadio]**
   * Duração: 5, 15, 30 ou 60 segundos
   * Tipo de arquivo: MP3
   * Tamanho máximo do arquivo: 320 kbps
   * Volume: 44,1 kHz

* **[!DNL Pandora]**
   * Duração: 15 ou 30 segundos
   * Tipo de arquivo: MP4 (no aplicativo), MP3 (desktop)
   * Tamanho máximo do arquivo: 2,2 MB

* **[!DNL SoundCloud]**
   * Duração: 6, 15 ou 30 segundos
   * Tipo de arquivo: MP3
   * Tamanho máximo do arquivo: 5 MB

* **[!DNL Spotify]**
   * Duração: até 30 segundos
   * Tipo de arquivo: OGG
   * Tamanho máximo do arquivo: 500 MB
   * Volume: RMS normalizado para -14; pico de dBFS normalizado para -0,2 dBFS

* **[!DNL TargetSpot]**
   * Duração: 15, 30 ou 60 segundos
   * Tipo de arquivo: MP3

* **[!DNL TuneIn]**
   * Duração: 10, 15 ou 30 segundos
   * Tipo de arquivo: MP3, OGG
   * Volume: 44,1 kHz

### Requisitos para os anúncios de banner de companhia (opcional)

**Tamanhos com suporte:** 300x250, 500x500, 640x640, 1024x1024

#### Requisitos adicionais do editor

* **[!DNL iHeartRadio]:**
   * Tipo de arquivo: JPEG, JPG, PNG, GIF, SWF, HTML
   * Tamanho máximo do arquivo: 2,2 MB
   * Dimensões: 300 x 250

* **[!DNL Pandora]:**
   * Tipo de arquivo: JPEG, GIF
   * Tamanho máximo do arquivo: Tamanho: 100 KB
   * Dimensões: 300 x 250 (móvel ou desktop) ou 500 x 500 (desktop)

* **[!DNL SoundCloud]:**
   * Tipo de arquivo: Static JPG, PNG
   * Tamanho máximo do arquivo: menos de 400 KB
   * Dimensões: 1024 x 1024

* **[!DNL Spotify]:**
   * Tipo de arquivo: Static JPG, PNG
   * Tamanho máximo do arquivo: 200 KB
   * Dimensões: 300 x 250

* **[!DNL TuneIn]:**
   * Tipo de arquivo: JPEG, JPG, PNG, GIF, HTML
   * Tamanho máximo do arquivo: 2 MB
   * Dimensões: 300 x 250

## Anúncios de exibição nativos

Cada anúncio pode incluir uma imagem estática ou um GIF em movimento (cinemgraph).

### Screens compatível

Os anúncios são entregues por padrão em dispositivos móveis e desktop. O direcionamento de dispositivo está disponível para ajustar o delivery.

### Assets necessário para todos os formatos nativos no feed

#### Ativo de imagem

**Resolução:** Mínimo de 600x600px; Mínimo recomendado de 1200x627px

**Tipo de arquivo:** JPEG (anúncio de imagem ou imagem de capa de anúncio de vídeo), GIF (cinemógrafo)

**Tamanho do Arquivo:** Menos de 1 MB (A imagem deve estar sem texto.)

#### Logotipo do anunciante

**Resolução:** 80x80px no mínimo; 300x300px no mínimo recomendado

**Tipo de arquivo:** JPEG ou PNG.

**Taxa de proporção:** taxa 1x1

>[!NOTE]
>
>Dependendo da imagem sobre a qual ela será sobreposta, escolha entre os recursos de logotipo claro ou escuro.

#### Texto/cópia

**Título:** Máximo de 200 caracteres; recomenda-se 25 caracteres

**Legenda:** Máximo de 200 caracteres; recomenda-se 100 caracteres

**Patrocinado por:** Máximo de 200 caracteres; recomenda-se 30 caracteres

**Call to action (Somente MoPub):** Máximo de 15 caracteres

>[!NOTE]
>
>O layout final é definido pelo editor no tempo de execução. Se um anúncio exceder a contagem de caracteres recomendada, alguns provedores de inventário poderão não entregar o anúncio, ou o editor ou o SSP poderá truncar o texto.

#### URL da landing page

O URL de click-through com rastreadores de cliques opcionais.

Requisitos para rastreadores de cliques:

* Pixels de rastreamento de impressão de terceiros: somente formato de URL de imagem 1x1

* Rastreadores de visibilidade do JavaScript: compatível somente com o IAS; imagens 1x1 no formato JS.append somente

* Pixels de rastreamento de cliques de terceiros: deve redirecionar para a landing page incorporada ao URL (redirecionamento HTTP 302)

* Os rastreadores de cliques da plataforma de gerenciamento de dados (DMP) com 200 ou mais respostas não são compatíveis.

>[!MORELIKETHIS]
>
>* [Sobre o Gerenciamento de Anúncios](ad-about.md)
>* [Criar um único anúncio](ad-create.md)
>* [Criar vários anúncios de terceiros](ad-create-multiple.md)
>* [Editar um anúncio](ad-edit.md)
