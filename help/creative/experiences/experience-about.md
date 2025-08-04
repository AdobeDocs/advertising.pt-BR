---
title: Sobre experiências no Advertising Creative
description: Saiba como configurar experiências de anúncio personalizadas e otimizar elementos de anúncio com base no desempenho.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 780c84aa8dadb52b55d5ca2bee6974b56972793b
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 0%

---

# Sobre as experiências no Advertising Creative 2.0

*Beta fechado*

Cada experiência de anúncio pode incluir um tipo de anúncio (exibição padrão, vídeo padrão ou exibição dinâmica). O [!DNL Advertising Creative 2.0] fornece duas estruturas diferentes de experiência de anúncio para os anúncios em uma única biblioteca criativa.

* **Experiências com direcionamento de árvore de decisão:** [!DNL Creative] permite configurar experiências de anúncio personalizadas em toda a jornada do cliente usando um modelo de árvore de decisão. Você pode personalizar todos os elementos de anúncios — imagens, títulos, ofertas e páginas de aterrissagem — com base no público-alvo.

  Por exemplo, você pode especificar o mesmo pacote criativo para as pessoas de Chicago e Nova York que estão em um segmento específico de público-alvo do Adobe Analytics, mas enviar as pessoas de Chicago para landing pages diferentes das de New Yorkers. Você também pode especificar um pacote diferente para as pessoas no segmento que vivem em qualquer lugar, exceto Chicago e Nova York, e um terceiro pacote para outras pessoas que não estão no segmento.

  As opções de direcionamento incluem:

   * Segmentos de público-alvo da Adobe Audience Manager, Adobe Analytics e Advertising DSP; quaisquer outros segmentos primários importados para a conta; seus segmentos personalizados da Advertising DSP; segmentos de terceiros fornecidos pela Advertising DSP; e quaisquer públicos-alvo existentes da Advertising DSP incorporados na Biblioteca de público-alvo

   * Localizações geográficas específicas, incluindo países, estados, DMAs nos Estados Unidos, cidades e códigos postais

   * Visualizadores para os quais pares de valor-chave específicos (destinos de transmissão de dados) são transmitidos pelo DSP, editor ou parceiro (como SKU=01234567890123 ou Carrinho=empty)

   * [!DNL Creative] redirecionando pixels e valores de atributo especificados

   * Tipos de dispositivos, sistemas operacionais e navegadores específicos

  Depois de criar uma ramificação de público-alvo na árvore decisória, é possível emparelhar o público-alvo com possíveis criativos atribuindo pacotes criativos à ramificação. Para cada experiência, você pode personalizar a otimização e o agendamento para os pacotes criativos e alterar as páginas de aterrissagem padrão e as URLs de rastreamento <!-- later: and any flexible attributes --> para criações individuais em cada pacote.

* **Experiências sem direcionamento de árvore de decisão:** [!DNL Creative] otimiza os elementos de anúncio para a experiência de anúncio sem restringir o público. Para cada experiência, você especifica datas de início e término e algumas configurações padrão, mas grande parte do fluxo de trabalho não está diretamente na experiência. Em vez de adicionar criações diretamente à experiência, use o [!UICONTROL Tag Manager] para criar uma tag de anúncio para cada tamanho de anúncio da experiência e, em seguida, adicionar criações a ela, configurar a otimização criativa e o agendamento e personalizar as páginas de aterrissagem e URLs de rastreamento<!-- later: and any flexible attributes -->.

>[!NOTE]
>
> Como os dois tipos de experiências têm workflows diferentes, você não pode alterar uma experiência não direcionada para uma experiência direcionada, nem uma experiência direcionada para uma experiência não direcionada.

## Veiculação e otimização de anúncios

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] veicula anúncios próprios e aciona anúncios de terceiros para a experiência com base nas opções de meta de direcionamento (quando aplicável), agendamento, rotação de anúncios e otimização especificadas, bem como no inventário de anúncios disponível.

* **Agendamento:** (opcional) agende criações específicas para serem executadas durante períodos sequenciais especificados.

* **Rotação do anúncio:** Gire as criações manualmente de acordo com os pesos relativos ou de forma algorítmica de acordo com a meta de otimização especificada.

* **Meta de otimização:** otimize os elementos de anúncio para a melhor taxa de cliques ou uma [meta personalizada do Advertising DSP](/help/dsp/optimization/custom-goal.md)

  O [!DNL Creative] otimiza as experiências de anúncios, dando compartilhamento de impressões aos ativos com melhor desempenho na experiência. Para experiências direcionadas a públicos-alvo específicos, os anúncios podem ser otimizados com base no desempenho dos elementos de anúncios individuais para os conjuntos de públicos-alvo. Para experiências sem metas de público-alvo específicas, os elementos de anúncio são otimizados exclusivamente com base no desempenho dos elementos de anúncio individuais.

Por exemplo, você pode agendar o Creative 1 para execução durante as duas primeiras semanas para otimizar a taxa de cliques e o Creative 2 para execução durante as duas semanas seguintes para otimizar uma meta personalizada especificada.

## Implementação e gerenciamento de experiências

Depois de criar uma experiência em tempo real (com todos os elementos de anúncio necessários), você pode [gerar uma marca de JavaScript ou iframe para toda a experiência](experience-tag-export.md). Você pode fazer upload da tag de experiência como um anúncio para uma campanha no Adobe Advertising DSP ou implementá-la como um anúncio em uma DSP de terceiros.

>[!NOTE]
>
>O comportamento hierárquico do direcionamento pode variar de acordo com a DSP. O Advertising DSP aplica o direcionamento no nível do anúncio, além do direcionamento no nível do posicionamento.

## Dados de desempenho para suas experiências

Os seguintes dados de desempenho estão disponíveis:

* Ao habilitar a opção [!UICONTROL Metrics] na exibição [!UICONTROL Creative] > [!UICONTROL Experiences], cada linha ou cartão de experiência indica o número de impressões e cliques recebidos pela experiência.

  ![Opção de métricas](/help/creative/assets/metrics-option.png "Opção de métricas")

* Você pode [exibir dados de desempenho detalhados para qualquer experiência](experience-performance-details.md) da exibição [!UICONTROL Experiences].

* Para monitorar o desempenho em suas experiências, crie um [Relatório Creative personalizado](/help/creative/report-custom-creative.md).

## Status da experiência {#experience-statuses}

O status de uma experiência é definido automaticamente, exceto por *Excluído*, que você define manualmente.

| Status | Descrição |
| ------ | ----------- |
| [!UICONTROL Live] | A experiência inclui todos os elementos necessários para que você possa gerar uma tag de experiência para implementar o como um anúncio em uma DSP. Uma experiência ao vivo pode ser agendada para começar no futuro. |
| [!UICONTROL Draft] | Nem todas as ramificações da experiência recebem criações, portanto, a experiência está incompleta e você não pode gerar uma tag de experiência. |
| [!UICONTROL Processing] | Uma experiência online anterior foi editada, mas agora está incompleta. Não é possível gerar uma tag de experiência para ela. **Observação:** se você já implementou uma marca de experiência para a experiência, a versão ativa anterior ainda poderá ser disponibilizada. Se posteriormente você concluir a experiência, tornando-a ativa novamente, a nova versão poderá ser disponibilizada usando a implementação de tag existente. |
| [!UICONTROL Deleted] | A experiência foi excluída de [!DNL Creative] e não é mais visível nas exibições [!UICONTROL Experiences]. |

>[!NOTE]
>
>Você pode alterar o status de um anúncio em uma DSP sem afetar o status da experiência em [!DNL Creative].

## A visualização [!UICONTROL Experiences]

A exibição [!UICONTROL Experiences] mostra todas as suas experiências de direcionamento e de não direcionamento. Você pode ver os nomes da experiência, o status, as datas de início e término, o número e as dimensões dos pacotes criativos ou criativos atribuídos e se a experiência inclui anúncios dinâmicos. Ao habilitar a opção [!UICONTROL Metrics] na exibição [!UICONTROL Experiences], cada cartão ou linha de experiência indica o número de impressões e cliques recebidos pela experiência. Quando estiver no modo de cartão, você pode rolar pelas criações em uma experiência com várias criações usando os botões &lt; e >.

Você pode criar e gerenciar suas experiências, criar e renomear tags de experiência de anúncio e exportar as tags nos formatos JavaScript e iframe para implementação em seus DSPs. Os anunciantes com o Advertising DSP podem, opcionalmente, fazer upload de tags de anúncio diretamente em uma campanha do Advertising DSP.

### Ações disponíveis

Estas são as ações principais disponíveis. Para obter uma lista completa, consulte o índice do capítulo Criativos > Experiências.

* [Baixar dados na exibição](experience-download-view.md)

* [Crie](/help/creative/experiences/experience-create-targeting.md) e [edite](/help/creative/experiences/experience-edit-targeting.md) uma experiência com direcionamento

* [Crie](/help/creative/experiences/experience-create-no-targeting.md), [edite](/help/creative/experiences/experience-edit-no-targeting.md) e [crie manualmente uma marca de anúncio](/help/creative/experiences/experience-tag-create-manually.md) para uma experiência sem segmentação

* [Clonar](experience-clone.md) uma experiência

* [Visualizar](experience-preview.md) uma experiência

* [Compartilhar uma URL de demonstração](experience-share-demo-url.md) para uma experiência

* [Exportar marcas de anúncio para uma experiência](experience-tag-export.md), incluindo, opcionalmente, o carregamento de marcas de anúncio diretamente para uma campanha do Advertising DSP

* [Excluir](experience-delete.md) uma experiência

>[!MORELIKETHIS]
>
>* [Criar uma experiência com o direcionamento da árvore de decisão](experience-create-targeting.md)
>* [Criar uma experiência sem direcionamento](experience-create-no-targeting.md)
