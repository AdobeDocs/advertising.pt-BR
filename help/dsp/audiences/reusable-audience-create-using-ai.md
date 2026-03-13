---
title: Criar um público-alvo reutilizável usando IA gerativa
description: Saiba como criar públicos-alvo reutilizáveis no Adobe Advertising DSP usando o agente de público-alvo assistido por IA. Descreva seu público-alvo em prompts em linguagem natural; o agente sugere segmentos de terceiros e cria expressões de público para usar como alvos ou exclusões.
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: f2d7428f70448421dd7b6d9c3d237783b800cd83
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Criar um público-alvo reutilizável usando IA gerativa

*recurso do Beta*

*Suporte somente para inglês*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Use o agente de público assistido por IA para gerar novos públicos reutilizáveis usando todos os segmentos de terceiros disponíveis para você, de acordo com seus requisitos declarados. Você pode usar seus públicos-alvo como destinos ou exclusões para vários posicionamentos.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Este recurso está no modo beta e está sujeito a alterações. Certifique-se de que a expressão de público gerado represente o público que você deseja antes de criar o público e usá-lo para seus posicionamentos.

## Crie um público reutilizável usando IA generativa

1. No menu principal, clique em **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Above the data table, click **[!UICONTROL Create]**.

1. Enter a unique **[!UICONTROL Audience Name]**.

1. (Optional) Deselect the option to **[!UICONTROL Share with all advertisers in my account]**.

   When you share an audience, the audience becomes available as a target or exclusion to all advertisers within the account. No entanto, os segmentos individuais no público-alvo estão disponíveis somente para os usuários com os quais os segmentos são compartilhados.

1. Clique em **[!UICONTROL Save]**.

1. Crie o público-alvo:

   For users with beta permissions, the AI option is the default. To [assemble the audience yourself](/help/dsp/audiences/reusable-audience-create.md), click the &quot;Switch to manual mode&quot; button at the bottom.

   1. Enter one or more prompts to describe the audience characteristics you want to include and exclude. To submit each prompt, click ![Submit prompt](/help/dsp/assets/submit-prompt.png "Submit prompt").

      For more information, see &quot;[Writing Prompts](#writing-prompts)&quot; and &quot;[Best Practices for Creating an Audience Brief](#audience-brief-best-practices).&quot;

      À medida que o agente de audiência encontra segmentos relevantes, ele cria uma expressão de audiência com base nos seus critérios. Ele também solicita sua aprovação antes de procurar segmentos correspondentes para reunir o público.

      Como opção, você pode ignorar a solicitação e continuar especificando critérios de público adicionais.

   1. Quando o agente de público-alvo apresentar uma expressão de público-alvo que descreva adequadamente seu público-alvo, peça ao agente de público-alvo para continuar com a montagem do público-alvo.

      Você pode digitar &quot;prosseguir&quot;, &quot;ok&quot;, &quot;sim&quot; ou outra palavra semelhante.

   1. (Se necessário) Especifique critérios adicionais. Quando o agente de público-alvo apresentar uma expressão de público-alvo que atenda a todos os seus critérios, peça ao agente de público-alvo para continuar com a montagem do público-alvo.

      Para reunir o público, digite “prosseguir”, “ok”, “sim”, ou outra palavra similar.

1. Quando estiver satisfeito com a audiência reunida, clique em **[!UICONTROL Create]** para criar a audiência especificada.

   >[!NOTE]
   >
   >Não será possível editar posteriormente a audiência usando o agente de audiência. Em vez disso, [edite manualmente a expressão de audiência](/help/dsp/audiences/reusable-audience-edit.md).

## Noções básicas de escrever prompts {#writing-prompts}

### O que um prompt deve incluir?

* Use clear, descriptive language to describe the target audience.

   * You can enter either complete sentences or just a string of characteristics. Punctuation isn&#39;t required except when necessary for clarity.

   * In general, prompts are case-insensitive.

   * The audience agent recognizes most common synonyms.

* Be specific and provide details about all audience characteristics that you want to include and any characteristics that you specifically want to exclude. Quanto mais detalhes você fornecer, maior a chance de obter os resultados que atendam às suas necessidades.

* Identify locations, device types, and data providers to include or to exclude.

* Iteratively provide details to refine your criteria and the generated audience expression before you save the audience.

* Learn about prompting through experimentation.

  If your prompt isn&#39;t clear, the audience agent will just request another prompt, so you can try again.

  The audience agent won&#39;t automatically save a generated audience expression as an audience. Você só pode salvar uma audiência clicando no botão [!UICONTROL Create], que está fora da área de prompt, para que você possa desfazer as alterações que não deseja manter.

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

### Exemplos de respostas do agente de público-alvo e como responder

When the audience agent needs a response from you, you can reply using keywords in the request or using common synonyms.

#### Audience agent asking you a question

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Your affirmative replies:  &quot;proceed,&quot; &quot;okay,&quot; &quot;ok,&quot; &quot;yes&quot;, or another similar word

You can also ignore the request and continue to specify additional audience criteria instead.

#### Audience agent asking you to choose from multiple options

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Sua resposta: `1`, `proceed`, `2`, `maximum reach` e assim por diante.

You can also ignore the request and continue to specify additional audience criteria instead.

## Best Practices for Creating an Audience Brief {#audience-brief-best-practices}

An audience brief is a strategic writeup that defines the target audience for a campaign. A well-crafted brief helps the DSP audience agent identify the most relevant segments to assemble your targetable audience.

### Essential Components of an Effective Audience Brief

Inclua no seu resumo o máximo possível de tipos de atributo de público da lista a seguir. Seja específico sobre os atributos que deseja excluir.

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

  Define o escopo do local incluindo país/países, região (EMEA, APAC, NA), densidade populacional (urbana/suburbana/rural).

* **Interesses e afinidades**

  Identifica paixões e preferências, como hobbies (esportes, artes, atividades ao ar livre), padrões de consumo de mídia, afinidades de marca e atividades de estilo de vida (viagens, restaurantes, entretenimento).

* **Psicografia**

  Captura a mentalidade e os valores, incluindo aspirações (busca de status, autoaperfeiçoamento), valores fundamentais (sustentabilidade, inovação, tradição), traços de personalidade (assumidores de riscos, primeiros usuários) e motivações de compra.

* **Behavioral Signals**

  Observable actions including purchase behavior (shopping frequency, channel preferences, brand loyalty), online behavior (website visits, content engagement, social media activity), and offline behavior (store visits, event attendance, memberships).

* **In-Market Intent**

  Identifies purchase readiness through product/service categories being researched, purchase timeline (immediate, near-term, long-term), and relevant life events triggering purchase decisions.

* **Life Stage**

  Current phase understanding including career stage (student, entry-level, mid-career, executive, retired), family stage (newlyweds, new parents, empty nesters), and major life transitions.

### Example of a Well-Structured Audience Brief for a Prospecting Campaign

The following is an example of a strong audience brief for a campaign to drive awareness and trial for a premium meal kit subscription service:

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Duplicar uma Audiência Reutilizável](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Editar um Público Reutilizável](/help/dsp/audiences/reusable-audience-edit.md)
>* [View Details About a Reusable Audience](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Compartilhar um Público Reutilizável](/help/dsp/audiences/reusable-audience-share.md)
>* [Exportar um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-export.md)
>* [Copiar a Chave do Segmento de um Público-alvo reutilizável para a Área de Transferência](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Excluir um público-alvo reutilizável](/help/dsp/audiences/reusable-audience-delete.md)
