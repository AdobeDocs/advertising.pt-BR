---
title: Sobre o Creative Studio no Advertising Creative
description: Saiba como usar o Creative Studio para criar conteúdo de anúncios assistidos por IA no Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 811
ht-degree: 0%

---

# Cerca de [!UICONTROL Creative Studio] em [!DNL Advertising Creative]

*recurso do Beta*

O [!UICONTROL Creative Studio] é um ambiente assistido por IA, no qual você pode compilar, redimensionar e refinar anúncios de exibição em vários formatos em uma única sessão. Você interage com a IA por meio de uma interface de bate-papo em linguagem natural para gerar e modificar conteúdo de anúncios — não é necessário trabalho de design manual para campos de conteúdo.

## Visão geral do Workspace

[!UICONTROL Creative Studio] está organizado em três guias:

**[!UICONTROL Creatives]** — O ponto inicial para a criação do anúncio. Mostra as criações existentes geradas no Creative Studio, organizadas em bibliotecas criativas recolhíveis. Aqui, você pode gerar anúncios de exibição padrão a partir de modelos, criar criações de exibição dinâmica a partir de dados de catálogo e gerenciar criações existentes (editar, gerar variações de anúncios, visualizar, duplicar, baixar, excluir, controle de qualidade e revisar logs de alteração). Consulte &quot;[Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)&quot; e &quot;[Gerenciar anúncios dinâmicos no Creative Studio](creative-studio-manage-dynamic-ads.md)&quot;.

**[!UICONTROL Templates]** — Mostra todos os modelos de exibição e de anúncio de vídeo disponíveis para a sua conta, com filtragem por origem (Todos, Modelos do Sistema, Modelos do Usuário), status e formato de anúncio. Você pode visualizar, adicionar favoritos, rotular, baixar e excluir modelos ou iniciar uma sessão de geração de anúncio diretamente de um modelo de anúncio de exibição existente. Consulte &quot;[Gerenciar modelos no Creative Studio](creative-studio-manage-templates.md)&quot;.

**[!UICONTROL Assets]** — Armazena imagens, vídeo e arquivos de áudio usados em modelos e disponíveis para anexar a mensagens de chat de IA durante sessões de geração de anúncios. Pesquise, filtre, faça upload, baixe e exclua ativos. Consulte [Gerenciar ativos no Creative Studio](creative-studio-manage-assets.md).

## Principais recursos

* **Geração de conteúdo de IA:** use o **[!UICONTROL Ad Variations Generator]** para gerar conceitos e variações de anúncios por meio de uma interface de chat em linguagem natural. O assistente de IA pode gerar títulos, subtítulos, CTAs, cópia do corpo e variações de imagem de fundo e criar novos modelos de tamanho na mesma sessão. Até 10 conceitos podem estar ativos por sessão.

* **Suporte para exibição e anúncio de vídeo:** crie e gerencie modelos de anúncio de exibição e modelos de anúncio de vídeo. Ao criar um modelo, escolha **[!UICONTROL Display Ad Template]** ou **[!UICONTROL Video Ad Template]** para corresponder ao formato da campanha.

* **Carregamento de modelo do HTML5:** importe modelos de anúncios do HTML5 existentes carregando-os como arquivos ZIP. A caixa de diálogo **[!UICONTROL Import Templates]** permite atribuir um anunciante e um nome de modelo antes da importação.

* **Suporte a vários tamanhos:** redimensiona anúncios para dimensões padrão IAB em uma única etapa. A IA ajusta automaticamente a inserção de conteúdo e o dimensionamento para cada formato, e os controles da tela (aumentar/diminuir o zoom, ajustar à tela, repetir animações) ajudam a revisar cada tamanho.

* **Saídas alinhadas à marca**: Quando seu [perfil de marca](/help/creative/brands/brand-manage.md) é aplicado, a IA usa os logotipos, as paletas de cores, as diretrizes de voz, os padrões de imagem e as diretrizes de canal da sua marca para manter o conteúdo gerado na marca.

* **Acesso à biblioteca de ativos:** anexe imagens e outros ativos diretamente às mensagens de chat da IA selecionando na biblioteca de ativos, mantendo o contexto visual disponível durante a geração de conteúdo.

* **Integração de feed:** para campanhas de anúncios dinâmicos, conecte um catálogo de produtos ou conteúdo para gerar anúncios em escala e, em seguida, use o agente de IA para filtrar, visualizar e verificar a qualidade de combinações de anúncios gerados pelo catálogo.

* **Organização do modelo:** marque modelos como favoritos, aplique rótulos e filtre por status, formato ou origem para manter sua biblioteca de modelos organizada.

## Fluxos de trabalho de criação de anúncios

| Fluxo de trabalho (WRK) | Quando usar |
| --- | --- |
| [Gerar anúncios padrão a partir de um modelo](creative-studio-manage-standard-ads.md) | Selecione um modelo de exibição ou vídeo e use o [!UICONTROL Ad Variations Generator] para criar variações de conteúdo geradas por IA. Melhor quando um modelo já existe e você deseja a geração de conteúdo assistido por IA. |
| [Gerenciar criações dinâmicas](creative-studio-manage-dynamic-ads.md) | Conecte um catálogo de produtos ou de conteúdo a um modelo, mapeie os campos do catálogo para os elementos do modelo e use o agente de IA para pré-visualizar e controlar a qualidade de todas as combinações de anúncios geradas. Melhor para campanhas orientadas por catálogo em larga escala. |
| Criar um novo modelo | Comece com uma tela em branco para criar um modelo de exibição ou vídeo. Melhor quando nenhum modelo existente atende às suas necessidades. |
| Fazer upload de modelos HTML5 | Importe um ou mais modelos de anúncios do HTML5 empacotados como arquivos ZIP. Melhor quando você tem criações do HTML5 prontas para produção compiladas fora do [!DNL Advertising Creative]. |

## Anúncios padrão versus anúncios dinâmicos

O [!UICONTROL Creative Studio] oferece suporte a dois modelos de conteúdo de anúncio que determinam como o agente de IA se comporta:

**Anúncios padrão** — você fornece ou gera todo o conteúdo do anúncio. O agente de IA pode gerar, modificar ou substituir qualquer campo de conteúdo (títulos, CTAs, imagens, cores, tom de cópia) dentro das restrições do layout do modelo. Anúncios padrão concluídos são salvos em uma biblioteca criativa selecionando um anunciante e uma biblioteca, com uma opção para anexá-los a pacotes. Anúncios padrão são melhores para campanhas de mensagens personalizadas.

**Anúncios dinâmicos** — o conteúdo é orientado por um produto ou catálogo de conteúdo. Um fluxo de trabalho guiado de quatro etapas orienta você ao selecionar um modelo, mapear campos de catálogo para elementos de modelo e configurar o conjunto de anúncios. Após a configuração, o agente de IA muda para uma função de controle de qualidade e visualização: ele pode filtrar anúncios por campos de catálogo, sinalizar problemas de qualidade (limites de caracteres, excesso de conteúdo, imagens quebradas, conformidade) e analisar combinações no catálogo, mas não pode modificar diretamente o conteúdo proveniente do catálogo. Para alterar o conteúdo dinâmico do anúncio, atualize o catálogo de origem.

>[!MORELIKETHIS]
>
>* [Gerenciar anúncios padrão no Creative Studio](creative-studio-manage-standard-ads.md)
>* [Gerenciar criações dinâmicas no Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Gerenciar modelos no Creative Studio](creative-studio-manage-templates.md)
>* [Gerenciar ativos no Creative Studio](creative-studio-manage-assets.md)
>* [Gerenciar perfis de marca no Advertising Creative](/help/creative/brands/brand-manage.md)

