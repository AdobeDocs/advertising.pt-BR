---
title: Visão geral da implementação do Adobe Advertising Creative
description: Saiba mais sobre o fluxo de trabalho básico para implementar o  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Visão geral da implementação do Adobe Advertising Creative

*Beta fechado*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

A equipe de operações do [!DNL Creative] trabalha com cada anunciante para configurar suas experiências criativas e criativas, implementando as experiências de anúncios como anúncios na DSP ou fornecendo à sua equipe tags de anúncios de terceiros para implementá-las e validando os dados iniciais de custo, clique e conversão.

De forma contínua, a Equipe de conta da Adobe, a equipe da agência ou o anunciante (dependendo dos termos do service level agreement) precisam monitorar cada experiência e editá-la conforme necessário para atender às metas do anunciante.

## Tarefas de configuração inicial para [!DNL Creative] experiências

A equipe de implementação e/ou sua agência trabalhará com você no seguinte:

1. Defina suas metas de personalização (como personalizar anúncios para prospecção ou redirecionamento); todos os dados originais, secundários e de terceiros que estão disponíveis, incluindo ativos criativos e segmentos de público-alvo; e sua estratégia para atingir suas metas.<!-- and CRM data? used how/where? -->

1. (Novas contas de anunciante) Configurar contas administrativas:

   1. Configure a conta do anunciante para [!DNL Creative] e também crie uma conta no Advertising Search, Social e Commerce.

      A configuração da conta do [!DNL Creative] está no Advertising DSP, mesmo que o anunciante não use o resto do DSP.

      Da mesma forma, mesmo que o anunciante não seja um cliente do [!DNL Search, Social, & Commerce], a conta do [!DNL Search, Social, & Commerce] será usada para criar marcas de rastreamento de conversão e configurar colunas de conversão no [!DNL Creative].

   1. (Se necessário) Crie contas de usuário para o anunciante para exibir e gerenciar suas experiências de criação e de anúncio e gerar relatórios.

1. (Opcional) Se você deseja criar segmentos de público-alvo primários para incluir como alvos para seus componentes de criação, crie as tags de uma das seguintes maneiras:

   * [Crie pixels de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md) para redirecionar anúncios para visitantes com atributos específicos a páginas de aterrissagem ou páginas de conversão específicas e, em seguida, gere marcas para inserir nas páginas da Web relevantes.

   * (Anunciantes com o DSP) No DSP, [crie segmentos de público-alvo personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear todos os visitantes de páginas de aterrissagem ou páginas de conversão específicas e, em seguida, gere tags para inserir nas páginas da Web relevantes.

   Ambos os tipos de tags são tags de imagem, que exibem uma imagem transparente de 1 pixel x 1 pixel (pixel), invisível para os usuários finais, na página da Web em que são adicionadas. Posteriormente, você pode configurar os elementos de criação em uma experiência de anúncio para direcionar pixels ou segmentos específicos de redirecionamento, de modo que os elementos de anúncio relevantes sejam exibidos somente para usuários que visitaram anteriormente as páginas do site associadas ao pixel ou segmento.

   O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

   **Observação:** você também pode usar seus públicos-alvo primários da Adobe Audience Manager e da Adobe Analytics como alvos criativos. Depois que um visitante é qualificado para um público-alvo compartilhado de [!DNL Analytics], as informações são ativadas em [!DNL Creative] em cerca de 24 a 48 horas. <!--Are times still true? -->

1. Configure a hierarquia da campanha nos DSPs nos quais você implementará as experiências de anúncio. Use o direcionamento compatível com o direcionamento nas experiências de anúncio que você implementará nas campanhas.

   O comportamento hierárquico do direcionamento pode variar de acordo com a DSP. O Advertising DSP aplica o direcionamento em nível de anúncio acima do direcionamento em nível de posicionamento (não em vez dele). Por exemplo, se uma disposição for direcionada a usuários na Austrália e um anúncio for direcionado a usuários no Japão, o anúncio será direcionado à ramificação &quot;Todos os outros&quot; para a experiência. Pense em toda a estrutura da campanha.

1. Configure experiências de anúncio com base em suas metas de publicidade:

   * **Fluxo de trabalho de automação:** A equipe de operações do [!DNL Creative] pode criar anúncios dinâmicos para sua organização usando modelos de anúncios e feeds de dados.

     Para obter mais informações, entre em contato com a equipe de conta da Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Fluxo de trabalho manual:** Configure manualmente as experiências de anúncio:

      1. [Configurar criações padrão para usar em suas experiências](/help/creative/creative-libraries/creative-add-standard.md):

         * Para criadores que [!DNL Creative] hospedará, carregue-os. Isso pode incluir ativos de imagem em uma conta do Adobe Experience Manager.

         * Para anúncios hospedados em um servidor de anúncios de terceiros compatível, aponte para os arquivos criativos.

      1. (Opcional) [Criações de grupo em pacotes](/help/creative/creative-libraries/bundle-manage.md) que você pode anexar a experiências direcionadas em uma etapa.

      1. Configurar [experiências de anúncio](/help/creative/experiences/experience-about.md):

         * Para [experiências de anúncios direcionadas](/help/creative/experiences/experience-create-targeting.md), criações em sequência e destinos de anúncios opcionais.

           Os destinos de anúncios podem incluir pixels de redirecionamento criados em [!DNL Creative]; segmentos de público-alvo no Adobe Experience Cloud (incluindo no DSP, Audience Manager ou [!DNL Analytics]); destinos geográficos; ou acionadores de dados específicos na página da Web (como SKU=01234567890123 ou Cart=empty).

         * Para [experiências de anúncio não direcionadas](/help/creative/experiences/experience-create-no-targeting.md), crie configurações gerais de experiência.

           Os destinos de anúncios podem incluir pixels de redirecionamento criados em [!DNL Creative]; segmentos de público-alvo no Adobe Experience Cloud (incluindo no DSP, Audience Manager ou [!DNL Analytics]); destinos geográficos; ou acionadores de dados específicos na página da Web (como SKU=01234567890123 ou Cart=empty).













1. Configure o rastreamento de conversão para suas experiências de anúncio:


Configurar o rastreamento de conversão. Dependendo da implementação, pode envolver a adição de
marcas de rastreamento de conversão para as páginas da Web do anunciante e/ou configuração de um
queda de feed para dados de conversão que o anunciante coletou separadamente.


Você pode gerar tags de rastreamento de conversão do Adobe Advertising no Advertising Search, Social e Commerce ou no Gerenciador dinâmico de tags da Adobe (anteriormente chamado de Gerenciador dinâmico de tags).
Observação: você deve usar tags de conversão do JavaScript, não tags de imagem.


O departamento de TI do anunciante ou outro grupo pode precisar programar ou ser informado
sobre, a implantação de tag.


(Opcional) No Search, Social e Commerce, faça cada conversão (propriedade da transação)
disponível como um conjunto de colunas individual em visualizações de dados e relatórios.


Uma conversão (propriedade de transação) é listada em Pesquisar, Social e Commerce depois de em
pelo menos um evento de conversão foi rastreado.


Se você não disponibilizar métricas específicas, todas as conversões serão consolidadas
em um conjunto de colunas &quot;Conversões&quot;.


Valide os dados que são rastreados.


(Opcional) Configurar a entrega de relatórios agendados para endereços de email especificados.


Para obter instruções, consulte o capítulo de ajuda em &quot;Relatórios&quot;.


Configure campanhas publicitárias no Advertising DSP ou outro DSP e forneça o JavaScript
ou iframe para as experiências de anúncio para o anunciante, que pode implementá-las como
anúncios de terceiros na DSP.


Monitore o desempenho de suas experiências de anúncio concluídas, visualizando anúncios predefinidos
detalhes de desempenho para experiências individuais ou criação de relatórios de desempenho personalizados.


(Conforme necessário) Atualize as experiências de anúncio com base no desempenho e nas mensagens atualizadas.






>[!MORELIKETHIS]
>
>* [Sobre o Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Como a interface do usuário está organizada](/help/creative/introduction/ui.md)
