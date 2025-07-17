---
title: Sobre suas bibliotecas criativas
description: Saiba mais sobre como gerenciar os elementos de criação para suas experiências de anúncio.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 056502f8c634ee62b750d7c4c188dc248b836a5a
workflow-type: tm+mt
source-wordcount: '1412'
ht-degree: 0%

---

# Sobre suas bibliotecas criativas

*Recurso beta fechado*

Suas bibliotecas criativas permitem gerenciar os elementos criativos que você usará em suas experiências de anúncio. Você pode criar várias bibliotecas, cada uma com um conjunto de criações e *pacotes criativos*, que são grupos de criações que você pode adicionar a uma experiência como uma unidade.

Suas bibliotecas podem incluir:

* **Criações individuais:** você pode incluir criações individuais diretamente em experiências de anúncio que não têm destinos de usuário definidos. Você também pode usar suas criações para criar pacotes, que podem ser incluídos em [experiências de anúncios](/help/creative/experiences/experience-about.md) direcionadas.

   * **Criações padrão**: você pode carregar e gerenciar criações em [vários formatos](#creative-creative-formats). Para cada criativo, especifique o idioma padrão para cada anúncio ao qual você associa o criativo e a landing page padrão que abre quando um usuário clica em um anúncio que inclui o criativo. Opcionalmente, é possível especificar rótulos para usar como filtros em várias exibições em [!DNL Creative] e como valores de coluna em [!UICONTROL Custom Creative Report] ao incluir o uso da dimensão [!UICONTROL Creative Label].

   * **Criações dinâmicas:** (somente clientes do Adobe Advertising DCO existentes) Os usuários administradores podem criar criações geradas dinamicamente, mapeando variáveis dinâmicas em um modelo de anúncio para valores em um arquivo de feed. Todos os usuários podem visualizar, duplicar e excluir anúncios dinâmicos existentes.

* **Pacotes de criação:** grupos de criação em pacotes para usar em várias experiências com destinos de usuário definidos. Você pode criar *conjuntos de exibição padrão* que consistem em anúncios de exibição padrão, *conjuntos de vídeo padrão* que consistem em anúncios de vídeo padrão e *conjuntos de exibição dinâmicos* que consistem em anúncios de exibição gerados dinamicamente.

## Formatos Creative compatíveis {#creative-creative-formats}

### Formatos para criações padrão

Você pode adicionar e gerenciar os seguintes tipos de criação nos [tamanhos de criação suportados](creative-sizes.md).

>[!IMPORTANT]
>
>* Mesmo que você pretenda usar o HTML5, o Flexible HTML5 ou criações de terceiros para suas experiências de anúncio de exibição padrão, também é necessário adicionar criações de imagem para cada tamanho criativo usado.
>* Cada experiência de exibição padrão requer uma criação de imagem padrão para cada tamanho criativo atribuído à experiência. As criações de imagem padrão são usadas quando um navegador não está habilitado para JavaScript ou quando o servidor de publicidade não pode personalizar o anúncio devido a atrasos.
>* Cada experiência de vídeo padrão requer uma criação de vídeo padrão para cada duração de criação atribuída à experiência.<!-- when is it used? -->

#### HTML5 flexível

Criativas HTML5 flexíveis são criativas HTML5 com todas as suas imagens e outros atributos como tags HTML padrão, que você pode editar diretamente em [!DNL Creative], em uma biblioteca criativa ou em uma experiência individual (o que cria uma variação do criativo original). No DSP, as criações flexíveis do HTML5 são para um único tamanho de anúncio específico (em pixels). Opcionalmente, é possível alterar os valores padrão dos atributos especificados em uma criação flexível do HTML5. Posteriormente, você pode especificar valores personalizados para os atributos em uma experiência específica, o que cria uma variação da criação principal.

Você pode fazer upload de criações flexíveis do HTML5 como arquivos ZIP ou usar um dos modelos disponíveis em sua conta como ponto de partida. Consulte as [especificações de criações flexíveis do HTML5](html5-creative-specification.md).

#### Criação do HTML5

Você pode fazer upload de criações simples ou estáticas do HTML5, com todos os atributos e imagens especificados, como arquivos ZIP. Não é possível editar atributos ou adicionar imagens; em vez disso, faça upload de um novo arquivo ZIP para adicionar um novo criativo. Consulte as [especificações de criações simples e estáticas do HTML5](html5-creative-specification.md).

#### Criação de imagens

É possível incluir criações de imagem no formato GIF, JPEG, JPG ou PNG. Você pode fazer upload de imagens aprovadas de suas contas do Adobe Experience Manager ou imagens de seu dispositivo ou rede.

Cada experiência de anúncio de exibição padrão requer uma criação de imagem padrão para cada tamanho criativo atribuído à experiência.

#### Criação de terceiros

Insira tags de rastreamento do JavaScript para criadores hospedados em servidores de publicidade de terceiros. O script varia de acordo com o servidor de publicidade; veja a seguir um exemplo:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Criações de vídeo {#creative-video-specs}

Você pode fazer upload de criações de vídeo primárias para a Web, dispositivos móveis ou TV conectada do seu dispositivo ou rede. Cada experiência de anúncio de vídeo padrão requer uma criação de vídeo padrão para cada duração de criação atribuída à experiência. Todas as criações de vídeo são transcodificadas automaticamente pelo DSP como tags VAST 2.0 para que você possa visualizá-las. No [!UICONTROL Tag Manager], você pode [aplicar transcodificação específica do editor](/help/creative/experiences/experience-tag-video-transcoding.md) a qualquer marca de experiência de vídeo e anúncios.

Consulte os seguintes requisitos de criação de vídeo. **Observação:** para carregar experiências com vídeo para a Advertising DSP, consulte também os [Requisitos para Assets com Vídeo de Alta Definição](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets) da DSP, que podem ser mais limitados.

**Tipo de Arquivo:** .mov, .mp4, .webm

**Tamanho do Arquivo:** Máximo de 512 MB

**Taxa de proporção do vídeo:** 16:9, 4:3

**Resolução de vídeo:** 640x360 para 360p, 1280x720 para 720p, 1920x1080 para 1080p

**Duração do Vídeo:** Máximo de 90 segundos

**Taxa de bits:** 600-1200 kbps para 360p, 1500-2500 kbps para 720p, 3000-5000+ kbps para 1080p

**Taxa de quadros do vídeo:** 23,98 quadros/s. Taxas de quadros adicionais podem ser aceitas com base nos requisitos regionais ou do editor

**Codec de vídeo:** H.264 (padrão do setor), AV1, H.265

**Formato de Áudio:** ACC (padrão do setor/MP4), Opus (WebM/AV1)

**Taxa de áudio:** 16-512 kbps

**Taxa de Amostragem de Áudio:** 44100-48000 Hz

**Taxa de Áudio:** 44,1kHz ou 48 kHz

**Outro Áudio:** O arquivo carregado deve ser não entrelaçado, misturado e conter uma faixa de áudio. Pode não haver som, mas uma faixa de áudio precisa ser incluída no arquivo de vídeo.

### Formato para anúncios dinâmicos

Os usuários administradores podem gerar dinamicamente criações no formato estático HTML5 e HTML5, mapeando variáveis dinâmicas em um modelo de anúncio para valores em um arquivo de feed. As criações dinâmicas podem incluir criações de suas experiências herdadas do Adobe Advertising Dynamic Creative Optimization (DCO).

## As [!UICONTROL Creative Libraries] visualizações

Consulte &quot;[Personalizar suas visualizações de dados](/help/creative/introduction/customize-data-views.md)&quot; para obter mais informações sobre como personalizar cada visualização.

### A visualização principal [!UICONTROL Creative Libraries]

A exibição principal do [!UICONTROL Creative Libraries] mostra todas as suas bibliotecas criativas. Os dados de cada biblioteca incluem o número de experiências às quais os pacotes da biblioteca são atribuídos, o número de pacotes, o número de criativos, o número de tamanhos de criação, o número de alvos de idioma padrão, a data de criação e a data da última modificação para qualquer elemento da biblioteca. O modo de tabela também inclui uma coluna para o anunciante.

Quando estiver no modo de cartão, você pode rolar pelas imagens em uma biblioteca com várias criações usando os botões &lt; e >.

#### Ações disponíveis

* [Criar uma nova biblioteca](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Para cada biblioteca criativa:

   * [Editar um nome de biblioteca](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Abrir uma biblioteca para exibir os elementos de criação e os pacotes atribuídos à biblioteca](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Excluir bibliotecas](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### As [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] visualizações

#### [!UICONTROL Standard Ads]

A guia [!UICONTROL Standard Ads] mostra todas as criações padrão que você criou. Os dados de cada criativo incluem o tamanho do criativo, o tipo de criativo e a data de criação. O modo de tabela também inclui colunas para o idioma padrão e a landing page padrão.

##### Ações disponíveis

* [Adicionar criações padrão a uma biblioteca](creative-add-standard.md)

* [Editar um criativo padrão](creative-edit-standard.md)

* [Pré-visualização de um criativo padrão](creative-preview.md)

* [Adicionar criações padrão a conjuntos de exibições padrão e remover criações padrão de um conjunto de exibições padrão](creative-attach-detach-bundles.md)

* [Adicionar criações de vídeo a pacotes de vídeo padrão e remover criações de vídeo de um pacote de vídeo padrão](creative-attach-detach-bundles.md)

* [Duplicar criações padrão](creative-duplicate.md)

* [Baixar criações padrão](creative-download.md)

* [Excluir criações padrão](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

A guia [!UICONTROL Dynamic Ads] mostra todas as criações dinâmicas que foram criadas dinamicamente para seus catálogos criativos, exceto todas as criações dinâmicas que você [excluiu manualmente](creative-delete.md) da guia [!UICONTROL Dynamic Ads]. Se você [duplicou manualmente](creative-duplicate.md) todas as criações dinâmicas desde que um catálogo foi processado pela última vez, a lista de criações para esse catálogo também incluirá as criações duplicadas.

Os dados de cada criativo incluem o tipo criativo, o tamanho criativo, o número de catálogos aos quais o criativo pertence e a data de criação. O modo de tabela também inclui colunas para o modelo pelo qual a criação foi gerada e a contagem da oferta.

>[!NOTE]
>
>Cada vez que um catálogo é processado, os dados são atualizados para os elementos de criação dinâmicos existentes para esse catálogo.

##### Ações disponíveis

A capacidade de criar e editar criações dinâmicas está disponível no momento somente na Equipe de conta da Adobe. No entanto, todos os usuários podem:

* [Visualizar criações dinâmicas](creative-preview.md)

* [Adicionar criações dinâmicas a conjuntos de exibição dinâmicos e remover criações dinâmicas de um conjunto de exibição dinâmico](creative-attach-detach-bundles.md)

* [Duplicar criações dinâmicas](creative-duplicate.md)

* [Excluir criações dinâmicas](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### A visualização [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

A exibição [!UICONTROL Bundles] mostra todos os seus contêineres de pacote padrão e dinâmicos. Você pode ver os nomes criativos, tamanhos criativos e idiomas dos criadores incluídos em cada pacote. Quando estiver no modo de cartão, você pode rolar pelas imagens em um pacote com várias criações usando os botões &lt; e >.

#### Ações disponíveis

* Adição de exibição padrão, vídeo padrão e pacotes de exibição dinâmicos a uma biblioteca

* Listar e visualizar as criações em um pacote

* Editar um nome de pacote

* Adicionar criações de exibição padrão a conjuntos de exibição padrão e remover criações de exibição padrão de um conjunto de exibição padrão

* Adicionar criações de vídeo padrão a pacotes de vídeo padrão e remover criações de vídeo padrão de um pacote de vídeo padrão

* Pacotes duplicados

* Excluir pacotes

>[!MORELIKETHIS]
>
>* [Gerenciar bibliotecas criativas](/help/creative/creative-libraries/creative-library-manage.md)
>* [Adicionar criações padrão a uma biblioteca criativa](creative-add-standard.md)
>* [Gerenciar pacotes criativos](bundle-manage.md)
>* [Personalizar suas visualizações de dados](/help/creative/introduction/customize-data-views.md)
