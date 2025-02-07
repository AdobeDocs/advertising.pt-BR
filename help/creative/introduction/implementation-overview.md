---
title: Visão geral da implementação do Adobe Advertising Creative
description: Saiba mais sobre o fluxo de trabalho básico para implementar o  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Visão geral da implementação do Adobe Advertising Creative

*Beta fechado*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

A equipe de operações do [!DNL Creative] trabalha com cada anunciante para configurar suas experiências criativas e criativas, implementando as experiências de anúncios como anúncios no DSP ou fornecendo à sua equipe tags de anúncios de terceiros para implementá-las e validando os dados iniciais de custo, clique e conversão.

De forma contínua, a Equipe de conta do Adobe, a equipe da agência ou o anunciante (dependendo dos termos do service level agreement) precisam monitorar cada experiência e editá-la conforme necessário para atender aos objetivos do anunciante.

## Tarefas de Instalação Iniciais para [!DNL Creative] Campanhas <!-- Experiences? "Campaigns" may be confusing now. -->

A equipe de implementação e/ou sua agência trabalhará com você no seguinte:

1. Defina suas metas de personalização (como personalizar anúncios para prospecção ou redirecionamento); todos os dados originais, secundários e de terceiros que estão disponíveis, incluindo ativos criativos, segmentos de público-alvo e dados de CRM <!-- used how/where? -->; e sua estratégia para atingir suas metas.

1. (Novas contas de anunciante) Configurar contas administrativas:

   1. Configure a conta do anunciante para [!DNL Creative]<!-- and/or DSP? --> e também crie uma conta no Advertising Search.

      A configuração da conta do [!DNL Creative] é feita no Advertising DSP, mesmo que o anunciante não seja um cliente DSP.

      Da mesma forma, mesmo que o anunciante não seja um cliente do [!DNL Search], a conta do [!DNL Search] será usada para criar marcas de rastreamento de conversão e configurar colunas de conversão no [!DNL Creative].

   1. (Se necessário) Crie contas de usuário para o anunciante para exibir e gerenciar suas experiências de criação e de anúncio e gerar relatórios.

1. (Opcional) Se você deseja criar segmentos de público-alvo primários para incluir como alvos para seus componentes de criação, crie as tags de uma das seguintes maneiras:

   * [Crie pixels de redirecionamento](/help/creative/pixels/retargeting-pixel-manage.md) para redirecionar anúncios para visitantes com atributos específicos a páginas de aterrissagem ou páginas de conversão específicas e, em seguida, gere marcas para inserir nas páginas da Web relevantes.

   * (Anunciantes com DSP) No DSP, [crie segmentos de público-alvo personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear todos os visitantes de páginas de aterrissagem ou páginas de conversão específicas e, em seguida, gere tags para inserir nas páginas da Web relevantes.

   Ambos os tipos de tags são tags de imagem, que exibem uma imagem transparente de 1 pixel x 1 pixel (pixel), invisível para os usuários finais, na página da Web em que são adicionadas. Posteriormente, você pode configurar os elementos de criação em uma experiência de anúncio para direcionar pixels ou segmentos específicos de redirecionamento, de modo que os elementos de anúncio relevantes sejam exibidos somente para usuários que visitaram anteriormente as páginas do site associadas ao pixel ou segmento.

   O departamento de TI do anunciante ou outro grupo pode precisar agendar ou ser informado sobre a implantação da tag.

   **Observação:** você também pode usar seus públicos-alvo primários da Adobe Audience Manager e da Adobe Analytics como alvos criativos. Depois que um visitante é qualificado para um público-alvo compartilhado de [!DNL Analytics], as informações são ativadas em [!DNL Creative] em cerca de 24 a 48 horas. <!--Still true? And what about AAM and DSP? -->

1. Configure experiências de anúncio com base em suas metas de publicidade:

   * **Fluxo de trabalho de automação:** A equipe de operações do [!DNL Creative] pode criar anúncios dinâmicos para sua organização usando modelos de anúncios e feeds de dados.

     Para obter mais informações, entre em contato com a equipe de conta do Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Fluxo de trabalho manual:** Configure manualmente as experiências de anúncio:

      1. Configurar criações para usar em suas experiências:

         * Para criadores que [!DNL Creative] hospedará, carregue-os.<!-- Add x-ref and reword if necessary to cover all cases -->

         * Para criadores hospedados em um servidor de anúncios de terceiros com suporte, [aponte para os arquivos criativos](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Opcional) [Criações de grupo em pacotes](/help/creative/creative-libraries/bundle-manage.md) que você pode anexar às experiências em uma etapa.

      1. Sequência de criações e destinos de anúncios opcionais como [experiências de anúncios](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Os destinos de anúncios podem incluir pixels de redirecionamento criados por você no [!DNL Creative]; segmentos de público-alvo no Adobe Experience Cloud (inclusive no DSP, Audience Manager ou [!DNL Analytics]); destinos geográficos; ou acionadores de dados específicos na página da Web (como SKU=01234567890123 ou Cart=empty).&lt;!— Não vejo segmentos de público disponíveis, e vejo destinos de raio (o que não funciona) mas não outros destinos geográficos — verifique todos esses. —>

1. Configure o rastreamento de conversão para suas experiências de anúncio:


Configurar o rastreamento de conversão. Dependendo da implementação, pode envolver a adição de
marcas de rastreamento de conversão para as páginas da Web do anunciante e/ou configuração de um
queda de feed para dados de conversão que o anunciante coletou separadamente.


Você pode gerar tags de rastreamento de conversão do Advertising Cloud no Advertising Cloud
Pesquise ou no Gerenciador dinâmico de tags do Adobe (anteriormente chamado de Gerenciador dinâmico de tags).
Observação: você deve usar tags de conversão do JavaScript, não tags de imagem.


O departamento de TI do anunciante ou outro grupo pode precisar programar ou ser informado
sobre, a implantação de tag.


(Opcional) No Advertising Cloud Search, faça cada conversão (propriedade de transação)
disponível como um conjunto de colunas individual em visualizações de dados e relatórios.


Uma conversão (propriedade de transação) é listada no Advertising Cloud Search depois de em
pelo menos um evento de conversão foi rastreado.


Se você não disponibilizar métricas específicas, todas as conversões serão consolidadas
em um conjunto de colunas &quot;Conversões&quot;.


Valide os dados que são rastreados.


(Opcional) Configurar a entrega de relatórios agendados para endereços de email especificados.


Para obter instruções, consulte o capítulo de ajuda em &quot;Relatórios&quot;.


Configurar campanhas publicitárias no Advertising Cloud DSP ou outro DSP e fornecer JavaScript
ou iframe para as experiências de anúncio para o anunciante, que pode implementá-las como
anúncios de terceiros no DSP.


Monitore o desempenho de suas experiências de anúncio concluídas, visualizando anúncios predefinidos
detalhes de desempenho para experiências individuais ou criação de relatórios de desempenho personalizados.


(Conforme necessário) Atualize as experiências de anúncio com base no desempenho e nas mensagens atualizadas.






>[!MORELIKETHIS]
>
>* [Sobre o Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Como a interface do usuário está organizada](/help/creative/introduction/ui.md)
