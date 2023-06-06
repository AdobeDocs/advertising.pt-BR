---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---
# Modelo de anúncio de texto - Classificações de etiquetas

**\[Componente\] [!UICONTROL Label Classifications] > \[Classificação de rótulo e valor\]:** (Opcional) Valores de até cinco classificações de etiquetas existentes a serem atribuídos aos diferentes componentes da campanha criados ou editados usando o modelo. Os valores de rótulo são herdados por entidades filhas (incluindo entidades filhas criadas posteriormente), de modo que não é necessário inserir valores para entidades filhas, a menos que você queira substituir os valores herdados. As classificações de etiquetas para grupos de produtos são aplicadas ao nível de unidade (mais granular).

Para cada componente de campanha ao qual deseja atribuir classificações de rótulo:

1. Clique na caixa de seleção ao lado de **\[Componente\][!UICONTROL Label Classifications]**.

1. Configure os valores de classificação de etiqueta para o modelo:

   * Para cada classificação e valor de rótulo a ser atribuído ao componente, faça o seguinte:

      1. Clique em **[!UICONTROL Add Label Classification]**.

      1. Selecione a classificação de etiqueta existente e, em seguida, selecione um valor existente ou insira um novo valor.

         O comprimento máximo para cada valor é de 100 caracteres e pode incluir caracteres ASCII e não ASCII.

         Para inserir um nome de coluna como um parâmetro dinâmico para um valor de classificação de rótulo, clique no campo de entrada (o segundo campo) e, em seguida, clique em um nome de coluna na lista de colunas.

         É possível incluir apenas um valor por classificação por componente de campanha. Por exemplo, uma campanha pode ter Color=Red, mas não Color=Red e Color=Blue.
   * Para alterar um valor de classificação de etiqueta existente, selecione ou insira um novo valor.

   * Para remover um valor de classificação de etiqueta existente, clique em **[!UICONTROL X]** ao lado do valor.
