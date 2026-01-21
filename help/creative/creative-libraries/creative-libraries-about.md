---
title: Sobre o bibliotecas do criativo
description: Aprenda a gerenciar os criativos de suas experiências de publicidade.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 8d549853be10ebfbb71b14e013b04178466e87fe
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# Sobre o bibliotecas do criativo

Seu criativo bibliotecas permitir que você gerenciar os criativos que usará em suas experiências publicidade. Você pode criar várias bibliotecas, cada uma com um conjunto de anúncios e *pacotes* de criativo, que são grupos de criativos que você pode adicionar a um experiência como uma unidade.

Seu bibliotecas pode incluir:

* **Criativos individuais:** você pode incluir anúncios individuais diretamente em publicidade experiências que não tenham definido usuário metas. Você também pode usar seus anúncios para criar pacotes, que podem ser incluídos nas experiências de publicidade direcionadas[&#128279;](/help/creative/experiences/experience-about.md).

   * **Anúncios padrão:** você pode upload e gerenciar anúncios em [vários formatos](#creative-creative-formats). Para cada criativo, especifique o idioma padrão para cada publicidade com a qual você associa os criativo e os landing page padrão que são abertos quando um usuário clica em uma publicidade que inclui o criativo. Como opção, você pode especificar rótulos para usar como filtros em várias exibições dentro [!DNL Creative] e como valores de coluna ao incluir o [!UICONTROL Custom Creative Report] uso da [!UICONTROL Creative Label] dimensão.

   * **Anúncios dinâmicos:** você pode criar anúncios gerados dinamicamente mapeando variáveis dinâmicas em um publicidade modelo a valores em um arquivo de feed. Todos os usuários podem pré-visualização, duplicado e excluir anúncios dinâmicos existentes.

* **Pacotes de criativos:** agrupe anúncios em pacotes para usar em várias experiências com metas de usuário definidas. É possível criar *pacotes de exibição padrão que consistem em anúncios* de exibição padrão, *pacotes de vídeo padrão que consistem em anúncios* de vídeo padrão e *pacotes de exibição dinâmicos que consistem em anúncios de exibição gerados* dinamicamente.

## Formatos de Creative suportados {#creative-creative-formats}

### Formatos para anúncios padrão

É possível adicionar e gerenciar os seguintes tipos de criativo nos [tamanhos](creative-sizes.md) de criativo suportados.

>[!IMPORTANT]
>
>* Mesmo se você pretende usar HTML5, HTML5 flexível ou anúncios de terceiros para suas experiências de anúncio de exibição padrão, você também deve adicionar anúncios de imagem para cada tamanho criativo usado.
>* Cada experiência de exibição padrão requer uma criativo de imagem padrão para cada criativo tamanho atribuído à experiência. Os anúncios de imagem padrão são usados quando um navegador não é JavaScript habilitado ou quando os servidor de publicidade não podem personalizar o publicidade por causa de atrasos.
>* Cada experiência de vídeo padrão requer uma criativo de vídeo padrão para cada criativo duração atribuída à experiência.<!-- when is it used? -->

#### HTML5 flexível

Os criativos HTML5 flexíveis são criativos em HTML5 com todas as suas imagens e outros atributos como tags HTML padrão, que você pode editar diretamente dentro [!DNL Creative], dentro de uma criativo biblioteca ou dentro de um experiência individual (que cria uma variação do criativo original). No DSP, anúncios HTML5 flexíveis são para um único tamanho de publicidade específico (em pixels). Como opção, você pode alterar os valores padrão dos atributos especificados em uma criativo HTML5 flexível. Posteriormente, é possível especificar valores personalizados para os atributos em um experiência específico, o que cria uma variação do criativo pai.

Você pode upload anúncios HTML5 flexíveis como arquivos ZIP ou usar um dos modelos disponíveis para suas conta como ponto de partida. Consulte as [especificações para anúncios](html5-creative-specification.md) HTML5 flexíveis.

#### Anúncios de exibição padrão

Anúncios de exibição padrão incluem:

* Anúncios HTML5 carregados localmente ou a partir do Adobe Systems GenStudio para Marketing de desempenho.
* Imagem arquivos carregados localmente ou a partir de Adobe Experience Manager.

##### Criativos de HTML5

* **Experiências GenStudio:** você pode importar todas as publicidade variantes de um [experiência de anúncio de exibição](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/display-ad-experiences) no [GenStudio para Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) de desempenho como um criativo HTML5. Links externos são convertidos em referências locais. O conteúdo HTML pode ter até 20 MB, e as imagens individuais podem ter até 50 MB.

  Depois de importar uma experiência GenStudio, você pode editar as metadados (nome, idioma, tags) para as criativo importadas, mas não as criativo conteúdo. Se você editar o experiência GenStudio no GenStudio, re importe os experiência [!DNL Creative] para usar a versão mais recente.

  >[!NOTE]
  >
  >Para usar esse recurso, o GenStudio conta e o Advertising Creative conta devem usar a mesma ID da organização e o usuário deve ter permissões para acessar o GenStudio.

* **Arquivos carregados:** você também pode upload anúncios HTML5 simples ou estáticos, com todos os atributos e imagens especificados, como arquivos ZIP. Não é possível editar atributos ou adicionar imagens; em vez disso, upload um novo arquivo ZIP para adicionar um novo criativo. Consulte as [especificações para anúncios HTML5 simples e estáticos](html5-creative-specification.md).

##### anúncios do Imagem

Você pode incluir anúncios de imagem no formato GIF, JPEG, JPG ou PNG. Você pode upload imagens aprovadas de suas contas do Adobe Experience Manager ou imagens de seu dispositivo ou rede.

Cada anúncio de exibição padrão experiência requer uma criativo de imagem padrão para cada criativo tamanho atribuído à experiência.

#### Anúncios de terceiros

Insira JavaScript tags rastreamento de anúncios hospedadas em servidores publicidade de terceiros. O script varia de acordo com servidor de publicidade; este é um exemplo:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### anúncios do Vídeo {#creative-video-specs}

Você pode upload anúncios de vídeo primários para TV web, móveis ou conectados de sua dispositivo ou rede. Cada publicidade de vídeo padrão experiência requer uma criativo de vídeo padrão para cada duração criativo atribuída ao experiência. DSP transcodifica automaticamente todos os anúncios de vídeo como tags VAST 2.0 para que você possa pré-visualização-los. Em [!UICONTROL Tag Manager], opcionalmente [, é possível aplicar transcodificação](/help/creative/experiences/experience-tag-video-transcoding.md) específica DSP a qualquer publicidade de vídeo experiência tag.

Consulte os requisitos de criativo do vídeo a seguir. **Observação:** se você upload experiências de vídeo para o Advertising DSP, consulte também os Requisitos de [alta definição DSP Vídeo Assets](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets), que podem ser mais limitados.

**Arquivo Tipo:** .mov, .mp4, .webm

**Arquivo tamanho:** máximo de 512 MB

**Taxa de proporção do Vídeo:** 16:9, 4:3

**Resolução Vídeo:** 640x360 para 360p, 1280x720 para 720p, 1920x1080 por 1080p

**Vídeo:** máximo de 90 segundos

**Taxa de bits:** 600-1200 kbps para 360p, 1500-2500 kbps para 720p, 3000-5000+ kbps para 1080p

**Vídeo Taxa de quadros:** 23,98 FPS. Taxas de quadros adicionais podem ser aceitas com base em requisitos regionais ou editor

**Vídeo Codec:** H.264 (padrão do setor), AV1, H.265

**Formato Áudio:** ACC (industry standard/MP4), Opus (WebM/AV1)

**taxa de bits Áudio:** 16-512 kbps

**Áudio Taxa de Amostra:** 44100-48000 Hz

**Taxa de Áudio:** 44,1kHz ou 48 kHz

**Áudio Outros:** o arquivo carregado deve estar não entrelaçado, misturado e conter uma áudio faixa. Pode não haver som, mas uma áudio faixa deve ser incluída no arquivo de vídeo.

### Formato para anúncios dinâmicos

Você pode gerar anúncios dinamicamente em formato HTML5 estático e HTML5 dinâmico mapeando variáveis dinâmicas em um publicidade modelo a valores em um arquivo de feed. Os anúncios dinâmicos podem incluir anúncios migrados de suas experiências herdadas Adobe Systems Advertising Dynamic Creative Optimization (DCO).

## As [!UICONTROL Creative Libraries] exibições

Consulte &quot;[Personalizar suas visualizações](/help/creative/introduction/customize-data-views.md) de dados&quot; para obter mais informações sobre como personalizar cada visualização.

### O [!UICONTROL Creative Libraries] visualização principal

A [!UICONTROL Creative Libraries] visualização principal mostra todos os bibliotecas de criativo. Os dados para cada biblioteca inclui o número de experiências às quais os pacotes do biblioteca são atribuídos, o número de pacotes, o número de criativos, o número de tamanhos de criativo, o número de metas de idioma padrão, a data de criação e a última data de modificação para qualquer elemento do biblioteca. O modo de tabela também inclui uma coluna para o anunciante.

Quando você está no cartão modo, você pode percorrer as imagens em um biblioteca com vários anúncios usando os &lt; and > botões.

#### Ações disponíveis

* [Criar um novo biblioteca](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Para cada biblioteca de criativo:

   * [Editar um nome biblioteca](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Abra uma biblioteca para visualização os anúncios e pacotes atribuídos ao biblioteca](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [bibliotecas de Excluir](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### As [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] visualizações

#### [!UICONTROL Standard Ads]

A [!UICONTROL Standard Ads] guia mostra todos os anúncios padrão criados por você. Os dados para cada criativo inclui o tamanho da criativo, o tipo de criativo e a data de criação. O modo de tabela também inclui colunas para o idioma padrão e o landing page padrão.

##### Ações disponíveis

* [Adicionar anúncios padrão a um biblioteca](creative-add-standard.md)

* [Editar um criativo padrão](creative-edit-standard.md)

* [Visualização um criativo padrão](creative-preview.md)

* [Adicione anúncios padrão a pacotes de exibição padrão e remova anúncios padrão de uma exibição padrão pacote](creative-attach-detach-bundles.md)

* [Adicione anúncios de vídeo a pacotes de vídeo padrão e remova os anúncios de vídeo de um pacote de vídeo padrão](creative-attach-detach-bundles.md)

* [Duplicar anúncios padrão](creative-duplicate.md)

* [Fazer download de anúncios padrão](creative-download.md)

* [Excluir anúncios padrão](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

A [!UICONTROL Dynamic Ads] guia mostra todos os anúncios dinâmicos criados dinamicamente para seus catálogos de criativo, exceto por qualquer anúncio dinâmico que você [excluiu](creative-delete.md) manualmente do [!UICONTROL Dynamic Ads] guia. Se você [duplicasse](creative-duplicate.md) manualmente qualquer anúncio<!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed --> dinâmico, o lista de anúncios desse catálogo também inclui os anúncios duplicado.

Os dados para cada criativo inclui o tipo de criativo, o tamanho da criativo, o número de catálogos aos quais a criativo pertence e a data de criação. O modo de tabela também inclui colunas para a publicidade modelo pela qual a criativo foi gerada e a contagem oferta.

>[!NOTE]
>
>Cada vez que um catálogo é processado, os dados são atualizados para os anúncios dinâmicos existentes para esse catálogo.<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### Ações disponíveis

* [Adicionar anúncios dinâmicos a um biblioteca](creative-add-dynamic.md)

* [Editar um criativo dinâmico](creative-edit-dynamic.md)

* [Visualização anúncios dinâmicos](creative-preview.md)

* [Adicione anúncios dinâmicos a pacotes de exibição dinâmicos e remova anúncios dinâmicos de uma exibição dinâmica pacote](creative-attach-detach-bundles.md)

* [Duplicar anúncios dinâmicos](creative-duplicate.md)

* [Excluir anúncios dinâmicos](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### O [!UICONTROL Creative Libraries] visualização do > [!UICONTROL Bundles]

A [!UICONTROL Bundles] visualização mostra todos os contêineres de pacote padrão e dinâmicos. Você pode ver os criativo nomes, tamanhos de criativo e idiomas para os anúncios incluídos em cada pacote. Quando você está no cartão modo, você pode percorrer as imagens em um pacote com vários anúncios usando os &lt; and > botões.

#### Ações disponíveis

* Adicione pacotes de exibição padrão, vídeo padrão e exibição dinâmica a uma biblioteca

* Lista e pré-visualização os criativos em um pacote

* Editar um nome pacote

* Adicione anúncios de exibição padrão a pacotes de exibição padrão e remova anúncios de exibição padrão de uma exibição padrão pacote

* Adicione anúncios de vídeo padrão a pacotes de vídeo padrão e remova anúncios de vídeo padrão de um pacote de vídeo padrão

* Duplicar pacotes

* Pacotes de Excluir

>[!MORELIKETHIS]
>
>* [Gerenciar bibliotecas de criativo](/help/creative/creative-libraries/creative-library-manage.md)
>* [Adicionar anúncios padrão a um biblioteca de criativo](creative-add-standard.md)
>* [Gerenciar pacotes de criativo](bundle-manage.md)
>* [Personalizar suas exibições de dados](/help/creative/introduction/customize-data-views.md)
