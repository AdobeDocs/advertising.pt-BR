---
title: Práticas recomendadas para configurar campanhas de desempenho
description: Conheça as práticas recomendadas para configurar suas campanhas focadas no desempenho, que incluem disposições otimizadas para o CPA mais baixo ou o ROAS mais alto.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Práticas recomendadas para configurar campanhas de desempenho

O DSP pode otimizar suas campanhas focadas em desempenho. Consulte as seguintes práticas recomendadas para campanhas de desempenho:

* Etapa 1 - Definir a meta
* Etapa 2 - Definir a estratégia
* Etapa 3 - Criar pacotes
* Etapa 4 - Criar estrutura de posicionamento
* Etapa 5 - Usar o Creative Assets correto

## Etapa 1 - Definir A Meta

É importante entender o objetivo da campanha, como obter o ROAS mais alto possível ou o CPA mais baixo possível. As campanhas de desempenho têm [metas de otimização](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;. Para cada pacote na campanha, especifique a meta de otimização de acordo.

![meta de otimização](/help/dsp/assets/optimization-goals.png)

Você também precisa determinar os eventos bem-sucedidos que levam à meta geral e criar metas personalizadas de acordo. Para cada pacote, especifique uma meta personalizada a ser usada com a meta de otimização geral para relatórios e otimização algorítmica usando o [!DNL Adobe AI]. Para obter mais informações sobre como criar metas personalizadas, incluindo práticas recomendadas, consulte [Metas personalizadas](custom-goal.md).

## Etapa 2 - Definir a estratégia

### Estratégias de prospecção

Os pacotes superiores do funnel incluem disposições com direcionamento muito amplo para alcançar novos consumidores líquidos.

#### Estratégias de posicionamento recomendadas para clientes potenciais

* Encontre novos públicos-alvo que provavelmente serão convertidos usando as seguintes táticas:

   * Modelagem semelhante de uma plataforma de gerenciamento de dados (DMP), como o Adobe Audience Manager.
   * Direcionamento comportamental usando dados de terceiros.
   * Direcionamento contextual.
   * Direcionamento de site/categoria.

* Usar o direcionamento de execução da rede (RON): é importante incluir um fluxo de posicionamento da rede sem direcionamento de público-alvo e com direcionamento amplo de inventário. Isso permite que o algoritmo habilitado para [!DNL Adobe AI] encontre usuários valiosos que podem ter cookies mais recentes que ainda não foram categorizados em um público-alvo.

### Estratégias de redirecionamento

Os pacotes inferiores do funnel incluem posicionamentos que direcionam os usuários que já estiveram na página da Web do anunciante ou para os quais o anunciante tem dados de CRM.

#### Estratégias de posicionamento recomendadas para redirecionamento

* Se o anunciante for um cliente do Adobe Analytics ou do Adobe Audience Manager, você poderá criar segmentos primários (como visitantes de página inicial, páginas de produtos ou abandonadores de carrinho) e usá-los como alvos de posicionamento no DSP.

* Evite atribuir muito orçamento a uma inserção direcionada ao público-alvo. Como regra geral, faça um orçamento de US$ 30 por 1.000 usuários por mês.

## Etapa 3 - Criar pacotes

A prática recomendada é criar pacotes separados para prospecção superior do funnel e para redirecionamento inferior do funnel. A otimização ocorre no nível do pacote, de modo que os dados de desempenho de todos os posicionamentos em um pacote sejam agrupados. Portanto, agrupe inserções em pacotes com desempenho esperado semelhante.

![exemplo de pacotes separados para prospecção e redirecionamento](/help/dsp/assets/p-r.png)

Além disso, use as configurações a seguir.

### Metas e orçamento

* **Ritmo e Limite:** Para selecionar uma meta de otimização de CPA ou ROAS, o pacote deve usar o ritmo no nível do pacote. Isso garante que todos os posicionamentos no pacote sejam otimizados para distribuir os gastos com base no desempenho e dimensionar para as metas selecionadas.

* **Datas de voo:** (pacotes de prospecção) Quando a campanha for executada por mais de 25 dias, use o recurso [!UICONTROL Activate Custom Flighting]. Primeiro, defina um voo personalizado para os primeiros 10 dias em aproximadamente 75% do orçamento diário necessário para reduzir os gastos durante a *fase de aprendizado*. Em seguida, defina um segundo voo personalizado para o restante do orçamento.

  Por exemplo, se você tiver US$ 100.000 para gastar em 30 dias, defina o orçamento do voo 1 (dias 1 a 10) para US$ 25.000 (75% x US$ 100.000/30 dias = US$ 2.500 por dia). Use o orçamento restante de US$ 75.000 para o voo 2 (dias 11 a 30).

* **Orçamento:** o DSP sempre tenta alocar 100% do orçamento do pacote uniformemente entre todos os posicionamentos em um pacote. Se uma inserção tiver gasto baixo ou nenhum gasto, recomendamos limitar o orçamento para permitir que mais do orçamento seja alocado para inserções com escala. Aguarde de 24 a 48 horas para que as alterações de orçamento sejam calibradas.

* **Metas de Otimização:** Use uma das duas metas de otimização de desempenho, *[!UICONTROL Highest Return on Ad Spend]* ou *[!UICONTROL Lowest Cost per Acquisition]*, dependendo da meta do pacote. Essas metas otimizam automaticamente o pacote em direção aos posicionamentos de ROAS mais alto ou CPA mais baixo, respectivamente.

* **Metas personalizadas:**
   * Se um novo pacote tiver o mesmo objetivo de um pacote existente, você poderá, opcionalmente, vincular o pacote existente para que o algoritmo possa usar os dados existentes de aprendizado de máquina.
   * Insira o [!UICONTROL Target CPA] ou [!UICONTROL Target ROAS] apropriado.

* **Ritmo de veiculação e Ritmo Intradiário:** Para ambos os tipos de ritmo, selecione *[!UICONTROL Even]* para maximizar suas metas de desempenho, acompanhando uniformemente ao longo de cada dia e durante todo o voo.

  >[!CAUTION]
  >
  >Use *[!UICONTROL FrontLoad]* e *[!UICONTROL Aggressive Front Load]* para o ritmo de veiculação e *[!UICONTROL ASAP]* para o ritmo intradiário somente quando estiver priorizando totalmente a entrega e o gasto em relação à otimização de desempenho, pois essas estratégias podem afetar negativamente seus KPIs de desempenho desejados.

## Etapa 4 - Criar estrutura de posicionamento

Menos é mais. Se você puder configurar menos de seis disposições por pacote, o orçamento disponível poderá mudar dinamicamente para as disposições de melhor desempenho com mais facilidade.

Além disso, adicione cada posicionamento a um pacote com um tipo de meta de pacote de *[!UICONTROL Prospecting]* ou *[!UICONTROL Retargeting]*, conforme apropriado.

A seguir estão as configurações de posicionamento recomendadas para campanhas de desempenho.

### Metas

Você deve configurar a otimização de CPA ou ROAS no nível do pacote (consulte Etapa 3 - Criar pacotes), mas pode adicionar outras configurações no nível de posicionamento.

* **Lance Máximo:**
   * Para inserções de prospecção, use um lance máximo baixo (US$ 5).
   * Para inserções de redirecionamento, use um lance máximo alto (US$ 12).

* **Filtros de pré-oferta:** minimize ou evite definir filtros de pré-oferta agressivos, que impeçam o posicionamento de atingir a escala. As práticas recomendadas incluem o seguinte:

   * Use um (1) filtro de pré-oferta por disposição. A utilização de vários filtros pré-oferta exige que ambos sejam atendidos, o que reduz a escala.

   * Considere definir filtros de pré-oferta menos rigorosos nos casos em que o direcionamento adicional (como público-alvo, geografia e direcionamento de site) é aplicado.

Consulte descrições de quando usar cada filtro de pré-oferta em [Filtros de pré-oferta no nível de posicionamento e Como usá-los](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventário

Para maximizar a escala, use o [!UICONTROL Public] (Open Exchange) e o inventário do [!UICONTROL On Demand].

### Direcionamento de site

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] somente
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Direcionamento de público

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Para inserções de prospecção, agrupe categorias de público-alvo semelhantes e tamanhos de público-alvo semelhantes em uma única inserção. Em seguida, com base no desempenho, execute um dos procedimentos a seguir:
      * Remova públicos com baixo desempenho dos posicionamentos existentes.
      * Mova públicos-alvo de alto desempenho para um local separado para controlar melhor os orçamentos.
   * Para inserções de redirecionamento, você deve incluir um segmento de público-alvo por inserção para controlar ofertas e orçamento com facilidade.

>[!NOTE]
>
>Seus anúncios têm melhor desempenho se um usuário puder ser acessado por apenas um posicionamento. Uma sobreposição significativa entre os usuários em vários posicionamentos pode causar concorrência, o que resulta em um ciclo de ofertas em aumento contínuo, elevando o custo por usuário. Portanto, se você incluir vários públicos-alvo, certifique-se de que eles não consistam em usuários/membros de público-alvo sobrepostos.
>
> Você pode evitar públicos-alvo sobrepostos criando públicos-alvo em camadas para suprimir os níveis mais altos e inclusivos dos posicionamentos, conforme necessário.

* **[!UICONTROL Frequency Capping]:**
   * Para inserções de prospecção, use limites de frequência apertados (uma impressão por dia).
   * Para inserções de redirecionamento, defina a limitação de inserção primária para 6-10 impressões por dia e a limitação secundária para uma impressão por hora.

* **[!UICONTROL Device Targeting]**:
   * Incluir [!UICONTROL Computer], [!UICONTROL Mobile] e [!UICONTROL Tablet].
   * Não direcionar [!UICONTROL Firefox] e [!UICONTROL Safari] devido a limitações de direcionamento e medição. Contate a equipe de conta da Adobe para obter mais detalhes sobre o suporte do [!DNL Adobe] para o [!DNL Safari ITP].
   * Se você direcionar o tráfego de web para dispositivos móveis, desabilite todos os navegadores móveis, exceto [!UICONTROL Chrome] e [!UICONTROL Edge].

### Segurança da marca e qualidade da mídia

O uso de filtragem contextual, bloqueio de fraude pré-oferta e/ou filtragem de [!UICONTROL Ads.txt] limita a escala de suas inserções, mas as usa se necessário.

## Etapa 5 - Usar o Creative Assets correto

* A prática recomendada é incluir o máximo possível de tamanhos de anúncio únicos para maximizar o alcance. O modelo de exibição universal permite fazer upload de qualquer tamanho de anúncio de exibição padrão.
* Verifique se todos os posicionamentos contêm *pelo menos* todos os tamanhos de anúncios de exibição primários (300x250, 728x90, 160x600, 300x600, 320x50 e 300x50).
* Atualizar criações com frequência para evitar fadiga criativa.

>[!MORELIKETHIS]
>
>* [Configurações do pacote](/help/dsp/campaign-management/packages/package-settings.md)
>* [Configurações de posicionamento](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Como a DSP otimiza suas campanhas](optimization-how-dsp-optimizes-campaigns.md)
>* [Metas de otimização e como usá-las](optimization-goals.md)
>* [Filtros de pré-oferta no nível de posicionamento e como usá-los](optimization-pre-bid-filters.md)
>* [Lista de Verificação de Inicialização da Campanha](/help/dsp/campaign-management/campaign-launch-checklist.md)
