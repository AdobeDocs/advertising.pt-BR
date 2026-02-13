---
title: Criar um público-alvo reutilizável usando IA gerativa
description: Saiba como criar públicos-alvo reutilizáveis no Adobe Advertising DSP usando o agente de público-alvo assistido por IA. Descreva seu público-alvo em prompts em linguagem natural; o agente sugere segmentos de terceiros e cria expressões de público para usar como alvos ou exclusões.
feature: DSP Audiences
hidefromtoc: true
hide: true
source-git-commit: 86053178969de362dda0c135ff8c85b9ec9f674e
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Criar um público-alvo reutilizável usando IA gerativa

*recurso do Beta*

*Solicitações somente no idioma inglês*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Use o agente de público-alvo assistido por IA para gerar novos públicos-alvo reutilizáveis usando todos os segmentos de terceiros disponíveis para você, de acordo com seus requisitos declarados. Você pode usar seus públicos-alvo como destinos ou exclusões para vários posicionamentos.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Esse recurso está no modo beta e está sujeito a alterações. Verifique se a expressão de público-alvo gerada representa o público-alvo que você deseja antes de criar o público-alvo e usá-lo para suas inserções.

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Acima da tabela de dados, clique em **[!UICONTROL Create]**.

1. Digite um **[!UICONTROL Audience Name]** exclusivo.

1. (Opcional) Desmarque a opção para **[!UICONTROL Share with all advertisers in my account]**.

   Quando você compartilha um público-alvo, o público-alvo se torna disponível como um alvo ou exclusão para todos os anunciantes na conta. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para usuários aos quais os segmentos são compartilhados.

1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   Para usuários com permissões beta, a opção AI é o padrão. Para [reunir o próprio público](/help/dsp/audiences/reusable-audience-create.md), clique no botão &quot;Alternar para modo manual&quot; na parte inferior.

   1. Insira um ou mais prompts para descrever as características do público-alvo que você deseja incluir e excluir. Para enviar cada prompt, clique em ![Enviar prompt](/help/dsp/assets/submit-prompt.png "Enviar prompt").

      Para obter mais informações, consulte &quot;[Escrevendo Prompts](#writing-prompts)&quot; e &quot;[Práticas recomendadas para criar um resumo de público-alvo](#audience-brief-best-practices).&quot;

      À medida que o agente de IA encontra segmentos relevantes, ele cria uma expressão de público-alvo com base em seus critérios. Ela também solicita sua aprovação antes de procurar segmentos correspondentes para montar o público-alvo.

      Como opção, você pode ignorar a solicitação e continuar especificando critérios de público adicionais.

   1. Quando o agente de IA apresentar uma expressão de público-alvo que descreva adequadamente seu público-alvo, peça ao agente de IA para continuar com a montagem do público-alvo.

      Você pode digitar &quot;prosseguir&quot;, &quot;ok&quot;, &quot;sim&quot; ou outra palavra semelhante.

1. (Se necessário) Especifique critérios adicionais. Quando o agente de IA apresentar uma expressão de público-alvo que atenda a todos os seus critérios, peça ao agente de IA para prosseguir com a montagem do público-alvo.

1. Quando estiver satisfeito com o público-alvo montado, clique em **[!UICONTROL Create]** para criar o público-alvo especificado.

   >[!NOTE]
   >
   >Não é possível editar o público posteriormente usando o agente de IA. Em vez disso, [edite a expressão de público-alvo manualmente](/help/dsp/audiences/reusable-audience-edit.md).

## Escrevendo Prompts {#writing-prompts}

### O que um prompt deve incluir?

* Use uma linguagem clara e descritiva para descrever o público-alvo.

  Em geral, os prompts não diferenciam maiúsculas de minúsculas, e a pontuação não é necessária, exceto para fornecer clareza.

* Seja específico e forneça detalhes sobre todas as características de público-alvo que deseja incluir e sobre quaisquer características que deseje excluir especificamente. Quanto mais detalhes você fornecer, maior a chance de obter os resultados que atendam às suas necessidades.

* Identifique locais, tipos de dispositivos e provedores de dados que serão incluídos ou excluídos.

* Forneça iterativamente detalhes para refinar seus critérios e a expressão de público gerada antes de salvar o público.

* Saiba mais sobre o prompt por meio da experimentação.

  O agente de público-alvo não salvará automaticamente uma expressão de público-alvo gerada como um público-alvo. Você só pode salvar um público-alvo clicando no botão [!UICONTROL Create], que está fora da área de prompt, para que você possa desfazer as alterações que não deseja manter.

Consulte &quot;[Práticas recomendadas para criar um resumo de público-alvo](#audience-brief-best-practices)&quot; para saber mais sobre como otimizar os prompts para públicos-alvo.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### O que você não pode incluir em um prompt?

* Referências a expressões de público-alvo existentes.

* Texto em idiomas além do inglês.

### Exemplos de respostas do agente de IA e como responder

Quando o agente de IA precisar de uma resposta sua, você poderá responder usando palavras-chave na solicitação ou usando termos comuns equivalentes.

#### Resposta do agente de IA fazendo uma pergunta

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Suas respostas afirmativas: &quot;prosseguir&quot;, &quot;ok&quot;, &quot;sim&quot;, ou outra palavra semelhante

Você também pode ignorar a solicitação e continuar a especificar critérios adicionais de público-alvo.

#### Resposta do agente de IA solicitando que você escolha entre várias opções

```
Would you like to:
1) Proceed with this expression,
2) Get maximum reach alternatives, or
3) Modify the expression manually?
```

Sua resposta: `1`, `proceed`, `2`, `maximum reach` e assim por diante.

Você também pode ignorar a solicitação e continuar a especificar critérios adicionais de público-alvo.

## Práticas recomendadas para criar um resumo do público-alvo {#audience-brief-best-practices}

Um resumo de público-alvo é um writeup estratégico que define o público-alvo de uma campanha. Um resumo bem elaborado ajuda o agente de público-alvo da DSP a identificar os segmentos mais relevantes para montar seu público-alvo direcionável.

### Componentes essenciais de um resumo de público-alvo eficiente

#### Atributos de público

Inclua quantos tipos de atributos forem possíveis da lista a seguir no seu resumo. Seja específico quanto aos atributos que deseja excluir.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Demografia**

  Inclui atributos como faixa etária, gênero, estado civil, composição da família (tamanho da família, presença de filhos, famílias de várias gerações).

* **Indicadores Socioeconômicos**

  Estabelece capacidade financeira por meio de faixas de renda familiar (HHI), nível de educação, cargos/cargos, status de emprego e status de propriedade da casa.

* **Parâmetros Geográficos**

  Define o escopo de localização incluindo país/países, região (EMEA, APAC, NA), densidade populacional (urbana/suburbana/rural).

* **Interesses e afinidades**

  Identifica paixões e preferências como hobbies (esportes, artes, atividades ao ar livre), padrões de consumo de mídia, afinidades de marca e atividades de estilo de vida (viagens, restaurantes, entretenimento).

* **Psicografia**

  Captura a mentalidade e os valores, incluindo aspirações (busca de status, autoaprimoramento), valores principais (sustentabilidade, inovação, tradição), traços de personalidade (assumidores de riscos, primeiros adeptos) e motivações de compra.

* **Sinais comportamentais**

  Ações observáveis, incluindo comportamento de compra (frequência de compras, preferências de canal, fidelidade à marca), comportamento online (visitas a sites, engajamento de conteúdo, atividade de redes sociais) e comportamento offline (visitas a lojas, presença em eventos, associações).

* **Intenção no Mercado**

  Identifica a prontidão da compra por meio de categorias de produto/serviço sendo pesquisadas, cronograma de compra (imediato, curto prazo, longo prazo) e eventos de vida relevantes que acionam decisões de compra.

* **Estágio da vida**

  Compreensão da fase atual incluindo estágio de carreira (estudante, nível de entrada, meio de carreira, executivo, aposentado), estágio de família (recém-casados, novos pais, ninhos vazios) e transições de vida principal.

### Exemplo de um resumo de público-alvo bem estruturado para uma campanha de prospecção

Este é um exemplo de um forte resumo de público-alvo de uma campanha para impulsionar a conscientização e a avaliação de um serviço de assinatura premium do kit de refeição:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplicar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Editar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-edit.md)
>* [Exibir detalhes sobre um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Compartilhar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-share.md)
>* [Exportar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-export.md)
>* [Copiar a Chave do Segmento de um Público-alvo reutilizável para a Área de Transferência](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Excluir um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-delete.md)
